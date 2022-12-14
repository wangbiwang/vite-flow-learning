# 浅谈 JavaScript 包管理器？

## 前言

学习 JavaScript 包管理器的一些笔记。
<!-- 大纲 

什么是 JavaScript 包管理器?

npm 、yarn 、pnpm区别？

npm install XXX 执行过程？

npm run XXX 执行过程？

npm create vite 执行过程？ -->

## 什么是 JavaScript 包管理器?

### 什么是包？

简单来说，包(package)可以是一段的代码，也可以是多个文件的集合。
每个包可能会，也可能不会依赖于别的包。

### 什么是包管理器？

包管理器就是一段代码程序，作用就是管理你项目依赖的外部代码包(package)

## 现在主流包管理器的区别？
现在主流的 JavaScript 包管理器有 npm、yarn、pnpm。
在2022年来看，各管理器的功能都差不多



## npm install XXX 执行过程？

## npm run XXX 执行过程？

简述一下执行过程,首先会去读项目的 package.json 文件，找到文件中scripts 中对应xxx命令，执行 xxx 。

例如npm run dev，就是执行了 vue-cli-service serve 命令。

```json
/* package.json */ 
"name": "vue-admin",
"version": "1.0.0",
"scripts": {
    "dev": "vite --mode development",
    "build:uat": "vite build --mode uat" 
},
```

为何不直接运行 vite --mode development ，而要执行npm run dev呢?

因为系统中没有vite --mode development这个命令，直接运行会报错。

执行npm run dev 相当于执行了vite --mode development这个命令，能成功执行不报错，为何？

## npm create vite 执行过程？
