---
title: "OpenChat：一个真正去中心化的 WhatsApp 替代品"
date: 2021-06-07T10:40:24+06:00
# post thumb
images:
  - "images/post/ecology/6-81.png"
#author
author: "ICPFans"
# description
description: "OpenChat：一个真正去中心化的 WhatsApp 替代品"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "featured" # available type (regular or featured)
draft: false
---
<center>
<img width = '70' height ='41' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<br>

<center>
<video id="video" height=380 width=680 controls="" preload="none" poster="http://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzNVBF2gwTS63gkf4aUppw6QreWIKRib87vNM3wJgOpia4OxN84e5ianFabia5pVuhYg0n4M06H7cltccw/0?wx_fmt=jpeg">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bf2zqag6aaatyalsre7pzqfbtgdn7gaa3ya.f10002.mp4?dis_k=a1c256965c57c137b3b7058e811e3653&amp;dis_t=1623227087&amp;spec_id=MzU1ODA4MjE5Ng%3D%3D1623227087&amp;vid=wxv_1870585010869616641&amp;format_id=10002&amp;support_redirect=1&amp;mmversion=false" type="video/mp4">
</video>
</center>

<br>


今年早些时候，WhatsApp 宣布了更新的隐私政策，要求用户接受他们的帐户详细信息、电话号码、元数据、财务交易、日志报告、位置、设备标识符和 IP 地址将与 Facebook 共享。



用户被告知接受新政策，否则将面临无法访问其帐户的风险。在随之而来的争议中，最后通牒发生了变化：如果用户不遵守，消息应用程序现在将逐渐降低服务水平，直到完全停止运行。



这就是我们构建 OpenChat 的原因，这是一个去中心化的消息服务，其功能与现有的消息应用程序（如 WhatsApp 和 Signal）非常相似，主要区别在于 OpenChat 在区块链互联网计算机上端到端运行。



您可以在此处试用开发中的 alpha 版本：https://oc.app



您的聊天消息由高级智能合约在链上处理和维护，在互联网计算机语言中有时称为“容器”，因为它们是一组 WebAssembly 字节码和持久内存页面，并使用软件参与者模型并行运行，这允许 dapps 扩展。



OpenChat 的架构将允许它扩展到数百万用户，同时仍可供普通用户免费使用。以前从未有可能在公共区块链上构建这样一个可扩展的系统，而且价格便宜到可以免费提供给用户。



此外，在撰写本文时在以太坊上存储 1 GB 数据的成本为 6086 万美元（在最近达到 8.69 亿美元的峰值之后），由于它的可扩展架构和“链密钥”密码学释放出的高效率，互联网计算机上的成本将保持稳定在每年每 GB 5 美元左右。



一旦在互联网计算机上启用代币化，OpenChat 将成为一个开放的互联网服务，这意味着 dapp 将完全去中心化并完全由社区管理 - 没有公司会跟踪和出售您的数据。



OpenChat 将由其治理代币的持有者拥有和管理，这些代币将广泛分发给世界各地的用户，以实现去中心化决策并激励平台参与。



作为一项开放的互联网服务，所有的改变都必须通过公共治理提案。任何想要参与平台治理的 OpenChat 代币持有者都可以对这些提案进行投票，只有获得足够支持的提案才会被采纳和实施。



OpenChat 限量发行，供公众自己试用。我们正处于测试阶段，目前有 10,000 名用户的限制。



该代码也将很快公开并向任何想要贡献的人开放。开放互联网服务的出现将有可能用 OpenChat 代币来奖励新功能和错误修复的贡献者，从而创建一个蓬勃发展的开放产品。



与此同时，终端用户将能够享受安全、直观和开放的聊天应用程序！


<br>
<center>
<img width = '70' height ='41' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<center><font color=#FF4C00>OpenChat 技术概述</font></center>
<br>


OpenChat 在互联网计算机区块链上安装的容器智能合约上运行。各种容器智能合约将运行中央服务，例如用户注册表和 WebRTC 连接处理。



所有消息都由智能合约处理和存储，但互联网计算机仍然需要 2 秒钟才能完成状态更改交易。因此，我们尝试使用 WebRTC 预先运行智能合约，这可以使它们更快地可用，并在聊天中保持“即时”（请注意，对于区块链来说，2 秒确实非常快）。智能合约代理并在托管聊天的 Web 浏览器之间建立点对点 WebRTC 连接。



请注意，互联网计算机上的智能合约可以安全地将交互式 Web 内容提供给最终用户的浏览器，然后该内容可以安全地与智能合约交互。因此，OpenChat 使用区块链端到端来提供其功能，并且不依赖于云服务或任何其他中心化和不安全的遗留技术。



为了使用简单的架构进行扩展，为每个用户创建了一个新的容器智能合约实例，其中存储了他们的聊天历史记录和配置信息的副本。互联网计算机的固有安全性意味着用户只能访问他们自己的容器数据（或者，在群聊的情况下，群参与者）。



