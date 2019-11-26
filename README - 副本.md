# Npm

npm 为你和你的团队打开了连接整个 JavaScript 天才世界的一扇大门。它是世界上最大的软件注册表，每星期大约有 30 亿次的下载量，包含超过 600000 个 _包（package）_ （即，代码模块）。来自各大洲的开源软件开发者使用 npm 互相分享和借鉴。包的结构使您能够轻松跟踪依赖项和版本。

Npm中文网：https://www.npmjs.cn

### npm 由三个独立的部分组成：

- 网站 [_https://npmjs.com_](https://npmjs.com) 
- 注册表（registry）
- 命令行工具 (CLI) [_https://docs.npmjs.com/cli/npm_](https://docs.npmjs.com/cli/npm) 

### 其中：

- 网站： 是开发者查找包（package）、设置参数以及管理 npm 使用体验的主要途径。
- 注册表：是一个巨大的数据库，保存了每个包（package）的信息。
- CLI：是通过命令行或终端运行。开发者通过 CLI 与 npm 打交道。


### Npm常用命令

| 命令                          | 注释                    |
| ---------------------------- | ---------------------    |
| npm -v                       | 显示版本，检查npm 是否正确安装     |
| npm install -g npm to update | 更新升级npm               |
| npm init 项目名               | 创建项目 手动填写配置信息         |
| npm init 项目名 -y            | 创建项目并自动生成配置信息         |
| npm list                     | 显示当前项目中已安装模块          |
| npm list -g                  | 显示所以已安装模块             |
| npm root                     | 显示当前项目 node_modules目录 |
| npm root -g                  | 显示全局node_modules目录    |
| npm show 模块名               | 显示当前项目模块详情            |
| npm update                   | 升级当前目录下的项目的所有模块       |
| npm update 模块名             | 升级当前目录下的项目的指定模块       |
| npm install 模块名            | 安装模块（局部安装）            |	
| npm install -g 模块名         | 全局安装模块                |
| npm install 模块1 模块2...    | 同时安装多个模块，中间用空格隔开     |
| npm cache clean --force        | 清除npm缓存                |
| npm update -g 模块名          | 升级全局安装的模块             |
| npm uninstall 模块名          | 删除指定的模块               |
| npm config list              | 显示npm相关信息             |


### Npm参数说明

- install 可以简写为 i； 例如：  npm i jquery
- 开发依赖（打包后不用的[如 less、sass、eslent等])--save-dev 可以简写为 -D； 例如：npm i jquery -D
- 运行依赖（打包后要用的[如 vue、axios等]） --save 可以简写为-S；例如：npm i jquery -S


### 删除全局 node_modules 中的模块 

- npm root -g //显示全局node_modules目录

1. 打开全局 node_modules 目录  【在CMD中输入：npm root -g】获取全局node_modules 目录  
2. 先删除和 node_modules 同级目录中的模块名文件 如：cnpm
3. 再删除和 node_modules 同级目录中的模块名.cmd文件 如：cnpm.cmd
4. 然后在删除 node_modules 里面的模块文件夹 如：cnpm


## ==注：node_modules 查找规则（向上查找）==

- package.json配置文件中保存了node_modules目录中的各个模块、版本号等信息。
- 可以在一个大目录下创建package.json，然后安装各种所需模块，生成node_modules目录。
- 在子目录中各自创建的项目，可以共用一个node_modules目录中的模块。
- 在子目录项目中正常引用模块，模块会自动向上查找node_modules目录中的模块。


## 发布自己的Npm模块(包)  【开发者生，封闭者死！】

也就是向[_https://npmjs.com_](https://npmjs.com)提交自己的模块！

1. 创建package.json配置文件**注：模块名一定是在 Npm仓库中是唯一的才行哦！！**

2. 编写要发布的模块

3. 注册npm账号（如查已有账号就略过）注册网址：https://www.npmjs.com/signup

4. npm adduser  //添加并登录用户到  https://registry.npmjs.org
   - Username：输入账号
   - Password：输入密码
   - Emali：输入邮箱
   
5. npm publish  //发布npm模块

6. **注：无论是发布模块 还是 删除包 都要保证 npm下载源是官方的下载源才行哦！！**
   - npm config list   //查看npm下载源
   
7. npm config set registry https://registry.npmjs.org   //将下载源设为官方的

8. npm config set registry https://registry.npm.taobao.org  //将下载源设为淘宝的

9. 淘宝NPM镜像：[https://npm.taobao.org](https://npm.taobao.org)
    - 由于npm 是国外的，网速不好，所以才用国内的淘宝NPM镜像
    - 这是一个完整 `npmjs.org` 镜像，你可以用此代替官方版本(只读)，同步频率目前为 **10分钟** 一次以保证尽量与官方服务同步。

10. 安装cnpm淘宝NPM镜像：
    - npm install -g cnpm --registry=https://registry.npm.taobao.org
    - cnpm 的用法和 npm的用法一样的
    - cnpm的下载速度比npm的快


## 删除已发布的Npm模块

1. 登录用户到  https://registry.npmjs.org
2. npm unpublish 模块名 --force    //删除已发布的Npm模块
    - 模块名：就是package.json配置文件中的 "name": 字段
3. 注：**删除后24内不能在用这个模块名，再进行发布哦！！**
   


## 在云服务器上配置和使用 Npm

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
