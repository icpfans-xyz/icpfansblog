---
title: "一文带你读懂无法索取ICPunks NFT的背后原因"
date: 2021-09-08T08:40:24+06:00
# post thumb
images:
  - "images/post/ecology/9-8.png"
#author
author: "ICPFans"
# description
description: "一文带你读懂无法索取ICPunks NFT的背后原因"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "featured" # available type (regular or featured)
draft: false
---

![](https://mmbiz.qpic.cn/mmbiz_jpg/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8iafrPb7WN3TZFLkJxwK3Y2blyicP9ibQz6S3icarExLDlBfZdH8IyVF20w/640?wx_fmt=jpeg)

ICPunks是Dfinity上第一个Cyptopunks风格创建的IC NFT项目，ICPunks上的NFT是引入ERC-721进行铸造的，该项目一共铸造10000个不同特征免费供于社区索取链上小丑，该项目10000个NFT的索取过程分为4个时间线：北京时间9月2日凌晨0点，北京时间凌晨2点，北京时间凌晨3点，北京时间凌晨4点，前三个时间线皆是白名单索取，凌晨4点时间线为普通参与者索取，在4点时间线时有大部分用户到点之后几乎大部分参与者无法索取NFT，本期文章带各位小伙探讨ICPunks无法索取的根本原因？



我们回忆一下当时UTC时间20:00（北京时间凌晨4点）当时在ICPunks官网无法索取的两个问题：第一个是ICPunks前端没有加载出Chaim功能无无法索取，第二个是Chaim按钮出现后大部分人Chaim不了NFT。



![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8Nnexn79YvLQhASBQRLLSt3UZTVUdP7kfhQJFC8rsMwRC30NHzzQx9A/640?wx_fmt=png)



以下部分资料由开发者论坛的队员提供，注意：以下均是个人分析，ICPunks官方解释出来可能会有变更：



我们在Plug钱包中查看交互过的Dapp查看到ICpunks Dapp由两个部署在ID为Pjljw的公共子网上的Canisters组成，通过IC.Rocks区块浏览器可以查看到该Canisters的分布详情。由此可见ICPunks 的Canisters均部署在ID为Pjijw 的子网上。

 <center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8mYpibMibkdMMfqaLSqwOBAh7ibiaq49mY3uRibsyAhqiaHms6IlZIBiatAn8g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

qcg3w-tyaaa-aaaah-qakea-cai

</center>

<center> 

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8oHETMMzFM4icF57EwqbW6fctanGvhJ6hlcnia9jzxDNSdSUiaqw2Fibacw/640?wx_fmt=png)

3hdbp-uiaaa-aaaah-qau4q-cai

</center> 

回到在开发者论坛队员提供的资料显示在UTC时间2021-09-01 16:00（北京时间0点）时第一波增加流量开始访问pjijw子网，该时间是ICPunks第一波白名单索取NFT的用户，在下图边界节点发送的HTTP请求显示在UTC时间16:00至19:00发送的HTTP请求只增不减，逐渐增长的流量发送的HTTP请求开始达到边界节点配置的速率限制，所以边界节点开始限制对子网上容器的消息请求，这不仅对ICPunks部署的容器造成了影响，也对pjijw子网上的其他容器造成影响，这就意味着边界节点开始限制用户发起的HTTP消息请求。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8gGjYAVtzC98VSRriaCNFCqgVJhw1jtQQ7eHI0xFrPsDjO9QeG1UXy8g/640?wx_fmt=png)

边界节点发起的HTTP请求

</center>



![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8rFZZicOP6iaWjuGiaNvsS3D6wv9XYxWyqekkia5YILXRMDwE0LFL7eOPwA/640?wx_fmt=png)



![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8ECRpAED5ayNgLXVA1zHSpQibTUmvzZzsSGYgZJAjw1yp2iaGRm9pQtcQ/640?wx_fmt=png)



而在UTC 20:00的时候从边界节点发起的HTTP请求急剧增加，这也是ICPunks全面开放的极端，当时发起HTTP请求的峰值达到了每秒38k次以上。

<center> 

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8zCyjRSQwkrpDy1NVazqFIhQkNXjMC9PTcCSlUM24Bcj0JgpTpDQ5hg/640?wx_fmt=png)

UTC 20:00 边界节点发起的HTTP请求

</center> 

在ICPunks还未启动Chaim时，节点和子网表现是正常的，而在开启Chaim索取时，大量的更新调用提交涌入子网，从每秒提交18次更新到超过每秒提交1000次更新调用请求。

 

以下图片是通过边界节点发起的请求响应的返回结果的数据：

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8HMxM232XtOuRqJJY8OWZlibFiczcj1UK1coZYWv5FRMZeUWYUb2xLGSQ/640?wx_fmt=png)

