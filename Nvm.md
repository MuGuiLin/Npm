# nvm是一个Node.js版本管理器 【为了解决node各种版本存在不兼容问题，nvm是让你在同一台机器上安装和切换不同版本的node的工具，nvm和n都是node版本管理工具】


## 使用NVM（Node Version Manager）控制Node.js版本
  
  ### 下载NVM

    - nvm是mac环境下管理nodejs的工具。在windows环境下推荐使用nvmw或者nvm-windows；

    - Nvm-windows  下载地址 https://github.com/coreybutler/nvm-windows   下载 nvm-setup.zip

  ### 安装NVM

    - 在安装nvm之前需要一个c++编译器，在mac上可以安装Xcode命令工具(已经安装可以忽略)

      xcode-select --install

    - 使用 curl安装

      curl -o- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash

    - 或者使用wget来安装

      wget -qO- https://raw.githubusercontent.com/creationix/nvm/v0.34.0/install.sh | bash 


  - NVM [github的地址](<https://github.com/creationix/nvm>)可以查看最新版本
  
	此时nvm就被安装在了/.nvm下啦!

# 注：在window系统，如果你之前有安装过nodejs,一定要把那个安装目录的名字改为其他名字如：以前是：C:\Program Files\nodejs，将其改为：C:\Program Files\nodejsx 就OK啦！

# 不然在nvm use xxx 后提示切换成功，但是在 node -v 发现还是之前的node版本的问题！

## NVM常用指令；

- 【查看版本】：

| 命令          | 说明 |
| ------------- | ---- |
| nvm version	| 查看版本 |
| nvm ls     	| 查看所有已经安装的Nodejs版本 |
| nvm ls-remote	| 列出远程服务器上所有可用的版本(列出所有可以安装的node版本号) |
| nvm list   	| 查看所有已经安装的Nodejs版本 |
| nvm root 		| 查看nvm安装路径 |
| nvm arch  	| 显示节点是否以32位或64位模式运行 |
| nvm current	| 当前node版本 |
	
	
- 【安装版本】：

| 命令         		 | 说明 |
| ------------------ | ---- |
| nvm install stable | 安装最新稳定版Nodejs |
| nvm install 8.11.1 | 安装指定版本 |
| nvm install 8.11	 | 安装 8.11.x系列最新版本 |
| nvm uninstall 8.11 | 删除 8.11.x系列最新版本 |



- 【切换版本】：

| 命令         		 | 说明 |
| ------------------ | ---- |
| nvm use 版本号     | 切换版本（这个是全局的）|
| nvm use 8.11.1     | 切换到8.11.1版本 |
| nvm use 8.11       | 切换到8.11.x最新版本 |
| nvm use node       | 切换到最新版本 |
	

- 【其他命令】：

| 命令         		 	| 说明 |
| --------------------- | ---- |
| nvm run 10.24 myApp.js| 在v10.24版本下运行 myApp.js |
| nvm alias default node| 设置默认版本为最新版本 |
| nvm on     			| 启用node.js版本管理 |
| nvm off       		| 禁用node.js版本管理 |
| nvm proxy [url]   	| 设置用于下载的代理。将[url]留空以查看当前代理。 将[url]设置为“无”以删除代理 |