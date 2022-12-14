# 浅谈 JavaScript 包管理器？

## 前言

### 学习 avaScript 包管理器的一些笔记。
<!-- 大纲 

什么是 JavaScript 包管理器?

npm 、yarn 、pnpm区别？

npm install XXX 执行过程？

npm run XXX 执行过程？

npm create vite 执行过程？ -->

## 为什么出现 JavaScript 包管理器?
<!-- 大纲 

包管理器的由来（为什么出现）

现在主流包管理器 -->



## 现在主流包管理器的区别？

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
