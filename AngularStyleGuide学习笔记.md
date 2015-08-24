### angular style guide 总结
+ 工程结构
	+ 一个组件一个文件,把controller service filter 分文件
	+ 按业务功能优先划分工程结构
+ 模块
	+ 制定一个命名规则 
		+ file
			+ controller  module.js    
			+ service  module.service.js
			+ directive  module.directive.js
			+ config module.config.js
		+ module
			+ controller  ModuleCtrl    
			+ service  moduleService
			+ directive  moduleDirective.js
	+ 使用自执行的匿名函数防止变量污染
	+ 使用简单的定义模块方式，即不使用变量
	+ 使用链式操作，定义更加具有可读性的函数
	+ 尽可能精简filter
+ controller
	+ 将需要绑定的函数放到上面
	+ 将controller中的逻辑代码转移到service中
		+ 隐藏依赖和引用详情
		+ 逻辑可以被多个controller复用
	+ controller仅仅只对应一个视图，不要尝试给多个视图使用
	+ routeProvider中使用resolve来提前controller的逻辑执行
+ services
	+ 业务逻辑封装成service而非factory
	+ 数据操作都放到service中
+ directive
	+ 限制只能element attributes替换
+ 其他
	+ 使用[] 注入依赖
	+ 需要在程序启动时运行的代码可以放到run里面
	+ 使用 $timeout $interval $window $document $http代替原生js
	+ 使用promise($q)避免回调
##### 参考文章
+ [angularjs-style-guide](https://github.com/mgechev/angularjs-style-guide/blob/master/README-zh-cn.md)
+ [angularjs-style-guide](https://github.com/johnpapa/angular-styleguide)