---
layout: post
title: LeetCode 刷题笔记：Basic Calculator
---

## 题目

### Basic Calculator

Implement a basic calculator to evaluate a simple expression string.

The expression string may contain open `(` and closing parentheses `)`, the plus `+` or minus sign `-`, **non-negative** integers and empty spaces `" "`.

You may assume that the given expression is always valid.

Some examples:

```ruby
"1 + 1" = 2
" 2-1 + 2 " = 3
"(1+(4+5+2)-3)+(6+8)" = 23
```
**Note: Do not** use the eval built-in library function.

## 思路

第一遍的思路是用正则不断取出括号计算，直到消除全部括号，最后计算剩余算式，返回。

```ruby
# @param {String} s
# @return {Integer}
def calculate(s)
  s.gsub! ' ', ''
  s.gsub! '-', '+-'
  calc = -> str do
    rt = str.chars.inject({:left=>0, :right=>[0]}) do |mem, var|
      if var == '+'
        mem[:left] += mem[:right].join.to_i
        mem[:right] = [0]
      elsif var == '-'
        if mem[:right][0] == '-'
          mem[:right][0] = 0
        else
          mem[:right] = [ '-', 0]
        end
      else
        mem[:right] << var
      end
      mem
    end
    rt[:left] + rt[:right].join.to_i
  end
  while s.include? '('
    s.sub!(/\([^()]*\)/) do |match|
      calc.call match[1, match.length - 2]
    end
  end
  calc.call s
end
```
计算的时候用了点小诡计，把减法视为与负数相加，这样能少写不少代码。但是，正则运行效率和书写效率成反比，柱状图里根本看不到自己的时间……

![截图1](/images/201508/snap_basic_calc_01.png)

第二遍把字符串翻成了数组，遇到括号闭合时计算括号里的内容，虽然代码多了十行，但是速度翻了一倍还多。

```ruby
# @param {String} s
# @return {Integer}
def calculate(s)
  data = s.chars.inject({:result=>[], :temp=>nil}) do |mem, var|
    if /\d/ =~ var
      mem[:temp] = 0 if mem[:temp].nil?
      mem[:temp] = mem[:temp] * 10 + var.to_i
    elsif /[\(|\)|+|-]/ =~ var
      mem[:result] << mem[:temp] if mem[:temp] != nil
      mem[:result] << var
      mem[:temp] = nil
    end
    mem
  end
  data[:result] << data[:temp] if !data[:temp].nil?

  calc = -> arr do
    arr.inject({:left=>0, :plus=>true}) do |mem, var|
      case var
      when '+'; mem[:plus] = true
      when '-'; mem[:plus] = false
      else mem[:left] += mem[:plus] ? var : 0 - var
      end
      mem
    end[:left]
  end

  calc.call(data[:result].inject({:out=>[], :last=>[]}) do |mem, var|
    if var == '('
      mem[:out] << var
      mem[:last] << mem[:out].size
    elsif var == ')'
      last = mem[:last].pop
      mem[:out] = mem[:out][0...last-1] + [calc.call(mem[:out][last..-1])]
    else
      mem[:out] << var
    end
    mem
  end[:out])
end
```

![截图2](/images/201508/snap_basic_calc_02.png)
虽然还是慢，但总算进了显示区间。
