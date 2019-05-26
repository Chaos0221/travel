# 笔记

### Stylus-CSS预编译
    安装: stylus stylus-loader （不需要配置）
    语法: 在varibles.styl中定义变量 使用前用@import引入

### iconfont 图标字体
    阿里巴巴矢量图标库
    下载图标字体文件 在main.js中引入
    <span class='iconfont'>#...</span>

### @import
    用~@代表src

### 自动化分页
    将内容数据放入computed中 二维数组 
    根据index判断应该在第几页
    pages[page0,page1]

### 超出字符隐藏
    overflow: hidden
    white-space: nowrap
    text-overflow: ellipsis

### slot
    当子组件的某些内容需要被父组件定制时使用
    页面中多次用到swiper 可把swiper中的组件写成slot

### mock
    只有static中的文件可以直接通过路径访问
    webpack-dev-server在config文件夹index.js中提供proxyTable接口 用来转发ajax请求路径
