---
title: "HashKey 崔晨：详解 DFINITY 上线后进展与竞争优劣势"
date: 2021-06-23T08:40:24+06:00
# post thumb
images:
  - "images/post/ecology/6-23.png"
#author
author: "ICPFans"
# description
description: "HashKey 崔晨：详解 DFINITY 上线后进展与竞争优劣势"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "regular" # available type (regular or featured)
draft: false
---

DFINITY 中的应用更偏向于传统互联网，而非以 DeFi 为主。

撰文：崔晨， 就职于 HashKey Capital Research
审核：邹传伟，万向区块链首席经济学家

DFINITY 团队成立于 2016 年，在 2018 年完成了 1.95 亿美元的募资，一举成为明星项目。而本计划于 2019 年上线的主网一再推迟，在这个过程中 DFINITY 的目标也转为互联网计算机，不再强调区块链的内容。最终在 2021 年 5 月 10 日，DFINITY 解锁所有代币的流通，意味着最终上线主网版本。万众瞩目的 DFINITY 表现如何？又与其他公链有何差异？本文将重点解读这两个问题。
<br>

#### 总体现状
<br>
现在 DFINITY 网络中已经上线 ICP 代币且开发流通，根据 CMC 数据显示，DFINITY 的市值排名保持在前十左右，与上线几个月的 Polkadot 位于同一水平。DFINITY 相应的浏览器也已经开放，从 DFINITY 的网络数据可以判断其现状。

DFINITY 以互联网计算机为愿景，让互联网成为公共计算的平台。互联网计算机在不宕机的容器中托管软件，用户可以不依赖于传统服务器与云计算企业。为了保证网络有足够的算力，DFINITY 对节点有专业要求，尤其需要高性能的 CPU 和 RAM，因此由专业的数据中心来运行节点。一般来说，数据中心会同时运行多个节点，这些节点也在维护不同的子网。如下图，子网可能由位于不同数据中心的不同节点来共同维护，以此避免网络中出现中心化故障。

