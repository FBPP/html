### web标准 是由 结构(Structure), 表现(presentation), 行为(behavior) 三个方面

+ 结构 对网页元素进行整理和分类 html
+ 表现 设置网页元素的版式, 颜色, 大小等外观样式 css
+ 网页模型定义及交   

#### html标签的关系:

包含关系

```html
<head>
    <title> </title>
</head>
```

并列关系

```html
<head> </head>
<title> </title>
```

#### html基本结构标签

```html
<html>
    <head>
        <title> 标题 </title>
    </head>
    <body>
        页面主体
    </body>
</html>   
```

```html
<!DOCTYPE html>
<html lang="en">
<head>
    <meta charset="UTF-8">
    <meta name="viewport" content="width=device-width, initial-scale=1.0">
    <title> </title>
</head>
<body>
    
</body>
</html>
```

#### <!DOCTYPE>

文档类型的声明标签(不是html标签), 告诉浏览器使用的是哪个html的版本

```
<!DOCTYPE  html> 告诉浏览器使用最新的html版本
```

#### \<html lang>

当前文档的显示语言

```php+HTML
<html lang = "en"> 英语
<html lang = "zh-CN"> 中文
```

#### \<meta>

``` html
<meta charset = "UTF-8"> UTF-8编码

name指定数据的名称
content指定数据的内容
<meta name="keywords" content="HTML5, 前端, css3"> keywords 表示网站的关键字 在搜索引擎搜索时会匹配这些关键字
<meta name="description" content="这是一个非常不错的网站"> description 指定网站的描述 在搜索引擎搜索出来的结果列表里会显示这些描述

http-equiv
<meta http-equiv="refresh" content="3;https://www.baidu.com"> 三秒后会跳转到百度
```

#### \<title>\</title>

```htm
title 标签里的内容会作为搜索结果的超链接显示
```

#### \<link>

```html
<link rel="stylesheet" href="xxx/xxx">   链接外部css 
<link rel="icon" href="favicon.ico">	链接收藏图标
	收藏图标一般放到网站的根目录下 名字一般为 favicon.ico
```



### html 常用标签

#### 标题标签 \<h1> 到 \<h6>

``` html
<h1> 一级标题 </h1>
```

标题独占一行 所有独占一行的元素都称为块元素

\<h>里的文字上下有一行空行

建议一个html页面只出现一个``` <h1></h1>```

\<h1>的重要性仅次于\<title>

#### \<hgroup>\<hgroup>

```html
<hgroup>
    <h1></h1>
    <h2></h2>
</hgroup>
```

\<hgroup>标签用于将一组有联系的\<h>标签分成一组



#### 段落标签 \<p>

paragraph 段落

```html
<p> 段落1 </p>
<p> 段落2 </p>
```

在浏览器窗口大小变化是 \<p> 标签内的文字会自动换行

#### 换行标签\<br /> (单标签)

break 换行

```html
<p>
    第一行 <br />
    第二行
</p>
```

#### 文本格式化标签

```html
加粗<strong></strong> 或者 <b></b> strong表示强调重要的内容

倾斜<em></em> 或者 <i></i> em表示语气的加重

删除线<del></del> 或者 <s></s>

下划线<ins></ins> 或者 <u></u>

```

在页面中不会独占一行的元素称为行内元素

#### \<blockquote>\</blockquote>

```html
XXX说过:<blockquote>
  ...  
</blockquote>
```

\<blockquote>标签表示长引用 是快元素

#### \<q>\</q>

```html
xx说:<q>...</q>
```

\<q>表示短引用 是行内元素

#### 块元素和行内元素嵌套的规则

块元素用来布局 行内元素用来包裹文字

一般不在行内元素里包裹块元素, \<p>标签里不能放块元素

浏览器解析源码是会自动修正 但是不一定按照预期修正

#### 盒子 \<div> 和 \<span>

division 分割分区

span 跨度, 跨距

div单独占一行 没有上下间距

span显示在同一行	大小由内容决定

#### 语义化块标签

```html
<header></header> 
<main></main>
<nav></nav>
<section></section>
<aside></aside>
<article></article>
<footer></footer>
```

本质上和div相同 但是各自的语义不同



#### 列表 

```html
无序列表 
<ul>
    <li></li>
    <li></li>
</ul>

有序列表
<ol>
    <li></li>
    <li></li>
</ol>

定义列表
<dl>
    <dt></dt>
    <dd></dd>
    
	<dt></dt>
    <dd></dd>
</dl>

列表之间可以互相嵌套
<ul>
    <li>
        <ul>
            <li></li>
        </ul>	
    </li>
</ul>
```



#### 图像标签 \<img src = "图像URL" />

src是图像的路径和文件名

src的其他属性:

alt 对图片的描述 方便搜索引擎识别 如果不写alt 就不会被浏览器识别; 在某些浏览器里替换文本 图像不能显示时 会显示这个文字

title 提示文本 鼠标放上去是提示

width 宽度

height 高度

宽和高如果只修改一个 另一个会等比例缩放 

在pc端一般不要修改图片大小 需要多大就裁多大

但在移动端 需要经常对图片进行缩放 一般是大图缩小

border 边框粗细

#### 图片的格式

jpeg(jpg) 

​		支持的颜色较多 不支持透明效果, 不支持动图

​		一般用来显示照片

gif

​	支持的颜色少 支持简单透明 支持动图

​	颜色单一的图 动图

png

​	支持的颜色多 支持复杂透明 不支持动图

webp

​	谷歌专门为网页图片设计的新格式

​	支持颜色多 支持复杂透明 支持动图 容量小

​	兼容性不好

base64

​	将图片用base64编码 可以在网页加载的第一个request下直接加载 速度很快

​	一般需要图片和网页一起加载是使用 如果过多的使用会占用流量



选择图片的一般原则 效果一样的 选占用存储小的

效果不一样的  选效果好的 占用内存很大 依然不能选



#### 超链接 \<a href  = "跳转目标" target = "目标弹出方式">文本或图像 \</a>

anchor 锚

href 可以是

​		外部链接url  ```href = "http://www.XXX.XXX" ``` 

​		内部链接 ``` href = "XXX.html"```

​		去顶部 ```href = "#"```

​		空链接 ``` href = "##" ```

​		下载链接 ```href = "XXX.zip" ```

​		 锚点链接 

```html
<a href = "#two"> 第二集 </a>
<h3 id = "two"> 第二集 </h3>
```

​		

文字 图像 表格 音频 视频 都可以添加超链接		

target值默认为_self 表示在当前页面跳转 如果是__blank另起窗口

a是行内元素 可以嵌套除他自身外的任何元素

#### \<base> 设置当前页面的所有超链接的默认属性

```html
<head>
    <base target = "_blank" />
</head>
```

####  注释标签和特殊字符

注释

```html
<!-- -->
```

空格 \&nbsp;

\<  \&lt;

\> \&gt;

