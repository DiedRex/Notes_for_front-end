#前端面试题目大全－HTML
1. Doctype作用？严格模式与混杂模式如何区分？它们有何意义?<br>
<br>
	- 触发器的作用，指示文档类型风格是严格模式的，声明引用 DTD。像WIndows平台的IE5和Netscape4则只提供了怪异模式，其他的浏览器都提供了两种模式的选择。大部分的doctype声明触发严格模式，使文档依据标准的严格模式渲染网页。至于怪异模式，我现在还没接触过。早期浏览器还没有遵循W3C标准的时候，为了保障自己的网页在多数浏览器上能够正确展现，网页开发者不得不遵循一套规则，不过遵循规则必须使得标准一致，于是发生了标准确立的竞争（microsoft和netscape）。严格模式活了下来，但是混杂模式还使存留的。所有现在浏览器都支持两种模式，doctype声明的是严格模式。

2. DoHTML5 为什么只需要写 <!DOCTYPE HTML>？<br>
3. 行内元素有哪些？块级元素有哪些？ 空(void)元素有那些？<br>
	- ```div | p | h1 | h6 | ol | ul | dl | table | address | blockquote | form <br>```
块级元素特点：<br/>
1、每个块级元素都从新的一行开始，并且其后的元素也另起一行。（真霸道，一个块级元素独占一行）
2、元素的高度、宽度、行高以及顶和底边距都可设置。
3、元素宽度在不设置的情况下，是它本身父容器的100%（和父元素的宽度一致），除非设定一个宽度。<br/>
常用的内联元素有：<br/>
```a | span |br| i | em | strong | label | q | var | cite | code |<br>```
内联元素特点：<br/>
1、和其他元素都在一行上；
2、元素的高度、宽度、行高及顶部和底部边距不可设置；
3、元素的宽度就是它包含的文字或图片的宽度，不可改变。<br/>
常用的内联块状元素有：
```img | input```
inline-block元素特点：
1、和其他元素都在一行上；
2、元素的高度、宽度、行高以及顶和底边距都可设置。
```知名的空元素： <br/> <hr/> <img/> <input/> <link/> <meta/> ```
4. 页面导入样式时，使用link和@import有什么区别？
	- 1.老祖宗的差别。link属于XHTML标签，而@import完全是CSS提供的一种方式。link标签除了可以加载CSS外，还可以做很多其它的事情，比如定义RSS，定义rel连接属性等，@import就只能加载CSS了。<br/> 
	<br>
	2.加载顺序的差别。当一个页面被加载的时候（就是被浏览者浏览的时候），link引用的CSS会同时被加载，而@import引用的CSS 会等到页面全部被下载完再被加载。所以有时候浏览@import加载CSS的页面时开始会没有样式（就是闪烁），网速慢的时候还挺明显（梦之都加载CSS 的方式就是使用@import，一边下载一边浏览梦之都网页时，就会出现上述问题）。<br/> <br/>
	3.兼容性的差别。由于@import是CSS2.1提出的所以老的浏览器不支持，@import只有在IE5以上的才能识别，而link标签无此问题。<br><br/>
	4.使用dom控制样式时的差别。当使用javascript控制dom去改变样式的时候，只能使用link标签，因为@import不是dom可以控制的。
5. 五大流浏览器内核及其代表
	>浏览器的内核是分为两个部分的，一是渲染引擎，另一个是JS引擎。现在JS引擎比较独立，内核更加倾向于说渲染引擎。
1、Trident内核：代表作品是IE，因IE捆绑在Windows中，所以占有极高的份额，又称为IE内核或MSHTML，此内核只能用于Windows平台，且不是开源的。
    代表作品还有腾讯、Maxthon（遨游）、360浏览器等。但由于市场份额比较大，曾经出现脱离了W3C标准的时候，同时IE版本比较多，
    存在很多的兼容性问题。
2、Gecko内核：代表作品是Firefox，即火狐浏览器。因火狐是最多的用户，故常被称为firefox内核它是开源的，最大优势是跨平台，在Microsoft Windows、Linux、MacOs X等主
  要操作系统中使用。
   Mozilla是网景公司在第一次浏览器大战败给微软之后创建的。有兴趣的同学可以了解一下浏览器大战
3、Webkit内核：代表作品是Safari、曾经的Chrome，是开源的项目。
4、Presto内核：代表作品是Opera，Presto是由Opera Software开发的浏览器排版引擎，它是世界公认最快的渲染速度的引擎。在13年之后，Opera宣布加入谷歌阵营，弃用了
   Presto 
