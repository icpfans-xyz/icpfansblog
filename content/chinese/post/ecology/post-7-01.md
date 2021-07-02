---
title: "详解Dfinity官网Grant展示项目"
date: 2021-07-01T08:40:24+06:00
# post thumb
images:
  - "images/post/ecology/7-1.png"
#author
author: "DfinitySZ"
# description
description: "详解Dfinity官网Grant展示项目"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "featured" # available type (regular or featured)
draft: false
---

![](https://mmbiz.qpic.cn/mmbiz_jpg/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMF51NmCcLzo9WoSV6vKgdDOWsRkjWM9lACDL0xHEYuaYMEe4GcYGpSlg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

自6月15号以来托管在Dfinity主网的容器数量增长10倍，处理的区块消息也突破了6000万块，主要得益于公共子网的开放，早期主网上线因整体网络容量有限，托管的容器需要经过白名单许可，公共子网上线之后，所有本地部署的容器可通过NNS提案部署到Dfinity网络中，公共子网适用于任何应用程序，这打开了Dfinity生态系统的开发大门，本期文章探讨已经部署在主网并且受到Dfinitry基金会Grant部分项目。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFYJIuEmBUangxSFUljSSGj9NEJLW5vkWoVO1qzZIpKhwYicFHJ2AMwFQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

<center>区块增长数据</center>

### Dfinity官网Grant生态项目展示：

![](https://mmbiz.qpic.cn/mmbiz_jpg/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMF7bMs1VcYTKtenQhNCzH228MrjS63ibB2BNu5ib2HvAWuuSSjupwCMs4Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


#### Internet Identity

Internet Identity 使用户能够在访问应Dfinity用程序时安全且匿名地进行身份验证，为用户登录的每个应用程序创建不同的身份，用户可以使用所有已注册的设备或身份验证方法登录同一帐户，与大多数身份验证服务不同，使用 Internet Identity 不用设置账户密码并且使用Internet Identity不会向任何应用程序提供个人身份信息。
Internet Identity利用 Web 身份验证 (WebAuthn) API 使用智能合约为 Internet 计算机上运行的应用程序提供安全的加密身份验证。Internet Identity 使用户能够使用内置于智能手机或笔记本电脑中的安全芯片或插入计算机 USB 端口的安全密钥来验证用户的身份并授权访问应用程序。前一段时间注册身份钱包大部分用户都因为设备或者浏览器问题都注册不了Internet Identity因为部分浏览器不支持webAuthn造成的，目前Chrome、Firefox和Edge浏览器不同程度支持WebAuthn、，Dfinity的大部分生态项目都需要使用Internet Identity验证使用，并且使用Internet Identity身份是反Gas模型的。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFfK06tseYJXibuJ6NiabsGZWiaJAIEdMibIe817mUFAOBJdwfnUsryDdFEg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* Internet Identity注册使用教程参考：手把手教你创建Dfinity身份钱包（超详细教程）
* Internet Identity注册链接：
nns.ic0.app
* Internet Identity开源代码：
https://github.com/dfinity/internet-identity 


#### IC.Rocks

IC.Rocks是Dfinity完整版的区块浏览器，其数据都是接入Dfinity容器数据，从查询ICP网络交易、网络升级、ICP铸造和销毁数据、铸币账户分配、神经元周期、容器数据、接电脑数据、Ledger账户、提案等数据都能在IC.Rocks上查询。这是生态唯一可以查看溯源网络状态的区块浏览器。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFdWL5CyqhicTQDBqVwiaovkY50hlQWKmD7JFx1hK7lPXShWsunYOl1rKQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：ic.rocks


#### NNS Dapp  

NNS Dapp允许任何人通过web浏览器页面与NNS Dapp的NNS神经元系统进行交互，该Dapp通过区块链提供端对端服务，使用NNS Dapp可以自由管理ICP代币，和神经元账户和参与投票获得投票奖励，该Dapp是一个完全民主治理的系统，负责监督网络和代币经济，在网络需要的拓展的时通过该系统来增加新的子网和节点保持网络的高性能，该Dapp也是由一组容器组成的，用户可通过Dapp使用质押ICP生成神经元账户来将提案发送到NNS治理容器中和使用该账户来对NNS治理容器中的提案进行投票获得治理奖励。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFG4rwZ2F4pzzsVnDoGSnh6nx8nick1F8ib0lGT0PiaJD0XIy5Vj2u8Xf8g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 向NNS治理容器提交提案：一文教你通过提案在Dfinity网络上部署Hello word
* NNS Dapp使用：Dfinity身份钱包使用教程完整版


#### Canlista
 
记录Dfinity网络上的容器注册表，通过搜索容器ID查看该容器的具体信息：查询容器的摘要描述和容器源代码，将Canlista和ic.rocks组合使用将会是非常不错的一个开发工具，Dfinity新手开发可以利用学习开发的一个组合工具，目前可以登录互联网身份来使用该工具。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMF5MC0eYLj5eUBYtMEuQdlLpyyrCVlm027CZ4R5KLxZYibwBSoB0kQCsQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：https://k7gat-daaaa-aaaae-qaahq-cai.ic0.app/


#### Sudograph

Sudograph是Dfinity上的graphQl数据库，其目标是成为构建Dfinity Dapp最简单开发工具，使用Sudograph时开发人员首先要使用GraphQl SDL定义成GraphQL模式，一旦定义了模式，就可以将其包含在容器中部署到Dfinity网络上，一个完整关系的数据库就是是从模式中生成，GraphQL查询支持各种CRUD操作和对关系数据的高级查询。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFsODQlGqpt81TliaGxlGvoITht7ibHiaCt3Bn8xmeJ50wvQc4Hek6F21Zw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

 
* Sudograph开源代码：
    https://github.com/sudograph/sudograph
* 使用Sudograph：
https://i67uk-hiaaa-aaaae-qaaka-cai.raw.ic0.app/



#### Reversi

Reversi是第一个完全托管在Dfinity网络上的的多人游戏，可以通过任何Web浏览器于任何地方的用户实时对战，Reversi是作为一个容器在Dfinity网络上运行的，游戏用户通过发送消息与托管Recerrsi的容器进行通信，通过进行异步函数调用使用该游戏。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFuQNjhEdiaxewpj6nULqRRjKWPAOH17ZlMX67VueozZu8I24Vic5bkbicQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* Reversi开源代码：
https://github.com/ninegua/reversi
* 开始对战：
https://ivg37-qiaaa-aaaab-aaaga-cai.ic0.app


<center>
<video id="video" height=380 width=680 controls="" preload="none" poster="http://mmbiz.qpic.cn/mmbiz_jpg/pTd1PaaakaQxyDjSr5k4s6ic1l63M3icPc8rn37kB8rJjK2CicIFvVArQenoheAKzrib9BeDZkw38TPxl0FgGkgzuQ/0?wx_fmt=jpeg">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bf2caaacaaal4anjzozonqfaegdaeiaaaia.f10002.mp4?dis_k=9db8467646eba135cda75e9033714545&amp;dis_t=1625198508&amp;spec_id=Mzg2MTYyNDAyMA%3D%3D1625198526&amp;vid=wxv_1934352346390511619&amp;format_id=10002&amp;support_redirect=1&amp;mmversion=false" type="video/mp4">
</video>
</center>
<center>Demo视频</center>


#### Fleek

Fleek 是 DFINITY 互联网计算机主网最早的应用之一，目前Fleek的所有功能都已经重新联机在Dfinity的主网中，Fleek上的11000基于传统和区块链的应用都能够在Dfinity的主网上运行，Fleek是一个开放式网络开发者平台，拥有在新兴网络上无缝构建站点和应用程序所需的一切功能，支持的基础协议有 DFINITY、以太坊、IPFS、Filecoin 等，提供的服务包括托管、存储、网关、域名和数据库等等。任何用户都可以通过Fleek部署Web3网页。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFgSUXbb98uD0ZUkZhlYHWINzQng5p3Zc76b6zR7711PCXoD8D4G4NFw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：https://fleek.co/



#### NNS Calculator

NNS Calculator是一个计算NNS投票奖励的计算器，它可以通过编辑变量根据投票的提案数量，溶解和质押时间和累计成熟度等数据来计算个人投票奖励收益率。
该Dapp计算的只是在个人投票权重不变情况下计算的收益率，投票权重的计算因素主要有质押ICP的数量、设置的质押和溶解时间等等，每天神经元中可能会有新加入的神经元质押新的ICP生成新的神经元，这时候在对比原有投票权重已经被稀释，NNS每天的投票奖励都是有一定数量的，但是投票的神经元可能会增加，这就相当于增加了全网的表决权，个人表决权如果不增加质押ICP或者增加溶解时间增加投票表决权，表决权就会被稀释，众所周知投票奖励是根据投票权重来分配的，此时获得奖励也就被稀释。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMF4zDg3ibCq0Bhb5JQFcADib1r0LpMA60d2WNCAQxPqribjoQXKvAZicCsMg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 具体的NNS 投票权重细节计算可以参考文章：Dfinity质押挖矿细节教程
* 使用链接：
https://networknervoussystem.com/


#### Stoic Wallet

Stoic Wallet是一个低门槛没有设备限制就可以创建数字钱包的一个平台，可以通过各种和方法对用户进行身份验证创建Internet Identity，其中该钱包主要功能有：创建子账户，创建神经元，实现ICP转账和给容器充入Cycles，该钱包对于Internet Identity来说实现来更低的参与门槛，用户可以不用考虑设备不支持webAuthn而导致的注册不了Internet Identity，并且增加了给容器便捷充入Cycles通道。该钱包可以链接Internet Identity来进行集成使用，使用Stoic Wallet钱包创建的助记词有12个单词，目前已经测试使用Internet Identity的助记词是无法双向导入的。Stoic Wallet支持PEM文件格式导入账户，目前Dfinity  Internet Identity的PEM文件可以通过Keysmith将BLP39助记词生成PEM文件。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFiaicfJU9mK15XibayEiaXOt5ljbNDNaMozru2x39aFTbDLQIeJHqQX1qAA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* Stoic Wallet官网：
https://www.stoicwallet.com/

* Keysmith工具：
     https://github.com/dfinity/keysmith
 

#### DFINITY Explorer

DFINITY Explorer 是一个始于 2018 年社区构建的Dfinity仪表板区块浏览器，目前提供有关网络、治理和 ICP 实用程序令牌的实时信息和统计数据，包括账户和交易信息。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFuL6zia7trscpWRBnao81TpZToLpmtpdkkM7ibEQujC8EOQLdiatpaPCQA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* DFINITY Explorer网页：
https://www.dfinityexplorer.org/#/datacenters


#### Agryo

Agryo是全球农业风险情报提供商，通过将农业数据带入链上使金融机构能够评估和管理作物田地的金融风险，以在全球范围内承保农业保险、贷款和贸易容器的金融服务。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFcU2N0Fibpq0hrzpXJ8OtdrtXkoLKBv7iaT2QibgNNLPFjAPHWpcuxelCQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：https://www.agryo.com/


#### OpenChat

OpenChat是在Dfinity上托管在子网上的软件容器上运行的一款加密聊天应用，并且它拥有各种各样的容器去运行中央服务，例如用户注册表和Webrtc连接处理，并且上面所有聊天信息都由软件容器处理和存储。通过使用WebRTC预先运行软件容器来保持即时加密聊天，代理软件容器将托管提案的Web浏览器之间建立点对点WebRTC连接。在OpenChat聊天可以随时打包带走聊天数据，并且OpenChat支持的功能还有多媒体消息即时发送、用户之间发送和接收Cycles。目前OpenChat的用户是限量1w，现在注册一个账户会赠送10t的Cycles，早期使用者和贡献者会得到后期OpenChat的代币，这些代币用户以后OpenChat采用的NNS治理模式来进行链上治理。

![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFYtUKpAAkXmJT0YcbqNEGChNdoO4t4GoyENeEpAco1KqfkJ9W5qmmTQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 注册链接：https://7e6iv-biaaa-aaaaf-aaada-cai.ic0.app/
* OpenChat详细介绍：Dfinity版WhatsApp—OpenChat


#### ORIGYN

ORIFYN是Dfinity基金会通过实物提供数字验证将奢侈品和NFT结合的平台，目前只能在Dfinity上使用，ORIFYN旨在保护人类的智慧资产ORIGYN采取先进的人工智慧能技术和去中心化体系对人类智慧创造出的珍贵物品进行识别，并鉴定证明其所有权归属，目前的业务范围包括：艺术品、数字媒体和奢侈品。ORIFYN的链上治理系统和采用的也是NNS治理系统，代币持有者通过质押代币获得投票权参加链上治理。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFbGtRN8goNBprzJafaY4UGNdlP1kylicOOsWLiaqNyAWeOaS1w812ymDQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：https://www.origyn.ch/


#### Distrikt

Distrikt是一个基于DFINITY的去中心化社交媒体网络，其前身为LinkedUp，致力于打造一个开放版本的LinkedIn。早在2020年初，DFINITY曾把LinkedUp作为demo在发布会上演示，以展示DFINITY上开发的便利性。今年二月，Dokia Capital 首席执行官Aurel Iancu决定为 LinkedUp 提供资金并成立一个专门的团队，扩展成了一个独立的项目 Distrikt。现在可以使用Internet Identity订阅早期使用者身份。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFoMmwsIkgDje8iaANdV4SxiaU17xAXFbf9NSWFB2cict69Ec2uumuBgDKw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 订阅链接：https://az5sd-cqaaa-aaaae-aaarq-cai.ic0.app/




#### DSCVR

DSVR基于ICP的去中心化社交内容平台，治理代币投票决定未来发展与内容审查，类似于Reddit这样的论坛dapp，目前是第一个完全完全运行在Dfinity网络上。目前登录需要用到Dfinity互联网身份。目前该项目已经完全托管在Dfinity主网上，早期使用者可以得到DSCVR代币奖励。
 
![](https://mmbiz.qpic.cn/mmbiz_png/pTd1PaaakaTCdorNOGsXRkW4hs2CcGMFKOWxLKnHr43oiaCLqxYLF0abBnpcFcEafTLpcfBAeB3PlOicYIiba3qIA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

* 官网：https://h5aet-waaaa-aaaab-qaamq-cai.raw.ic0.app/

以上是目前Dfinity官网上展示的Grant所有项目，都是已经部署在主网上的Dapp ，目前展示的项目只有Grant项目的一部分，后期还会有更多的Grant项目展示，公共子网的开放打开了Dfinity生态系统的开发大门，未来还会有越来越多的生态应用上线，Dfinity目前还是初创生态，未来的想象空间还有很大，让我们一起拭目以待。

##### 作者 DfinitySZ
##### 转载 [原文链接](https://mp.weixin.qq.com/s/AjRAZXGi41YdFVu3OKDGuQ)