#### \<iframe>\</iframe> 内联框架

在网页里显示另一个网页 但是内联框架中的网页不会被搜索引擎检索

#### \<audio>\</audio>

```html
<audio>
    <source src="./source/audio.mp3"> 
    <source src="./source/audio.ogg"> 如果浏览器不支持MP3格式 试试ogg
    <embed src="./source/audio.mp3" type="audio/mp3" width="300" height="100">如果浏览器(IE8)不支持<audio>				</audio>标签 看看浏览器是否支持<embed>(一个老的标签) 因为浏览器不支持的标签会被浏览器忽略
</audio>
```

#### \<video>\</video>

```html
<video>
    <source src="./source/flower.webm"> webm是google开发的视频格式
    <source src="./source/flower.mp4"> 如果浏览器不支持webm格式 看看是否支持mp4格式
    <embed src="./source/flower.mp4" type="video.mp4">
</video>
```

#### 表格

```html
<table>
    <tr>
        <th>
        </th>
    </tr>
    <tr>
        <td>
        </td>
    </tr>
</table>
```

#### 表格结构标签

头部区域 ```<thead> </thead>```

主体区域 ``` <tbody> </tbody>```

脚 ```<tfoot></tfoot>```

#### 合并单元格

跨行 rowspan = "单元格个数" 将单元格合并到上面

跨列 colspan = "单元格个数" 将单元格合并到左边

#### 标题

```<caption></caption>```

#### 表单

form 

```html
<form action=""></form> action属性指定表单提交的地址
```

input

```html
<input type="text" name="username"> type指定input的类型 name是填写数据的键
<input type="password" name="password"> 
<input type="submit" value="注册"> value指定按钮的文本

<input type="radio" name="hello" value="a"> 单选按钮 name属性的值必须相同 value的值时单选按钮的值 checked默认选中
<input type="radio" name="hello" valie="b" checked>

<input type="checkbox" name="hello" value="a"> 多选框
<input type="checkbox" name="hello" value="b">
<input type="checkbox" name="hello" value="c" checked>
<lable for="">XXX</lable> 使用for指定input元素 点击文字也会选中该元素

<input type="email">
<input type="url">
<input type="number">
<input type="datetime-local">
<input type="month">
<input type="date">
<input type="week">
<input type="color">
<input type="range">
```

 select

```html
<select name="haha">
    <option value="a">选项1</option>
    <option selected value="b">选项1</option>
    <option value="c">选项1</option>
    <optgroup lable="组标题">
        <option></option>
    </optgroup>
</select>
```

input属性

```html
autocomplete="off" 关闭自动补全 和name属性配合使用 记录相同name属性 相同浏览器 提交成功的属性
readonly 只读
disabled 禁用 
autofocus 自动获取焦点
required 非空验证
```



-------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------------

## css层叠样式表

#### style属性 内联样式 行内样式

```html
<p style="color: red; font-size: 30px;">xxxx</p>
```

开发是不要使用内联样式

#### \<style>\</style>标签 内部样式表

```html
<head>
    <style>
        p{
            color: red;
          	font-size: 30px;
        }
    </style>
</head>
```

可以对多个标签设置样式 在本页面内可以实现复用 \<style>标签里遵循css语法规范 不支持html语法规范

#### \<link>\</link> 外部样式表

```html
<head>
    <link rel="stylesheet" href="style.css">
</head>
```

外部样式表可以跨网页复用 作为外部资源 也会被浏览器缓存 加快网页的加载速度

#### /**/ 注释

#### 基本选择器

```css
元素选择器
p{
    
}

<p></p>
<p></p>


id选择器
#red{
    
}
<p id="red"></p>

类选择器
.blue{
    
}
.font{
    
}
<p class="blue font"></p>
<p class="blue"></p>

通配选择器
*{
    
}

```

#### 复合选择器

```css
交集选择器 
	语法: 选择器1选择器2选择器n{} (多个选择器连着写)
	如果交集选择器里有元素选择器 必须以元素选择器开头
div.red{
    
}

<div class="red"></div> 只会对div有效
<p class="red"></p> 对p无效

并集选择器
	语法: 选择器1, 选择器2, 选择器n{}
	同时选择多个选择器设置样式
h1, span{
    
}

<h1></h1>
<span></span>
```

#### 关系选择器

```html
子元素选择器
	语法: 父元素 > 子元素1 > 子元素n{}
	选中指定元素的子元素
div > span {

}

<div>
	<p>
        <span></span> 样式不会改变
    </p>
    <span></span> 样式会改变
</div>

后代元素选择器
	语法: 祖先元素 后代元素1 后代元素n{}
	选中指定元素的所有指定后代元素
div span {

}

<div>
	<p>
        <span></span> 样式会改变
    </p>
    <span></span> 样式会改变
</div>

兄弟元素选择器
	语法: 兄 + 弟{}
	选中指定元素的下第一个兄弟元素
div + span {

}

<div>
    
</div>
<span></span> 样式会改变
<span></span> 样式不会改变
<span></span> 样式不会改变

	语法: 兄 ~ 弟{}
	选中指定元素下面的所有兄弟元素
div ~ span {

}

<span></span> 样式不会改变	
<div>
    
</div>
<span></span> 样式会改变
<span></span> 样式会改变
<span></span> 样式会改变
```

#### 属性选择器

```html
[属性名] 选择含有指定属性名的元素
[title]{

}
<p title="">
    
</p>

[属性名=属性值] 选择含有指定属性名和属性值的元素
[title = abc]{

}
<p title = "abc">
    
</p>

[属性名~=属性值] 选择含有指定属性名和包含独立单词为属性值的元素
[title ~= abc] {

}
<p title="a abc a">
    
</p>

[属性名^=属性值] 选择含有指定属性名和以指定属性值开头的元素
[title ^= abc] {

}
<p title = "abcde">
    
</p>

[属性名$=属性值] 选择含有指定属性名和以指定属性值为结尾的元素
[title $= abc]{

}
<p title = "deabc">
    
</p>

[属性名*=属性值] 选择含有指定属性名和属性值里含有指定属性值的元素
[title *= "abc"]

<P title = "deabcde">
    
</P>
```



#### 伪类选择器

```html
伪类是不存在的类 它表示的是元素的一种状态 比如第一个子元素 被点击的元素 鼠标移入的元素
	伪类一般情况下用:开头
	:first-child 第一个子元素
	:last-child 最后一个子元素
	:nth-child() 写在括号里面的是
		    具体数字 表示第几
			n 表示整数
			2n 表示选中偶数位的元素
			2n + 1 表示选中奇数位的元素
			odd 选中奇数位的元素
			even 选中偶数位的元素
	:nth-last-child() 倒序
<style>
    ul > li :first-child{
        
    }  
</style>

<ul>
    <li></li>
    <li></li>
</ul>


	:first-of-type
	:last-of-type
	:nth-of-type() 
	:nth-last-of-type() 这几个和上面的child类似 不过是在同类型间选择
<style>
    ul > li : first-of-type{
        
    }
</style>
<ul>
    <span></span>
    <li></li> 选择这个li
    <li></li>
</ul>


	:not() 除了

ul>li:not(:nth-of-type(3)) {

}

<ul>
    <span></span>
    <li></li>
    <li></li>
    <li></li> 第三个样式不会受到影响
</ul>

	:only-child 唯一的
	
	:empty 空内容
```

