#js代码笔记
- js绑定代码的三种方法
   - DOM元素中直接绑定
   - javascript代码中绑定
   - 绑定事件监听函数
   
###在DOM元素中进行绑定



###DOM元素获取
1. 在这个文档中，找到ID叫做“menu”的元素，得到这个元素中所有的“li”标签的内容<br>
如果写成var ttt=document.getElementById("menu").getElementsByTagName("li"); <br>
那么,ttt就是一个数组，存放了这些"li""/li"的内容

>
	function getData() {
	var list = Document.getElementById('source').getElementByTagName('li');
	var data = num[];<br>
	for(var i = 0;i<list.length;i++){
		var city = list[i].innerHTML.split('空气质量:')[0];
		var num  = list[i].children[0].innerHTML;
		data.push([city,num]);
	}
  	return data;
	}



1. ```ECMAscript6新增特殊属性```
	- let，局部变量，有｛｝含括。在｛｝外无法使用。var是函数变量，只要定义了，在某个函数中即可食用，使用后就停留在此函数的作用域中。
	- const 定义常量，定义之后无法修改，不可修改，const声明时必须赋值，定义后无法赋值－通常用于引入库引入模版。
	- 反当引号，1前面的建｀｀，称为字符串模版。eg:var str =\`我是一名程序员\`，如果var a = '产品经理'；字符串插入可用var str =\`我是一名${a}\`,调用变量a。console.log(str);即时我是一名产品经理。以前是'abc'+变量名+'ef';现在是\` abc${变量名｝ef \`;
	- 结构赋值：var [a,b,c] = 1,5,12;congsole.log(a,b,c);输出1，5，12。还可以 var [a,b,c]=[a:5,b:1,c:12];输出是5，1，121。
	- 结构赋值必须有模式匹配，比如var arr=[{a:"kk",b:"233",c:"gba"}];var[{a,b,c}]=arr;console.log(a,b,c);输出是kk, 233,gba;结果必须要匹配，括号引号要 对上。
	- 结构赋值可以给默认值，比如var {time=12,id=0}={};console.log(time)是12。
2. ```数组复制```的方法。
	- 循环 ----即时var arr1和var arr2两个数组，用一个for循环一一对应复制。
	- Array方法 ----即是是用 var arr2 = Array.from(arr1);
	- 黑科技方法 ----var arr2 = [...arr1],...是一个标记。
3. js中的等性运算符比较复杂
	- 在 ECMAScript 中，等号由双等号（==）表示，当且仅当两个运算数相等时，它返回 true。非等号由感叹号加等号（!=）表示，当且仅当两个运算数不相等时，它返回 true。为确定两个运算数是否相等，这两个运算符都会进行```类型转换(类型转换只是为了比较，并没有更改运算符本身的数据类型)```
	- 如果一个运算数是 Boolean 值，在检查相等性之前，把它转换成数字值。false 转换成 0，true 为 1。
	- 如果一个运算数是字符串，另一个是数字，在检查相等性之前，要尝试把字符串转换成数字。
	- 如果一个运算数是对象，另一个是字符串，在检查相等性之前，要尝试把对象转换成字符串
	- 如果一个运算数是对象，另一个是数字，在检查相等性之前，要尝试把对象转换成数字
	- 即使两个数都是 NaN，等号仍然返回 false，因为根据规则，NaN 不等于 NaN。
	- 值 null 和 undefined 相等
	- 在检查相等性时，不能把 null 和 undefined 转换成其他值。
	- 如果某个运算数是 NaN，等号将返回 false，非等号将返回 true。
	- 如果某个运算数是 NaN，等号将返回 false，非等号将返回 true
	- 如果两个运算数都是对象，那么比较的是它们的引用值。如果两个运算数指向同一对象，那么等号返回 true，否则两个运算数不等。
4. js中的```全等号和非全等号```
	- 等号和非等号的同类运算符是全等号和非全等号。这两个运算符所做的与等号和非等号相同，只是它们在检查相等性前，不执行类型转换
	- 全等号由三个等号表示（===），只有在无需类型转换运算数就相等的情况下，才返回 true
	- 非全等号由感叹号加两个等号（!==）表示，只有在无需类型转换运算数不相等的情况下，才返回 true。
5. break和continue
	- break 语句可以立即退出循环，阻止再次反复执行任何代码。
而 continue 语句只是退出当前循环，根据控制表达式还允许继续进行下一次循环。
	- break 语句和 continue 语句都可以与有标签的语句联合使用，返回代码中的特定位置。如break obtion1;就是break到obtion1:下的代码进行运行。continue也一样
6. with 语句用于设置代码在特定对象中的作用域。
	- with 语句是运行缓慢的代码块，尤其是在已设置了属性值时。大多数情况下，如果可能，最好避免使用它。
7. arguments对象无需明确指出参数名，就能访问到函数
	- 还可以用 arguments 对象检测函数的参数个数，引用属性 arguments.length 。
8. function的length方法 声明了函数期望的参数个数.
9. JavaScript 内存管理 & 垃圾回收机制linkline:<https://neveryu.github.io/2017/02/18/js-memory-management-and-gc/>
10. 函数的call方法，函数名.call(obj,参数1，参数2),使用前先实例化一个名为obj的对象，以及此函数。
11. 同上的还有一个apply(),使用方法相识，函数名.apply(obj,Array("参数1"，"参数2"));后面参数是一个数字，从0到max一一对应。
12. javascript获得dom节点后改变样式要＋.style.样式。
13. 经常使用的dom方法
	- document.getElementById("id名"),获得id名节点
	- document.getElementByTagName('li')，获得li下的所有节点，得到其数组。
	- document.getElementById("id名").appendChild(node),node是前面的到的节点内容，把node节点内容放到id名节点的最后面。
	- removeChild(node);节点方法，去掉id名下的node节点，使用前定义node使其指向要删除的节点。
	- replaceChild(node);@extend previous;代替id名下的点。
	- insertBefore(node);@extend previous;node插入到节点之前。
	- createAttribute();创建属性节点。
	- createElement();创建元素节点(元素指的是li，h1,ul,p等等等等)。
	- createTextNode(node);创建文本节点，node是"我是谁"之类的字符串。
	- getAttribute();返回指定的属性值。
	- setAttribute("属性名"，"value");将某节点的属性设置更改。
14. javascript Dom Event对象事件触发方法。
	- <http://www.w3school.com.cn/jsref/dom_obj_event.asp>
15. for...in 循环，即索引循环，eg:for（var i in arr){console.log(i)};输出0，1，2，3;可遍历json，不能遍历map对象。
16. for...of 循环, 即数组内容循环 eg:for(var i in arr){console.log(i)};输出apple,banana orange pear等。
	- 不可以遍历json，配合map对象使用，循环map对象。
	- map对象，和json格式相似。for(var key of map.keys()){console.log(key);}输出 0，1，2，3;map使用前要实例化，var map = new Map();for（var val of values()){console.log(val);}输出apple,banana,orange,pear;
17. 箭头函数<https://www.liaoxuefeng.com/wiki/001434446689867b27157e896e74d51a89c25cc8b43bdb3000/001438565969057627e5435793645b7acaee3b6869d1374000>
18. promise对象，用于传递异步操作的数据，并根据padding（等待）到成功resovle或者失败rejected两种函数，然后予以执行对应的函数方法。var p1 = new Promise(function(resovle,reject))｛｝<br>	- p1.then --------------------------（function(resovle,reject)）继续判定是否执行。
	- p1.catch  -----------------------获取promise对象的异常
	- p1.race() -----------------------返回一个promise对象，虽先执行返回谁
	- p1.reject()---------------------- 生成一个失败的的promise对象
	- p1.resolve()--------------------- 生成一个成果的promise对象。
19. javascript的BOM，指的是Browser Object Model常用的方法和属性 最大的是window对象。
	- window.innerHeight（document.body.clientHeight） ----------------设置浏览器的高度
	- window.innerWidth (document.body.clinetWidth)-----------------设置浏览器的宽度
	- window.open()  ----------------打开一个新窗口
	- window.close() ---------------关闭单前窗口
20. 对于Window Screen、Location对象，History，Navigator,window可以省略。
	- screen.availWidth --------可用的屏幕宽度
	- screen.availHeigt --------可用的屏幕高度
	- location.href -----------返回页面的url地址
	- location.pathname ----------- 返回url的路径名。
	- location.assign("http://baidu.com") -----------加载到url地址页面。
	- history.back() ------------后退前一额页面
	- history.forward -----------前进到前一个页面
21. javascript的弹窗有三种，分别为alert()警告窗，comfirm()确认窗，prompt()提示框
22. Bom中记时事件setInterval()
	- var myVar=setInterval(function(){myTimer()},1000);
	- clearTimenout(myVar) ------------------ 计时器的执行
23. javascript变量的生命周期
	- javascript变量生命周期在他声明时初始化，局部变量在函数执行完毕后销毁，全局变量在页面关闭后销毁。
24. javascript的事件响应机制
	- <http://www.ruanyifeng.com/blog/2014/10/event-loop.html>
25. Web语意化。
	- 即时使得机器和人能够更好的理解代码的内容，不管是h5新增的nav，footer等标签，都是语意化的一部分。
	- 什么是语义化？其实简单说来就是让机器可以读懂内容
26. 有必要说明一下setInterval()跟setTimeout的区别了。简单来说，setInterval()执行多次，setTimeout()只执行一次
27. event.target
	- target事件属性可返回事件的目标节点(触发该事件的节点)，如生成事件的元素，文档，窗口