5、Blink内核：由Google和Opera Software开发的浏览器排版引擎，2013年4月发布。现在Chrome内核是Blink。谷歌还开发了自己的JS引擎，V8，使JS运行速度极大地提高了
讲解比较粗糙，有兴趣的同学可以google搜索下，我就算是抛砖引玉了


6. 你对浏览器内核的理解<br>
	- ```主要分成两部分：渲染引擎(layout engineer或 Rendering Engine) 和 JS 引擎。
渲染引擎：负责取得网页的内容（HTML、 XML 、图像等等）、整理讯息（例如加入 CSS 等），以及计算网页的显示方式，然后会输出至显示器或打印机。浏览器的内核的不同对于网页的语法解释会有不同，所以渲染的效果也不相同。所有网页浏览器、电子邮件客户端以及其它需要编辑、显示网络内容的应用程序都需要内核。
JS引擎则：解析和执行 javascript 来实现网页的动态效果。
最开始渲染引擎和JS引擎并没有区分的很明确，后来 JS 引擎越来越独立，内核就倾向于只指渲染引擎。```
7. 网页验证码是干嘛的，是为了解决什么安全问题？<br>
   - 比较常见的3个用处，防止恶意注册，增加识别能力，植入广告增加收入。
8. 浏览器的渲染机制和原理
	- linkline:<https://mp.weixin.qq.com/s?__biz=MzAxODE2MjM1MA==&mid=2651552869&idx=2&sn=d1adefd78fea714936cdde2092247c52&chksm=8025aba4b75222b27457bc0e5323ab014663b51077d5623c8d45aac5a0b23c59ecadb08ab661&scene=0&key=2f0c8982c7c8cae3dee3c248324245a3fd868fb429946133ad05860504c0a556fe1c5f56b1ff758f7a9cc302496917704b32d7825fed17813167856a45c5faf56be382bd0212c5cc37533aafd6c22c53&ascene=0&uin=MTUzMTQyNDMzNw%3D%3D&devicetype=iMac+MacBookPro12%2C1+OSX+OSX+10.11.6+build(15G31)&version=12010310&nettype=WIFI&fontScale=100&pass_ticket=LxNBCeH4WiZVlUh1lC7z2Iy3kVTu4HNCWt1IKoBS%2BFJhBNyBQwk0jr8naXbfAuoy>
9. HTML5的form如何关闭自动完成功能？<br>

	- 1、在IE的Internet选项菜单里的内容--自动完成里面设置<br>2、设置Form的autocomplete为"on"或者"off"来开启或者关闭自动完成功能<br>3、设置输入框的autocomplete为"on"或者"off"来开启或者关闭该输入框的自动完成功能
10. Label的作用是什么？是怎么用的？（加 for 或 包裹）?
	- FOR属性
		- 功能：表示Label标签要绑定的HTML元素，你点击这个标签的时候，所绑定的元素将获取焦点。
	用法：姓名

	- ACCESSKEY属性：
	  - 功能：表示访问Label标签所绑定的元素的热键，当您按下热键，所绑定的元素将获取焦点。
	用法：姓名

	  - 局限性：accessKey属性所设置的快捷键不能与浏览器的快捷键冲突，否则将优先激活浏览器的快捷键。
11. 如何在页面上实现一个圆形的可点击区域？
	- linkline:<https://www.nowcoder.com/questionTerminal/fe155273580e46dfa2b15875e94a8b96?orderByHotValue=1&questionTypes=111111&page=1&onlyReference=false>
12. 如何实现浏览器内多个标签页之间的通信?
	- 使用本地存储方法
>1.cookie       
 （1）客户端和服务器端都会请求服务器，性能下降
 （2）存储限制，4k
 （3）页面的cookie是共享的
storage
    只是在客户端使用，不会请求服务器处理,存储量比较大,只能存储字符串，非字符串的数据在存储之前会被转换为字符串
   1. seessionStorage
        临时性的，页面打开有，页面关闭没有
        数据不共享
   2.localStorage
        永久性的存储
        数据共享
   3.api
        clear（）删除所有值，ff中没有实现
        getItem（）根据指定的名字name获取对应的值
        key（index）获得index处的值
        removeItem（name）删除由name指定的明值对
        setItem(name，value)
13. tite与h1的区别 、b与strong的区别 、i与em的区别
	- linkline:<http://www.jianshu.com/p/59691c0900d3>
14. hr标签指的是分割线