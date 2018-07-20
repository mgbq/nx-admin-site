---
pageClass: getting-started
---

# Introduction

[![vue](https://img.shields.io/badge/vue-2.5.10-brightgreen.svg)](https://github.com/vuejs/vue)
[![element-ui](https://img.shields.io/badge/element--ui-2.3.2-brightgreen.svg)](https://github.com/ElemeFE/element)
[![Build Status](https://travis-ci.org/mgbq/nx-admin.svg?branch=master)](https://travis-ci.org/mgbq/nx-admin)
[![license](https://img.shields.io/github/license/mashape/apistatus.svg)](https://github.com/mgbq/nx-admin/blob/master/LICENSE)
[![GitHub release](https://img.shields.io/badge/release-1.2-blue.svg)](https://github.com/mgbq/nx-admin/releases)
[![GitHub stars](https://img.shields.io/github/stars/mgbq/nx-admin.svg?style=social&label=Stars)](https://github.com/mgbq/nx-admin)

[nx-admin](https://github.com/mgbq/nx-admin) is a front-end management background integration solution based on Vue 2.0 that uses the Element 
UI component library. It uses the latest front-end technology stack, provides a typical business model, and provides various components that can help you quickly build enterprise-level back-office product prototypes.

:::tip
The project is positioned as a background integration solution and is not suitable for secondary development as a basic template.

- Integrated Solution: [nx-admin](https://github.com/mgbq/nx-admin)
- Basic Template: [nxAdmin-template](https://github.com/mgbq/nxAdmin-template)
  :::

<br/>


## Features
```
- Login / Logout

- Permission Authentication
  - Page permission
  - Directive permission

- Multi-environment build
  - dev sit stage prod
  
- Global Features
  - Lock screen
  - Query
  - Go to github
  - I18n
  - Multiple dynamic themes
  - Dynamic sidebar (supports multi-level routing)
  - Dynamic breadcrumb
  - Tags-view(Tab page Support right-click operation)
  - Svg Sprite
  - Mock data
  - Screenfull
  - Responsive Sidebar
  
- Editor
  - Rich Text Editor
  - Markdown Editor

- Excel
  - Export Excel
  - Export zip
  - Upload Excel
  - Visualization Excel

- Table
  - Tree Table
  - Inline Edit Table


- Error Page
  - 401
  - 404

- Components
  - Back To Top
  - Drag Dialog
  - Drag Kanban
  - Drag List
  - SplitPane
  - Dropzone
  - Sticky
  - CountTo

- Dashboard
- V-charts
- Animation
- Clipboard
- Markdown to html
- Fontawesome
- Vuex Local persistent storage ,packaging H5 of SessionStorage and LocalStorage
- Right click menu
- Github-emoji
- Third party website
- Dynamic text description

```

## Preparation

You need to install [node](http://nodejs.org/) and [git](https://git-scm.com/) locally. The project is based on [ES2015+](http://es6.ruanyifeng.com/), [vue](https://cn.vuejs.org/index.html), [vuex](https://vuex.vuejs.org/zh-cn/), [vue-router](https://router.vuejs.org/zh-cn/), [axios](https://github.com/axios/axios) and [element-ui](https://github.com/ElemeFE/element), all request data is simulated using [Mock.js](https://github.com/nuysoft/Mock).
 Understanding and learning this knowledge in advance will greatly help the use of this project.
 
 ## related documents
[老板让我十分钟上手nx-admin](https://juejin.im/post/5b43226c51882519ad616c2a)

[Vue2.0实现的用户权限控制](http://blog.csdn.net/qq_32340877/article/details/79416344)

[Vue2.0-基于elementui换肤[自定义主题]](https://blog.csdn.net/qq_32340877/article/details/80176987)

[Vue国际化处理 vue-i18n 以及项目自动切换中英文](https://blog.csdn.net/qq_32340877/article/details/80148913)

[搭建 Vue2 单元测试环境(karma+mocha+webpack3)](https://juejin.im/post/5b051519f265da0b8f62e94e)

[Vue实现首屏加载等待动画](https://juejin.im/post/5b336699e51d4558a846dcc2)

[Vue项目中添加锁屏功能](https://juejin.im/post/5b35e05ee51d4558a75ea159)

[Vue项目添加动态浏览器头部title](https://juejin.im/post/5b446e24e51d45194d4fce14)

#### This project borrows from the pattern of the flower vents  [vueAdmin-template](https://github.com/PanJiaChen/vueAdmin-template)

This project does not support low version browsers (e.g. IE). Please add polyfill yourself if you need them.

Note: This project uses element-ui@2.3.0+ version, so the minimum compatible vue@2.5.0+


## Project Structure

This project has built the following templates, and have built a scaffold based on Vue, which should help you prototyping production-ready admin interfaces. It covers almost everything you need.

```bash
├── build                      // webpack config files
├── config                     // main project config
├── src                        // main source code
│   ├── api                    // api service
│   ├── assets                 // module assets like fonts,images (processed by webpack)
│   ├── components             // global components
│   ├── directive              // global directive
│   ├── filters                // global filter
│   ├── icons                  // svg icons
│   ├── lang                   // i18nlanguage
│   ├── mock                   // mock data
│   ├── router                 // router
│   ├── store                  // store
│   ├── styles                 // global css
│   ├── utils                  // global utils
│   ├── vendor                 // vendor
│   ├── views                  // views
│   ├── App.vue                // main app component
│   ├── main.js                // app entry file
│   └── permission.js          // permission authentication
├── static                     // pure static assets (directly copied)
│   └── Tinymce                // rich text editor
├── .babelrc                   // babel config
├── .eslintrc.js               // eslint config
├── .gitignore                 // sensible defaults for gitignore
├── favicon.ico                // favicon ico
├── index.html                 // index.html template
└── package.json               // package.json

```
## Getting Started
```js
# clone the projice
git clone https://github.com/mgbq/nx-admin.git

# install dependency
npm install

# develop
npm run dev
```

This will automatically open http://localhost:9528.

If you see the following page then you have succeeded.

![](https://mgbq.github.io/onlinePreview/nxadmin.png)

We have built-in models, standard components, mock data, hot module reloading, state management, i18n, global router, etc. You can continue exploring other documents for more details on those topics

<br/>

::: tip 
Suggestion： You can use nx-admin as a toolbox or as an integration solution repository, It is recommended to do secondary development on the basis of nxAdmin-template, if you need any additional feature, you can copy from nx-admin.
:::

## Contribution

The repository of documentation is [nx-admin-site](https://github.com/mgbq/nx-admin-site) based on [vuepress](https://github.com/vuejs/vuepress)development.

There may be some spelling or translation errors in the course of writing this document. It is welcome to point out by issue or pr. After all, English is not my mother tongue

 [nx-admin](https://github.com/mgbq/nx-admin)  is also continuing to iterate, summarize and summarize more features, and summarize the best practices of product templates/components/business scenarios in the middle and back office. This project is also very much looking forward to your participation and [feedback](https://github.com/mgbq/nx-admin/issues)。

## Donate


If you think this project is useful, you can buy a glass of juice for the author ❤️
[Donate](/donate/)

