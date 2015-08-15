---
layout: post
title: 使用 VSC 编辑 Markdown
---

最近网站换了主题，一直想写点东西，但是苦于没什么话题可写。正巧，前两天试用了一下微软新发布的轻量级编辑器 Visual Studio Code。虽然还是预览版，但对于 Markdown 的支持，我已经十分满意。尤其在预览方面已经超越了我之前用的 Mou，于是想简单安利一下。

当然，本文是在 VSC 上编辑的。

![截图1](/images/20150814/snap01.png)

VSC 是 VS 家族全新的、免费的、轻量化的、偏向 Web 开发的编辑器。可以编辑的语言肯定不止 Markdown 一种，但是它对 Markdown 的支持度已经足够吸引我，本文着重点也是在 VSC 预览 Markdown 的方面。你可以从这里获取到它：https://code.visualstudio.com/

## Markdown Preview

VSC 天生支持 Markdown 的编辑和预览，在打开 md 文件后，可以用 `⇧⌘V` 快捷键来切换原始文本和预览视图。
当然我们也可以像 Mou 之类的 md 编辑器一样，将窗口分成两块，一边显示编辑文本，一边显示预览。

![官网图例](https://code.visualstudio.com/Content/images/MDPreview.png)

## Using your own CSS

VSC 让我赞赏的是，它可以通过配置 `"markdown.styles": []` 来实现自定义的预览效果，更赞的是 VSC 支持使用 url 来指定 css 文件。

```js
// Place your settings in this file to overwrite the default settings
{
	// A list of URLs or local paths to CSS style sheets to use from the markdown preview.
	"markdown.styles": [
		"http://shy07.com/stylesheets/style.css",
		"http://shy07.com/stylesheets/syntax.css",
		"http://shy07.com/stylesheets/responsive.css"
	]
}
```

![截图2](/images/20150814/snap02.png)

截图是引用本站 css url 的显示效果， 可以说已经和现在看到的页面效果很接近了。另外，从截图还可以看出 VSC 的预览支持 Github 风格的表格语法。  

VSC 的语言支持情况：

|Features                          |Languages                              |
|:---------------------------------|:--------------------------------------|
|Syntax coloring, bracket matching |Batch, C++, Clojure, Coffee Script, Dockerfile, F#, Go, Jade, Java, HandleBars, Ini, Lua, Makefile, Objective-C, Perl, PowerShell, Python, R, Razor, Ruby, Rust, SQL, Visual Basic, XML
|+ Snippets                        |Groovy, Markdown, PHP, Swift           |
|+ IntelliSense, linting, outline  |CSS, HTML, JavaScript, JSON, Less, Sass|
|+ Refactoring, find all references|TypeScript                             |

  
此外，VSC 还支持 Markdown 代码片段，在 User Snippets 中设置自己的代码片段以后，可以通过 `⌃Space` 快捷键使用。至于，编译输出 HTML 等功能都不是本文的重点，所以就不介绍了。

从官网的介绍来看，相比 Sublime Text、Atom 这些同类产品，VSC 的核心竞争力是 "code-edit-debug cycle"。而 VSC 对于 Markdown 的支持度，正好成为一个相当有力的佐证。  

之前用 Windows 的时候，我就是 VS 的拥趸。现在 MAC 上可以用到免费轻量的 VS，我没有什么理由不支持。而微软能以这样开放的姿态讨好开发者，我也相当看好 VSC 的前景，虽然我知道微软其实在下一盘很大的棋……