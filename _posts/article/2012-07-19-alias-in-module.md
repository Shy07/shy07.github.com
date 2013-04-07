---
layout: post
title: module 中使用 alias
category: article
description: 写来告诉6R小朋友怎么在module里用alias的，雕虫小技而已
---
<blockquote>写来告诉6R小朋友怎么在module里用alias的，雕虫小技而已</blockquote>

```Ruby
module A
  def p_a
    p "a"
  end
  alias 打印a p_a
end
B = A
include B
p_a  #=>"a"
打印a	#=>"a"
```
