# HTML
对于中文网页需要使用 <meta charset="utf-8"> 声明编码，否则会出现乱码。有些浏览器(如 360 浏览器)会设置 GBK 为默认编码，则你需要设置为 <meta charset="gbk">
```
<!DOCTYPE html>
<html>
<head>
<meta charset="utf-8">
<title>hello world(runoob.com)</title>
</head>
<body>
    <h1>我的第一个标题</h1>
    <p>我的第一个段落。</p>
</body>
</html>
```
注意:HTML中不支持 空格、回车、制表符，它们都会被解析成一个空白字符。

1. <!DOCTYPE> 声明
<!DOCTYPE>声明有助于浏览器中正确显示网页。
网络上有很多不同的文件，如果能够正确声明HTML的版本，浏览器就能正确显示网页内容。
doctype 声明是不区分大小写的。

## HTML基础
- HTML 标题
HTML 标题（Heading）是通过`<h1> - <h6>` 标签来定义的。
- HTML 段落
HTML 段落是通过标签 `<p> `来定义的。
- HTML 链接
HTML 链接是通过标签 `<a>` 来定义的。
```
<a href="https://www.baidu.com">这是一个链接</a>
```
- HTML 图像
HTML 图像是通过标签 `<img>` 来定义的.
```
<img decoding="async" src="/images/logo.png" width="258" height="39" />
```
## HTML 属性
属性值应该始终被包括在引号内。
双引号是最常用的，不过使用单引号也没有问题。
在某些个别的情况下，比如属性值本身就含有双引号，那么您必须使用单引号.
下面列出了适用于大多数 HTML 元素的属性：
| 属性  | 描述                                                          |
|-------|---------------------------------------------------------------|
| class | 为html元素定义一个或多个类名（classname）(类名从样式文件引入) |
| id    | 定义元素的唯一id                                              |
| style | 规定元素的行内样式（inline style）                            |
| title | 描述了元素的额外信息 (作为工具条使用)                         |

## HTML 标题
HTML 水平线
`<hr>` 标签在 HTML 页面中创建水平线
HTML 注释
`<!-- 这是一个注释 -->`

## HTML 段落
段落是通过 `<p>` 标签定义的。
注意：浏览器会自动地在段落的前后添加空行。（</p> 是块级元素）
如果您希望在不产生一个新段落的情况下进行换行（新行），请使用 `<br>` 标签

当显示页面时，浏览器会移除源代码中多余的空格和空行。所有连续的空格或空行都会被算作一个空格。需要注意的是，HTML 代码中的所有连续的空行（换行）也被显示为一个空格。
## HTML 文本格式化
HTML 使用标签 `<b>`("bold") 与 `<i>`("italic") 对输出的文本进行格式
```
<b>加粗文本</b><br><br>
<i>斜体文本</i><br><br>
<code>电脑自动输出</code><br><br>
这是 <sub> 下标</sub> 和 <sup> 上标</sup>
<big>这个文本字体放大</big>
<em>这个文本是斜体的</em>
<small>这个文本是缩小的</small>
<pre>
此例演示如何使用 pre 标签
对空行和    空格
进行控制
</pre>
<kbd>键盘输入</kbd>
<tt>打字机文本</tt>
<samp>计算机代码样本</samp>
<var>计算机变量</var>

<address>
Written by <a href="mailto:webmaster@example.com">Jon Doe</a>.<br> 
Visit us at:<br>
Example.com<br>
Box 564, Disneyland<br>
USA
</address>

<abbr title="etcetera">etc.</abbr>
<br />
<acronym title="World Wide Web">WWW</acronym>
//在某些浏览器中，当您把鼠标移至缩略词语上时，title 可用于展示表达的完整版本
<p>WWF's goal is to: 
<q>Build a future where people live in harmony with nature.</q>
We hope they succeed.</p>
//块引用
<p>My favorite color is <del>blue</del> <ins>red</ins>!</p>
```
- HTML 文本格式化标签

| 标签     | 描述         |
|----------|--------------|
| `<b>`      | 定义粗体文本 |
| `<em>`     | 定义着重文字 |
| `<i>`      | 定义斜体字   |
| `<small>`  | 定义小号字   |
| `<strong>` | 定义加重语气 |
| `<sub>`    | 定义下标字   |
| `<sup>`    | 定义上标字   |
| `<ins>`    | 定义插入字   |
| `<del>`    | 定义删除字   |

