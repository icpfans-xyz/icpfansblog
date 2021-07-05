---
title: "DFINITY的身份与账户体系解析"
date: 2021-07-03T06:40:24+06:00
# post thumb
images:
  - "images/post/tutorials/7-3.png"
#author
author: "youkers"
# description
description: "DFINITY的身份与账户体系解析"
# Taxonomies
categories: ["Dfinity","技术教程"]
tags: ["Dfinity","技术教程"]
type: "featured" # available type (regular or featured)
draft: false
---

<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>
<br>

DFINITY自2021年5月份主网上线以来，更多的开发者和用户开始陆续进入使用，由于dfinity使用了新的身份账户体系跟BTC、以太坊等区块链钱包账户有所区别，许多人对dfinity的身份、账户、ICP代币、canister容器等概念之间的关系不是很清楚，甚至有点混乱。希望通过这篇文章清楚地介绍他们之间关系及如何使用。

首先讲解几个使用DFINITY必须要了解的概念

- Internet Identity 互联网身份,以下简称II。登录验证DFINITY用户的身份，使用dfinity身份需要有安全硬件的验证，具体可以是硬件设备指纹解锁、面部识别或轻触 YubiKey。

- Principal ID(II) 登录 canister容器 后产生的Id，63个字节。登录不同canister容器Principal ID也会不一样， 这为用户创建了多个链上分身，防止其身份被追踪。

- Account ID  代币（ICP代币）转账交易地址，32字节钱包账户。

- Canister   DFINITY上运行应用、智能合约的容器。

- ICP 代币   DFINITY上发行的代币，类似以太坊上发行的ERC20协议代币，ICP账本及交易数据在一个Ledger canister特殊容器上面。

-  cycles  支持canister容器运行的燃料，需要使用ICP兑换，cycles是DFINITY链上原生代币，类似以太坊链上交易消耗的gas费。**只能是canister 容器持有cycles。**

- 容器角色   有Controller(超级管理员) 和 custodian（保管人），Principal 对Canister容器管理的角色权限。

**容器controller角色有以下权限：**

1. 添加和移除其他Principals 成为超级管理员

2. 授权和取消授权其他Principals作为保管人

3. 添加cycles 钱包地址簿

4. 访问获取cycles钱包余额和所有其他钱包相关信息

5. 给其容器发送cycles

6. 接收其他容器发送的cycles

7. 在调用其他容器时充当“消息调用者”主体

8. 创建容器和额外的cycles 钱包

9. 重命名cycles 钱包

**容器custodian 角色具有的权限**：

1. 访问获取cycles钱包余额和所有其他钱包相关信息

2. 给其容器发送cycles

3. 接收其他容器发送的cycles

4. 在调用其他容器时充当“消息调用者”主体

5. 创建容器



通过下面这张图有个直观的了解

![](/images/post/tutorials/7-3-1.png)



- 用户(II)通过浏览器WebAuthn 安全硬件的验证登录canister容器，登录到不同的canister会有不同的Principal Id。

- Principal 下可以创建多个Account Id, Account之间可进行ICP代币转账交易。

- Principal 如果有canister 容器角色，可以对容器cycles 钱包进行操作，如转账和接收cycles等。

- Legder 特殊容器，ICP代币发行及交易信息存储的容器

DFINITY与大多数身份验证服务不同，无需使用用户名或密码，而是使用从智能手机进行人脸识别、计算机解锁密码或安全密钥即可登录开放的网络服，使用起来更方便、更安全。

作者：[youkers](/author/youkers)

<br>

参考文献
<br>
1.[https://mp.weixin.qq.com/s/qR1e0xmb31yQeahKZexhNQ](https://mp.weixin.qq.com/s/qR1e0xmb31yQeahKZexhNQ)对DFINITY的去中心化身份、账户与钱包介绍，开发者能如何利用？
<br>
2.[https://mp.weixin.qq.com/s/QVXO20q0r7grMsB-cCUZRg](https://mp.weixin.qq.com/s/QVXO20q0r7grMsB-cCUZRg) 互联网身份：用户名和密码的终结

