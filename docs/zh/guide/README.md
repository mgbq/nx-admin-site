---
pageClass: getting-started
---

# 介绍

[![vue](https://img.shields.io/badge/vue-2.5.10-brightgreen.svg)](https://github.com/vuejs/vue)
[![element-ui](https://img.shields.io/badge/element--ui-2.3.2-brightgreen.svg)](https://github.com/ElemeFE/element)
[![Build Status](https://travis-ci.org/mgbq/nx-admin.svg?branch=master)](https://travis-ci.org/mgbq/nx-admin)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/mgbq/nx-admin/blob/master/LICENSE)
[![GitHub release](https://img.shields.io/badge/release-1.2-blue.svg)](https://github.com/mgbq/nx-admin/releases)
[![GitHub stars](https://img.shields.io/github/stars/mgbq/nx-admin.svg?style=social&label=Stars)](https://github.com/mgbq/nx-admin)

[nx-admin](https://github.com/mgbq/nx-admin) 是基于 Vue2.0，配合使用 Element UI 组件库的一个前端管理后台集成解决方案。它使用了最新的前端技术栈，提炼了典型的业务模型，提供了丰富的功能组件，它可以帮助你快速搭建企业级中后台产品原型。

:::tip 建议
本项目的定位是后台集成方案，不适合当基础模板来进行二次开发。

- 集成方案: [nx-admin](https://github.com/mgbq/nx-admin)
- 基础模板: [nxAdmin-template](https://github.com/mgbq/nxAdmin-template)
  :::

<br/>

## 功能
```
- 登录 / 注销

- 权限验证
  - 页面权限
  - 指令权限

- 多环境发布
  - dev sit stage prod

- 全局功能
  - 国际化多语言
  - 锁屏
  - 疑问
  - 转到github
  - 多种动态换肤
  - 动态侧边栏（支持多级路由嵌套）
  - 动态面包屑
  - 快捷导航(标签页)
  - Svg Sprite 图标
  - 本地mock数据
  - Screenfull全屏
  - 自适应收缩侧边栏

- 编辑器
  - 富文本
  - Markdown

- Excel
  - 导出excel
  - 导出zip
  - 导入excel
  - 前端可视化excel

- 表格
  - 树形表格
  - 内联编辑

- 错误页面
  - 401
  - 404

- 組件
  - 返回顶部
  - 拖拽Dialog
  - 拖拽看板
  - 列表拖拽
  - SplitPane
  - Dropzone
  - Sticky
  - CountTo

- 综合实例
- Dashboard
- v-charts 图表
- Clipboard(剪贴复制)
- Markdown2html
- 首屏加载等待动画
- Fontawesome 图标库
- vuex本地持久化存储,封装h5的sessionStorage和localStorage
- 右键菜单
- github-emoji
- 第三方网站
- 动态文字说明

```

<br/>

## 前序准备

你需要在本地安装 [node](http://nodejs.org/) 和 [git](https://git-scm.com/)。本项目技术栈基于 [ES2015+](http://es6.ruanyifeng.com/)、[vue](https://cn.vuejs.org/index.html)、[vuex](https://vuex.vuejs.org/zh-cn/)、[vue-router](https://router.vuejs.org/zh-cn/) 、[axios](https://github.com/axios/axios) 和 [element-ui](https://github.com/ElemeFE/element)，所有的请求数据都使用[Mock.js](https://github.com/nuysoft/Mock)模拟，提前了解和学习这些知识会对使用本项目有很大的帮助。

## 相关文档

[老板让我十分钟上手nx-admin](https://juejin.im/post/5b43226c51882519ad616c2a)

[Vue2.0实现的用户权限控制](http://blog.csdn.net/qq_32340877/article/details/79416344)

[Vue2.0-基于elementui换肤[自定义主题]](https://blog.csdn.net/qq_32340877/article/details/80176987)

[Vue国际化处理 vue-i18n 以及项目自动切换中英文](https://blog.csdn.net/qq_32340877/article/details/80148913)

[搭建 Vue2 单元测试环境(karma+mocha+webpack3)](https://juejin.im/post/5b051519f265da0b8f62e94e)

[Vue实现首屏加载等待动画](https://juejin.im/post/5b336699e51d4558a846dcc2)

[Vue项目中添加锁屏功能](https://juejin.im/post/5b35e05ee51d4558a75ea159)

[Vue项目添加动态浏览器头部title](https://juejin.im/post/5b446e24e51d45194d4fce14)


**本项目不支持低版本浏览器(如 ie)，有需求请自行添加 polyfill [详情](https://github.com/mgbq/nx-admin/wiki#babel-polyfill)**

**注意：该项目使用 element-ui@2.3.0+ 版本，所以最低兼容 vue@2.5.0+**

## 目录结构

本项目已经为你生成了一个完整的开发框架，提供了涵盖中后台开发的各类功能和坑位，下面是整个项目的目录结构。

```bash
├── build                      // 构建相关
├── config                     // 配置相关
├── src                        // 源代码
│   ├── api                    // 所有请求
│   ├── assets                 // 主题 字体等静态资源
│   ├── components             // 全局公用组件
│   ├── directive              // 全局指令
│   ├── filters                // 全局 filter
│   ├── icons                  // 项目所有 svg icons
│   ├── lang                   // 国际化 language
│   ├── mock                   // 项目mock 模拟数据
│   ├── router                 // 路由
│   ├── store                  // 全局 store管理
│   ├── styles                 // 全局样式
│   ├── utils                  // 全局公用方法
│   ├── vendor                 // 公用vendor
│   ├── views                  // views 所有页面
│   ├── App.vue                // 入口页面
│   ├── main.js                // 入口文件 加载组件 初始化等
│   └── permission.js          // 权限管理
├── static                     // 第三方不打包资源
│   └── Tinymce                // 富文本
├── .babelrc                   // babel-loader 配置
├── .eslintrc.js               // eslint 配置项
├── .gitignore                 // git 忽略项
├── .travis.yml                // 自动化CI配置
├── favicon.ico                // favicon图标
├── index.html                 // html模板
└── package.json               // package.json
```

## 安装

```bash
# 克隆项目
git clone https://github.com/mgbq/nx-admin.git

# 安装依赖
npm install

# 本地开发 启动项目
npm run dev
```

<br/>

::: tip
强烈建议不要用直接使用 cnpm 安装，会有各种诡异的 bug，可以通过重新指定 registry 来解决 npm 安装速度慢的问题。若还是不行，可使用 [yarn](https://github.com/yarnpkg/yarn) 替代 `npm`。

:::

```bash
npm install --registry=https://registry.npm.taobao.org
```

<br/>

启动完成后会自动打开浏览器访问 http://localhost:9528， 你看到下面的页面就代表操作成功了。

![](https://mgbq.github.io/onlinePreview/nxadmin.png)

接下来你可以修改代码进行业务开发了，我们内建了典型业务模板、常用业务组件、模拟数据、HMR 实时预览、状态管理、国际化、全局路由等等各种实用的功能来辅助开发，你可以继续阅读和探索左侧的其他文档。

<br/>

::: tip 建议
你可以把 `nx-admin`当做工具箱或者集成方案仓库，在 `nxAdmin-template` 的基础上进行二次开发，想要什么功能或者组件就去 `nx-admin` 那里复制过来。
:::

## Contribution

本文档项目地址 [nx-admin-site](https://github.com/mgbq/nx-admin-site) 基于 [vuepress](https://github.com/vuejs/vuepress)开发。

有任何修改和建议都可以该项目 pr 和 issue

[nx-admin](https://github.com/mgbq/nx-admin) 还在持续迭代中，逐步沉淀和总结出更多功能和相应的实现代码，总结中后台产品模板/组件/业务场景的最佳实践。本项目也十分期待你的参与和[反馈](https://github.com/mgbq/nx-admin/issues)。

## 捐赠

如果你觉得这个项目帮助到了你，你可以帮作者买一杯果汁表示鼓励 :heart:
[Donate](/zh/donate/)
