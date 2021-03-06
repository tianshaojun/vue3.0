# vue3.0

![](https://github.com/tianshaojun/vue3.0/blob/master/md_img/01.jpg)

### 1.vue3新特性

![](https://github.com/tianshaojun/vue3.0/blob/master/md_img/02.png)

### 2.vue-cli搭建vue3开发环境

+ @vue/cli 4.5.4以上版本
+ 项目初始化  vue create vue3-1

### 3.用vue-cli图形界面搭建vue3开发环境

+ 启动图形界面  vue ui

### 4.项目初始结构和重要文件讲解

```
|node_modules        --所有的项目依赖包都放在这个目录下
|-public             -- 公共文件夹
---|favicon.ico      -- 网站的显示图标
---|index.html       -- 入口的html文件
|-src                -- 源文件目录，编写的代码基本都在这个目录下
---|assets           -- 放置静态文件的目录，比如logo.png就放在这里
---|components       -- Vue的组件文件，自定义的组件都会放到这
---|App.vue          -- 根组件，这个在Vue2中也有
---|main.ts          -- 入口文件，因为采用了TypeScript所以是ts结尾
---|shims-vue.d.ts   -- 类文件(也叫定义文件)，因为.vue结尾的文件在ts中不认可，所以要有定义文件
|-.browserslistrc    -- 在不同前端工具之间公用目标浏览器和node版本的配置文件，作用是设置兼容性
|-.eslintrc.js       -- Eslint的配置文件，不用作过多介绍
|-.gitignore         -- 用来配置那些文件不归git管理
|-package.json       -- 命令配置和包管理文件
|-README.md          -- 项目的说明文件，使用markdown语法进行编写
|-tsconfig.json      -- 关于TypoScript的配置文件
|-yarn.lock          -- 使用yarn后自动生成的文件，由Yarn管理，安装yarn包时的重要信息存储到yarn.lock文件中
```

### 5.setup()和ref()

+ setup代替了vue2中的data和methods属性
+ 在template中使用的变量，必须用ref包装一下
+ return出去的数据和方法，在模板中才可以使用

### 6.reactive()函数优化程序

+ reactive / toRefs

### 7.Vue3.x的生命周期和钩子函数

+ setup() :开始创建组件之前，在beforeCreate和created之前执行。创建的是data和method
+ onBeforeMount() : 组件挂载到节点上之前执行的函数。
+ onMounted() : 组件挂载完成后执行的函数。
+ onBeforeUpdate(): 组件更新之前执行的函数。
+ onUpdated(): 组件更新完成之后执行的函数。
+ onBeforeUnmount(): 组件卸载之前执行的函数。
+ onUnmounted(): 组件卸载完成后执行的函数
+ onActivated(): 被包含在<keep-alive>中的组件，会多出两个生命周期钩子函数。被激活时执行。
+ onDeactivated(): 比如从 A 组件，切换到 B 组件，A 组件消失时执行。
+ onErrorCaptured(): 当捕获一个来自子孙组件的异常时激活钩子函数。
  
#### Vue2.x和Vue3.x生命周期对比

Vue2--------------vue3
+ beforeCreate  -> setup()
+ created       -> setup()
+ beforeMount   -> onBeforeMount
+ mounted       -> onMounted
+ beforeUpdate  -> onBeforeUpdate
+ updated       -> onUpdated
+ beforeDestroy -> onBeforeUnmount
+ destroyed     -> onUnmounted
+ activated     -> onActivated
+ deactivated   -> onDeactivated
+ errorCaptured -> onErrorCaptured

### 8.onRenderTracked()和onRenderTriggered()钩子函数使用

+ onRenderTracked状态跟踪
+ onRenderTriggeded状态触发

### 9.watch

### 10.独立模块化的使用

### 11.深入使用模块化

### 12.Teleport瞬间移动函数(独立组件)

### 13.Suspense-初识异步请求组件

### 14.Suspense-深入学习















