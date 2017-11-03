#前端面试大全xxxScript篇
1. <font size=5>ECMAScript 提供了两种把非数字的原始值转换成数字的方法？</font><font size=3>
	- parseInt()parseInt() 方法首先查看位置 0 处的字符，判断它是否是个有效数字；如果不是，该方法将返回 NaN，不再继续执行其他操作。但如果该字符是有效数字，该方法将查看位置 1 处的字符，进行同样的测试。这一过程将持续到发现非有效数字的字符为止，此时 parseInt() 将把该字符之前的字符串转换成数字
	- parseFloat() 与 parseInt() 方法的处理方式相似，从位置 0 开始查看每个字符，直到找到第一个非有效的字符为止，然后把该字符之前的字符串转换成整数
2. <font size=5>强制类型转换方法有？</font><font size =3>
	- Boolean(value)、Number(value)、String(value。
	- toString() 方法，即把 12 转换成 "12"，把 true 转换成 "true"，把 false 转换成 "false"，以此类推,把任何类型的值转换成字符串类型
	
3. <font size=5>回答一下同步异步阻塞和非阻塞的关系？</font><font size =3>
	- <https://www.zhihu.com/question/19732473></font>
4. 浅谈一下cookie、sessonstorge,localstorge的区别
	- <http://jerryzou.com/posts/cookie-and-web-storage/>
5. 
 