\<a>\</a>标签的特殊伪类

```css
正常链接(未被访问过的链接)
a:link{

}

访问过的链接
a:visited{

}
/*
	访问后的状态只能改变字体颜色
*/
```

使用于所有的标签的伪类

```css
鼠标停在标签上时
a:hover{
    
}
鼠标点击时
a:active{
    
}
```

#### 伪元素

```css
::first-letter 第一个字母
p::first-letter{
	font-size:50px;
}


::first-line 第一行
p::first-line{
	color: green;   
}

::selection 选中的
p::selection{
    color: green;
}

::before 元素的开始位置
div::before{
    content: '「'
}

::after 元素的结束位置
div::after{
    content" '」'
}

::before和::after的元素不存在于html标签的文本中 不可以被选中
伪元素默认是行内显示模式
```

#### 继承

文本样式 会应用到它的后代

```html
p{
	color: green;  会被span继承
	background-color: orange 不会被span继承
	text-align: center; 会被span继承
}

<p>
    <span></span>
</p>
```

#### 选择器的权重 

样式的冲突:不同选择器对相同的元素相同的样式设置的不同的值时 就发生了冲突

发生样式冲突是 应用哪个样式 由选择器的权重(优先级)决定

选择器的权重

​	内联选择器  1, 0, 0, 0

​	id选择器	0, 1, 0, 0

​	类选择器	0, 0, 1, 0

​	元素选择器 0, 0, 0, 1

​	通配选择器 0, 0, 0, 0

​	继承的样式 没有优先级

比较选择器时 将所有的选择器的权重相加计算

```html
div.red{
    font-size: 20px;
}
.red{
    font-size: 10px
}

<div class="red">
    
</div> 这个div的字体大小是20px
<span class="red"></span>
```

并集选择器的优先级是单独计算的

多个低级选择器优先级累加的和不会超过比它优先级更高的选择器

相同的优先级的选择器后面的会覆盖前面的样式

在css样式后加上 !important 这个样式的优先级就会变成最高 开发时要慎用

#### 长度单位

```css
px 像素
div{
    width: 10px;
    height: 10px;
}

% 百分比 相对于父元素的百分比
div{
    widht: 50%;
    height: 50%;
}

em 当前元素的字体大小为单位 浏览器的字体大小默认是16px
div{
    font-size: 20px;
    width: 10em;    200px
}

rem 根元素(html)字体大小为单位 
html{
    font-size: 20px;
}
div{
    widht: 10rem;   200px;
}

```

#### 颜色单位

```css
英文描述
red, green, chocolate

rgb值 rgb值是光的三原色
	rgb(255, 255, 255)

rgba值: 在rgb值的基础上加不透明度(0 ~ 1)
	rgba(105, 123, 123, .5)
十六进制rgb值:
	#ff00aa
	如果颜色两两相同可以简写 #f0a

hsl值:
	h 色相(0 ~ 360)
`	s 饱和度(0% ~ 100%)
	l 亮度(0% ~ 100%)
hsla值
	a透明度
```

#### 文档流

网页是一个多层结构 一层摞一层

通过css可以分别问每一层设置样式

作为用户只能看到最上面一层

这些层中 最下面一层称为文档流 文档流失网页的基础 我们所创建的元素默认都是在文档流中排列

对于我们来说元素有两种状态: 在文档流中 脱离文档流

元素在文档流中的特点:

​	块元素:

​			独占一行 垂直排列

​			默认的宽度撑满父元素

​			默认的高度被子元素撑满

​	行内元素:

​			不会独占一行 只占用自身大小

​			默认自左向右排列 如果一行中不能容下这些行内元素 会换到第二行继续自左向右排列

​			默认的宽度和高度都会被子元素撑开 

​			盒子之间有一个或多个空格时 会出现一个默认等宽的间距

​	行内块

​			img 表单元素是行内快元素

​			行内快元素不独占一行 默认沿基线对齐

​			可以设置宽高 宽高默认由内容决定 

​			盒子之间有一个或多个空格时 会出现一个默认等宽的间距

#### 盒子模型

盒子模型 又叫框模型

css将页面中的所有元素设置为一个矩形的盒子

将元素设置为盒子后 对页面布局就变成了把不同的盒子摆放到不同的位置

每一个盒子都由以下几个部分组成

​	内容区 content

​	边框 border

​	内边距 padding

​	外边距 margin

```css
.box1{
    /*
    	内容区: 元素的子元素和内容都在内容区中排列
    	width和height设置内容区的大小
    */
    width: 200px;
    height: 200px;
    background-color: red;
    /*
    	边框是盒子边缘 边框里面属于盒子内部 出了边框是盒子外部
    	要设置边框 至少设置三个样式
    		边框的宽度: border-width
    		边框的颜色: border-color
    		边框的样式: border-style		
    	边框的宽度会影响整个盒子的大小 不会影响盒子内容的大小
    
    	border-width一般会有默认值3px
    	border-width可以用来指定4个方向的边框宽度
    		值的情况:
    			4个值 上 右 下 左
    			3个值 上 左右 下
    			2个值 上下 左右
    			1个值 上下左右
    	除了border-width 还有border-xxx-width
    	xxx可以是 top right bottom left
    	用来单独指定一个边
    	
    	border-color用来指定边框的颜色 用法同border-width
    	border-color如果省略自动使用color的颜色
    
    	border-style 指定边框样式
    		solid 实线
    		dotted 点
    		dashed 虚线
    		double 双线
    		none 无边框(默认值)
    
    */
    
    border-width: 10px;
    border-color: green;
    border-style: soild;
    
}

<div class="box1"></div>
	/*
		border简写属性 通过该属性可以同时设置边框的所有相关属性 没有顺序要求
		border:10px red solid; 
		border: red 10px solid;
		border-top:10px red solid;
		border-right:
		border-bottom:
		border-left:
	*/


