---
title: "岂能止于2.0智能合约的Canisters"
date: 2021-08-24T06:40:24+06:00
# post thumb
images:
  - "images/post/dynamic/8-24.png"
#author
author: "ICPFans"
# description
description: "岂能止于2.0智能合约的Canisters"
# Taxonomies
categories: ["Dfinity","进展"]
tags: ["Dfinity","进展"]
type: "featured" # available type (regular or featured)
draft: false
---

![](https://mmbiz.qpic.cn/mmbiz_jpg/pTd1PaaakaRnD6uxqRvHnazfvAEB90JUs1EvGKJtor8RV0bjicFNHRnamtvvjVfbnsQjvnO6ZElFXQG7XChjdag/640?wx_fmt=jpeg)

每一个Dfinity Dapp都是由一些形形色色的Canisters（容器）组成的，它们可能各有不同，但是它们都是组成Dapp的关键单元，它们之间是具有互操作性的，Caniste是组成Dfinity全栈关键部分之一。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaRnD6uxqRvHnazfvAEB90JU1dewUiaZDPKdGucz8JDO9ViaGVT3zdbnteiaX5G2vcvvNzXb3V64OicUibA/640?wx_fmt=png)

</center>

Canisters类似于Container，因为两者都是被部署为一个软件单元，它们都包含应用程序或者互联网服务的编译代码和依赖项。Contaniner运行应用程序与环境分离，从而实现轻松可靠的部署，然而Canisters和Contaniner最大不同之处在于Canisters不仅存储当前软件状态，还存储了先前用户与Canisters的交互记录，Conitaniner 化的程序可能包含有关应用程序运行环境状态的信息，但Canisters能够保留用户使用应用程序功能导致的状态更改记录。


将容器部署到程序子网中后，该Canisters Dapp用户可以通过Web浏览器来访问Canisters定义的入口点函数实现与Canisters进行交互，并且用户可以通过入口点发送消息调用容器函数：非提交查询调用和提提交更新调用。



**查询调用：允许用户在不更改Canisters函数的情况下查询Canisters当前状态或调用Canisters当前状态进行操作**



- 同步并立即回复

- 可以对持有容器的任何节点进行查询调用，不需要该子网节点进行共识来验证结果。

- 不允许持久化容器状态的更改，查询调用智能用来执行读取容器操作。

- 不允许被调用的容器调用其他公开函数的容器（这个限制是暂时的，未来的查询调用将可以调用公开函数的容器。）

 

**更新调用：允许用户更改Canisters状态并保留更改**



- 异步回复

- 必须通过共识之后才能返回更新调用的结果，由于需要达成共识所以更改容器的状态可能 需要一些时间，更新调用涉及使用基于actor的编程模型（具有状态隔离）来允许并发和异步处理，参与更新调用的子网节点必须要达到3分之2节点结果达成一致才能执行。

- 被调用的容器可以调用其他公开函数的容器

 

注意：目前基于强大的数据中心查询调用的延迟是毫秒级的，更新调用也达到了秒级，如果你是一名想在Dfinity上构建一个Dapp一定要突认识查询调用以及更新调用的区别。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaRnD6uxqRvHnazfvAEB90JUzDh2Xh1029MhWdIicIaVZj1Wb1ASyibK6CaN3mzQdGCY4q2ub1fG2TKg/640?wx_fmt=png)

</center>

通常所有Canisters都是以消耗CPU Cycles的形式用于执行更新线程计算、路由消息的宽带和用于持久化数据的内存（容器维护Cycless的账户余额用于支付其Dapp所消耗通信、计算和存储的成本），目前cycles 的价格锚定 SDR，1SDR = 1 Trillion Cycles。SDR 的价格是国际货币基金组织设定的一篮子货币加权得来的，包括美元人民币等，相对稳定，虽然Cycles是由ICP来进行兑换，但是在NNS神经元系统中会有不断的提案来进行调节Cycles与ICP兑换比例保证Dfinity网络稳定的计算成本，最重要的是可以通过设置容器可以消耗Cycles的限制防止Dapp被恶意代码攻击耗尽容器中的Cycles。 



Canisters采用的是反Gas Token模型，用户在使用Dapp或与Dapp交互的过程中无需付出成本，这就和使用传统云服务的时候是一样的，用户在使用产品产生的计算和存储成本都由项目方承担，而其他大多数区块链都会向用户收取相对应的Gas费用，例如目前的Ethereum虽然经过了ELP-1559升级：引入Base Fee（基础费用）机制根据以太坊区块利用自动调整Gas Price的机制，但是这种机制依旧没有改变Gas 昂贵的本质。