很快，一旦代码开源，就可以识别和验证在每个容器上运行的软件的精确版本，链接回源控制中的特定修订版。此外，作为一项开放的互联网服务，OpenChat 将拥有一个与NNS类似的治理系统，因此只有通过 OpenChat 代币持有者的全球社区投票和接受的提案才能进行更改。



考虑到互联网计算机的安全性、在任何时候运行的软件的可见性以及 OpenChat 社区本身将负责批准每个更改的事实，一旦 SEV-ES 在互联网计算机节点上启用后，用户可以非常确信，除了他们的消息接收者之外，他们的数据现在或将来不会被除他们自己之外的任何人访问。



为了增加安全性，OpenChat 将适时在已经安全的互联网计算机网络上提供端到端加密。启用此选项后，聊天数据将只能由聊天参与者在他们自己的设备上访问，否则将在关联容器的内存中加密。这类似于 WhatsApp 保护用户数据的方式，但这意味着搜索聊天记录的唯一方法是在设备上。



如前所述，聊天记录将存储在为其所有者创建的相关智能合约中。目前，单个容器智能合约最多只能使用 4 GB 的持久内存（尽管我们相信这会在未来增加），这将限制一些用户希望维护的聊天记录和媒体数量（群聊同上）。



为了解决这个问题，我们将为用户提供在我们将在区块链上创建的 BigMap 智能合约数据库版本中维护图像和视频的能力，该数据库可以存储无限量的数据。



这可能会使用内容寻址，这样广泛共享的媒体将只存储一次，这样更高效且更具成本效益，尽管可以说是以引入一些隐私问题为代价 - 但是我们将致力于解决这些问题。



<br>
<center>
<img width = '70' height ='41' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<center><font color=#FF4C00>特征</font></center>
<br>



以下是 OpenChat 当前提供的一些标准功能，这些功能是用户对典型消息传递应用程序的期望：



+ 向其他用户发送消息的能力，用勾号指示 OpenChat 服务何时收到消息并由收件人阅读



+ 发送媒体消息（例如，照片、视频等）的能力



+ 在线用户的即时消息传递



+ 查看您的联系人当前是否正在键入消息的能力



+ 群聊功能



+ 很快，通知集成，这样即使您没有在浏览器中打开 OpenChat，您也可以查看是否有消息在等待……



以下是一些典型的消息传递应用程序中没有的 OpenChat 功能：



+ 与互联网身份区块链身份验证技术集成，使用户无需用户名或密码即可以安全无摩擦的方式匿名使用其任何设备登录（本质上，WebAuthn 协议允许 Web 浏览器与 TPM 芯片集成，例如通过 MacBook 上的指纹传感器、手机上的面容 ID 系统或 HSM 设备，例如 YubiKey）。



+ 一旦在托管互联网计算机区块链网络的节点机器上启用 SEV，就能够在不影响安全性的情况下搜索整个聊天历史记录。



+ 将 cycles 发送给其他开发人员的能力，用于驱动互联网计算机上的计算 - 以及其他尚未公布的高级标记化功能。



<br>
<center>
<img width = '70' height ='41' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<center><font color=#FF4C00>下一步</font></center>
<br>




在不久的将来，随着 OpenChat 向开放的互联网服务转型，早期采用者和贡献者将获得 OpenChat 代币奖励，可用于参与服务的治理（我们将采用服务神经系统模型，即源自互联网计算机的网络神经系统）。



我们认为，用户应该参与他们通过治理而变得有价值的服务，最终也应该成为团队的一员，并通过参与充当论坛的公共聊天组的审核等任务来获得奖励。



在 Twitter 上关注 @OpenChat 以了解 OpenChat 的最新发展，并在 OpenChat 代码公开时收到通知！



我们欢迎您的贡献，并期待看到您将如何帮助 OpenChat 和更广泛的互联网计算机生态系统成长和发展。



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeoXldqchJNicQPXP89AhRdB7mYkRqLvtRF8CfpjialibsVCxf97caIAsSg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

<center>背景知识</center>

<br>

<center> <strong>OpenChat：未来的去中心化社交应用 | DFINITY 上线发布会</strong></center>

<br>

北京时间 5 月 8 日凌晨 1 时，万众瞩目的“天王级”项目 DFINITY 正式上线 Mercury Beta 主网，这意味着 DFINITY 初步实现了互联网计算机的去中心化，使网络神经系统（NNS）这一算法治理系统能够搭载数千个独立数据中心和数百万台特殊节点机器。



伴随着 DFINITY 的成熟，一个基于区块链的互联网计算机诞生了。DFINITY 不仅仅是一个公链项目，而是基于区块链构建了更为完善的互联网服务，这是一次不亚于以太坊和比特币的巨大创新。



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSe5NjohDFeDpHmibVAk16lH7hMI4uaolNlAkxhHYXSPINkickeGwxbly2g/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


为了迎接业界这一历史性的时刻，DFINITY 联合 36 氪及 Odaily 星球日报于 5 月 8 日 20:00 举办了「 DFINITY 互联网计算机主网上线发布会」，我们与去中心化的建设者一起探讨了技术与应用、机遇与挑战、商业与生态。