- HTML "计算机输出" 标签

| 标签   | 描述               |
|--------|--------------------|
| `<code>` | 定义计算机代码     |
| `<kbd>`  | 定义键盘码         |
| `<samp>` | 定义计算机代码样本 |
| `<var>`  | 定义变量           |
| `<pre>`  | 定义预格式文本     |

- HTML 引文, 引用, 及标签定义

| 标签   | 描述               |
|--------|--------------------|
| <code> | 定义计算机代码     |
| <kbd>  | 定义键盘码         |
| <samp> | 定义计算机代码样本 |
| <var>  | 定义变量           |
| <pre>  | 定义预格式文本     |

## HTML 链接
`<a href="url">链接文本</a>`
- HTML 链接 - target 属性
使用 target 属性，你可以定义被链接的文档在何处显示。下面的这行会在新窗口打开文档：
`<a href="https://www.baidu.com/" target="_blank" >访问</a>`
- HTML 链接- id 属性
id 属性可用于创建一个 HTML 文档书签。
提示: 书签不会以任何特殊方式显示，即在 HTML 页面中是不显示的，所以对于读者来说是隐藏的。
```
<a id="tips">有用的提示部分</a>
<a href="#tips">访问有用的提示部分</a>
```
- 图片链接
```
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>web hello</title> 
</head>
<body>

<p>创建图片链接:
<a href="url">
<img  border="10" src="url" alt="HTML" width="32" height="32"></a></p>

<p>无边框的图片链接:
<a href="url">
<img border="0" src="url" alt="HTML" width="32" height="32"></a></p>

</body>
</html>
```

- 创建电子邮件链接
```
<!DOCTYPE html>
<html>
<head> 
<meta charset="utf-8"> 
<title>菜鸟教程(runoob.com)</title> 
</head>
<body>

<p>
这是一个电子邮件链接：
<a href="mailto:someone@example.com?Subject=Hello%20again" target="_top">
发送邮件</a>
</p>

<p>
<b>注意:</b> 单词之间空格使用 %20 代替，以确保浏览器可以正常显示文本。
</p>

</body>
</html>
```
## HTML `<head>`
- HTML `<head>` 元素
- HTML `<title>` 元素
- HTML `<title>` 元素
- HTML `<base>` 元素
`<base>` 标签描述了基本的链接地址/链接目标，该标签作为HTML文档中所有的链接标签的默认链接;
- HTML `<link>` 元素
`<link>` 标签定义了文档与外部资源之间的关系。`<link>` 标签通常用于链接到样式表;
- HTML <style> 元素
`<style>` 标签定义了HTML文档的样式文件引用地址.在`<style>` 元素中你也可以直接添加样式来渲染 HTML 文档;
- HTML `<meta>` 元素
meta标签描述了一些基本的元数据。
`<meta>` 标签提供了元数据.元数据也不显示在页面上，但会被浏览器解析。
META 元素通常用于指定网页的描述，关键词，文件的最后修改时间，作者，和其他元数据。
元数据可以使用于浏览器（如何显示内容或重新加载页面），搜索引擎（关键词），或其他Web服务。
`<meta>` 一般放置于 `<head>` 区域
- HTML `<script>` 元素
`<script>`标签用于加载脚本文件，如： JavaScript。
`<script>` 元素在以后的章节中会详细描述。
## HTML 样式- CSS
CSS 可以通过以下方式添加到HTML中:
- 内联样式- 在HTML元素中使用"style" 属性
- 内部样式表 -在HTML文档头部 <head> 区域使用<style> 元素 来包含CSS
- 外部引用 - 使用外部 CSS 文件
内联样式
`<p style="color:blue;margin-left:20px;">这是一个段落。</p>`
HTML样式实例 - 背景颜色
```
<body style="background-color:yellow;">
<h2 style="background-color:red;">这是一个标题</h2>
<p style="background-color:green;">这是一个段落。</p>
</body>
```
HTML 样式实例 - 字体, 字体颜色 ，字体大小
```
<h1 style="font-family:verdana;">一个标题</h1>
<p style="font-family:arial;color:red;font-size:20px;">一个段落。</p>
```
HTML 样式实例 - 文本对齐方式
```
<h1 style="text-align:center;">居中对齐的标题</h1>
<p>这是一个段落。</p>
```
