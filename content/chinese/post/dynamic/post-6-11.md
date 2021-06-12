---
title: "两方案看Dapp如何应对前端托管的风险"
date: 2021-06-11T10:40:24+06:00
# post thumb
images:
  - "images/post/dynamic/6-11.png"
#author
author: "ICPFans"
# description
description: "两方案看Dapp如何应对前端托管的风险"
# Taxonomies
categories: ["Dfinity","进展"]
tags: ["Dfinity","进展"]
type: "featured" # available type (regular or featured)
draft: false
---

我们都知道常见的DeFI应用一般都采用三层架构，前端-中间件-后端（智能合约），而这个三层架构当中只有后端是部署在区块链上，一经部署不可更改。而前端和中间件都是部署在中心化的服务器上，这也意味着前端和中间件这些衍生的结构容易受到攻击和作恶。



## 简介：常见DeFI的架构


![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvT37RVGNR0A7s7S8ZQr8AFDiaQEEoE9Uicfpbpbmx1j7MquFXcYRlImTLw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

当我们使用DeFi应用的时候，各个环节是如何协作的呢？图上所示的是一个正常网络环境下的调用。当我们输入{website}的时候，用户的游览器会访问DNS服务器，去查询{website}对应的IP。查到这个IP之后，对面DNS服务器会返回IP地址，游览器会再次根据IP地址去寻找web服务器。一般来说，我们的网址所需要的图片，文字，交互等内容会放在web服务器上（可能是真的物理服务器，也可能是云）游览器读到这些信息之后就会返回呈现给用户。之后用户的点击，都会经由游览器，Web服务器，去和链上的智能合约进行交互。经过用户的签名之后，行为会经由共识机制和链上广播，变成可信的状态。

那么这个过程之中，项目和用户分别存在什么风险呢？



1. 托管平台的干预。早年应用部署在单个服务器上，单一服务器的物理状态成为风险之一。随着技术成熟，云逐渐出现，通过将计算分布在大量分布式计算机上，避免了单一服务器的物理风险。但是目前这种技术的仍然存在风险，这种风险就是云平台作恶的风险，前端的数据信息暴露在big-tech的视野之下，无从躲避。

2. 偷换前端。目前来看，大多数项目都会开源前端代码让用户独立审查，用户下载前端代码在本地运行之后，便可自行与托管在区块链上的智能合约进行交互。通过这一流程，用户可以评估前端的风险。但是由于实际前端仍然托管在中心化的服务器上，用户很难验证公开前端是否就是目前正在运行中的前端，前端仍然存在偷梁换柱的可能。举例来讲，正常前端连接到官方的智能合约，而恶意前端就可能连接到恶意合约，通过用户授权对用户造成伤害。



为了应对上述两类风险，市场上看到了一些实践，主要是Uniswap的IPFS方案和Liquity的ICP方案。



## 方案一：Uniswap的IPFS的方案


![](https://mmbiz.qpic.cn/mmbiz_jpg/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvTtuwuoCrAN91k53dCQ6ObUWKicNd6vQWzaW1SSMchojqRxmG1I3SianJg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

Uniswap直接将前端部署上IPFS，他们具体是怎么做的呢？1）前端文件存放于Github，通过Github Action向IPFS部署，每天至少一次。2）通过pinata.cloud用户的游览器可以获取前端的页面。

![](https://mmbiz.qpic.cn/mmbiz_jpg/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvTjVknjWzUK1KiaWCHldg01y6ib9wkuvlJH5FscicuMNHr4lsfGGREibE9xw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

从用户视角来说来说，当他们在登录Uniswap的时候，互联网到底发生了什么呢？用户登录 app.uniswap.org，游览器查看DNS记录找到了前往cloudflare-ipfs.com的CNAME，再通过Cloudflare’s IPFS gateway的云网关，查询DNSLink record，找到存放在IPFS上的hash码，最终通过hash码获取前端的文件。



## 方案二：Liquity的ICP方案


Liquity是以太坊上的抵押型算法稳定币，该Dapp拥有一个非常有趣的特性：开放式前端。开放式前端，指的是不同的前端运营商可以独立运行前端，并且设置自己的kickrate（kickrate会调节用户所得到的相关收入和奖励，如果kickrate=99%，意味客户拿到99%，前端拿到1%）

在结构上，Liquity分为前端界面和后端智能合约，在商业上，Liquity也将由前端运营商和后端智能合约开发商，分开运作。Waterslide是Liquity的前端运营商之一，也是第一个部署在Dfinity上的DeFi前端，下面介绍的实践主要来自于Waterslide。


![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvTLpeJMh6qLaZibpiajdgctp6LjsKeLFPLqOR2KTZVRwYDToTfaPMpict1Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



ICP方案当中前端应用的主体身份是根据域名来的。也就是说域名和Canister的内容是永远联系在一起的，这一点适合传统互联网截然不同的。当项目组创造了自己Canister，并将前端页面所需要的的文件托管在canister中，caniser就会被分配特定的域名，用户会直接通过DNS访问特定域名https://{website}.ic0.app（什么是Canister？可以理解为分布式Docker，详细细节可以参考）也因此用户和前端页面通过Dfinity紧紧地联系在了一起。那么具体Canister具体是怎么运行前端的呢？



### 运行canister


![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvTbPpwFibSpqI6sYr1K3Zum2jbrZGDMuwWCodJ5yuiaTb8eVeFZOdCc3Fw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

运行canister的时候，系统会显示两个Controller和Module hash，前者是治理容器对于运行容器管理的ID，这个码一般情况是不可更改的，除非向治理结点提出提案；后者，是每一次Wasm部署完后的证明。



### 提交Commit更改

运行Canister以后，我们会需要升级，但这种升级是需要NNS来进行审批的。（NNS可以简单理解为子网的创建者，他将管理整个网络的事务。详细参考[《完整解析|网络神经系统（NNS）是怎么运行的》](https://mp.weixin.qq.com/s?__biz=Mzg4NDYzMDc1Ng==&mid=2247483736&idx=1&sn=fb250c17a0354c67a703cce6fad8c356&scene=21#wechat_redirect)）我们会将所需更新的文件同步到github，并将Canister更新的申请提交到NNS当中，申请文件当中包含几个要素：Commit ID，Controller，Module hash，Repo的位置。

图片 bd51eab就是我们Commit的代码，NNS的治理Canister会根据我们的proposal对Canister进行升级。

![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvTOQV2gJf99uoy28wwgVjYGlIbdzl4vpmnavVK7SYgJzoTd3Y5ukR57Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

当我们再一次同步canister的时候，会发现tag: mainnet-20210527T2203Z，这与我们提交的Proposal号相一致，也就证明NNS已经对我们的proposal已经进行了升级。

![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHt9icqiaHb3K4UnA1lwzAGRvT3B6cQ44FiaTOjKrlic917q5UrVvlfq4595157ZGUwJIJGFr77Joic3YyA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

### 用户是如何连接到前端的？
Waterslide网站前端托管在Canister之中，用户输入网址以后，通过DNS服务器会连接到https://{specific}.ic0.app.然后这个域名会通过Certifying Service Worker提供的Controller（如 'rdmx6-jaaaa-aaaaa-aaadq-cai'） 连接到对应的Canister，那么也就读取到了Canister当中的网页文件。用户与Canister之间的交互是直接的，这些行为都会被完整的记录下来。



### 两种方案的对比与启

<table >
<tr>
<td bgcolor=white>   </td>
<td bgcolor=white>ICP</td>
<td bgcolor=white>IPFS</td>
<td bgcolor=white>评价</td>
</tr>
<tr>
<td bgcolor=white>域名</td>
<td bgcolor=white>后缀：.ic0.app</td>
<td bgcolor=white>前缀：https://cloudflare-ipfs.com/ipns/</td>
<td bgcolor=white>前者系统未来可以适配，ICP的DNS系统，创建“靓号“；后者需要通过传统DNS进行桥接</td>
</tr>
<tr>
<td bgcolor=white>安全性</td>
<td bgcolor=white>域名和容器紧密绑定</td>
<td bgcolor=white>域名和托管文件绑定，但较为松散</td>
<td bgcolor=white>ICP当中的域名等同于Canister的身份，改名字需要上“公安”。</td>
</tr>
<tr>
<td bgcolor=white>历史痕迹</td>
<td bgcolor=white>ICP未来将创设容器将各个容器的更新记录进行归集，让每一次提交都变得可信（参考资料）</td>
<td bgcolor=white>依赖中心化github action进行推送</td>
<td bgcolor=white></td>
</tr>
<tr>
<td bgcolor=white>交互</td>
<td bgcolor=white>I由于用户与前端的交互数据也将沉淀，意味着前端的导流能力也具有可信基础</td>
<td bgcolor=white>不具备类似能力</td>
<td bgcolor=white></td>
</tr>
</table> 

	
这张表格梳理了两种方案架构上的优劣，可以发现IPFS是短期方案，而ICP更有利于长期的布局。而在商业上，ICP更有利于前端自身的商业变现，如果我们过去将DeFi后端智能合约等价于DeFi，那么随着ICP的成熟，将使得前端运营成为独立于后端智能合约的另一股力量。为什么那么说呢？因为ICP将用户和前端页面之间的价值流可信化了。不可造假的流量和交互，成为了资产定价的重要基础，这也将大大提升前端页面的玩法和创造力。结合Dfinity和ETH的交互，价值层归价值层，应用层归应用层（参考《ICP与ETH互操作的原理与启示 》）这将会为我们带来无穷的想象空间。



### Tips：
截止目前为止，ICP本身的容器并不能记录自身历史的数据，但是官方（nomeata语）有意愿创建一个可以记录wasm部署hash的Canister，这样一来就可以针对不可信主体提供可信的历史记录

从ICP论坛当中的沟通来看，目前ICP整体的开发任务量仍然很大。目前Proposal的处理感觉仍较为简陋。



参考材料：


https://aws.amazon.com/tw/route53/what-is-dns/

https://blog.waterslide.app/waterslide-the-first-defi-frontend-on-dfinitys-internet-computer/

https://www.reddit.com/r/dfinity/comments/n1xosf/value_proposition_in_comparison_to_market_leaders/

https://multicoin.capital/zh/2020/11/24/the-defi-stack/

作者：Yolo

##### 转载 [原文链接](https://mp.weixin.qq.com/s/xJFWzhjQTjUcsfqP9PjPSA)