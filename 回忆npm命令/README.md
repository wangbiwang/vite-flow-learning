# 回忆npm命令

## npm 命令

## npm install XXX 执行过程？



## npm run XXX 执行过程？
简述：首先会去读项目的package.json文件，找到文件中scripts中对应xxx命令，执行xxx。
--
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
-因为系统中没有vite --mode development这个命令，直接运行会报错。

执行npm run dev 相当于执行了vite --mode development这个命令，能成功执行不报错，为何？

## npm create vite 执行过程？