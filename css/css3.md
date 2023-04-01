# 1. 精灵图
一个网页中往往会应用很多小的背景图像作为修饰，当网页中的图像过多时，服务器就会频繁地接收和发送<br>
请求图片，造成服务器请求压力过大，这将大大降低页面的加载速度。<br>
因此，为了有效地减少服务器接收和发送请求的次数，提高页面的加载速度，出现了 CSS 精灵技术（也称<br>
CSS Sprites、CSS 雪碧）。<br>
核心原理：将网页中的一些小背景图像整合到一张大图中 ，这样服务器只需要一次请求就可以了。<br>

## 1.1 精灵图（sprites）的使用
1. 精灵技术主要针对于背景图片使用。就是把多个小背景图片整合到一张大图片中。<br>
2. 这个大图片也称为 sprites 精灵图 或者 雪碧图<br>
3. 移动背景图片位置， 此时可以使用 background-position 。<br>
4. 移动的距离就是这个目标图片的 x 和 y 坐标。注意网页中的坐标有所不同<br>
5. 因为一般情况下都是往上往左移动，所以数值是负值。<br>
6. 使用精灵图的时候需要精确测量，每个小背景图片的大小和位置。<br>

# 2. 字体图标
字体图标使用场景： 主要用于显示网页中通用、常用的一些小图标。<br>
精灵图是有诸多优点的，但是缺点很明显。<br>
1. 图片文件还是比较大的。<br>
2. 图片本身放大和缩小会失真。<br>
3. 一旦图片制作完毕想要更换非常复杂。<br>
此时，有一种技术的出现很好的解决了以上问题，就是字体图标 iconfont。<br>
字体图标可以为前端工程师提供一种方便高效的图标使用方式，展示的是图标，本质属于字体。<br>

## 2.1 字体图标的优点
轻量级：一个图标字体要比一系列的图像要小。一旦字体加载了，图标就会马上渲染出来，减少了服务器请求<br>
灵活性：本质其实是文字，可以很随意的改变颜色、产生阴影、透明效果、旋转等<br>
兼容性：几乎支持所有的浏览器，请放心使用<br>
注意： 字体图标不能替代精灵技术，只是对工作中图标部分技术的提升和优化。<br>
总结：<br>
1. 如果遇到一些结构和样式比较简单的小图标，就用字体图标。<br>
2. 如果遇到一些结构和样式复杂一点的小图片，就用精灵图。<br>

## 2.2 字体图标
### 2.2.1 字体图标的下载<br>
  icomoon 字库 http://icomoon.io<br>
  阿里 iconfont 字库 http://www.iconfont.cn/<br>
  把下载包里面的 fonts 文件夹放入页面根目录下<br>
  不同浏览器所支持的字体格式是不一样的，字体图标之所以兼容，就是因为包含了主流浏览器支持的字体文件。<br>
  1. TureType(.ttf)格式.ttf字体是Windows和Mac的最常见的字体，支持这种字体的浏览器有IE9+、Firefox3.5+、<br>
  Chrome4+、Safari3+、Opera10+、iOS Mobile、Safari4.2+；<br>
  2. Web Open Font Format(.woff)格式woff字体，支持这种字体的浏览器有IE9+、Firefox3.5+、Chrome6+、<br>
  Safari3.6+、Opera11.1+；<br>
  3. Embedded Open Type(.eot)格式.eot字体是IE专用字体，支持这种字体的浏览器有IE4+；<br>
  4. SVG(.svg)格式.svg字体是基于SVG字体渲染的一种格式，支持这种字体的浏览器有Chrome4+、Safari3.1+、<br>
  Opera10.0+、iOS Mobile Safari3.2+；<br>
### 2.2.2 字体图标的引入 （引入到我们html页面中）<br>
  1. 在 CSS 样式中全局声明字体： 简单理解把这些字体文件通过css引入到我们页面中。
一定注意字体文件路径的问题。
```
@font-face {
 font-family: 'icomoon';
 src: url('fonts/icomoon.eot?7kkyc2');
 src: url('fonts/icomoon.eot?7kkyc2#iefix') format('embedded-opentype'),
 url('fonts/icomoon.ttf?7kkyc2') format('truetype'),
 url('fonts/icomoon.woff?7kkyc2') format('woff'),
 url('fonts/icomoon.svg?7kkyc2#icomoon') format('svg');
 font-weight: normal;
 font-style: normal;
}
```
```
span {
 font-family: "icomoon";
}
```
### 2.2.3 字体图标的追加 （以后添加新的小图标）
如果工作中，原来的字体图标不够用了，我们需要添加新的字体图标到原来的字体文件中。<br>
把压缩包里面的 selection.json 从新上传，然后选中自己想要新的图标，从新下载压缩包，并替换原来的文件即可。<br>

