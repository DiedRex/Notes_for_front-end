#Vue.js笔记
标签属性指令

1. v-once ,只能执行一次插值，不可更改
2. v-html,就像markdown一样根据标签输出类似样式的html内容
3. v-if,true则显示，false则隐藏
4. v-bind,表示将属性和值进行绑定。v-bind:href="url"，缩写形式是:href="url"
5. v-on，监听dom实践。v-on:click="doSomething"，缩写形式@click="doSomething"
6. v-model，双向绑定数据
7. v-show 和 v-if的区别  <http://www.jianshu.com/p/4d03ba22bef9>
8. v-for 循环指令n in 10,([1,2,3]),(object),((value, key) in object)
9. v-bind:class="{ active: isActive, 'text-danger': hasError }"绑定多个样式
	- 使用时，data{isActive:true(false),hasError:true(false)}
10. data也可以被类型嵌套使用。
11.  v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }可以直接绑定样式