```

padding

```css
.box1{
    /*
    内边距
    	内容区和边框之间的距离是内边距
    	一共有四个方向的内边距
    	内边距的设置会影响盒子大小
    	背景颜色会延伸到内边距上
    	盒子可见框的大小 = 内容区widht + 2 * padding + 2 * border-width
    */
    	padding: 10px 20px 30px 40px;
        padding-top: 100px;
    	padding-right: 100px;
    	padding-bottom: 100px;
    	padding-left: 100px;
         
}
```

margin

```css
.box1{
    /*
    	外边距
    		外边距不会影响盒子可见框的大小
    		外边距会影响盒子的位置和占用空间
    		margin-top:上外边距 设置一个正值 元素会向下移动
    		margin-right: 默认情况下设置margin-right不会产生任何效果
    		margin-bottom: 下外边距 设置一个正值 其下面的元素会向下移动
    		margin-left: 左外边距 设置一个正值 元素会向右移动
    
    		margin也可以设置为负值 负值会产生相反的效果
    
    		简写属性 margin:
    		
    		元素在页面中是按照左上到右下的顺序排列的 默认情况下设置左上会移动自身 设置右下会移动其他元素
    		
    */
}
```

#### 水平方向布局

```css
/*
	一个元素在其父元素中 水平布局必须满足以下等式
	margin-left + border-left + padding-left + width + padding-right + border-right + margin-right = 包含块内容区的宽度
	若七个值中没有auto 则会调整margin-right
	这七个值中 margin-left width margin-right 可以设置为auto
	如果某个值设置为auto 则会调整这个值
	如果没有设置width width默认为auto
	如果margin 和 width设置为auto 则margin会调整为0 width会调整为最大
	如果margin-left 和 margin-right 都设置为auto 且width不是auto 这会调整这两个margin值相同
	如果没有设置auto的值总和大于父元素内容区的宽度 则设置为auto的值 或者margin-right(没有设置为auto的值) 会自动调整为负数
*/
/*
	行内块元素 横向布局的问题
		由于行内块 默认是基线对齐 给行内快设置垂直方向的内外边距时会影响水平方向的布局
*/
/*
	行内元素 横向布局问题
		由于行内元素沿着基线对齐 垂直方向上的内外边距不起作用
*/
```

#### 垂直方向布局

```css
/*
	父元素高度不写就会被子元素内容撑开 写了就该是多少就是多少

	如果子元素大小超过父元素 则子元素会从父元素中溢出
	使用overflow属性来设置父元素处理溢出的子元素
	可选值:
		visible 默认值 子元素会从父元素中溢出 在元素外面的位置显示
		hidden 溢出内容将会裁剪不会显示
		scroll 生成两个滚动条 通过滚动条来查看完整内容
		auto 根据需要生成滚动条

		overflow-x 单独处理水平溢出
		overflow-y 单独处理垂直溢出

*/
```

#### 垂直外边距重叠

```css
/*
	相邻的垂直方向外边距发生重叠现象
	兄弟元素
		兄弟元素的相邻外边距会取两者之间的较大值(两者都是正值)
		特殊情况
			如果相邻的外边距一正一负 则取两者的和
			如果相邻的外边距都是负值 则取两者中绝对值较大的

		兄弟元素之间的外边距的重叠 对于开发是有利的 所以我们不需要进行处理
		
		父子元素
			父子元素间相邻外边距 子元素会传递给父元素(上外边距)
			父子的外边距的折叠会影响到页面的布局, 必须要进行处理
*/
```

#### 行内元素

```css
/*
	行内元素的盒模型
		行内元素不支持宽度和高度 width height 行内元素的内容区大小由内容决定 不能手动修改
		行内元素可以设置padding, border, margin 但是垂直方向上的padding, border, margin 不会影响页面布局
*/
```

#### 元素的显示类型display和显示状态visibility

```css
display设置元素的类型
	可选值:
		inline 将元素设置为行内元素
		block 将元素设置为块元素
		inline-block 将元素设置为行内块元素
		table 将元素设置为一个表格
		none 元素不在页面中显示

visibility 设置元素的显示状态
	可选值:
		visiable 默认值 正常显示
		hidden 隐藏 但是依然占用空间
```

#### 浏览器的默认样式

```css
通常情况下 浏览器会有默认样式 默认样式会影响页面布局
使用第三方的 reset.css normalize.css 重置默认样式
```

#### 盒子的大小

```css
默认情况下 盒子的大小由内容区 内边距 和 边框 共同决定
box-sizing 用来设置盒子的得计算方式(width 和 height的作用)
可选值:
content-box: 默认值 width 和 height设置内容区的大小
border-box: width 和 height设置整个盒子的可见框的大小
```

#### 轮廓和圆角

轮廓

```css
/*	
	outline 设置元素的轮廓 用法类似border
	outline与border的不同是不会更改可见框大小 不会影响布局
*/
div{
    outline: 1px soild red;
    outline-top:;
    outline-width:;
}
```

阴影

```css
/*
	box-shadow 设置元素阴影效果 阴影效果不会更改元素的可见框大小 不会影响布局
	第一个值 水平偏移量 正值向右移动 负值向左移动
	第二个值 垂直偏移量 正值向下移动 负值向上移动
	第三个值 阴影模糊半径
	第四个值 扩展(可选)
	第五个值 阴影颜色

	向内阴影 inset
*/
	box-shadow: 0px 0px 10px rgba(0, 0, 0, .5);
```

圆角

```css
/*
	border-radius设置四个圆角	
		可选值
			四个值 左上 右上 右下 左下
			三个值 左上 右上和左下 右下
'			两个值 左上和右下 右上和左下
			一个值 设置四个角
		每个值可以用 1px/1px 设置椭圆 水平半径/垂直半径
*/
	border-radius: 10px 20px 30px 40px
	border-radius: 10px
	border-radius: 10px / 20px;
/*
	border-top-left-radius border-top-right-radius
	border-bottom-left-radius border-bottom-right-radius
		可选值:
			一个值 设置圆半径
			两个值 设置椭圆 水平半径 垂直半径
*/
```

#### 浮动

```css
/*
	使用float设置元素的浮动
		可选值:
			none 默认值 不浮动
			left 元素向左浮动
			right 元素向右浮动	
		注意: 元素浮动后会脱离文档流 不再占用文档流的位置 水平布局的等式不再成立
			浮动元素下面的还在文档流中的元素会自动向上移动

	浮动的特点:
		1. 浮动元素脱离文档流 不再占用文档流的位置
		2. 设置浮动后元素会向父元素的左侧或右侧浮动
		3. 浮动元素默认不会从父元素中移出
		4. 浮动元素在向左和向右浮动时 不会超过它前面的浮动元素
		5. 如果浮动元素上面是一个没有浮动的元素 则浮动元素无法上移
		6. 浮动元素不会超过它上面的兄弟元素 最多和它一样高
		7. 浮动元素不会盖住文字 文字会自动环绕在浮动元素周围 所以可以利用浮动来设置文字环绕图片的效果(这也是float的初衷)
*/

/*
	元素脱离文档流后的特点:
		块元素:
			块元素不再独占页面一行
			默认宽度和高度都被内容撑开
		行内元素:
			会变成块元素	
		综上 元素脱离文档流 	就不分快元素和行内元素了
*/

