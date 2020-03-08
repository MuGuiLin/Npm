# Bower
```
	Bower是Twitter推出的，它主要是一个包管理工具【前端套件管理】，它依赖 Node.js和Npm，简单来说就是一个静态资源共享平台。可用于搜索、安装和卸载如JavaScript、HTML、CSS之类的网络资源。
	
	一般来说在前端开发工作中，或多或少会用到一些依赖包，以前的开发人员如果要用的话，就得到网上到处找，然后下各种插件，极大浪费了时间，并且删除的时候也麻烦。

	Bower的安装和升级全都依赖于NPM！
```


## Npm 和 Bower：

```
	简单的说，npm是进行后端开发中，使用的模块安装工具，而bower，是前端的模块安装工具。
	
	Bower与NPM最大的区别在于，NPM主要运用于Node.js项目的内部依赖包管理，安装的模块位于项目根目录下的node_modules文件夹内。
	
	而Bower大部分情况下用于前端开发，对于CSS/JS/模板等内容进行依赖管理，依赖的下载目录结构可以自定义。
```



## 安装Bower:

- npm install -g bower



## 删除Bower:

- npm rm -g bower



## Bower初始化

- bower init 	// 一直按Enter键直到完成，就生成bower.json文件了



## 使用Bower安装前端模块

- bower install 					// 安装bower.json文件中的模块
- bower install 模块名				// 安装指定模块

### 这里以安装angular 和 jquery 为例：

- bower install --save angular   	// --save  （将它加入到json文件中

- bower install jquery   			// 安装jquery



## Bower常用命令：

| 命令          | 说明 |
| ------------- | ---- |
| bower -v      | 查看版本|
| bower i -h    | 查看帮助|



