### JavaScript秘密花园学习笔记

+ 对象
	+ 对象使用和属性
		+ 除了null和undefined外，所有变量都是对象
			+ js的数据类型包括 字符串 数字 布尔 数组 对象 null undefined
		+ 定义一个简单的对象 var o = {}  这个对象从Object.prototype继承下来
		+ 删除一个对象的某个属性只能使用 delete o.name
	+ 原型
		+ 在js中查找属性时，js会向上遍历原型链，直到找到给定的属性为止
		+ 如果一个属性在原型链上端则会对查找时间到来不好的影响
		+ 当我们需要判断一个值是否是原型链上的属性，需要使用Object.prototype.hasOwnProperty
	+ 函数
		+ this的五种情况
			+ 全局范围内 this，this指向全局对象
			+ 函数调用内 foo(), this指向全局对象
			+ 方法调用 test.foo(), this指向test对象
			+ 构造函数 new foo(), this指向新创建的对象
			+ 显示设置 Foo.method = function(){function test(){// this 指向全局对象} test();}
		+ 闭包和引用
			+ 闭包就是读取其他函数中的内部变量的函数，将变量始终保存在内存中
			+ 闭包的作用
				+ 匿名自执行函数
				+ 缓存
				+ 实现封装
				+ 实现面向对象中的对象
		+ 改变行参的值会影响到arguments
		+ 构造函数
			+ 通过new关键字调用的函数都是构造函数
		+ 作用域
			+ 不定义变量将会导致隐式全局变量（包括函数内的变量）
			+ JS是函数作用域：变量在声明它们的函数体以及这个函数体嵌套的任意函数体内都是有定义的
		+ 数组
			+ for in会枚举原型链上所有的属性，速度比普通循环慢好几倍
			+ length属性getter方法会简单的返回数组长度，setter会截断数组（缩小截断，扩大没效果）




#### 参考
[JavaScript秘密花园](http://bonsaiden.github.io/JavaScript-Garden/zh/#object)