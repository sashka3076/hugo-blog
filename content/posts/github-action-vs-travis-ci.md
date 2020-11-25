---
title: "GitHub Action 和 Travis CI 对比"
date: 2020-07-16T10:08:00+08:00
tags: ["github", "ci", "吐槽"] 
draft: false
toc: true
---

## 引言

![](https://blog-1251237404.cos.ap-guangzhou.myqcloud.com/ci.png)

[Travis CI](https://travis-ci.org/) 用了好几年了，主要用途就是实现我的静态博客自动发布，[GitHub Action](https://github.com/features/actions) 我是今年才开始用，今天我从自己的使用经验对比一下两个平台的使用感受。

<!--more-->

## Travis CI

### 优点

- 开源项目免费使用，私有项目收费使用。开源项目没其他的限制，对于开源项目非常友好。
- 作为一个老牌的 CI，使用的人多，这意味着你能在网上找到大量的资料。

### 缺点

- 好像一直被墙，国内要自备梯子才能使用。不知道为啥这个网站被墙。
- 我们公司使用的是付费版的 Travis CI，但是每次晚上发布版本的时候 Travis CI 一直要排队 Build，一次差不多要等个十几分钟，有点接受不了。
- 官方提供了很多服务，很方便，但是也有很多暗箱，比方说我配置了每次跑完 CI 无论成功与否都会给 Slack 发通知告知，但是不知道是不是我改了什么，突然收不到这个通知了，我调试了半天，还是没成功，也没办法看到任何日志，debug 默认还要发邮件申请开通，太不方便了。

## GitHub Action

GitHub 估计已经看到 CI 的市场了，于是自己开发了一个 Action，但是思路完全不一样，学起来也很快，而且用户可以自己写 step，然后把 step 可以共享给其他人用，减少很多重复开发，方便的很。

### 优点

- 跟 Github 结合的很好，如果你的代码正好托管在 Github 上，真的是使用起来很方便。
- 虽然 Action 起步晚，但是因为设计的好，生态发展起来非常快（原因上面已经说了），学习起来也非常快。
- 收费模式去产品首页就介绍了，免费用户 2,000分钟/月，足够我们个人用户使用了。**并且私有项目也可以使用哦**，这算是一个大亮点了。
- 同样的功能，代码在 GitHub 上，对比了两个 CI 执行的速度，Action 要更快一些。

### 缺点

- 功能还是有局限性，但是大部分情况已经够用了。
- 稳定性比 Travis CI 差，昨晚上在调试 GitHub Action 突然不 work 了，我却只能措手无策。最近 GitHub 500 的频率有点多，真为它感到担心。
- 功能还是比较简陋，我们甚至都不能主动触发 GitHub Action 。

## 最后

总结一下，反正我自己的代码大部分都在 GitHub 上，所以已经我决定已经优先考虑使用 GitHub Action，如果它不能满足我的需求，我再去看看 Travis CI。

关于使用实例，大家可以去看我的博客，也就是这个项目的代码示例：[forecho/hugo-blog](https://github.com/forecho/hugo-blog)