# 一、HTML5 的新特性
## 1.1 HTML5 新增的语义化标签
- `<header>`：头部标签
- `<nav>`：导航标签
- `<article>`：内容标签
- `<section>`：定义文档某个区域
- `<aside>`：侧边栏标签
- `<footer>`：尾部标签

## 1.2 HTML5 新增的多媒体标签
1. 音频：`<audio>` <br>
2. 视频：`<video>`<br>
## 1.3 HTML5 新增的 input 类型
| 值                | 描述                                                                              |
|-------------------|-----------------------------------------------------------------------------------|
| numberNew         | 定义用于输入数字的字段。                                                          |
| telNew            | 定义用于输入电话号码的字段。                                                      |
| searchNew         | 定义用于输入搜索字符串的文本字段。                                                |
| colorNew          | 定义拾色器。                                                                      |
| dateNew           | 定义 date 控件（包括年、月、日，不包括时间）。                                    |
| datetimeNew       | 定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，基于 UTC 时区）。 |
| datetime-localNew | 定义 date 和 time 控件（包括年、月、日、时、分、秒、几分之一秒，不带时区）。      |
| emailNew          | 定义用于 e-mail 地址的字段。                                                      |
| monthNew          | 定义 month 和 year 控件（不带时区）。                                             |
| rangeNew          | 定义用于精确值不重要的输入数字的控件（比如 slider 控件）。                        |
| timeNew           | 定义用于输入时间的控件（不带时区）。                                              |
| urlNew            | 定义用于输入 URL 的字段。                                                         |
| weekNew           | 定义 week 和 year 控件（不带时区）。                                              |

## 1.4 HTML5 新增的表单属性
| 属性         | 值        | 描述                                 |
|--------------|-----------|--------------------------------------|
| required     | required  | 必填                                 |
| placeholder  | 提示文本  | 表单的提示信息，存在默认值将不显示   |
| autofocus    | autofocus | 页面加载完成自动聚焦到指定表单       |
| autocomplete | off/on    | 浏览器基于用户以前输入的内容自动补充 |
| multiple     | multiple  | 可以多选文件提交                     |

可以通过以下设置方式修改placeholder里面的字体颜色：
```
input::placeholder {
 color: pink;
 }
```