/*
	当浮动元素溢出其父元素时 会影响后面的盒子中的元素
*/
```

#### BFC(Block Formatting Context) 块级格式化环境

```css
/*
	高度塌陷问题
		如果父元素在文档流内 如果高度没有定死 其高度会被子元素撑满
			如果子元素脱离文档流 则父元素因为没有内容撑满 父元素高度丢失 父元素下面的其他元素会向上移动 影响页面布局
*/

<style>
.outer {
    border: 1px solid red;
}
.inner{
    width: 100px;
    height: 100px;
    background-color: #bfa;
    float: left;
}
</style>

<div class="outer">
	<div class="inner"></div>
</div>
<div style="width: 100; height: 100px; background-color: yellow"></div>
/*
	BFC是css的隐含属性 可以为一个元素开启BFC
		开启BFC的元素会变成一个独立的布局区域 对BFC的子元素设置样式不会影响BFC外面的布局

	元素开启BFC后的特点:
		不会被浮动元素覆盖
		子元素和父元素的外边距不会重叠
		开启BFC的元素会包含浮动的子元素

	开启BFC的方式: 所有开启BFC的方式都是间接开启 都会产生副作用
		float不为none
		将元素设置为行内块元素inline-block
		overflow 设置为 非visible
*/

```

#### clear

```css
/*
	如果不希望某个元素因为其他元素的浮动改变位置 可以通过clear来清除浮动对当前元素的影响
	clear的原理是为元素设置了margin(但是不会显示出来)
	可选值:
		left 清除左册浮动元素对当前元素的硬性
		right 清除右侧浮动元素对当前元素的影响
		both 清除两侧中影响最大的
*/
/*
	clear解决高度塌陷问题
	为浮动的子元素添加after
*/
box::after{
	clear: both;
    display: block; after是行内元素 设置为块元素才会在box下方
}
```

#### clearfix

```css
/*
	子元素和父元素上边距重叠会导致子元素设置margin-top会传递给父元素
	设置 box::before隔开两个元素
*/
box::before{
    content: '';
    display: table;
}



.clearfix::before, clearfix::after
{
    content: '';
    display: table;
    clear: both;
}

/*
	clearfix可以同时解决外面距重叠和高度塌陷问题
*/
```

#### position定位

```css
/*
	通过定位可以将元素摆放到页面的任意位置
	position设置定位
		可选值:
			static 默认值 元素静止 没有开启定位
			relative 开启元素相对定位
			absolute 开启元素绝对定位
			fixed 开启元素的固定定位
			sticky 开启元素的粘滞定位
	偏移量(offset)
		当元素开启定位后可以通过偏移量设置元素的位置 使用偏移量设置元素位置不会影响布局
		top 定位元素和定位位置上边的距离
		bottom 定位元素和定位位置下边的距离
		left 定位元素和定位位置左边的距离
		right 定位元素和定位位置右边的距离
*/

```

相对定位 relative

```css
/*
	position: relative;
	相对定位元素的特点:
		元素开启相对定位后 如果不设置偏移量元素不会发生任何变化
		相对定位参照元素在文档流中的位置进行定位的
		相对定位会提升元素的层级
		相对定位不会使元素脱离文档流
		相对定位不会改变元素的性质是块还是行内
*/
```

绝对定位 absolute

```css
/*
	position: absolute
	绝对定位的特点:
		开启绝对定位后 如果不设置偏移元素的位置不会发生变化
		开启绝对定位后 元素会从文档流中脱离
		绝对定位会改变元素的性质 
		绝对定位会改变元素的性质 行内变成块 块的宽度会被内容撑开而不是独占一行
		绝对定位会提升元素的层级
 		绝对定位是相对于其包含块进行定位的

	包含块(containing block)
		正常情况下:
			包含块就是里当前元素最近的祖先块元素
			<div><div></div></div>
			<div><span><em></em></span></div> em的包含块是div而不是span 因为span不是块元素
		绝对定位下:
			包含块是离它最近的开启了定位的祖先元素
				如果所有的祖先元素都没有开启定位则根元素就是它的包含块
		html(根元素, 初始包含块)
*/
```

固定定位 fixed

```css
/*
	position: fixed
	固定定位也是一种绝对定位的特点 所以固定定位的大部分特点和绝对定位一样
		唯一不同是固定定位永远参照浏览器的视口进行定位
		固定定位的元素不会随网页的滚动而滚动
*/
```

粘滞定位

```css
/*	
	position: sticky
	粘滞定位和相对定位的特点基本一致
		不同的是粘滞定位可以在元素到达某个位置时将其固定

	兼容性不好
*/
```

#### 绝对定位布局

```css
/*
	开启绝对定位后:
	
	水平布局
	left + margin-left + border-left + padding-left + width + padding-right + border-right + margin-right + right = 包含块内容区宽度
	水平方向添加了left 和 right两个值
	 	当发生过度约束:
			如果9个值中没有auto 自动调整right 使等式满足
			如果有auto 自动调整auto
		可设置auto的值 margin width left right
		left和right默认为auto 等式不满足时 会优先调整这两个值使等式满足
	垂直方向
	top + margin-top + border-top + padding-top + height + padding-bottom + border-bottom + margin-bottom + bottom = 包含块内容区的高度
	发生过度约束时 和水平布局类似
	
*/
/*
	水平垂直居中
	left: 0;
	right: 0;
	top: 0;
	bottom: 0;
	margin: auto;
*/
```

#### 定位的层级

```css
/*
	对于开启了定位的元素 可以通过z-index设置元素的层级
	z-index需要设置一个整数作为参数 值越大层级越高
	层级越高的元素优先显示
	如果元素的层级一样 则优先显示靠下的元素
	祖先元素的层级再高也不会盖住后代元素
	z-index < 0 层级低于标准流
	如果 a 和 b 的层级不为默认 且 a的层级 小于 b的层级
		则a的子元素son_a无论层级有多高 都无法超过 b以及son_b
	如果 a 和 b 的层级是默认
		则设置 son_a 的层级 可以超过 b 和 son_b
*/
```

#### 字体

```css
/*
	font-family 字体族(字体的格式)
		可选值:
			serif 衬线字体		
			sans-serif 非衬线字体
			monospace 等宽字体
	 	font-family可以指定多个字体 多个字体用,隔开字体生效时优先使用第一个, 第一个元素无法使用则使用第二个 以此类推
		font-family: Microsoft YaHei, Heiti SC, sans-serif
	
	@font-face{ 指定字体 可以将服务器的字体让用户使用
		font-family: 'myfont'; 起一个字体名字
		src: url('font/XXX.ttf'); 服务器中字体的路径
	}
	注意 加载速度
		版权
		浏览器不支持格式 多用src备用多个格式 类似video audio

	font-style
		可选值
			normal 正常
			italic 倾斜
*/
```

####  图标字体

```css
/*
	网页中的图标 可以通过引入图片来引入图标 但是图片占用存储空间较大 本身不灵活(不能修改颜色 放大会失真)
	使用图标时 可以将图标设置为字体 使用font-face对字体进行引入
	这样就可以使用字体的方式使用图标
*/

