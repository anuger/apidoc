# apidoc-plus
 基于[apidoc](https://github.com/apidoc/apidoc)添加了一些开发中很有用的功能.支持直接启动静态服务和api服务,支持mock.js  
 apidoc文档:[apidocjs.com](http://apidocjs.com)  
 mockjs文档:[mockjs.com](http://mockjs.com)

### 功能列表
1. 根据注释生成html页面
2. mock服务
3. http static server

### 安装方法
> npm install -g git+https://github.com/anuger/apidoc-plus.git

### 使用(在apidoc原有参数上添加了以下参数)
> apidoc -sm -p 3000 -i "扫描目录" -o "生成目录"  
> 启动后访问http://localhost:3000/(api路径)即可请求到mock数据  
> -s 启动静态服务,展示api文档  
> -m 启动mock服务  
> --port 指定http服务端口
> apidoc -h 可查看帮助  

### 添加mock数据
在@apiSuccessExample中使用mockjs语法即可,例:
```
* @apiSuccessExample Success-Response:
* {
*       "state": 200,
*       "data|10":[{
*           "name":"@cname"
*       }]
* }
```
