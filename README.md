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
HTML 标题（Heading）是通过`<h1> - `<h6>` 标签来定义的。
- HTML 段落
HTML 段落是通过标签 <p> 来定义的。
- HTML 链接
HTML 链接是通过标签 <a> 来定义的。
```
<a href="https://www.baidu.com">这是一个链接</a>
```
- HTML 图像
HTML 图像是通过标签 <img> 来定义的.
```
<img decoding="async" src="/images/logo.png" width="258" height="39" />
```