```

font Awesome 图标字体库

```css
/*
导入css和webfonts两个文件夹

用法1: 使用class指定图标字体
    引入all.css <link rel="stylesheet" href="css/all.css"> 
    使用class属性 起名为"fas XXX" 或者"fab XXX" XXX是图标的名字
用法2: 通过伪元素设置图标字体
	使用伪元素选择器::before 或 ::after
	在content中设置字体的编码 content: '\f1b0'
	设置字体样式
		fab字体: font-family: 'Font Awesome 5 Brands';
		fas字体: font-family: 'Font Awesome 5 Free';
				font-weight: 900;
用法3: 通过实体使用图标字体
	&#x图标编码
<span class="fas">&#xf1b0;</span>
*/
```
iconfont

```css
/*
	导入项目 下载到本地
	link引入iconfont.css
	用法1:
		设置class="iconfont" 通用实体使用&#x
	用法2:
		设置class="iconfont icon-XXX"
	用法3:
		设置伪类
		content: '\eXXX';
		font-family: 'iconfont';
	
*/
```

#### 行高

```css
/*
	行高是文字占用的实际高度
		可以通过line-height设置行高
			行高也可以指定一个整数 行高是字体大小的指定倍数
	字体框
		字体框是字体存在的格子 设置font-size是设置字体框的高度
	行高会在字体框的上下平均分配(可以将行高设置和元素的高度相等的值 文字会在元素中垂直居中, 如果元素的高度未指定 则默认为auto被行高撑开)
	通过行高可以设置多行文本的间距(line-height - font-size)
*/

/*
	文本的4条线:
		顶线
		中线
		基线
		底线
*/
```

#### 复合属性 

```css
/*
	如果复合属性和单属性同时存在时 把复合属性写在单属性的前面
*/
```



#### font简写属性

```css
/*
	font: font-weight font-style font-size/line-height font-family
		
	font-weight font-style line-height 可以省略 默认为normal
*/
font: bold italic 50px/1 Microsoft Yahei, serif;
```

#### 文本的样式

```css
/*
	text-align 水平居中
		也可以让 行内元素 水平居中
		可选值:
			left 左侧对齐
			right 右侧对齐
			center 居中对齐
			justify 两端对齐
*/
span{
    text-align: center;
}
/*
	vertical-align 垂直对齐
		可选值:
			baseline 默认值 基线对齐
			top 顶部对齐
			bottom 底部对齐	
			middle 居中对齐 middle 是关于'X'中心对齐
*/
img{
    vertical-align: top; 消除基线和底部的空隙
}

/*
	text-decoration 文本修饰
		可选值:
			none 什么都没有
			underline 下划线
			line-through 删除线
			overline 上划线
*/

	text-decoration: underline red dotted; 颜色和样式兼容性不好

/*
	white-space 设置网页如何处理空白
		可选值:
			normal 正常
			nowrap 不换行
			pre 保留空白
*/
	white-space: normal;
	overflow: hidden;
	text-overflow: ellipsis;
/*
	word-break: break-all 强制换行
*/
/*
	文本的溢出样式
	overflow: hidden
	text-overflow
		ellipsis
	
*/
/*
	text-shadow 文字阴影
*/
/*
	文字边框
		可选值:
			边框粗细 颜色
		-webkit-text-stroke: 1px gray;
*/

/*
	文字裁剪
        -webkit-background-clip: text;
        color: transparent;
*/  
```

#### 背景图片

```css
/*
	background-image 设置背景图片
		可以同时设置背景图片和背景颜色 这样背景颜色会成为背景图片的背景色
		如果背景图片大小小于元素 背景图片会自动在元素中平铺将元素铺满
		如果背景图片大于元素 会一部分背景无法完全显示
		如果背景图片和元素大小一样大 会直接正常显示
		背景图如果设置为 no-repeat 则默认延伸到padding区
		背景图如果设置为 repeat 则默认延伸到border区
*/
	background-image: url("./img/xxx.png");
/*
	background-repeat 设置背景图片的重复方式
		可选值:
			repeat 默认值 背景会沿x轴y轴双向重复
			repeat-x 沿着x轴重复
			repeat-y 沿着y轴重复
			no-repeat 北背景图片不重复
*/

	background-repeat: no-repeat;
/*
	background-position 用来设置背景图片位置
		设置方式:
			通过top left right bottom center 几个表示方位的词来设置背景图片的位置
				使用方位词必须同时指定两个值 如果只写一个第二个默认是center
			通过偏移量设置
				水平方向偏移量 垂直方向偏移量
*/
	background-position: center;
	background-position: -10px 10px;

/*
	background-clip
		可选值:
			border-box 默认值 背景会出现在边框的下边
			padding-box 背景不会出现在边框 只会出现在内容区和内边距
			content-box 背景只会出现在内容区
*/
		
/*
	background-origin 背景图片的偏移量(background-position)计算原点
		可选值:
			padding-box 默认值 从内边距开始计算
			content-box 从内容区开始计算
			border-box 从边框开始计算
*/
/*
	background-size 设置背景图片大小
		第一个值表示宽度 第二个值表示高度
		如果只写一个 第二个值默认auto
			cover 图片比例不变 将元素铺满
			contain 图片比例不变 将图片在元素中完整显示
*/
/*
	background-attachment
		背景图片是否跟随元素移动
		可选值:
			scroll 默认值 背景图片跟随元素移动
			fixed 背景图片会固定在页面中 background-position相对于视口定位
*/
/*
	background 简写属性
		注意: background-size必须在background-position后并用/隔开
		background-origin必须写在background-clip前面
*/
/*
	多重背景 background: url(xxx),
					    url(xxx);
		前面的url会压住后面的url
*/
```

####  CSS-Sprite(雪碧图)

```css
/*	
	图片的闪烁问题:
		图片属于网页中的外部资源 外部资源需要浏览器发送请求才能加载
		浏览器加载外部资源时按需加载
		如果一个a标签的:link :hover :active 使用三个图片 则会在三种状态下各加载一次 每次加载都会发送请求 会造成图片闪烁 影			响体验
	解决闪烁问题:
		可以将多个小图片放到一个大图片中 通过background-position显示相应的图片
		这样所有图片可以同时加载到网页中 避免出现闪烁问题
	雪碧图使用步骤:
		1.确定使用的图标
		2.测量图标的大小
		3.根据测量结果创建一个元素
		4.将雪碧图设置为元素的背景图片
		5.设置一个偏移量以显示正确的图片
	雪碧图的特点:
		一次性将多个图片加载进页面 降低请求次数 加快访问速度 提升用户体验
*/

