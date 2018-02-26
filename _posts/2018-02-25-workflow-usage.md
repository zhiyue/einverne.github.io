---
layout: post
title: "Workflow for iOS 使用"
tagline: ""
description: ""
category: 经验总结
tags: [workflow, ifttt, automatic, ios, ]
last_updated: 
---

Workflow 是iOS上一款可以实现自动化过程的应用，在iOS 的框架内是先自定义的流程，比如发送最后拍摄的一张照片到 Instagram 这样的操作。他被 Apple 买下之后就免费开放给所有人使用了。有效的使用 Workflow 能够简化在手机上重复的操作。

Workflow 的功能应该由使用者决定，而不是开发者，所以 Workflow 和编程语言一样，需要学习。

## Workflow
下面先介绍一些 Workflow 能够做到的事情，然后从中去学习 Workflow 制作的过程，从而能够自己完成自动化流程。

### 图片九宫格
将方形图片切割为9格图片，Workflow [地址](https://workflow.is/workflows/7319fb05a18f49f7bbfc2ed28bb46724)

### 隐身相机
在不启动相机界面的同时拍照，并保存到相册， Workflow [地址](https://workflow.is/workflows/2466e3f50b6e4cae8f72137cfcd75a26) 这一个 Workflow 只有一个选项选择前置还是后置摄像头，如果你想要更加复杂的 Workflow 允许你选择连拍数量的可以使用[这个](https://workflow.is/workflows/8728b548747c46a4b04c38878e3db417)

### 下载到小米路由器
在手机上复制下载链接运行该Workflow即可，[地址](https://workflow.is/workflows/f505f2141b474fba825407624efcb14c)

### 切分全景图
将横向的全景图切分为多个图片方便分享到 Instagram，[地址](https://workflow.is/workflows/b67ce0525f4c44d8983f75af66d6efe4)

### 每天领取支付宝红包
支付宝去年推出的分享领红包活动，虽然一开始诚意满满，不过后来就只能每天领1毛了，不过1毛也是肉嘛，反正 Workflow 点一下够省事，[地址](https://workflow.is/workflows/3bdc85bd9f7f4c5798a65dd1962c0cfe)

还有更多好用的可以从下面的网站上获取，我平时常用的

- App Store 换区
- Instagram 下载
- Google以图搜图

更多的 Workflow 可以从下面网址获取

- <http://workflow.sspai.com/>
- <https://workflow.is/>

还有一个实用技巧就是实用 Google 的 site 搜索语法，比如想要搜索 Instagram 相关的 Workflow，则可以在 Google 中输入 `Instagram site:https://workflow.is/workflows/`。

如果你常用 RSS，那么可以在 InoReader 中订阅该组合包: <http://www.inoreader.com/bundle/0014cd63bb38>

## 自定义
通过上面的一些例子应该可以看到一些端倪，其实 Workflow 就是把一些常用的操作给编程化，比如最简单的支付宝领取红包，其实就是使用 Safari 打开一个链接。如果再复杂一些比如切割图片，涉及到一些宽高计算，可能还有些 IF 的判断。如果再复杂一些比如 Instagram 图片下载，涉及到了下载网页内容用正则去匹配关心的内容，在比如Google以图搜图，涉及到了Post请求，然后拼凑网页链接再打开。

最最重要的一点就是网络服务提供足够的API能够让 Workflow 能够轻易的调用，如果有翻译服务提供了公开可调用的API，我们就可以在 Workflow 中，获取粘贴板内容，将内容发送给翻译服务请求结果，并且将结果以通知或者其他形式告诉给用户，这样一个翻译的 Workflow 就实现了。

