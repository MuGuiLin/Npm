# Npm常用命令

命令|注释
--|--
npm install -g npm to update| #更新升级npm
npm -v| #显示版本，检查npm 是否正确安装。  
npm install express| #安装express模块  
npm install -g express| #全局安装express模块  
npm list| #列出已安装模块  
npm show express| #显示模块详情  
npm update| #升级当前目录下的项目的所有模块  
npm update express| #升级当前目录下的项目的指定模块  
npm update -g express| #升级全局安装的express模块  
npm uninstall express| #删除指定的模块

  
  
  ## ==在云服务器上配置和使用 Npm==
  
#### 1、配置 npm
npm 是 Node.js 的包管理和分发工具。它可以让 Node.js 开发者能够更加轻松的共享代码和共用代码片段下载 node 的压缩包中已经包含了 npm , 我们只需要将其软链接到 bin 目录下即可。
```ssh
ln -s /usr/local/node-v6/bin/npm /bin/npm
```


#### 2、配置环境变量
将 /usr/local/node-v6/bin 目录添加到 $PATH 环境变量中可以方便地使用通过 npm 全局安装的第三方工具。
```ssh
echo 'export PATH=/usr/local/node-v6/bin:$PATH' >> /etc/profile
```

	

#### 3、生效环境变量
```ssh
source /etc/profile
```


#### 4、使用 npm，通过 npm 安装进程管理模块 forever。
```ssh
npm install forever -g 
```