```

#### 渐变

```css
/*
	渐变可以实现复杂的背景 可以实现一个颜色向另一个颜色过渡效果 
	渐变是图片 需要通过background-image设置
*/
```
线性渐变, 颜色沿着一条直线发生变化
```css
	linear-gradient()
		linear-gradient(red, yellow) 红色在开头 黄色在结尾 中间是过渡区域
		线性渐变的开头 我们可以指定一个渐变的方向
		to top
		to right
		to left
		to bottom
	
		deg 度数
		turn 圈数
		不同的方向可以组合 比如 to top left
		
		渐变可以指定多个颜色 多个颜色默认平均分布
			也可以手动指定渐变的分布情况(指定渐变颜色的起始位置)

		linear-gradient(to 90deg, red 50px, yello 100px, green 200px)
```
```css
/*
	平铺线性变换 repeating-linear-gradient()
*/
```

径向渐变 

```css
/*
	默认情况下径向渐变的形状根据元素的形状来计算的
	正方形 圆形
	长方形 椭圆
	默认半径是 圆心 到 最远角 的距离
	语法:
		radial-gradient(大小 at 位置, 颜色 位置, 颜色 位置, ...);
 			大小:
				circle 圆形
				ellipse 椭圆
				closest-side 近边
				closest-corner 近角
				farthest-side 远边
				farthest-corner 远角
				xxpx xxpx 具体值
			位置:
				top right left center bottom 
				xxpx xxpx
*/
```

```css
/*
	重复径向渐变 repeating-radial-gradient
*/
```



#### table样式

```css
/*
	table是一个块元素 但是默认宽度不是100% 而是被内容撑开 margin-right独占一行
		width 设置表格宽度 
		height 设置表格高度
		border 设置表格的边框
		border-spacing 指定单元格边框的距离	
		border-collapse: collapse 设置单元格边框的合并
		
	tr 如果表格没有使用tbody而是直接使用tr
		那么浏览器会自动创建一个tbody 并且将tr全部放到tbody中
		tr不是table的子元素
	td
		border 设置单元格的边框
		td里的内容默认是垂直居中的 可以通过vertical-align设置文字的垂直方向的对齐方式
		text-aligh设置水平对齐方式
*/
/*
		单元格元素
		display: table-cell 设置一个元素称为单元格元素
*/
```

不要使用表格来布局

#### 过渡 transition

```css
/*
	transition-property 指定要执行过渡的属性
		只能过渡计算属性 过渡必须是一个有效值向另一个有效值过过渡(不能为auto)
		多个属性用 , 隔开
		使用all可以过渡所有属性
*/
	transition-property: height, color;
	transition-property: all;
/*
	transition-duration 指定过渡的持续时间
		时间单位 s ms
		多个值用 , 隔开 和transition-property 指定的值一一对应
*/
	transition-duration: 1s, 200ms;
/*
	transition-timing-function 过渡的时序函数
		指定过渡的执行方式
		可选值:
			ease 默认值 缓慢过渡 慢速开始 慢速结束
			linear 匀速
			ease-in 加速
			ease-out 减速
			ease-in-out 先加速后减速
			cubic-bezier() 贝塞尔曲线
				http://cubic-bezier.com
			steps() 分步执行过渡效果
				可以设置第二个值 用 , 隔开
					end 默认值 在时间结束时执行过渡
					start 在时间开始是执行过渡
*/
	transition-timing-function: cubic-bezier(1,.01,0,.99);
	transition-timing-function: steps(2, start);
/*
	transition-delay 过渡效果延迟, 等待一段时间后执行过渡
*/
	transition-delay: 2s;
/*
	transition简写属性 transition-duration 在 transition-delay 前面
*/
/*
	多个过渡用 , 隔开
*/
	transition: width 1s linear .5s,
				height 2s ease-in;
```

#### 动画animation

```css
/*
	设置关键帧 使用@keyfranmes 指定一个名字 
*/
@keyframes name{    
    /* from表示动画开始的位置 也可以写成0% */
    from{
        margin-left: 0;
        background-color: red;
    }
    /* to表示动画结束位置 也可以写成100% */
    to{
        margin-left: 700px;
        background-color: green;
    }
}

/*
	animation-name 指定关键帧名字
*/
animation-name: name;
/*
	animation-duration 动画执行时间 
	animation-timing-function 动画的时序函数
	animation-delay 延时

	animation-iteration-count 动画执行次数
		可选值:
			次数 
			infinite 无限执行	

	animation-direction 动画运行的方向
		可选值:
			normal 默认值 从 from 向 to 运动
			reverse 从 to 向 from 运动
			alternate 从 from 向 to 运动 交替执行
			alternate-reverse 从 to 向 from 运动 交替执行

	animation-play-state 设置动画执行状态
		可选值:
			running 默认值 动画执行
			paused 动画暂停

	animation-fill-mode 动画填充模式
		可选值:
			none 默认值 动画执行完毕回到原本的样式
			forwards 动画执行完毕会停止在to的样式
			backwards 动画延时等待时 元素处于from样式
			both 结合forwards 和 backwards

	animation 简写属性 duration 必须在 delay 前面
		
*/
/*
	关键帧
		可以指定多个x%来指定动画从from到to的中间阶段的样式
*/
@keyframes name{
    from{
        margin-top: 10px;
    }
    %20, %40, %60, %80{
        margin-top: 10px;
    }
    to{
        margin-top: 20px
    }
}
/*
	animation 动画库
*/
```

#### 变形

```css
/*
	变形是指通过css改变元素的 形状 和 位置
		变形不会影响到页面布局
		transform 设置变形效果 指定多个值用空格隔开
			平移:
				translateX() 沿着X轴方向平移
				translateY() 沿着Y轴平移
				translateZ() 沿着Z轴平移
					平移单位也可以是百分比 是自身的长度的百分比
*/

/*
	设置不定长/高元素的居中	
*/
.box{
    position: absolute;
    left: 50%;
    right: 50%;
    transform: translateX(-50%) translateY(-50%);
}
/*
	设置元素漂浮效果
*/
.box{
	transition: transform .3s, box-shadow .3s;
}
.box:hover{
    transform: translateY(-10px);
    box-shadow: 0 10px 10px rgba(0, 0, 0, .3);
}

/*
	元素变形的坐标轴会跟元素一起移动 而不是宏观坐标 坐标轴的原点是元素的中心

	设置body的css属性指定网页的视距perspective 指定视距后才能开启立体效果 否则变换只能呈现2d的平面效果

	z轴默认垂直于屏幕 正向朝着屏幕外的方向
		translateZ() 调整元素在Z轴的位置 
*/
/*
	transform: translate(x, y);
*/
/*
	transform-style
	设置元素的子元素位于3d空间中还是平面
		flat 平面
		preserve-3d 3d空间
*/
```

旋转

```css
/*
	transform 可以指定元素沿x y z 轴旋转
		rotateX()
		rotateY()
		rotateZ()
	旋转单位可以是:
			度数 deg
			圈数 turn
*/
	transform: rotateX(45deg);
	transform: rotateY(.25turn);