ETH Gas 昂贵的本质在于二级市场ETH Token价格的变量（随着ETH价格的上涨，网络计算成本以及使用网络服务成本抬高），而Dfinity底层采用原生通证Cycles（稳定币）以及反Gas Token 模型作为驱动计算的结构，这种结构对开发人员以及用户来说都受益：对于开发人员来说他们不需要因为二级市场ICP价格的变量而担心在Dfinity开发成本被太高，而对用户来说他们不用考虑因为没有持有ICP代币而无法使用网络服务以及与Dapp交互过程需要付出Gas成本。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaRnD6uxqRvHnazfvAEB90JU8LYlzXJoDLxTcY5VBsI4SEwiaE5PzkP8hMDTeZV6KoLiaia9JUBTecSRA/640?wx_fmt=png)

</center>

Canisters不仅拥有当下智能合约相同的特性，也拥有智能合约之上的拓展（Actor、进程、WebAssembly）特性。智能合约是运行在链上的自动化程序，它们驻留在链上特定的地址代码（智能合约功能）和数据（智能合约状态）的集合，虽然任何人都可以通过编写智能合约部署到ETH网络中但是目前部署一个智能合约在ETH网络上的还是很昂贵，ETH链上存储1GB数据早在2018年的时候就达到了168万美元，而在Dfinity上创建一个容器并存储一年1GB数据所需的成本仅仅只要6美元不到（目前创建容器的Gas为0.142美元、存储1GB数据30天的Gas为0.467美元）。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaRnD6uxqRvHnazfvAEB90JUicMn78IgfSwI6bgGNhhBorAI6bCabY7LAB8aaFNx2GhrdhLHic9Ahu5Q/640?wx_fmt=png)

</center>


Dfinity计算成本数据查看：

https://sdk.dfinity.org/docs/developers-guide/computation-and-storage-costs.html



在当下的区块链技术来说，网络性能依旧是目前最大的难题，一个区块链网络随着时间增长的还有网络的负荷，而Dfinity采用的是Scalout的设计来解决网络负载问题：在网络性能负荷过载的情况下通过添加新的子网（添加新的节点组成新子网添加全网计算力和存储容量）来保持网络的均衡负载，并且Dfinity上的智能合约（Canisters）也是可以进行扩容的（这是智能合约的一大突破性），在计算方面Canisters没有选择以太坊智能合约全局原子性的设计，所以Dapp会由不同的Canisters组成，计算Canister做计算的工作，存储容器做存储的工作，所以每个容器都由自己的执行线程，最重要的是Canisters可以通过分叉原有Canisters和创建一个新的Canisters来增加整体Dapp的吞吐量和内容容量。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaRnD6uxqRvHnazfvAEB90JUZtlfMaCfk2Xnc8kMMQkZVRXj861l07BELfn5UUAXFVfB51CYGWO2qw/640?wx_fmt=png)

</center>

Dfinity目前Canisters的天花板是在于单个容器因为32位Wasm的虚拟机4GB的限制导致了Canisters的内存上限，针对这种情况Dfinity团队采用Stable Menmory（不受代码升级升级一影响内存管理）的扩容方法使容器的容量内存上限受制于子网的在内存总量（该方法让容器尽可能使用托管该容器子网多的内存量300GB），而另外一种方法是在于64位wasm虚拟机的实现，这意味着容器的容量将会达到TB级别。



在官方的路线图计划中Canisters的扩容仅仅只是第一步，接下来第二步Canisters将会拓展Canisters ECDSA阈值签名技术使Canisters在不存储私钥的前提下也能对数据做出签名，并且该签名可以通过公钥验证，这也是使Canisters能够集成BTC和ETH智能合约的先决条件之一，这意味着原来必须在私密环境下才能把私钥交给程序来做，现在可以放在一个去中心化的环境里来做，在第三步中Dfinity团队将对Canisters中应用AMD SEV的技术在一定程度上保护Canisters中用户的隐私数据，哪怕是节点运营商也无法窥探用户隐私。



来源：DfinitySZ
##### 转载 [原文链接](https://mp.weixin.qq.com/s/AoQydEgwESUWltDitenh4A)