---
title: "介绍 Quill，一个用于互联网计算机的分类帐和治理工具包"
date: 2021-06-22T08:40:24+06:00
# post thumb
images:
  - "images/post/ecology/6-22.png"
#author
author: "ICPFans"
# description
description: "介绍 Quill，一个用于互联网计算机的分类帐和治理工具包"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "featured" # available type (regular or featured)
draft: false
---

<center>
<img width = '118' height ='50' src ="https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzO5kmTW67t1ty1icJD4eF8R53YZQlPrDSiaEZicTXyjqYxaGpLRbrZ76reKSpiaial6m10vLNBfYYibJhww/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<br>

<center>
<video id="video" height=380 width=680 controls="" preload="none" poster="http://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzMUWJVloTiaNEtIpQQBTyEYK53mHCDgaRovnJyOKdWzfP1vBReUT1pEPkAdh4xAsyibtm1ibibuAcQdyg/0?wx_fmt=jpeg">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bf2jiac6aaafqais2omnbqfaswdf5faalya.f10002.mp4?dis_k=f7f979903641f26422884751bb090b33&amp;dis_t=1624352358&amp;spec_id=MzU1ODA4MjE5Ng%3D%3D1624352367&amp;vid=wxv_1919857209270714372&amp;format_id=10002&amp;support_redirect=1&amp;mmversion=false" type="video/mp4">
</video>
</center>

<br>

<center>
<img width = '22' height ='10' src ="https://mmbiz.qpic.cn/mmbiz_gif/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahDludaEbzkicWs0CSQPHQhynrIHnzsibkZDkiawQBFE7UHmicib1rNEkQDcw/640?wx_fmt=gif&tp=webp&wxfrom=5&wx_lazy=1"/>
</center>
<br>

为了支持自托管选项来管理互联网计算机的 ICP 实用程序代币，DFINITY 基金会研发团队宣布开源版本 Quill。



Quill 被定位为分类帐和治理工具包，可最大限度地提高管理钱包的安全性和便利性，提供一种简单的方法来在离线计算机上为互联网计算机的分类帐和治理容器创建签名消息。



这些消息必须传输到在线机器并发送到互联网计算机才能生效。



<center>
<img width = '118' height ='50' src ="https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzO5kmTW67t1ty1icJD4eF8R53YZQlPrDSiaEZicTXyjqYxaGpLRbrZ76reKSpiaial6m10vLNBfYYibJhww/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
<br>
<font color=red size=4>动机</font>
</center>
<br>


在持有代币时，用户通常会遇到过多的应用程序，大致可以分为以下几类：



* 中心化钱包服务

* 热钱包（连接到互联网的设备上的应用程序）

* 冷钱包（离线或“不触网”设备上的应用程序）



与所有事情一样，选择上述选项之一归结为便利性和安全性之间的权衡。



在中心化服务上持有代币非常方便且用户友好，但您为此付出的代价是您失去了对属于您资产所在地址的私钥的控制。



使用所谓的热钱包可以让您完全控制您的私钥，流行的热钱包是智能手机应用程序、桌面应用程序或浏览器扩展程序。您可以通过将您的密钥加载到应用程序中来操作它们，然后应用程序就可以代表您控制您的资产。



但是，您的私钥暴露给连接到互联网的应用程序这一事实跨越了一个严重的攻击面，不幸的是，该攻击面在过去已被多次利用。



例如，用户可能会被诱骗下载冒名顶替的热钱包应用程序，或者合法应用程序可能会因注入恶意依赖项而受到损害，从而劫持密钥并从您的帐户中窃取所有资金。



冷钱包选项涉及使用完全与互联网断开连接的设备，这怎么可能？这就是“加密货币”的“加密”前缀发挥作用的地方。区块链在加密协议上运行，该协议由可加密验证的消息驱动。



也就是说，如果您可以在离线计算机上制作这样的消息，那么您可以简单地将其传输到您的在线计算机上并广播到区块链，无论它是如何以及在何处制作的，区块链都会接受它。



在这种情况下，如果您的私钥仅暴露给离线计算机，并且这台计算机永远处于离线状态，那么您的密钥可能受到威胁的攻击面就会小得多。



重要的是要注意，还有其他方法可以利用此设置，例如已被攻陷的软件安装在脱机计算机上。



例如，离线计算机上的恶意程序可能会在交易被签名之前更改交易内容，因此维护离线计算机的安全性至关重要。



可以说，所有这三种不同的方法都提供了更高级别的安全性以及更低的便利性级别。



为了解决这种缺乏便利性的问题，DFINITY 基金会一直在积极开发 Quill，以最大限度地提高用户的易用性，同时确保您的冷钱包的安全性达到最高水平。



<center>
<img width = '118' height ='50' src ="https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzO5kmTW67t1ty1icJD4eF8R53YZQlPrDSiaEZicTXyjqYxaGpLRbrZ76reKSpiaial6m10vLNBfYYibJhww/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
<br>
<font color=red size=4>Quill</font>
</center>
<br>



Quill 为自我监管提供了分类账和治理工具包。如前所述，它为使用自我监管的代币持有者提供了一种简单的方法，可以在离线计算机上为互联网计算机的分类帐和治理容器创建签名消息。



这些消息必须传输到在线机器并发送到互联网计算机才能执行。



Quill 有很好的文档记录，您可以通过调用以下 help 命令开始探索其 API：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VWuHCAFTq6RkjPB48I26ricfLq5n8WkgxkSqmzJJ49xeaJydOf3icKibYw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


