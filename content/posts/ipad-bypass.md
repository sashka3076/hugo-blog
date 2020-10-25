---
title: "iPad Apple ID 解激活锁"
date: 2020-10-25T15:12:00+08:00
tags: ["经验分享"] 
draft: false
toc: true
---

## 引言

前几天我弟因为在 iPad Air 上 登录了别人的 Apple ID 下载软件，被别人恶意锁了设备。

出现这种情况，是因为他在 iPad 的「设置」里面登录了别人的 Apple ID（如果是在 App Store 登录就没事），别人就可以远程通过「查找」App 标记为「丢失」了，然后你的设备所有数据就会被抹除，并且无法使用。只会出现激活锁界面。

![20201025I8trlT](https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/20201025I8trlT.png)

## 解决方案

要解决这个问题就两种方案：

- 找 Apple 客服，证明这个设备是你的，只能通过带有序列号的发票或者盒子两种方式。然后他们会帮你解。
- 登录启动「丢失」设备的 Apple ID。

很不幸的是我第一次遇到这种情况，没什么经验，这个 iPad Air 是我 2013 年买的，这都快7年了，盒子早就不见踪影了，而且当时是在淘宝上买的，也没有电子发票。我们也尝试过第一种方案，但是无果。

这次事件，很明显是别人有意恶意锁你的设备，而且他还给我弟发消息要求给 300 多块钱才肯解，这不是勒索吗？我知道的时候很气愤，但是我弟也有错。

这设备当时是 3000 多块钱买的，容量只有16G，现在也能用，就是比较卡，除了屏幕大没啥优点了，我觉得 300 块钱没必要。

某宝上也有花钱解设备锁的，至少是 200 块钱，我觉得也没必要，于是昨天周六我决定自己动手帮他解设备锁。

## 解激活锁

说了那么多，我们终于进入正题了，解激活锁主要是分两个步骤，首先是越狱，然后通过另外一个软件绕过激活锁。

当然这种方式还是会有缺陷的，不是完美解锁，听说不能打电话，放在 iPad 也不能打电话，不能在「设置」登录 Apple ID 了，也就是说不能使用 iCloud 了，但是可以在 Apple Store 登录，可以下载 App，也够我们用了。

### 越狱

越狱工具使用的是 [checkra1n](https://checkra.in/)，直接去官网下载安装，按照教程使用就可以了，步骤很简单的。

这里要提一下我们碰到的坑，我最开始使用的是最新版 checkra1n ，但是越狱的过程中报错了，后来我想想是不是我的设备太老了，而且我们的 iPad 还是 iOS 12 的系统版本，于是我就去 [All Releases](https://checkra.in/releases/) 页面找 iPad Air 字样，找到了 0.9.7 版本，最后试了一下果然就成功了。

### 绕过激活锁

这一步花了我们不少时间，网上最有名的是使用 Checkm8 软件，他们绕过激活锁功能只有 PRO 版本才有，而且这个功能是收费的，按设备收费，一个设备 19.99 美元，现在我终于知道为什么某宝上的服务都是 200 多了。

虽然 19.99 美元 不是很贵，但我认为 7 年前的 iPad 不值，于是我就去网上找其他软件，而且大多数都是 Windows 平台的软件，还好我电脑虚拟机安装了 Windows 系统。最好好不容易找到了一个，操作了一番成功了，但是当我测试是否支持重启的时候，发现它重启之后就白苹果了，还好我们可以通过电脑的 iTunes 恢复 iPad 系统，就是很浪费事件，而且又要重新越狱一次。

最后让我成功绕过激活锁的是 XgRiNdA 这款软件，激活步骤非常简单，免费而且支持重启，但是只能在 Windows 软件。介绍和下载链接就从这篇文章中找吧 - [《Free Untethered iCloud Bypass by XgRiNdA all devices checkra1n supported》](https://myicloud.info/free-untethered-icloud-bypass-by-xgrinda-all-devices-checkra1n/)

## 最后

现在你知道 Apple 设备盒子还是有点用的了吧，建议你回头有时间把盒子上的序列号拍下来。

当然我知道解 Apple ID 激活锁的设备也有可能是非正常渠道获取到的，所以这篇文章我的主要目的并不是在教你如何解 Apple ID 激活锁，而是分享我的经验，以及一点安全知识。如果这篇文章对你有帮助，那就把它分享给更多人吧。