在发布会上，软件工程师 Yan Chen 通过演讲为我们分享了一款基于 DFINITY 互联网计算机构建的去中心化社交应用 OpenChat。



以下为 Yan Chen 的具体演讲内容，由 Odaily 星球日报整理。



大家好，我叫 Yan Chen，是 DFINITY 的一名工程师。今天，我给大家演示的是一个基于互联网计算机构建的聊天 APP - OpenChat。



通常用户使用任何一款 APP 的首个步骤就是注册账号，其实这是一个很复杂的过程，你需要找到一个没有被使用的用户名，一个安全同时可被记住的密码。



在互联网计算机中，我们通过区块链和密码学的技术，开发了一个通用的身份认证系统。通过这个系统，你可以使用任何的加密设备，比如笔记本电脑当中的指纹识别，或者手机上的人脸识别以及 USB 密钥来进行身份认证，从而避免了用户在每个 APP 上建立账号的麻烦。



下面我将给大家演示一下 OpenChat 的登录界面是如何进行身份认证的。我们点击登录（Sign In）就会自动跳转到身份认证服务，点击注册新用户，然后输入设备名字，比如说 MacBook ，再选择使用 MacBook 上的指纹来进行注册。



现在我点击一下 Mac 上的指纹识别，再点击确认，这样我的指纹信息就被发送到了互联网计算机的后端当中，你可以看到我们已经注册成功了。



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSecIC5licbuMs6mgFO5Vf8hyvwZaXSC8I4Fk8TgNczSqicbkJgeSWhGuSg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


注册成功后我们会得到一个用户编码，这个编码就相当于你登录时的用户名，你需要把它记下来，但是这里面没有任何密码信息，因为所有的密码都是隐藏在支持指纹或者人脸识别的加密硬件当中。 



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeYPMqyoo0Pz4ahly52XQ737YCWWNO621Tc3VAkQtgpsqNgKAFotmG9Q/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


然后我们试着登录，灰框之内就是 OpenChat 的地址，点击继续（Proceed）。接着我们就进入了 OpenChat，我们需要先设置一个用户名，比如说小强，再然后我们可以选择某一个其他用户发起聊天，比如说小明。



我们可以给他发文字消息，也可以发送图片或者是别的附件比如说 PDF 的文件。 



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeQU0au2XywgXaDV9sPCcawDyLO6lF4Wd1ia4xsbnichENiamg0TH0j3frw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

我们再打开一个新的窗口，用小明的账号登录。现在我们可以看到刚才小强发给小明的消息在小明的账户上也显示了出来，我们可以回一个消息，从小强的窗口来看消息传递没有任何延时。 



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeFMrtkDfDVptceiccrvFUuvVh1OZ8zqFuofJK47icBqTXxIGfbiaw2yZuw/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


我们可以看到，当小明在输入消息的时候，小强的屏幕会显示 Typing（对方正在输入），同样，在小强输入消息的时候，小明的窗口也会实时反映出这个状态。通过 P2P 的传输，信息能够更快地传达至对方的屏幕上。 



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeFAzVNJicMzn2SJfNzVErMgwlOsBP6LTwyg970QEiaD9SD0xWJnicFWicmQ/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


对于多人聊天场景，我们可以添加一个聊天群，然后把小明和小红都加进来。这时候我们可以看到在小明的屏幕上会出现一个聊天群的消息。我们登陆小红的账号，可以看到该账号也接收到了这个消息。



OpenChat 还支持聊天记录搜索功能，比如说我在这里输入一个想要搜索的消息，点击之后就可以跳转至相应的聊天段落。与传统社交 App 的聊天搜索功能不同的是，传统的聊天 App 出于安全性考虑使用的是 N2N 的方法，所以你只能搜索存在你手机（或其他设备）上的聊天记录。



OpenChat 则是把所有信息都存在了互联网计算机上，这将支持搜索所有的聊天历史记录，不论你是在哪一个设备上存储了东西，都可以在同一台设备上被搜索到。



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSeOY60fUubSnqOgnxccpsRHaJnCicmh6R4a3qSKQr6lExSVZJRFibksicYA/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


OpenChat 还支持在聊天中发送货币，比如在这里我们可以发送 cycles，cycles 是在互联网计算机当中驱动 APP 运行的一个货币单位。



初始的时候每个人都有 10 T 的 cycles，在这里我们让小强跟给小明发送 2.5 T 的 cycles，然后打开小明的窗口，可以看到小明的 cycles 余额变成了 12.5 T，小明这边则降到了 7.5 T。



更多细节及视频，请查看：OpenChat 线上演示



![图片](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOmaP8cd0tnUyUQa5DYnicSe4RtSyhI6Exatw8cmaXzC2mgyibzTkpgllDghWFnsZD3uhUcsZ6qibsBg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


作者：Matt Grogan and Hamish Peebles

翻译：Catherine
来源：DFINITY公众号
##### [原文链接](https://mp.weixin.qq.com/s/FP4wGJyxK7YzjWdhef27cA)