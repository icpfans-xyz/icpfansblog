---
title: "ICP 本地开发环境快速搭建教程"
date: 2020-05-11T9:40:24+06:00
# post thumb
images:
  - "images/post/post-3.jpg"
#author
author: "张三"
# description
description: "ICP 入门教程"
# Taxonomies
categories: ["教程"]
tags: ["tutorial","教程"]
type: "featured" # available type (regular or featured)
draft: false
---

### 本教程适用于有一定基础的以太坊生态链开发者。
<br>
<hr>
&nbsp;&nbsp;&nbsp;&nbsp;此快速入门方案假定您是第一次安装DFINITY Canister SDK，并且正在作为本地开发环境的一部分运行Internet计算机。 首先，让我们构建并部署一个简单的Hello应用程序，该应用程序只有一个功能-greet。 greet函数接受一个text参数，并以类似于Hello的问候语返回结果，大家好！ 如果您使用命令行运行该应用程序，请在终端中输入；如果您使用浏览器访问该应用程序，则请在HTML页面中输入。

<br>
<br>

### 在你开始之前
<hr>
在下载并安装此版本的DFINITY Canister SDK之前，请验证以下内容：

+ 您具有Internet连接，并可以访问本地macOS或Linux计算机上的Shell终端。
当前，DFINITY Canister SDK仅在具有macOS或Linux操作系统的计算机上运行。
+ 如果要在项目中包括用于前端开发的默认模板文件，则已经安装了node.js。

本教程假定您知道如何在计算机上执行常见任务（例如打开终端并运行命令）。 如果不确定如何在本地计算机上打开新的终端外壳或如何安装node.js，请参阅针对新手的预备步骤。 如果您无须满足先决条件就可以满足要求，请继续下载并安装。

<hr>

### 下载并安装

您可以直接从本地计算机的终端外壳中下载最新版本的DFINITY容器软件开发套件（SDK）。
+ 打开本地计算机上的终端。

例如，打开“应用程序，实用程序”，然后双击“终端”或按⌘+空格键以打开“搜索”，然后键入terminal。

+ 通过运行以下命令下载并安装DFINITY Canister SDK软件包：

```javascript
sh -ci "$(curl -fsSL https://sdk.dfinity.org/install.sh)"
```