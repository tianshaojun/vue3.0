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
frendEnds
|  node_modules                  所有的项目依赖包都放在这个目录下




│  .babelrc						// 按需引入vant中的组件
│  babel.config.js					// es babel配置
│  package-lock.json				// 锁定安装时的包的版本号和来源
│  package.json					// 依赖的版本管理
│  README.md					// 项目说明手册
│  vue.config.js					// 配置文件
│  yarn.lock						// 由yarn管理，自动生成。如用npm不会影响
│  
├─public						// vue cli自动将index.html放入public中
│      favicon.ico				// 网站头像
│      index.html				// 总的入口文件，挂在id为app的div下动态渲染路由模板
│      
└─src
    │  App.vue					// 是vue的主组件，所有页面都是在App.vue下进行切换的
    │  main.js					// js入口文件，影响全局，作用是引入全局使用的库、公共的样式和方法、设置路由等
    │  
    ├─api						// 放置与后台 api 相关的文件
    │      axiosConfig.js			// axios 库的实例配置文件、使用配置的 axios 实例接入 api 获取数据的函数的集合的文件
    │      http.js				// 后台数据接口统一管理文件
    │      
    ├─assets					// 静态资源
    │  ├─fonts				// 阿里iconfont字体图标库
    │  │      demo.css
    │  │      demo_index.html
    │  │      iconfont.css
    │  │      iconfont.eot
    │  │      iconfont.js
    │  │      iconfont.json
    │  │      iconfont.svg
    │  │      iconfont.ttf
    │  │      iconfont.woff
    │  │      iconfont.woff2
    │  │      
    │  ├─images				// 图片存放
    │  │      gray_2.png
    │  │      logo.png
    │  │      pep.png
    │  │      
    │  └─styles				// 样式
    │      │  404.scss
    │      │  about.scss
    │      │  common.scss
    │      │  home.scss
    │      │  login.scss
    │      │  read.scss
    │      │  
    │      ├─components		// 放置公共组件的样式
    │      │      count.scss
    │      │      headerNav.scss
    │      │      loading.scss
    │      │      tab.scss
    │      │      
    │      └─variable			// 放置全局公共变量样式
    │              variable.scss
    │              
    ├─components				// 放置公共组件
    │      Count.vue
    │      HeaderNav.vue
    │      Loading.vue
    │      Tab.vue
    │      
    ├─markdown				// 放置.md文件描述
    │      pep_dev.md
    │      
    ├─router					// 放置路由设置文件，指定路由对应的组件
    │      index.js
    │      
    ├─store						// 放置vuex需要的状态关联文件，设置公共的 state、mutations 等
    │  │  index.js
    │  │  
    │  ├─modules				// 模块化
    │  │      count.js
    │  │      
    │  └─mutationsType			// mutationsType名字统一管理，得于排错
    │          index.js
    │          
    ├─utils						// 全局可引用的工具包、公共的js方法
    │      cookie.js
    │      filter.js
    │      rem.js
    │      
    └─views					// 放置主要页面的组件。例如登录页、用户信息页等。通常是这里的组件本身写入一些结构，再引入通用模块组件，形成完整的页面
        ├─404
        │      index.vue
        │      
        ├─About
        │      index.vue
        │      
        ├─Home
        │      index.vue
        │      
        ├─Login
        │      index.vue
        │      
        └─Read
                index.vue
```







