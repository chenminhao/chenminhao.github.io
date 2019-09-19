---
title: react基础总结
categories:
- 前端
tags:
- 命令
---
### 创建并启动项目

```javaScript
// 安装脚手架工具
1. npm install -g create-react-app

//创建项目
2. create-react-app reactdemo

// cd 到项目里面
3. cd reactdemo

//运行项目
4. npm start

//生成项目
5. npm run build
```
### 基础语法

绑定属性注意：           
1. class 要变成 className   
2. for 要变成  htmlFor
3. style属性和以前的写法有些不一样
```html
<div style={{'color':'blue'}}>{this.state.title}</div>
<div style={{'color':this.state.color}}>{this.state.title}</div>
```