![](https://img.chainnews.com/material/images/fbc1c54e85685cb6a10567abf5598039_nABZpGw.png-article)
<center>
图 1：数据中心与节点
</center>
<br>

目前 DFINITY 共存在 14 个子网，共由 105 个节点维护，这个节点分布在 16 个数据中心中。其中 10 个数据中心位于美国，3 个位于新加坡，还有的位于罗马尼亚、瑞士和德国，平均每个数据中心运行 7 个节点，这些节点共由 53 家运营商管理。目前来说，DFINITY 无论在节点数量还是分布都显得过于中心化。以太坊的节点同样在美国分布最多，占据了 39% 的节点数量，比特币节点分布最多的美国所占比例为 19.5%。DFINITY、比特币和以太坊网络不同，节点不需要算力挖矿来争夺记账权。网络容量通过内存表示，DFINITY 网络的总内存为 0.205PB。这些差距与 DFINITY 才起步有关，项目方预计在十年内的数据中心数量达到数千个，节点数量达到数百个。

DFINITY 上线两个星期区块高度就达到 1200 万以上，以太坊达到同一高度花费了六年时间，目前 DFINITY 的出块速度为每秒 12 个区块左右，虽然出块速度较快，但网络中传输的信息与以太坊相差百倍，这也与其仍处于起步阶段有关。

<br>

#### 技术与治理进展
<br>

##### 技术目标与实现
<br>
DFINITY 以互联网计算机作为发展目标，开发者可以将应用部署在互联网计算机中，无需使用传统的数据库和服务器。因此要保证网络的可扩展性，同时也要防止攻击、保护隐私等。为了实现作为互联网计算机的功能，DFINITY 在技术上有所优化和创新，主要体现在用户的身份验证系统、容器、子网、共识机制和 Chain Key 等。

###### 用户身份验证系统

在目前的互联网中，用户通过账户和密码进行登录，并将信息上传到服务器中。但实际上这种方式并不安全，黑客很有可能攻击公司服务器或服务器提供商获取数据。DFINITY 则采用数字签名系统替代账户和密码，也就是加密技术中的公私钥，包括密钥生成、签名和验证。其他区块链协议同样会使用数字签名系统，用户使用私钥登录钱包，再通过钱包进行转账等各种操作。如果私钥丢失或被人窃取，就意味着永久丢失地址中的财产。DFINITY 提供了一种不同于互联网账户密码登录，也不同于区块链私钥登录的互联网身份验证系统。

DFINITY 的互联网身份可以通过三种方式验证登录：设备（智能手机或笔记本电脑）中的生物识别系统，设备解锁的密码，或插入计算机 USB 的安全密钥。用户在首次注册时会在设备的芯片中生成加密密钥，并与生成的用户号绑定。如果用户的用户号丢失，或者登录的设备丢失，都会导致无法连接到 DFINITY 的互联网身份，因此官方建议在同一个用户号下添加多个设备。互联网身份还可以为用户在不同容器前端赋予不同身份，这样用户在与每个应用交互时，应用不能将用户在不同应用中的行为关联起来。

###### 容器（Canister）与子网（Subnet）

DFINITY 中的计算单位被称为容器，包含程序和状态，是智能合约的一种衍化形式。容器允许应用程序与环境分离，并能储存当前的软件状态和用户交互的记录，以及使用应用功能引起的状态更新。容器与用户或容器之间的交互行为是储存在区块链上的，因此它运行的过程是不可篡改且不可阻止的，这也是互联网计算机不需要防火墙的原因。容器也可以运行网页前端，这是与智能合约的不同，只要有燃料供给容器就能保持运行。容器运行的燃料为 Cycles，通过由网络代币 ICP 单项兑换而来。兑换比例非固定，因此可以维持 Cycles 的价格相对稳定。在容器中预存 Cycles 可以让用户在不持有代币的情况下使用互联网服务，这方面与其他公链不同。

容器由位于数据中心的节点负责运行，它们被分配在不同的子网上，以此来实现互联网计算机的扩容。每个子网都运行自己的区块链，链上的容器可以透明地调用同一子网或者其他子网上的容器。对于整个系统来说，在同一子网中调用还是跨子网调用容器是没有区别的，背后都涉及节点间的复制和计算。在这些子网中有一个比较特殊，它负责维护互联网计算机的治理系统，也就是网络神经元系统（NNS，Network Nervous System）。

![](https://img.chainnews.com/material/images/ff49005c9623546191c98b3e8804f1fc_hBf08Wq.png-article)
<center>
图 2：节点维护子网，容器分布在子网中
</center>
<br>

###### 共识机制

互联网计算机中的子网由多个节点来维护，每个节点都需要保存子网所有容器的状态，并处理新的进程。为了网络的安全和可靠，每个节点的备份要完全相同，消息的处理顺序也要保持一致，以达成一致的状态，因此需要节点对收到的消息进行共识。也就是节点通过点对点网络收集外界的信息，信息在路由传递之前通过共识层达成统一的消息并创建公证过的区块。在 DFINITY 中采用 VRF 和 BLS （随机可验证方程和门限签名）算法，实现能满足三分之一容错率的区块链协议。

![](https://img.chainnews.com/material/images/49ad75de3f145ae89e5f363c4af4ef2b_kGdIl39.png-article)
<center>
图 3：DFINITY 中信息的处理过程
</center>
<br>
在 DFINITY 中，共识通过四步达成：产生区块，公证，随机数信标，以及最终确认。在每轮共识开始时，节点将收集到的消息汇总成区块并进行广播，再由节点进行签名公证，在公证达成一致后，各公证节点的签名会压缩成多签以节约空间。随机信标的引入是防止在同一区块高度上出现多个区块，并且促使共识快速达成。每个区块都存在一个随机信标，它是由节点通过 BLS 的方式生成且不可预测。在收到区块的随机信标后，节点使用 BLS 框架对其进行签名，如果一个区块有超过 50% 的公证者签名，区块上的签名会被聚集成多签的同时产生随机数信标。

![](https://img.chainnews.com/material/images/9c8fa9e77a2b5bcf82933264e2ac5c8a_1UjgR45.png-article)
<center>
图 4：随机信标的生成
</center>
<br>
通过随机信标可以对节点进行排名，区块的公证时间被分割，排名在先的节点先进行公证，如果超时换为下一位。如果存在多个公证区块，那么排名在先的公证区块成为最终区块。公证节点在观察到高度为 h 的区块后，如果决定不再公证高度小于等于 h 的区块，则对此区块发起最终签名确认，超过三分之二的节点对同一区块进行确认后，则达成了区块的最终确认。

###### Chain Key Technology

Chain Key 是 DFINITY 实现子网扩建和进行密钥管理的技术，能够保证网络的安全可用。Chain Key 关系到互联网计算机的密钥系统，包括对信息的验证，密钥的管理和分配方式，主要应用了 BLS （门限签名）和非交互的密钥生成系统技术。在 DFINITY 中，可以使用唯一的公钥验证信息，而不是需要像其他区块链一样下载全节点账簿。而且每个子网都存在一个由 NNS 发放的固定公钥，公钥可以验证来自子网发送的签名信息。在发送信息时，不是由节点单独进行签名，而是由子网中节点共同签名，即使用门限签名的方式对信息进行签名确认，保证足够容错率的同时确保信息经过足够多的节点确认。门限签名指的是对消息进行签名时，需要多个私钥且达到一定数量的签名才可以进行汇总表示子网整体对信息的确认。

NNS 网络对密钥管理和分配需要无交互的分布式密钥生成系统，它可以对密钥进行拆分，增加密钥持有者的节点数，同时不破坏整体的密钥。在 DFINITY 中，每个子网都有一个永久的公钥用于验证子网发送的信息，而子网的私钥被拆分给各节点，节点持有这些被拆分的私钥进行门限签名来传输信息。私钥拆分与分享通过委托商执行，他要将加密后的私钥和公钥发送给各节点，同时发送一个无需交互的零知识证明，以求在不展示私钥分片的情况下可以证实节点收到的部分是正确有效的。

![](https://img.chainnews.com/material/images/33ac5640e1605f9bb3b4ced9bf476ffa_66p7fYV.png-article)
<center>
图 5：对密钥进行可验证地拆分
</center>
<br>
除此之外，为了防止发送公私钥的委托商作恶，委托商还要采用分布式的方式。只要有一个委托商是诚实的，生成的密钥足够随机，就不会影响到节点得到的密钥。在子网中添加节点时，还可以对已存在节点的私钥进行「再分享」（re-sharing）。进行再分享后，持有私钥的节点会改变，但整体子网的公钥不会变。这让 NNS 很容易地对子网中的节点进行管理，同时在外界看来子网的验证公钥不变，不影响子网对外保持通信，保持安全可信赖的环境。

![](https://img.chainnews.com/material/images/a3ee7d91b72c504a831027a3d31c61c0_G9kOWdn.png-article)
<center>
图 6：密钥的分享以及再分享
</center>
<br>

新的节点加入子网或者节点掉线时，都需要更新子网中储存容器的状态，每隔一段时间节点会签署一个「catchup package」来解决这个问题。如果子网中超过三分之一的节点损坏，NNS 可以再重新部署子网，「catchup package」还可以用于子网的恢复以及子网升级场景。
<br>

##### 治理方式与现状
<br>
DFINITY 通过网络神经元系统（NNS，Network Nervous System）治理，每个持有 ICP 的人都可以锁定成立神经元来参与 DFINITY 链上治理。参与治理可以获得系统奖励，类似于 PoS 中的 Staking 行为。投票奖励会逐渐减少，从 10% 到第八年减少到 5%。锁定在神经元 ICP 的数量比例和解锁延迟时间代表了其投票权重，用户需要为自己的选择负责。如果提案和投票的内容损害网络发展，那么锁定在神经元的 ICP 价值也会下降。要注意的是，解锁时的溶解时间的意思是从提现开始，到完全恢复流动性的时间，而非其他公链中的锁定时间。如果神经元无法判断决策的内容，它可以选择弃票，或者追随信任的神经元投票。这种追随关系是非固定且不可见，被称为流动民主，所以可以隐藏神经元真实的投票权重。


![](https://img.chainnews.com/material/images/dab99382e06f5d96a51fa10a68a17c7c_9RxJwC8.png-article)
<center>
图 7：ICP 治理奖励
</center>
<br>

NNS 最主要的工作在于协调节点与子网的关系以及密钥分配，上文中提到的非交互的密钥分享系统就是通过 NNS 实现的。NNS 通过两种容器实现：一个是治理容器，其中包括可以进行投票的提案和神经元信息，第二种包括互联网计算机中的各种配置。神经元支持的提案包括添加节点，节点奖励的发放等。
<br>

##### 生态构建及分布
<br>
DFINITY 的愿景为互联网计算机，这会比普通区块链公链囊括更多的应用。在过去的应用开发和 IT 部署中，存在开发成本高的问题，需要选择商业云服务平台，维护数据库和防火墙，使用购买专业或开源的操作系统等，而且后期维护也要花费很大成本，互联网计算机的应用则节约了这部分成本。基于此，DFINITY 没有像其他公链一样，应用完全集中在 DeFi 和 NFT 领域，而是分布在各个领域。

近期 DFINITY 基金会启动了 2.2 亿美元的开发者奖励计划，这个计划是直接发放奖励，不是以投资的方式参与项目。目前基金会鼓励的项目包括几方面，包括开发工具包，开发者工具，基础设施，应用和开放互联网服务等。

![](https://img.chainnews.com/material/images/6832809ff1605872863b15b8934bdad1.png-article)
<center>
表 1：部分 DFINITY 基金会发放的 Grant
</center>
<br>
除此之外，DFINITY 的社交媒体平台 CanCan 也受到了很多关注，它的运营方式很类似于 TikTok，用户可以获得激励积分的奖励并兑换为治理代币。CanCan 已经将代码开源，应用程序不到 1000 行代码，并且不需要 Web 服务、防火墙或外部数据库等。DFINITY 设立了 Beacon Fund 来进行项目投资。下图是目前 DFINITY 中已存在的社区项目。


![](https://img.chainnews.com/material/images/6cdac1048a2e57f8b0dd4c7765d1e2dc_Cy5U0nb.png-article)
<center>
图 8：DFINITY 的生态应用（图源：ICPSquad）
</center>
<br>
上图中可以看出，除了本身受到很多关注的 DeFi 应用外，DFINITY 中社交应用也占据了很大比重，这与 DFINITY 网络扩展性足以支持社交软件应用有关，也和官方最初支持产品是社交类应用有关。一个有趣的现象，DFINITY 中的社交软件很多都是模仿已经存在的媒体应用，在已有应用的基础上加入了经济奖励。实际上其他公链已经进行了此方面的尝试，但 DFINITY 生态中应用的前端同样可以放在容器中运行，而且身份验证系统让用户更容易地接触到互联网计算机，DFINITY 中的社交应用与公链中的社交应用会有所差异。
<br>

##### 与其他公链的异同
<br>
DFINITY 虽然在规划中不重点提及区块链的内容，但 DFINITY 的底层还是基于区块链系统，其中涉及了公私钥的密码学应用，不可篡改执行的容器，共识机制，代币的激励机制，以及治理等，这些方面的设计与其他公链有些相似。例如和智能合约很类似的容器概念，抵押参与治理并获得奖励，使用共识机制达成节点统一，使用燃料 Cycles 推动容器运行等。

在细节上，DFINITY 与其他公链又存在很多不同。相较于其他公链而言，DFINITY 的 NNS 治理系统被赋予了很大权力。虽然究其本质是还是投票数量和质押时间长的用户治理比重大，但用户质押 ICP 的溶解时间是在锁定成为神经元的一刻就已决定了，溶解时间意味着用户决定取消锁仓到用户拿到解锁 ICP 的时间。相较于其他公链来说，DFINITY 治理锁定代币的时间会更长，与神经元在系统中具有最高权力有关。

虽然 DFINITY 是开放的网络，但节点的加入和分配都需要经过 NNS 系统提案才可以完成，这方面与其他公链有所不同。运行节点需要专业的数据中心，个人用家庭电脑不能满足 DFINITY 的运行需求。节点加入、子网分配和扩容也是通过 NNS。DFINITY 系统中有创新的 Chain Key 技术，可以保证在不影响子网通信的情况下，增减子网的节点并扩充子网，这点其他公链很难做到。

在 Token 的设计上，DFINITY 的双币模型区别于其他公链，支持容器运行的燃料 Cycles 需要使用 ICP 兑换购买，兑换比例的不固定可以让 Cycles 维持一个稳定的价格，避免由于 ICP 的价格涨跌而影响到 Cycles，这样让容器运营者的花费维持稳定。

对于 DFINITY 的用户，登录认证系统不同于其他公链。登录时无需使用钱包，通过硬件设施、电脑或智能手机就可以完成用户 ID 的注册和使用，极大缩减了用户的学习和使用成本。容器的燃料 Cycles 不需要使用者进行储存，实际上用户在使用容器时是无感的，而大多数公链需要使用者支付运行智能合约的费用。

生态应用上，DFINITY 也表现出了与其他公链的不同。在目前的环境下，很多公链聚焦在 DeFi 或 NFT 应用，模仿以太坊上的热门应用来进行竞争。可以看出，DFINITY 中的应用以「复刻」互联网应用，并加之经济激励为主。但碍于可扩展性和用户门槛，这条路在以太坊及其他公链上没有走通。
<br>

##### 思考与总结
<br>
DFINITY 的愿景在于让人们将应用直接部署在互联网中来保证安全，这需要使用区块链作为底层来实现不可篡改和防作恶。区块链的扩展性往往限制了其使用，因此在 DFINITY 中的优化与创新就在解决这些问题。DFINITY 需要数据中心承担运行节点的需求，保证网络的可靠。NNS 负责子网与节点的管理，能够在系统必要时添加子网，在子网中实现对节点数量增减的管理，因此来保证网络活性。共识中的门限签名和可验证随机函数可以让节点迅速达成共识。技术以及权力更大的治理机制让 DFINITY 有别于其他公链。DFINITY 中的身份验证系统也降低了学习门槛，让用户在使用时更贴近于互联网的体验。

在这些技术的支撑下，DFINITY 中的应用更偏向于传统互联网，而非以 DeFi 为主。目前 DFINITY 上的应用大多为模仿互联网应用，让本来的互联网应用加上通证以及治理系统。例如 DSCVR，界面也与 Reddit 很相似。但 DFINITY 的目标不局限于区块链公链。对于企业来说，部署在互联网计算机上可以节约成本；对于用户来说，使用互联网计算机接近于互联网的体验。完全模仿互联网应用的区块链应用能否成为爆款，是值得关注的地方。作为互联网计算机，发展分布式商业将成为 DFINITY 的机会。

DFINITY 未来的计划还包括集成以太坊，通过在 DFINITY 中创建特殊的智能合约实现容器与智能合约的互操作性。现在处于理论概念阶段，如果能够实现互通，这两者都将发生巨大改变，DFINITY 会作为以太坊的类二层网络运行，以太坊也可以直接使用 DFINITY 的身份验证系统。

*免责声明：作为Dfinity信息平台，本站所发布文章仅代表作者个人观点，与ICPFans立场无关。文章内的信息、意见等均仅供参考，并非作为或被视为实际投资建议。*

##### 转载 [原文链接](https://www.chainnews.com/articles/439546364345.htm)