/*
	正值为顺时针旋转
	元素旋转有先后顺序
		transform: translateZ(400px) rotateY(180deg); 往后旋转
		transform: rotateY(180deg) translateZ(400px); 向前旋转
	backface-visibility 是否显示元素背面
		visible  默认值 显示
		hidden 隐藏
*/
```

缩放

```css
/*
		scaleX()
		scaleY()
		scaleZ()
		scale() 每个轴都缩放
*/
	transform: scale(1.2); 放大1.2倍
```

变形原点

```css
/*
	transform-origin
			center 默认值
		可选值
			水平 垂直 
			水平 left center right 数值
			垂直 top center bottom 数值
*/
```



#### less

看文档

#### flex

```css
/*
	flex(弹性盒 伸缩盒)
		是css中的又一种布局手段, 它主要用来替代浮动完成页面布局
		flex可以使元素具有弹性 让元素可以跟随页面大小的改变而改变
		弹性容器
			要使用弹性盒 必须将一个元素设置为弹性容器
			使用display 设置弹性容器
				display: flex 块弹性容器
				display: inline-flex 行内弹性容器

			flex-direction 指定容器中弹性元素的排列方式
				可选值: 
					row 默认值 弹性元素在容器中水平排列(左向右)
					row-reverse 弹性元素在容器中反向水平排列(从右向左)
					column 弹性元素纵向排列(自上向下)
					column-reverse 弹性元素纵向反向排列(自下向上)

				主轴: 弹性元素的排列方向称为主轴
				侧轴: 与主轴方向垂直的称为侧轴
			flex-wrap 设置元素在弹性容器中是否自动换行
				可选值:
					nowrap 默认值 元素不会自动换行
					wrap 元素沿着辅轴的方向自动换行
					wrap-reverse 元素沿着辅轴反方向自动换行
			flex-flow flex-wrap 和 flex-direction的简写属性
				flex-flow: row wrap;

			justfy-content 如何分配主轴上的空白(主轴上的元素如何排列)
				可选值:
					flex-start 元素沿着主轴起边排列
					flex-end 元素沿着主轴终边排列		
					center 元素居中排列
					space-around 空白分布到每一个元素两侧
					space-evenly 空白均匀分布
					space-between 空白分布到元素之间

			align-items 元素在辅轴上如何对齐
				可选值:
					stretch 默认值 将长度设置为相同的值
					flex-start 沿着辅轴起边对齐
					flex-end 沿着辅轴终边对齐
					center 居中对齐
					baseline 基线对齐
			align-content 如何分配辅轴上的空白
				可选值: 和justfy-content一样

			注意: 当 align-items 和 align-content 同时存在时 align-items 失效

		弹性元素
			弹性容器的子元素是弹性元素(弹性项)
			一个弹性元素可以同时是弹性容器
			flex-grow 指定弹性元素的伸展系数
				当父元素有多余的空间时 子元素如何伸展 
				父元素的剩余空间 会按比例分配
				0 默认值 不伸展
			flex-shrink 弹性元素收缩系数
				当父元素空间不足以容纳子元素时 对子元素收缩
				子元素按比例收缩 flex-shrink 根据缩减系数和元素大小计算的
				0 默认值 不收缩
			flex-basis 指定元素在主轴上的基础长度
				如果主轴是横向的 则该值就是元素的宽度
				如果主轴是纵向的 则该值就是元素的高度
				auto 默认值 表示参考元素自身的高度或宽度
					如果指定了具体的值 则以该值为准
			flex  简写属性 可以设置flex-grow flex-shrink flex-basis 必须按顺序指定
				还有一些可选值:
					initial 等价于flex: 0 1 auto;
					auto  等价于flex: 1 1 auto;
					none 等价于flex: 0 0 auto;

			align-self 覆盖当前弹性元素上的align-items

			order 指定元素的排列顺序
			
*/
```

#### 像素比 

```css
/*
	像素比 = 物理像素 / 逻辑像素
*/
```

#### vw

```css
/*
	视口 即 显示窗口
		手机出厂时默认的视口大小都是 980px
		苹果公司提出将网页视口大小设置成和屏幕的大小一样大
			<meta name="viewport" content="width=device-width", initial-scale="1.0">
	1vw = 1% view port width
	100vw = view port width

	x_px / width_px = 1vw / 100vw
	x_px = width_px (1 / 100)vw
	1_px = 1vw / x
	
	由于font-size在一些浏览器里如果<12px 会设置为12px 
		则需要把font-size扩大40倍 在使用rem时 /40
*/
html {
	font-size: (1 / x) * 40vw;
}
div {
    width: 20/40rem;
}

```

#### 媒体查询

```css
/*
	响应式布局
		网页可以根据不同的设备 或 窗口大小呈现出不同的效果
		使用响应式布局 可以使一个网页适应所有的设备
		响应式布局的关键是媒体查询
		通过媒体查询 可以为不同设备 或不同的状态分别设置样式


	媒体查询
		语法 @media 查询规则
		媒体类型
			all 所有设备
			print 打印设备
			screen	带屏幕的设备
			speech 屏幕阅读器
		可以使用 , 链接多个媒体类型 表示 或 
		可以在每一类型前面加一个only 表示只有
			only的使用主要是为了兼容一些老的浏览器

	媒体特征
		width 视口的宽度
		height 视口的高度
		
		min-width 视口的最小宽度(视口大于指定宽度时生效)
		max-width 视口的最大宽度(视口大于指定宽度时生效)

		样式的分界点, 我们称其为断点, 也是网页的样式会在这个点时发生变化
		一般比较常用的断点
			< 768 超小屏幕
			> 768 小屏幕
			> 992 中屏幕
			> 1200 大屏幕
*/
@media only screen and (min-width: 768px) and (max-width: 1199px) {
}
/*
	@media依然是css语句 遵循css的 继承 和 覆盖 特性
*/
/*
	@media 可以写在 css 选择器里
	@media 可以写在 link标签 里 为指定特定的css设置media属性
		<link rel="stylesheet" href="xx.css" media="only screen and (min-width: 768px) and (max-width: 1199px)">
*/
/*
	(orientation: portrait) 横屏
	(orientation: landscape) 竖屏
*/
```

#### 网页的版心和通栏

```css
/*
	pc端的版心是固定宽高水平居中的盒子 用来显示网页内容
	通栏是无固定宽度 自适应的盒子
*/
```

#### 文字隐藏的方式

```css
/*
	font-size: 0px;

	让子元素溢出父元素 设置父元素 overflow: hidden;	
*/
```

#### 透明

```css
/*
	透明度
		元素中的所有内容都透明
*/
opacity: .5
```

#### favicon.ico

```html
<!--
	放置在根目录里
	网络搜索 "ico转换" 搜索转换工具
-->
<link ref="shortcut icon" href="favicon.ico" />

```

#### 浏览器内核

```css
浏览器        内核              前缀
chrome       webkit(blink)    -webkit-
safari       webkit           -webkit-
firefox  	 gecko			  -moz-
ie           trident          -ms-
opera        presto           -0-
```