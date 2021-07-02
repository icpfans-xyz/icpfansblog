---
title: "ICP与ETH互操作的原理与启示"
date: 2021-06-12T06:40:24+06:00
# post thumb
images:
  - "images/post/dynamic/6-12.png"
#author
author: "ICPFans"
# description
description: "ICP与ETH互操作的原理与启示"
# Taxonomies
categories: ["Dfinity","进展"]
tags: ["Dfinity","进展"]
type: "regular" # available type (regular or featured)
draft: false
---

这篇文章是Dfinity创始人Dominic Williams5月28日Medium《Internet Computer <> Ethereum Integration Explained》的笔记，解答了我几个疑惑：



1. ICP和ETH的定位和关系？

2. ICP目前是如何与ETH交互的？面临哪些问题？

3. ICP和ETH的互操作性将带来哪些机会？



### ICP与ETH的定位和关系：


![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHumibiaNdReZsLJfw7n6ndEr1O2lyiaHicUPI8J3CHNmKj0YLyZWOYibzkaeJ7o1qgL8cGicdLzibI7dB1cg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



ICP与ETH设计初衷不同，定位不同，是相互补充的关系。ICP的结构是由独立节点构成的不同子网，其计算资源由各地计算中心提供，计算中心所使用的的硬件设备经过特殊的定制。是一个由计算中心-神经元（子网）-容器（canisters）构成的双层结构。以太坊与其相比，计算的底层开放度更大，任何人都能提供计算。其结构是矿工（计算）-智能合约（smart contract）的单层结构。不同的结构设计使得功能侧重不同，ICP倾向于终端用户的应用层，而ETH则倾向高价值资产的金融结算层。随着ETH网络被越来越多的人接受，GAS费快速抬升，计算资源非常紧张，1GB的智能合约将耗费价值1亿USD的ETH（最新数据），而在ICP运行这类应用的花费将低于5USD的Cycle。


![](https://mmbiz.qpic.cn/mmbiz_png/QwB0IHJuPHumibiaNdReZsLJfw7n6ndEr1dmXhC7rNxUoGHmLYS4HcA8rtl6ia8KQibAHYCUzZK9xX1ica9MFwcgO4Q/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



未来人们很可能在ICP上使用消费级应用，而沉淀后的数据资产经过打包，交易，形成金融资产。这部分金融资产则很可能被传送到ETH上进行金融相关的操作。利用ICP容器的运算存储性能，用户可以获得更丰富的web3.0服务；而利用ETH智能合约的原子性和不可篡改性，用户的高价值资产得以获得更大的安全性。



此外，ICP的 Chain Key特性可以使得用户直接通过数字身份（Face ID，指纹，YubiKeys）连接以太坊，而不必管理复杂的钱包。这些特征都将大大丰富两者的生态。



### ICP与ETH互操作的原理：


we will introduce support for a threshold variant of ECDSA. In essence, this will enable smart contracts on the Internet Computer to create Bitcoin and Ethereum transactions pertaining to public keys on those chains, without holding corresponding private keys (which will not even exist, and instead take the form of private key shares securely distributed across independent nodes).



ICP用的也是椭圆曲线数字签名算法（ ECDSA），对于ICP用户而言，可以在没有私钥的情况下创建链上的交易。具体实现方式，就是通过子网多签私钥，再由公钥验证，从而实现整个交易。也就是说，ICP到ETH网络的互操作性，是通过ICP上子网多签来实现的，先由子网多签发起交易，再由子网在ICP内部交易。简单说，BLS 门限签名的作用就相当于一个私钥了。



解决完了如果从ICP到ETH链，那么如何从ETH返回执行的结果呢？



阶段一：由于目前的ETH具有原子性，因此每一个地址的状态都会经由PoW的方式来验证并且同步。因此当我们在ICP上需要获取ETH状态时，我们可以检测ETH区块的状态，每当区块被验证时（要在一定区块之后，这样正确率才能有保证），ETH上的智能合约就能从区块所有数据中读取我们想要的状态，并传输给ICP上的智能合约。当ICP智能合约运算完成以后，可以直接通过预言机将信息和数据传回给ETH。从而形成一个ICP与ETH的操作闭环。



由于从ETH向ICP需要智能合约的功能，这一切运转在ETH上，这意味着这类操作是非常昂贵的。当ICP大量需要ETH传输信息的时候，高昂的成本将限制ICP和ETH之间的整合与协作。



阶段二：为了节省ETH智能合约功能的成本，我们会同步ETH节点状态到ICP的智能合约。这个合约不仅会扫描以太坊的区块，同时也会更新以太坊的全部数据。一旦这个工作完成，意味着查询以太坊状态的同时不会影响以太坊的状态（主要由于EIP1559以后，智能合约的运转会燃烧ETH，全网状态会因此改变。），并且调用智能合约的成本也将几乎为0。一方面ICP将运转ETH的一个节点，另一方面ETH的实时状态也将同步在ICP网络之上。



### 潜在的机会


+ 进入第二阶段，意味着ICP对ETH调取合约，获取状态的成本会降低到很低的位置。但与此同时，另一个问题浮出水面。由于ICP全网对于ETH状态的获取，依赖ICP网络运营的ETH节点。一旦结点出现问题，那么就会带来巨大的安全隐患。那么我们是否能构建，节点/智能合约双互操作体系来逐步过渡和渐进？渐进地取舍效率与安全，才能配合ICP的发展水平。



### 总结
+ ICP到ETH，主要通过子网多签创建智能合约的方式。

+ 第一阶段：ETH返回ICP数据，利用ETH智能合约获取ETH区块具体状态，然后返回。第二阶段：ETH返回ICP数据，在ICP创立Canister同步ETH结点的完整信息，从第一阶段：向ETH上智能合约了解信息（互操作），进化到第二阶段：向ICP上同步ETH结点的智能合约了解信息（互操作）。

+ 前期问题集中于互操作的成本上，后期问题集中于安全性上，如何在成本和安全性上取舍做出更好的互操作方案，是一个潜在的发展方向。

作者：Yolo

##### 转载 [原文链接](https://mp.weixin.qq.com/s/FMOqngQ_TAfFnjRVKiW46A)