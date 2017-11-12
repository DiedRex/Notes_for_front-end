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
11. v-bind:style="{ color: activeColor, fontSize: fontSize + 'px' }可以直接绑定样式
12. 全局指令由directive在'script'标签下注册，局部指令在根之下用'directives'属性注册
13. Vue-router的使用步骤
	- main.js引入路由
	- 安装路由插件，Vue.use(路由名)
	- 创建路由对象并对路由插件进行配置
	- 将路由对象传递到vue实例中，option中(Vue独立时要 import引入)
	- 在app.vue模版中加入<router-view />表示使用路由链接的组件内容。
14. 被使用的是儿子组件，用组件的是父亲。父亲需要引用才能使用对应的儿子组件。
15. 全局组件不需要在使用的时候引用声明，但要在main.js中声明一次，vue.component('组件名'，组件对象)
16. props定义的变量内容是在被引用组件(子组件)中声明的。父组件可以创变量和产量两种数据.自组件声明props
	- 常量: prop1 = "常量值"
	- 变量: prop2 = "变量名"
	- 根属性props["prop1","prop2"]
	- 在页面中直接食用{{prop1}}
17.编程导航的两个方法是
	- this.$router.push('路径')，push后可以接参数到具体地址（name:'',query:{id:1,name:2}）
	- this.$router.go(1||-1),1是表示前进（下一页），－1是表示后退（上一页）超出［－1，1］则报错
18.vue中获取原生dom对象，在元素上ref="xxx",在代码中通过this.$refs.xxx获取其元素
	- 原生dom标签获取的是原生DOM对象
	- 如果是组件标签，获取的是就是组件对象 $el在获取到其dom元素
19.重定向和404notFound
	- 网页默认是'/'
	- 重定向`{path:'/',redirect:'/home'}`或者`{path:'/',redirect:{name:'/home'}}`
	- 404:在路由规则的最后一个规则，写一个很强大的匹配	`{ paht:'*',component:404notFound.vue}`
20. 多视图和路由之前的区别
	- 以前:一个行为（router)＝一个坑（router－view)+一个路由（component)+一个组件（.vue）
	- 现在:一个行为(router) = 多个坑(router-view)+一个路由（components)+多个组件（.vue）
	- components实际是一个对象，其中key是一个（name,在坑中要有对应的姓名）属性,value指的是对应的组件对象。
21. 