# 3. css三角
```
div {
 width: 0;
 height: 0;
 line-height: 0;
 font-size: 0;
 border: 50px solid transparent;
 border-left-color: pink;
}
```
# 4. CSS 用户界面样式
## 4.1 更改用户的鼠标样式
```
li {cursor: pointer; }
```
| 值          | 描述                               |
|-------------|------------------------------------|
| default     | 默认光标（通常是一个箭头）         |
| pointer     | 光标呈现为指示链接的指针（一只手） |
| move        | 此光标指示某对象可被移动。         |
| text        | 此光标指示文本。                   |
| not-allowed | 禁止                               |

## 4.2 轮廓线 outline
给表单添加 outline: 0; 或者 outline: none; 样式之后，就可以去掉默认的蓝色边框。
```
input {outline: none; }
```
## 4.3 防止拖拽文本域 resize
实际开发中，我们文本域右下角是不可以拖拽的。
```
textarea{ resize: none;}
```
# 5. vertical-align 属性应用
CSS 的 vertical-align 属性使用场景： 经常用于设置图片或者表单(行内块元素）和文字垂直对齐。<br>
官方解释： 用于设置一个元素的垂直对齐方式，但是它只针对于行内元素或者行内块元素有效。<br>
```
vertical-align : baseline | top | middle | bottom
```
| 值       | 描述                                       |
|----------|--------------------------------------------|
| baseline | 默认。元素放置在父元素的基线上。           |
| top      | 把元素的顶端与行中最高元素的顶端对齐       |
| middle   | 把此元素放置在父元素的中部。               |
| bottom   | 使元素及其后代元素的底部与整行的底部对齐。 |

## 5.1 图片、表单和文字对齐
图片、表单都属于行内块元素，默认的 vertical-align 是基线对齐。<br>
此时可以给图片、表单这些行内块元素的 vertical-align 属性设置为 middle 就可以让文字和图片垂直
居中对齐了<br>

## 5.2 解决图片底部默认空白缝隙问题
bug：图片底侧会有一个空白缝隙，原因是行内块元素会和文字的基线对齐。<br>
主要解决方法有两种：<br>
1. 给图片添加 vertical-align:middle | top| bottom 等。 （提倡使用的）<br>
2. 把图片转换为块级元素 display: block;<br>

# 6. 溢出的文字省略号显示
## 6.1. 单行文本溢出显示省略号
1. 单行文本溢出显示省略号--必须满足三个条件
```
/*1. 先强制一行内显示文本*/
 white-space: nowrap; （ 默认 normal 自动换行）
 /*2. 超出的部分隐藏*/
 overflow: hidden;
 /*3. 文字用省略号替代超出的部分*/
 text-overflow: ellipsis;
 ```
## 6.2. 多行文本溢出显示省略号
多行文本溢出显示省略号，有较大兼容性问题， 适合于webKit浏览器或移动端（移动端大部分是webkit内核）
```
overflow: hidden;
text-overflow: ellipsis;
/* 弹性伸缩盒子模型显示 */
display: -webkit-box;
/* 限制在一个块元素显示的文本的行数 */
-webkit-line-clamp: 2;
/* 设置或检索伸缩盒对象的子元素的排列方式 */
-webkit-box-orient: vertical;
```

# 7. 常见布局技巧
## 7.1 margin负值运用
1.让每个盒子margin 往左侧移动 -1px 正好压住相邻盒子边框<br>
2.鼠标经过某个盒子的时候，提高当前盒子的层级即可（如果没有有定位，则加相对定位（保留位置），如果有定位，则加z-index）
## 7.2 文字围绕浮动元素
巧妙运用浮动元素不会压住文字的特性
## 7.3 行内块巧妙运用
页码在页面中间显示:<br>
1. 把这些链接盒子转换为行内块， 之后给父级指定 text-align:center;<br>
2. 利用行内块元素中间有缝隙，并且给父级添加 text-align:center; 行内块元素会水平会居中
## 7.4  CSS 三角强化
```
width: 0;
height: 0;
border-color: transparent red transparent transparent;
border-style: solid;
border-width: 22px 8px 0 0;
```
# 8. CSS 初始化
不同浏览器对有些标签的默认值是不同的，为了消除不同浏览器对HTML文本呈现的差异，照顾浏览器的兼容，我们需要对CSS 初始化

