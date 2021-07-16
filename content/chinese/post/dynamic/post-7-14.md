---
title: "Dfinity认知介绍三：Dfinity的技术架构和共识机制"
date: 2021-07-14T06:40:24+06:00
# post thumb
images:
  - "images/post/dynamic/7-14.png"
#author
author: "ICPFans"
# description
description: "Dfinity认知介绍三：Dfinity的技术架构和共识机制"
# Taxonomies
categories: ["Dfinity","进展"]
tags: ["Dfinity","进展"]
type: "featured" # available type (regular or featured)
draft: false
---

<center>
<font color=#F0672C size="5">Dfinity的技术架构</font>

</center>
<br/>

Dfinity基于区块链计算协议ICP运行，采用了分层结构，主要包含**软件容器、子网、节点**以及**数据中心**。它可以看作是由很多个子网（Subnet）组成，在每个特定功能和属性的子网中有多个软件容器（Canister，Dfinity 中的可互操作的基础单元，也就是我们熟知的智能合约），在软件容器中包含了用户上传的代码和状态。Dfinity 的最底层是托管专用硬件的独立数据中心，数据中心之上运行节点（Node），节点负责处理子网容器中的数据和状态执行。


<center>

![](http://mmbiz.qpic.cn/mmbiz_jpg/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24w1v7ISAccIpMrdUuOFEuHxx3bCllAyibYSKndTAXticvIMAlLcpD1Obsw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1&retryload=7)

</center>

<font color=#F0672C size="4">子网</font>



子网是互联网计算机组成部分，负责托管计算机软件容器的不同子集，以NNS方式汇聚节点创建子网，节点机器将通过ICP协作，对称复制相关数据和计算。



<center>

![](data:image/gif;base64,iVBORw0KGgoAAAANSUhEUgAAAAEAAAABCAYAAAAfFcSJAAAADUlEQVQImWNgYGBgAAAABQABh6FO1AAAAABJRU5ErkJggg==)

</center>

NNS构建子网时会合并独立节点，通过容错技术和密码技术确保子网防篡改并且不可阻挡。子网对用户和软件是透明的，他们仅需知道容器的身份即可共享。



公开、透明是互联网计算机设计的基本原则。也就是说，只要知道容器的身份和功能签名就能调用功能。Dfinity的无缝链接，使得在无需了解网络基础运行的情况下，获得许可的软件可以直接调用其他软件。


<center>

![](https://mmbiz.qpic.cn/mmbiz_png/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24wA7k1IgFsZ9P0UkuPBibgLPfMHp1z1ocsQ6ibTJA4WSRPqjCIdZOicqTxw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

</center>

比如这里有虚拟子网ABC，它托管了11个容器。NNS需要它拆分，子网ABC生成新子网XYZ，ABC仍使用1~6容器，XYZ使用7~11容器，这样就能保证所有容器的服务都不会被中断。



另外，想在互联网计算机上创建容器，必须针对数据、基准、系统等特定子网类型。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24wV8HnIjw9jtbvguKMNDqJtdwJl41uesh70z5Th2SGyJncSBAq7UZTkw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

</center>

不同的子网类型会为容器带来不同的属性和功能，比如容器被托管在数据子网，它就仅能处理查询，不能调用其他容器。想要调用，就需要一个系统子网。如果再希望保留ICP token的余额，就需要一个受信任的子网。



<font color=#F0672C size="4">容器</font>



容器在虚拟机管理程序内运行，通过指定的API交互。它内部是WebAssembly字节码，通过编译Rust或Motoko之类的编程语言来创建。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24wA5VQAjic9LCS8Fu6icKH5QyM3f1e1F4ic076Wbyia7yuFQYMQzgkfYfGOA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

</center>

它们可以更新调用或查询调用，当将函数作为更新调用时，对数据做的任何更改都会保留；而将函数作为查询调用使，那对内存的所有更改都会被丢弃。

<center>

![](https://mmbiz.qpic.cn/mmbiz_png/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24w5kEf3N9825T5jtY0IlwAAqqDYWMXma0LS96DuhNltibwuXTDPYojpfQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

</center>
<center><font size="2" color=#A0A0A0>用户在请求自定义新闻源</font></center>

<center><font size="2" color=#A0A0A0>并且以很快速度获得了新生成的内容</font></center>



所以，容器可以创建新的容器并且可以分叉。

<center>

<font color=#F0672C size="5">Dfinity的共识机制</font>


</center>
<br/>


Dfinity由基于股权证明（POS）的四层共识机制提供支持。它由一个身份层、一个随机数信标层、一个区块链层和一个公证层组成。这些层共同实现了可证明的安全性和对已知攻击（如女巫攻击和51%攻击）的抵抗力；达成了接近互联网服务器延迟的区块间延迟；保持了去中心化，确保网络可以扩展以支持数百万的节点参与。Dfinity在共识机制上的创新能够突破区块链理论的“不可能三角”。


<center>

![](https://mmbiz.qpic.cn/mmbiz_jpg/FWVRP8nXH9oUicEiat4mlsff0jqfW9B24wDPc1cwjlecsCCA4dVic5VwyfoI11ST8ODw6iarZQxibCklJehyLyibCrJA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

</center>


**准备工作**

* 节点创建私钥公钥，建立匿名的永久身份。

* 节点加入网络需要抵押固定的token作为staking。

* 节点随机的与其他节点组成阀值组（完全随机，一个节点可存在于多个阀值组）。

* 阀值组中，运行分布式密钥协议（DKG），每个节点获取该组的“验证签名”密钥（不同于个人密钥，由一组的私钥数学拆分而来）。

* 系统还是根据DKG产生阀值组的共同公钥，并对阀值组进行注册。

* 准备就绪，开始等待参与共识。



**参与共识**

* 系统根据R-1轮次生成的随机数，在已有的阀值组中随机的选择R轮的委员会。

* 选出的委员会分成两部分，提案组与验证组，提案组先收集用户发送的交易，检验合法后进行打包，出块与常见区块链项目一致。

* 公证委员会持续接收并验证区块，包括接受区块、检验合法、计算优先级、签名并广播。

* 随机数信标持续的收集公证者广播的签名部分，并记录数目。

* 一但对单个区块，接受了超过50%公证者的签名，马上聚合签名，产出公证Zr（本质是时间戳）并写入区块广播。同时产生根据这些签名产生随机数，广播。

* 同步正确区块，R+1轮开始，回到step1。



**ICP基金会**

ICP基金会是全面布局Web3.0未来发展的Dfinity专项生态基金会，首期生态基金已完成募资1000万美金。基金会将致力于深耕互联网计算机生态项目投资，搭建链接传统产业应用与去中心化互联网计算机网络的桥梁，并赋予所投资的项目“媒体宣发、项目路演、社群导流、技术孵化、产业对接”等全站式支持。



如有优秀项目推荐，请联系邮箱：icpfoundation@tianrukj.com，我们随时愿意帮助和提供资金。



图片
来源：ICP 基金会
##### 转载 [原文链接](https://mp.weixin.qq.com/s/k-aWXqJVj19DpWKS8eOlxg)