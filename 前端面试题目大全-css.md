#前端面试大全CSS篇
1. 介绍一下标准的CSS的盒子模型？与低版本IE的盒子模型有什么不同的？
	- linkline:	<https://github.com/ivanberry/CSS-Knowledge/issues/3>
2. CSS选择符有哪些？哪些属性可以继承？优先级算法如何计算？
	- 1、id选择器（#）| 类选择器(.) ｜标签选择器（div、h1、p）|相邻选择器（h1+p）|子选择器
     
3. CSS优先级算法如何计算？
	- 	优先级就近原则，同权重情况下样式定义最近者为准;
载入样式以最后载入的定位为准;
优先级为:!important > id > class > tag
important比内联优先级高(style)
4. CSS3新增伪类有那些？
	- 
p:first-of-type 选择属于其父元素的首个 ```<p> 元素的每个 <p> 元素。```<br>
p:last-of-type  选择属于其父元素的最后 ```<p> 元素的每个 <p> 元素。```<br>
p:only-of-type  选择属于其父元素唯一的 ```<p> 元素的每个 <p> 元素。```<br>
p:only-child    选择属于其父元素的唯一子元素的每个```<p> 元素。```<br>
p:nth-child(2)  选择属于其父元素的第二个子元素的每个``` <p> 元素。```<br>
:enabled :disabled 控制表单控件的禁用状态。<br>
:checked        单选框或复选框被选中。<br>
5. 如何居中div？如何居中一个浮动元素？如何让绝对定位的div居中？
	- 内容居中｛text-align:center；}
	- div水平居中｛margin:0 auto;}
	- 垂直居中｛position:absolute;left:50%;top:50%;margin-left:宽度的一半px;margin-top:高度的一半;}
	- 居中一个浮动元素｛第一种，position:relative很重要。
如果父元素相对定位，子元素绝对定位，此时依旧是margin-left: 50%, left: -5px;5px时子元素高度的一半｝
	- 绝对定位的div居中｛position:absolute;top:50%;left:50%;argin-left:高度的一半px;margin-top:宽度的一半;｝
6. display有哪些值？说明他们的作用？
	- linkline:<http://blog.csdn.net/sjinsa/article/details/70820204><br>
	常用的有:<br>
	none:表示此元素不显示<br>
	block:此元素讲以块级元素显示，此元素前后将带有换行符；<br>
	inline:默认值，元素会被显示为内联元素，前后没有换行符；<br>
	inline-block:行内块级元素。<br>
7. position的值relative和absolute定位原点是？
	- relative（相对定位）：定位原点是元素本身所在位置；<br> 
absolute（绝对定位）：定位原点是离自己这一级元素最近的一级position设置为absolute或者relative的父元素的左上角为原点的
8. CSS3有哪些新特性？
	- linkline:<https://www.nowcoder.com/questionTerminal/85d16107dc074d52a69f2e86f08a69b1>
9. 3栏布局之中间宽度自适应（双飞燕布局、圣杯布局）
	- 原理：父div设置padding为边沿需要流出来的宽度比如padding:0 120px 0 140px;(120和140是留)
	- 然后中间的div设｛position:relative;width:100%;｝先把空间挤满；
	- 左边的设置为｛position:absoulte;top:20px;width:200px;margin-right:-100%;left:200px;
	- 右边的设置为{position:absoulte;top:20px;width:200px;margin-left:-100%;right:200px;
	- 自适应布局-------------------<https://www.zhihu.com/question/21504052>
10. sass的4种style变异方法
	- sass --watch test.scss:test.css --style nested  嵌套输出<br>
	- sass --watch test.scss:test.css --style expanded  展开大括号对齐的嵌套输出
	- sass --watch test.scss:test.css --style compact 紧凑在一行的输出
	- sass --watch test.scss:test.css --style compressed 压缩代码输出 <br/>
	```默认情下使用的是第一种```
11. sass的变量命名符和伪类命名等符号
	- $变量命名符号;
	- &伪类的标志前缀;
	- @mixin与@include连用，一个定义宏，一个使用宏。
	- @extend继承存在的类样式块
	- %占位符，必须配合@extend使用
12. sass运算px和in是同种符号可以运算，但px和em不是同类符号不可运算，运算时运算符号的两旁必须留有空格，乘除法的两个运算符不能同时带单位。
13. 非块级标签的垂直居中
	- 比如```a | span |br| i | em | strong | label | q | var | cite | code |<br>```等可以设置｛text-align:center;line-height:父元素高度;}前提是span等标签设置｛display:inline-block(或者block);设置宽高;或者父亲div的高度｝
14. css气泡框的实现
	- linkline:<http://www.ruanyifeng.com/blog/2010/04/css_speech_bubbles.html>插入的空元素的上下左右四个border皆是一个三角形，合成一个正方形。
15. css3响应式布局<https://www.zhihu.com/question/20976405>
	- 弹性图片----------img{max-width:100%;}
	- @media
	- 流式布局
	- 自适应布局
	- Flexbox
16.