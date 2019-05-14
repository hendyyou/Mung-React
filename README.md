## [React版Mung](https://github.com/mochixuan/Mung-React)
## [React-Native版Mung](https://github.com/mochixuan/Mung)
## [Flutter版Mung](https://github.com/mochixuan/Mung-Flutter)

# 2019-5-14通知：豆瓣API忽然下线了。
```
紧急修复方法：
需要运行的修改config/webpackDevServer.config.js里的

"target": "https://api.douban.com/v2"
修改为 
"target": "https://douban.uieee.com/v2",
或者
"target": "http://t.yushu.im/v2",
```
网上查找的资料可以运行，测过有效。但这两个都是别的开发者自己写的不能保证长期有效，这次豆瓣把API停了也没说原因，可能过几天就好了，所以地址还是不改，不能运行的可以改一下就可以了，测过有效。

- [豆瓣API官方讨论](https://www.douban.com/group/345245/)
- [豆瓣API镜像1](https://github.com/zce/weapp-demo/blob/master/README.md)
- [豆瓣API镜像2](https://www.imooc.com/wenda/detail/385141)

---

# Mung-React

> npm start //运行

### 1. Mung-React：是一个基于React编写，使用豆瓣开源API开发的一个项目。

![image](https://github.com/mochixuan/Mung/blob/master/Ui/ui/ic_launcher.png?raw=true)

-------------------

### 2. 功能概述

- **数据保存** ：支持断网加载缓存数据。
- **主题换肤** ：现在只支持切换主题颜色，本项目没几张图片。
- **查看电影详情** ：支持查看电影详情包括评论。
- **一键搜索**： 支持标签和语句查找相关的电影。

-------------------

### 3. 运行结果图

![image](https://github.com/mochixuan/Mung/blob/master/Ui/ppt/icon_ppt1.png?raw=true)
![image](https://github.com/mochixuan/Mung/blob/master/Ui/ppt/icon_ppt2.png?raw=true)

-------------------

### 4. 使用到的框架

- **antd-mobile** ：阿里的UI库，主要用到里面列表显示、Toast提醒。
- **Mobx** ：实现状态管理。
- **react-loading** ：加载进度条。
- **react-router-dom** ：路由管理。
- **react-transition-group** ：实现动画效果。
- **SCSS**： 样式编写方便、清晰。

-------------------

### 5. 总结
这是一个React项目主要，之前写过一个纯React-Native项目Mung没有使用状态管理库和UI库(除渐变库),相比React-Native,现在React水平还是比较一般，尤其是webpack、babel配置等方面，后续有时间还得多看看。里面还有一个ant-design按需加载的问题，使用react-app-rewired配置后和scss发生冲突，有时间再改下。