图一



![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8qUU1ZSEYlibQH5cElyicFHeGTk1JReKJDzjU163Nr2nxUKgtICOy93Rg/640?wx_fmt=png)

图二

</center> 


我们可以看得到在图一在UTC时间16:00之前状态峰值相对于来说处于一个稳定的状况，自ICPunks第一批百名单开始（UTC时间16:00）之后，大批流量涌入通过边界节点不断的发起调用请求之后，子网节点开始返回403结果，而在UTC时间20:00 ICPunks全面启动的的时候，返回403结果的数量更是达到了一个新的临界点（403结果是被子网节点拒绝的调用请求）。而在图二中ICPunks全面开启之后返回202结果只有少数部分（202 HTTP状态代表消息调用被受理）这意味在ICPunks从20:00开始之后只有少部分人的调用请求被受理了，而大部分人的调用请求被节点拒绝，也就能表明当时出现Chaim界面之后只有少数人可以索取，大部分用户则是被拒绝请求的。

 

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8TbJISVHnCexdHDpvmiaOQjnicvbKf3dsjmXaBceUVLGJdXuDYBLPZFmg/640?wx_fmt=png)



由于ICPunks全面开启（UTC时间20:00）之后大量流量涌入导致pjljw子网的最终区块的确定率从1秒/块下降至1秒/0.3个区块。

 

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8tj1qfI68kF5vI0A5ZdT3icNcYjKyeoIZcjGh11Pcw4JprobHicbojdWA/640?wx_fmt=png)



并且这个阶段pjljw子网通过入口的消息调用限制为每秒50条。



在根据开发者论坛队员给出的资料我们可以将ICPunks造成pjljw子网网络拥堵的时间线流程分为：



- 2021-09-01 16:00 ：ICPunks第一批白名单Chaim，倒计时开始流量开始涌入
- 2021-09-01 16:15 ：在查询调用中边界节点开始速率限制，速率限制随着20:00的临近继续增加。
- 2021-09-01 19:00：第二波Chaim发生，导致流量的进一步增加，但由于第二波Chaim的参与者数量有限，所以在更新调用的量仍然很低。
- 2021-09-01 20:00：Icpunks全面开始Chaim导致流量急剧增加，以每秒发起38 rep达到边界节点的峰值从个人导致pjljw子网因为大量请求涌入导致区块最终确定率降至0.3块/秒。
- 2021-09-01 20:40：随着NFT的索取降低，流量开始逐渐减少，流量请求降低至10k rep/每秒，并随着时间继续下降。
- 2021-09-01 20:45：pjljw子网恢复正常完成率。

根据开发者论坛队员的描述：在客户端（浏览器的控制台日志中）显示边界节点网关.ic0.app返回大量的报错代码500，而ICPunks的静态资源是通过Dfinity提供服务的，所以只有ICPuks的前端加载足够多的静态资源才能够发挥作用：这也是为什么这么多用户除了不断的重新加载页面而什么都做不了的原因。

 

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTQ27rvdTGuZ9Ec5Q1OYRK8eMcRywBRo39bGZGW3enCZUm4iaaNljrE9kaYIdq1XkD54YtXdRoGQ9g/640?wx_fmt=png)


从UTC20:00时间之后边界节点涌入大量流量并向ICPunks的两个容器发送高频的调用消息请求，而容器高频更新负载导致子网性能下降，这个因素导致用户无法与ICPunks上的Canisters进行交互索取NFT，以及访问pjljw子网上的其他容器，并且这段时间内大多数消息请求要么会被受到速率限制，要么会被节点直接拒绝（因为消息请求过载）或者会被返回不同的报错结果，所以在当时只有一小部分用户的调用请求被受理，而大部分用户的请求是被拒绝的，而第一批白名单的用户能够正常Chaim他们的NFT是因为当时他们并没有受到速率限制并且当时子网的完成率是正常的。



尽管在当时的流量很高pjljw子网也继续处理查询调用和更新调用的请求，边界节点也继续为流量提供服务，速率限制是为了保护子网免受大量流量的影响，因为未经过过滤的流量可能会导致子网节点更多终端。



在开发者论坛中队员表示会通过改进以下要求防止再次出现此类事件的再次发生：



- 改进有关如何在IC拓展去中心化应用程序的文档。

- 在边界节点上启用（符合标准）HTTP缓存并向开发人员传达最佳实践。

- 在区块之间评估节点上查询API调用结果的缓存。

- 使用多线程进行执行调用（目前使用64内核中的一个进行单线程执行）

- 负载测试并根据更显示的流量负载调整速率限制。



来源：DfinitySZ

##### 转载 [原文链接](https://mp.weixin.qq.com/s/say5FmHoGkzMwDiLNOJCzg)