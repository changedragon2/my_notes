```code
#--------------html------------------
html event 事件
    onchange            ---> 元素被改变
    onclick             ---> 元素被点击
    onmouseover         ---> 鼠标移动到元素上
    onmouseout          ---> 鼠标移开元素
    onkeydown           ---> 用户按下键盘按键
    onload              ---> 浏览器完成页面加载

#--------use style with three ways-------
/* 内联样式表 inline stylesheet
   
<p style="color:red;font-size:10px">

-----------*/
/* 内部样式表

<style type="text/css">
	body{background-color:red}
	p{font-family:monospace}
</style>
-----------*/

/* 外部样式表

<head>
<link rel="stylesheet" type="text/css" href="css/mystyle.css">
</head>

-----------*/

#--------attributes in style---------
font-family:
	monospace
	verdana
	times
	arial

font-size:
	15px

background-color:

color:	#XXXXXX | rgb(xx,xx,xx) | 
	#BAEBDF
	#ACBCCF
	PowderBlue

text-align:
	center

text-decoration:
	none			---> set no underline in <a>

-------------------------------------

#---------global attributes-------
id			----> identifier is unique
class		----> symbol not unique


#-------- Tag ------------

  opening tag		       closing tag
      ^						   ^
	  |						   |
------|------------------------|--------
|	<tag>	 	 xxx		</tag>     |
------------------|---------------------
	|    |	      |        |      | 
	|    |		  v        |      |
	|	 |-----content-----|      |         <tag attribute="value">  xxx  </tag>
	|                             |         <tag attribute="value" />
	|<--------- Element---------->|
		 

/* block level element 块级元素
<h1>~<h4> <p> <ul> <table> <div>
/* inline element 内联元素
<b> <td> <a> <img> <span>

<a href="url">--------------</a>			hypertext reference
attributes:
	href="url"
		   |                               |-> CarbonCopy          |-> BlindCarbonCopy
		   L--> "mailto:3275822459@qq.com?cc=someoby@example.com&bcc=somebody2@example.com&
			subject=This%20is%20Theme&body=This%20is%20contents"  -------> send mail
                         |-> blank
		   |--> #id_label		---> label define in id
	download="filename" ----> define download file name for href="path/to/file"
	target="value"
			|--> _blank
			|--> _self
			|--> _top
			|--> _parent
			|--> framename   ---> use iframe name label as target
	name="label" ----------define a anchor use with <a href="#label" ></a>

		
<img src="path/to/file" />
attributes:
	src="path/to/file"	----> define path to image file
	alt="alternate text"----> use alternate text when img src not found
	width="pixels | %"  ----> set image width
	height="pixels | %" ----> set image height
	align="value"		----> set text align with image ( not recommend)
			|--> bottom		--> default
			|--> middle
			|--> top
	ismap="url"			----> map image
	usemap="url"		----> use image map, with <map><area /></map>	

<area />
attributes:
	shape="value"
			|--> circle
			|--> rect
	coords="x,y,r" | "x1,y1,x2,y2"
			|--> circle location(x,y), radius r
			|--> rect start location(x1,y1), ending location(x2,y2)
	href="url"
	target="_blank" | "_self" | ...
	alt="alternate text"

/* list
<ul><li>----</li></ul>					----> unordered list
attributes:
	type="value"
			|--> disc		---> disc shape
			|--> circle		---> circle shape
			|--> square		---> square shape
<ol><li>----</li></ol>					----> ordered list
attributes:
	type="value"
			|--> (null)		---> use integer
			|--> A			---> use A,B,C...
			|--> a			---> use a,b,c...
			|--> I | i		---> use I II III IV... or i ii iii iv...
<dl><dt><dd>---</dd></dt></dl>			----> defined list
	dt ---> define item
	dd ---> define description
-------------*/




/*--- no closing tag ---
<br />		new line
<hr />		horizon line
<img />		image
<link />	link
-----------------------*/

<i>-----------</i>					italic font
<strong>------</strong>		    	strong
<b>-----------</b>					bold font
<big>---------</big>				big font size
<em>----------</em>					emphasized
<small>-------</small>				small font size

<del>---------</del>				deleted text
<ins>---------</ins>				inserted text

<sub>---------</sub>				subscript
<sup>---------</sup>				superscript

<pre>---------</pre>				preformat text, it keep blank and new line
							it's suitable for show computer program code

<code>--------</code>				computer code
<kbd>---------</kbd>				keyboard input
<tt>----------</tt>					teletype text
<samp>--------</samp>				sample text	
<var>---------</var>				computer variable


<address>							address
Written by <a href="mailto:3275822459@qq.com">changedragon2</a>.<br />
Visit me at http://10.42.0.1:9170/
Anhui, fuyang
China
</address>

<cite>--------</cite>				define title of books
<dfn>---------</dfn>				define item or abbreviation

<abbr title="orignal contents">ori</abbr>			show abbreviation in title
<acronym title="orignal contents">oc</acronym>		show acronym in title	

<bdo dir="rtl">-------</bdo>				show text from right to left

<blockquote>----------</blockquote>			define long quote, insert new line and padding
<q>-------------------</q>					define short quote

/* inline frame
<iframe src="url">------</iframe>
attributes:
	src="url"
	width="pixels"
	height="pixels"
	frameborder="value"		set frame border size
					|--> 0  no border
    name="label"	


<button>---------</button>			----> define a button
attributes:
	onclick

#------------------------CSS-------------------------------

		attribute  <--|    |--> value 
         ^       _____|____|      ^ 
         |      |     |        |--|
	h1 {color:red; font-size:15px;}

/* CSS层叠顺序 */
	行内样式表 >> 外部or内部样式表 >> 浏览器默认样式

/* 注释 */
	/* comments */	CSS无 // 注释

/* color */
	Tomato, DodgerBlue, MediumSeaGreen


/* CSS selector
1.simple selector 简单选择器
----by tag 
		p{color:red; text-align:center;}
		p,h4{font-size: 15px;}
		
----by id	/* '#' define style with id="label" */
		#label{background-color:lightblue;}
		p#label{xxx:xx;}	---> <p>元素且id值为label

----by class '.' define style with class="label"
		.label{padding:40px;}
		p.label{xxx:xx;}	---> <p>元素且class值为label

----all element
		*{font-family: monospace;}

2.combination selector
----descendant selector('blank') 后代选择器
		div p {background-color: #ff00ff;}		---> 选择div内的所有p元素
----child selector('>') 子选择器
		div > p {background-color: #ff00ff;}	---> 选择div内的所有子级p元素
----adjacent brother selector('+') 相邻兄弟选择器
		div + p {background-color: #ff00ff;}	---> 选择div后相邻的p元素
----generic brother selector('~') 通用兄弟选择器
		div ~ p {background-color: #ff00ff;}	---> 选择div后同级别的p元素

3.pseudo class selector 伪类选择器
		[selector]:[pseudo-class] {color: #ff00ff;}
pseudo-class:
	link				      ---> unvisited link
	visited			      ---> visited link
	hover				      ---> mouse hang on link
	active				    ---> active link
  first-child       ---> the first child
  last-child        ---> the last child
  lang(language)    ---> special language
  checked           ---> 选中的元素
  disabled          ---> 禁用的元素
  empty             ---> 没有子元素
  enabled           ---> 已启用的元素
  first-of-type
  last-of-type
  in-range          ---> 具有指定范围值
  valid
  invalid           ---> 具有无效值
	...

		a:link {color: #ff0000;}	---> 设置未被选择的链接为红色
    p i:first-child { color: #ff0000;}  ---> 所有p中的第一个i元素
    p:first-child i{ color: #ff0000;}   ---> 第一个p中的所有i元素
    q:lang(en) { quotes: "~" "~" ;}     ---> 为lang="en"的q元素定义引号

  伪元素：
    [selector]::[pseudo-elements] { color: #ff0000;}
  after
  before
  first-letter
  first-line
  selection

4.attribute selector 属性选择器
	[attribute] {xxx:xx;}
	[attribute="value"] {xxx:xx;}	---> 值为value
	[attribute~="value"] {xxx:xx;}  ---> 含有value单词的值 不包含连字符'-'
	[attribute|="value"] {xxx:xx;}	---> 以value开头单词的值 包含连字符'-'
	[attribute^="value"] {xxx:xx;}	---> 以value开头 不必是完整单词
	[attribute$="value"] {xxx:xx;}	---> 以value结尾 不必是完整单词
	[attribute*="value"] {xxx:xx;}	---> 包含value	不必是完整单词
		a[target] {background-color: #ff00ff;}			---> 选择带有target属性的<a>元素
		a[target="_blank"] {background-color: #ff00ff}	---> 选择有target属性且值为_blank的<a>元素
		[title~="flower"] {border: 5px solid yellow;}	---> 选择title属性且值含有flower的元素


/* text */
color:					----> 文本颜色
text-align:				----> 文本水平对齐方式
	left
	center
	right
	justify		---> 拉伸每一行 使每一行具有相等的宽度 且左右边距是直的
direction/unicode-bidi:
  rtl		bidi-override
vertical-align:			----> 元素垂直对齐方式
	top
	middle
	bottom
text-decoration:		----> 设置或删除文本装饰
	overline		---> 上划线	
	line-through	---> 穿过文本
	underline		---> 下划线
	none			---> 可用于删除链接的下划线
text-transform:
	uppercase		---> 文本字母都变为大写
	lowercase		---> 文本字母都变为小写
	capitalize		---> 单词首字母大写

text-indent:			----> 文本缩进

text-shadow:			----> 文本添加阴影
	[h-shadow]px	---> 水平阴影,允许负值(必须)
	[v-shadow]px    ---> 垂直阴影,允许负值(必须)
	[blur]px		---> 模糊距离
	[color]			---> 阴影颜色
  p{text-shadow: 2px 2px 5px red;}

letter-spacing:			----> 字符间距
word-spacing:			----> 单词间距
	0		 ---> 正常
	[num]px  ---> 增大num个像素
	-[num]px ---> 减小num个像素

line-height:			----> 行间距
    normal
    number
    lenght
    %
    inherit

white-space:
	nowrap	 ---> 禁用元素内文本换行

/* font */
font-family:			----> 设置字体
font-style:
	normal	 ---> 正常
	italic   ---> 斜体
	oblique  ---> 倾斜 和斜体相似 支持较少
font-weight:			----> 字体粗细
	normal
	lighter
	bold
	[num]
font-variant:			----> 字体变体
	normal
	small-caps	---> 小型大写字母
font-size:				----> 字体大小
	[num]em		---> 推荐使用 1em = 16px
	[num]px
	[num]vm		---> 响应式字体大小 1vw = 视口宽度的 1%

/* color */
opacity:                ----> 设置透明度 子元素会继承透明度(可使用RGBA)

/* hidden */
display:                ----> 设置元素显示方式
    inline      ---> default 显示为内联元素
    block       ---> 显示为块级元素
    none        ---> 不显示
    inline-block
    list-item
    run-in
    table
    inline-table
    ...
    inherit
visibility:             ----> 设置元素是否可见
    visible     ---> default
    hidden      ---> 隐藏 仍占用空间
    collapse    ---> 表格中使用可删除行列 其他元素呈现为hidden
    inherit

/* overflow */ 溢出
overflow:               ----> 元素内容太大无法容纳时处理方式
                    仅适用指定高度的块元素
    visible     ---> default 溢出不裁减 在元素渲染
    hidden      ---> 溢出部分裁减 不可见
    scroll      ---> 溢出部分裁减 且添加滚动条可查看其余内容
    auto        ---> 类似scroll 仅必要时添加滚动条
overflow-x/overflow-y   ----> 处理水平/垂直方向溢出

/* float and clear */ 浮动和清除
float:                  ----> 规定元素如何浮动
    none        ---> default 不浮动
    left/right  ---> 浮动到其容器左右侧
    inherit
clear                   ----> 规定哪些元素可以浮动与被清除元素旁
    none        ---> default 允许两侧有浮动元素
    left/right  ---> 左侧/右侧 不允许浮动元素
    both        ---> 两侧不允许浮动元素
    inherit
.clearfix{overflow: auto;} 防止浮动元素溢出 可能看到滚动条
.clearfix::after{
    content: "";
    clear: both;
    display: table;
}

/* list */
list-style-type:		----> 列表标记类型
	circle
	square
	upper-roman/lower-roman		---> 罗马数字
	upper-alpha/lower-alpha
	none
list-style-image:		----> 将图像作为列表标记项
	url('path/to/img')
list-style-position:	----> 指定标记项位置
	outside			---> default position
	inside
----简写
list-style:
	list-style: square inside url("xxx.gif")


			

/* background
background-color: lightblue;
background-image: url("path/to/file");
background-repeat:
    repeat-x/repeat-y
    no-repeat
background-position:
background-attachment:      ----> 背景图像是滚动还是固定
    fixed
    scroll
background-size:            ----> 背景图像大小
{object.style.backgroundSize}
    [length-width length-height]
    %
    cover
    contain


/* border */
border-style:		----> 边框样式
	dotted		---> 点线
	dashed		---> 虚线
	solid		---> 实线
	double		---> 双边框
	groove		---> 3D
	ridge		---> 3D
	inset		---> 3D
	outset		---> 3D
	none		---> no border
	hidden		---> hidden border
border-width:		----> 边框宽度
	[num]px
	[num]pt
	[num]cm
	[num]em
	thin
	medium
	thick
border-color:		----> 边框颜色 未设置将继承元素颜色
	[name]
	[HEX]
	[RGB]
	[HSL]
	transparent
----简写
  border		----> 指定所有边框 boder-style必须指定
			  |--------------------------^
    border: solid 5px red;
----指定
  border-left	---> 指定左边框
  border-bottom-style	---> 指定下边框样式
--------
border-radius:		----> 添加圆角边框
	[num]px;

/* margin */ 外边距
----简写
margin:				----> 所有外边距 允许负值
	auto
	length[px, pt, cm]
	%
	inherit		---> 继承父元素
margin-top
margin-right
margin-bottom
margin-left

/* padding */ 内边距
----简写
padding:			----> 所以内边距 不允许负值
	length[px, pt, cm]
	%
	inherit
padding-top
padding-right
padding-bottom
padding-left

box-sizing: border-box      保持总宽度不变 即使增加了左右内边距 

/* width height */	 宽度和高度 不包括内外边距和边框
width/height:
	auto
	length[px, cm]
	%
	initial
	inherit
max-width/max-height:			----> 为宽度和高度设置最大值 易于在小窗口使用
min-width/min-height:			----> 为宽度和高度设置最小值
	length[px, cm]
	%
	none		---> 无最值	

/* position */ 位置
position:                       ----> 设置元素定位方式
    static      ---> default 静态 不受top bottom left right属性影响
    
    relative    ---> 相对正常位置定位
    fixed       ---> 固定 相对窗口定位 滚动页面也始终位于同一位置
    absolute    ---> 相对最近的祖先元素(非static)定位 若没有则使用body 会随页面一起滚动
    sticky      ---> 粘性定位 在相对和固定之间切换 /*对Safari加上 position:-webkit-sticky */
left/right/top/bottom:          ----> 设置元素位置 不适用static元素
    [num]px
z-index:                        ----> 设置重叠元素的堆叠顺序 
clip:                           ----> 裁减绝对定位元素
    auto        ---> 不裁减
    [shape]
        |--> rect(top, right, bottom, left)
            例如clip: rect(10px,  64px,  74px, 0px) 裁减64x64 pixels 图片得到32x32 pixels
                         v
                |--32px--|
    - -  /      --------------------
       o- >-----~~~~~~~~~~------------< 10px
    - -  \  |   ~~~保留~~~         -
           32px ~~~~~~~~~~         -
            |   ~~~内容~~~         -
          >-----~~~~~~~~~~------------< 74px
                -        -         -
                -        -         -
                -        -         -
                --------------------
                         -
                         ^
                         64px

    inherit

/* outline */ 轮廓
注意：轮廓与边框不同！不同之处在于：轮廓是在元素边框之外绘制的，并且可能与其他内容重叠。同样
，轮廓也不是元素尺寸的一部分；元素的总宽度和高度不受轮廓线宽度的影响。
outline-style:					----> 轮廓样式
	dotted
	dashed
	solid
	double
	groove
	ridge
	inset
	outset
	none
	hidden
outline-color:
outline-width:
outline-offset:			---> 轮廓偏移 在轮廓与边框之间加入透明空间
----简写
	outline



    margin-left                         margin-right
     ^                                       ^
     |  padding-left         padding-right   |
     |_     ^                          ^     |
       |    |                          |     |
    |<-->|<-->|<------------------->|<--->|<--->|
    --------------------------------------------- ---
    -            margin(外边距)                 -  |---> margin-top
    -                                -> border  -  |
    -     ___________________________|____      -  _    -> border-top-width
    -    |                                |     -  |
    -    |      padding(内边距)           |     -  |---> padding-top
    -    |                                |     -  _
    -    |   _ ----------------------     |     -  ^
    -    |   ^ -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   | -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   h -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   e -~~~~~~~~~~~~~~~~~~~~-     |     -
    -    |   i -~~~Elements(元素)~~~-     |     -  -----------> height
    -    |   g -~~~~~~~~~~~~~~~~~~~~-     |     -
    -    |   h -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   t -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   | -~~~~~~~~~~~~~~~~~~~~-     |     -  |
    -    |   v -~~~~~~~~~~~~~~~~~~~~-     |     -  V
    -    |   _ ----------------------     |     -  _
    -    |     |<------width------->|     |     -  |
    -    |                                |     -  |---> padding-bottom 
    -    ----------------------------------     -  _ 
    -                                           -  |
    -                                           -  |----> margin-bottom
    ---------------------------------------------  _



#--------------------JavaScript-------------------------
--注释
// or /* */

javascript 对大小写敏感

getElementById("id_label")					----> get element with id

--change contents
document.getElementById('id_label').innerHTML
--change attribute
document.getElementById('id_label').[attribute]
--change css element
document.getElementById('id_label').style.fontSize = '[num]px'
--hidden element
document.getElementById('id_label').style.display = 'none'
--display hidden element
document.getElementById('id_label').style.display = 'block'

--外置脚本
<script src="path/to/js"></script>

--output
window.alert()      --警告框输出
console.log()       --控制台输出
document.write()    --页面输出(会覆盖原始内容)

var         --声明变量， 可以在声明前使用变量
let         --声明块作用域变量
const       类似let，但是必须声明时赋值

/ * data type */ 数据类型
var length = 7;                                         ----> 数值
var string = "Gates";                                   ----> 字符串
var example = ["Posrch", "Volove", "Bshel"];            ----> 数组
var object = {name:"change", age:"20", sex:"male"};     ----> 对象 对象无法比较

运算符
==          ---> 值相等为 true
===         ---> 值相等且类型相同为 true

typeof          返回变量类型
  原始数据值
     |--> string
     |--> number
     |--> boolean
     |--> undefined
  负责数据
     |--> function
     |--> object        如 数组 对象 null

undefine 和 null
typeof undefined    // undefined
typeof null         // object
null === undefined  // false
null == undefind    // ture

/* function */ 函数
function func_name(argv1, argv2,...){
    /* function body */
}

this        ---> 该函数的拥有者

/* string */ 字符串
length属性                                              ----> 返回字符串的长度
[variable_string].length

---搜索字符串
indexOf('string') / lastIndexOf('string')               ----> 查找字符串 未找到返回 -1
[variable_string].indexOf('xxx')        ----> 返回字符串xxx第一次出现的位置 0是第一个 
[variable_string].lastIndexOf('xxx')    ----> 返回字符串最后出现的位置
indexOf('string', position) / lastIndexOf('string', position)  position是搜索的起始位置

search()            ----> 搜索字符串 返回匹配的位置

indexOf() 和 search() 区别 
search() 无法设置第二个参数 可以使用正则表达式
indexOf() 无法使用更强大的搜索值(正则表达式)

---提取字符串
slice(start, end)
substring(start, end)
substr(start, length)


/* backslash escape */ 转义字符
\'      ---> '
\"      ---> "
\\      ---> \
\b      ---> [backspace] 退格
\f      ---> 换页
\n      ---> 换行
\r      ---> 回车
\t      ---> 水平制表符
\v      ---> 垂直制表符


```