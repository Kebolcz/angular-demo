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
