# Initial
- 初始化项目时,需要安装依赖包,不能在超级管理员权限下操作.  
- 只能使用 `sudo cnpm install --allow-root` 进行操作,但是还是不能安装 `bower` ,使用 `sudo cnpm install bower ` 安装bower  
- 使用 `sudo bower install --allow-root`安装包,如`jQuery`,`angular`,`angular-route`等等  
- 使用 `sudo npm start --allow-root` 启动服务器  

---

# AngularJS自动初始化  
- AngularJS会在`DOMContentLoaded`事件触发时执行，并通过ng-app指令 寻找你的应用根作用域。如果ng-app指令找到了，那么AngularJS将会:  
* 载入和 指令 内容相关的模块  
* 创建一个应用的“注入器(injector)”  
* 已拥有ng-app 指令 的标签为根节点来编译其中的DOM。这使得你可以只指定DOM中的一部分作为你的AngularJS应用。  
---

# AngularJS双向绑定  
- 

---  
  
# AngularJS依赖注入  
- AngularJS是通过控制器构造函数的参数名字来推断依赖服务名称的 ,使用fn.toString()获取需要的服务名称.  
* 为了克服压缩引起的服务参数的名称被压缩致使参数失效的问题,这时候注入器不知道应该注入什么服务.  
* 只要在控制器函数里面给$inject属性赋值一个依赖服务标识符的数组  
	```
		PhoneListCtrl.$inject = ['$scope', '$http'];
	```  
* 使用Javascript数组方式构造控制器：把要注入的服务放到一个字符串数组（代表依赖的名字）里  
	```
		var PhoneListCtrl = ['$scope', '$http', function($scope, $http) { /* constructor body */ }];
	```  

--- 

# AngularJS路由  
- AngularJS中应用的路由通过$routeProvider来声明，它是$route服务的提供者。这项服务使得控制器、视图模板与当前浏览器的URL可以轻易集成。  
- 

---  
 
# 关于依赖注入（DI），注入器（Injector）和服务提供者（Providers）  
- 当应用引导时，AngularJS会创建一个注入器，我们应用后面所有依赖注入的服务都会需要它  
- 注入器唯一的职责是载入指定的服务模块，在这些模块中注册所有定义的服务提供者，并且当需要时给一个指定的函数注入依赖（服务）。    

---  

# Restful++++定制服务  
- restful架构  
``` url: http://www.ruanyifeng.com/blog/2011/09/restful ```  
* 每一个URI代表一种资源；  
* 客户端和服务器之间，传递这种资源的某种表现层;  
* 客户端通过四个HTTP动词，对服务器端资源进行操作，实现"表现层状态转化"。