要获得每个 Quill 命令的帮助，只需附加命令名称：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3Via5UdTj7t7GT3B6r7ia4LDj3wr9AXgOr5LBHCf0aAYYs4drjkPPshic0g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


几乎所有操作所需的主要参数是您的密钥的路径，Quill 目前仅支持 PEM 格式的密钥。根据维基百科：



* 隐私增强邮件（PEM）是一种基于 1993 年定义“隐私增强邮件”的 IETF 标准集，用于存储和发送加密密钥、证书和其他数据的事实上的文件格式。



大多数成熟的工具都支持 PEM 格式的私钥序列化，您还可以使用 DFINITY 的 keysmith 工具从您的 BIP39 种子短语生成 PEM 文件，您也可以使用 keysmith 或使用您选择的任何其他工具生成该文件。



当您生成 PEM 文件时，您可以使用它来显示相应的委托人 ID 和帐号，您可以使用它们来接收 ICP 令牌转移：


![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VUWALmlgwMl3eKvRyK8CLzJJ57rCdF0MghzjgrVOibdIpJicIicTkxFlkw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


要签署转移到某人的帐户，只需运行：


![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VGiasCI2JUCiclof80Xrse3kpnmYyianPkOdibmLYt4rib64j2lQOzeEpMzw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


这将生成一条包含两条签名消息的消息，分别是实际的转账交易和请求状态查询：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3V8VHwAVCystbSt19y3bk3BvUKXd6yKKVCyCTicGTl2fRcQTHcBVIia8IQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


为了获得最大的安全性，重要的是要注意，您必须在将签名交易传输到在线计算机之前验证其内容，以排除对原始输入的任何有害危害（例如交换目标地址）。



理想情况下，您应该使用由与签名工具不同的受信任方开发的工具。但是如果你自己编译 Quill 并事先检查源代码，你可以使用 Quill 来显示已验证交易的内容。



为此，您可以在离线计算机上使用 send 带有 --dry-run 选项的命令（这很好，因为我们不会在试运行模式下将其发送到任何地方）：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3V8AdY7KUIicYjFYiar0KG2EnvhJPt6QnlujABxhicicKiaUpmwYicjXAb99Yg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


确认交易无误后，您现在可以将此消息传输到在线计算机，将其保存为文件，并在在线计算机上使用 Quill 将其广播到互联网计算机：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VPf5PpbfX5V7uHhmpSdrh1EpQ6xnbqM0BfQwUggic8n3tO2jtibjCgBew/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


上面发生的事情是，Quill 首先要求明确确认，然后将交易提交给互联网计算机，然后轮询交易状态。



请注意，在上面的示例中，我们使用了一个不包含 ICP 令牌的测试帐户，因此互联网计算机返回了相应的错误。



同样的方法适用于所有治理命令，例如，要将您的 ICP 代币抵押到新的或现有的神经元，请使用以下命令：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VZ8Et3qOprPMBzECMz1FlYWd9AJ6DbLB3jCVd3NI6Ebr1BK04QRrkwg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


我们在抵押或充值时使用 8 个字符长的 ASCII 名称来识别神经元的原因是现有治理 API 的结果，超出了本文的范围。



在任何情况下，成功执行上述命令都会返回神经元 id，该 id 需要用于后续的神经元配置。此外，目前建议您为神经元命名并写下来。



可以轻松恢复神经元的名称 - 这只是用作交易的备忘录，将质押的 ICP 代币转移到治理子账户 - 但这是未来的工作，将在稍后解决。



对于神经元配置，您可以使用以下 neuron-stake 命令：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3V859YdEEngiaI7yibpN12dl09PsfMwntlefXLYUickh7WaQ8P6MazKa2nA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


因此，推荐的工作流程是：



* 1.使用 neuron-stake 命令将您的 ICP 代币抵押给神经元。



* 2.使用 neuron-manage 命令和 --additional-dissolve-delay-seconds 选项指定溶解延迟。



* 3.使用 neuron-manage 命令和 --start-dissolving 选项开始溶解神经元（如果需要）。



* 4.使用 neuron-manage 命令和 --add-hot-key 选项将您的互联网身份的主体 ID 添加为热键。



此工作流程将允许您从冷钱包创建神经元，同时使您能够使用 NNS dapp 查看有关您的神经元的所有详细信息，例如质押数量、成熟度、投票历史，甚至进行一些基本控制，例如配置追随者。



请注意，在第四步中，您应该使用与您的互联网身份相对应的主体 ID，该 ID 显示在 NNS dapp 的 UI 中的“神经元”选项卡上。



对于希望采用技术含量较低的方式进行托管和神经元抵押的用户，第三方代币托管服务也将很快支持互联网计算机神经元操作。



有关 Staking 的更多详细信息，请访问：[通过在网络神经系统里面质押获得可观的投票奖励](http://mp.weixin.qq.com/s?__biz=MzU1ODA4MjE5Ng==&mid=2247487136&idx=1&sn=1b42faa181dd75c6fb364bdf0b069bc0&chksm=fc2abf5bcb5d364d179d1a8f181d7298f25ba69ee929785f44d10892f05877ca5fe1f248ca7e&scene=21#wechat_redirect)。



开始在 sdk.dfinity.org 上构建并加入我们的开发者社区 forum.dfinity.org。



![](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOLHMd9IhhOe0ibmyaCuEv3VYxvWNlwAaHIc1HFQmK1PysvINrtDo01HKpUj1nOTK3lfmITJHF8y2w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


作者：DFINITY 高级软件工程师 Christian Müller

翻译：Catherine

##### 转载 [原文链接](https://mp.weixin.qq.com/s/FDfzJlkFwCCn0H2m7rNx4Q)