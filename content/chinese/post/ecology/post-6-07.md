---
title: "验证互联网身份代码：演练"
date: 2021-06-07T10:40:24+06:00
# post thumb
images:
  - "images/post/ecology/6-71.png"
#author
author: "ICPFans"
# description
description: "验证互联网身份代码：演练"
# Taxonomies
categories: ["Dfinity","生态"]
tags: ["Dfinity","生态"]
type: "featured" # available type (regular or featured)
draft: false
---
<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>
<br>

<center>
<video id="video" height=380 width=680 controls="" preload="none" poster="http://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzNVBF2gwTS63gkf4aUppw6QIrbu4hV8gOvL4LbEu0smM30hFNWotaR7PtIb62ibWQXiadVcbxLNcickw/0?wx_fmt=jpeg">
      <source id="mp4" src="http://mpvideo.qpic.cn/0b78umabsaaa6uamiru7bjqfbi6ddgrqagia.f10002.mp4?dis_k=3e6e63e095fa3a24c4b5e5eb47cae4bb&amp;dis_t=1623134367&amp;spec_id=MzU1ODA4MjE5Ng%3D%3D1623134367&amp;vid=wxv_1870615142732775424&amp;format_id=10002" type="video/mp4">
</video>
</center>

<br>

在互联网计算机上，用户可以使用互联网身份密码认证系统登录各种 dapp，如 NNS dapp、OpenChat 等。这样做时，他们相信该服务会妥善保管他们的凭据 - 但他们可能想直接确认互联网身份真的没有跟踪他们。



互联网身份是否真的在运行它声称运行的代码？为了帮助您回答这个问题，我将引导您完成验证步骤。



当然，以下内容也适用于其他容器，但在这种情况下，我将坚持使用互联网身份。



<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>找出正在运行的内容</font></center>



互联网计算机上的智能合约，即容器智能合约，是一个 WebAssembly 模块。



互联网计算机故意不会让你只需要下载任何容器的 WASM 代码，因为也许有些开发商想保持其代码私有。但它确实公开了 Wasm 模块的哈希值，最简单的方法是使用 dfx：



![图片](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3z3lLpzKtWOX1vRR6LYvdQUicmKX3Cuf3smYBcVRPUbeqXzFdG79um8dA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


这里的“控制器”是治理容器的容器 ID，这告诉您互联网身份由网络神经系统 (NNS) 控制，并且其代码只能通过投票的提案进行更改。这很好，如果控制器只是，比如说，我，我可以更改互联网身份代码并接管您的所有身份。



“模块哈希”是部署的 .wasm 的 SHA-256 哈希，所以让我们跟随那个踪迹。



<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>找到正确的提交</font></center>



由于互联网身份的升级是通过向 NNS 提出的提案完成的，我们应该在 https://github.com/ic-association/nns-proposals 存储库中的 proposals/network_canister_management 目录中找到对此类提案的描述。



![图片](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3zjk4zoWic9nKLzQewEwspfdHHPgBX6OG67fym4cSOE7me28NE1odlosQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)
<center>Github 的近期 NNS 提案列表</center>


我们必须找到升级互联网身份的最新提案，不幸的是，该文件夹包含许多容器的建议，并且文件命名不是很有帮助。我通常从底部浏览列表并查看第二列，其中包含创建或修改文件的最新提交的标题。



在这种情况下，倒数第二个是我们关心的：



https://github.com/ic-association/nns-proposals/blob/main/proposals/network_canister_management/20210527T2203Z.md。



该文件列出了基本原理，概述了更改，最重要的是，它表示这 bd51eab 是我们要升级到的提交。



该文件还说 wasm 哈希是 d4a...c04，它与我们上面看到的相匹配。这很好，看来我们真的找到了最新的升级互联网身份的提案，而且提案实际上通过了。



警告：如果你是偏执狂，不要相信这个文件。没有什么可以阻止提案提议者创建一个指向一个修订的文件，同时实际上在提案中包含不同的代码。这就是为什么需要进行下一步验证的原因。



<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>获取源</font></center>




现在我们有了修订版，我们可以获取源代码并查看修订版 bd51eab：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3zJ3SUfOYs71Qb0QtkdpibFoViczdmtw3PYSy4QHtq8CQNGJbc7qLWIDYA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


在最后一行中，您会看到互联网身份团队使用包含提案描述文件名的标记名称标记了该修订。很整齐！



<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>重现构建</font></center>



README.md 具有以下构建指令：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3zhAJ6wa8dGjIsIKspFGv9ze4fRDP7RcLYI2icC79RTS9fuwFOQibhkOrA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


实际上，运行第一个命令就足够了，因为它还打印了哈希值（我们不需要从 Docker 容器中复制 .wasm）：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3z02yibTFvu68hLLlIrax8DZfwj307O6AKWrkPq2DcZT0XfgaBDBLZkyQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


成功！哈希匹配。



你不相信我？自己尝试一下（如果你得到不同的哈希值，请告诉我们 - 也许我被黑了）。如果您没有为 Docker 配置足够的 RAM，这可能会失败，8GB 应该够了。



此时，您拥有了从您面前的代码到运行在 https://identity.ic0.app 的互联网身份的信任路径，包括前端代码，您可以开始审核源代码。



<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>容器 ID 呢？</font></center>



如果您密切注意，您可能已经注意到我们获得了容器 rdmx6-jaaaa-aaaaa-aaadq-cai 的模块，但我们正在访问 https://identity.ic0.app 上的 Web 应用程序。那么这个联系在哪里呢？



将来，我希望互联网计算机上有某种形式的类似于 DNS 的“好主机名注册表”，用于存储从好名称到容器 ID 的映射，并且您将能够查询“哪个容器以安全的方式（例如使用认证变量）服务 rdmx6-jaaaa-aaaaa-aaadq-cai”。



但是由于我们还没有那个，但仍然希望您能够为互联网身份使用一个好听的名称（并且以后不必更改名称，这会引起头痛），我们现在对这个映射进行了硬编码。



这里的相关代码是您的浏览器在访问任何 *.ic0.app URL 时下载的 “Certifying Service Worker”。然后，这段代码将拦截对该域的所有请求，将其映射到查询调用，然后使用认证变量来验证响应。事实上，映射在代码中：



![](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzOjestA7HicXP7PnZEZFcA3zBrMiabEyk1VHZ6UckNWdPH3qXdakDOSU2IPpibkZQXQszDJnMPJDiaiaYg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


<center>
<img width = '66' height ='66' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahoVKOZ0SpP9QM3PcGeibaWejr79o6491ARaQHbCyibDyPeRUP4ibiamMefw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1"/>
</center>

<center><font color=#00D5FF>其他容器呢？</font></center>




原则上，相同的方法适用于其他容器，无论是 OpenChat、NNS 容器等。但细节会有所不同，因为每个容器开发人员可能有自己的方式：



传达其容器的来源的位置和修订版

建造容器



特别是，如果没有可重复的方式来构建容器，这将失败，这就是为什么像 https://reproducible-builds.org/ 这样的项目通常如此重要的原因。



如果您想讨论这篇文章，请考虑加入 DFINITY 论坛并在以下位置发表评论：



https://forum.dfinity.org/t/verifying-the-code-of-the-internet-identity-service-a-walk-through/4650



开始在 sdk.dfinity.org 上构建并加入我们的开发者社区 forum.dfinity.org。



![](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzOjestA7HicXP7PnZEZFcA3zQaqxK6Mt7yWQj6IelbaaoA0AAJVYEv8qDS4bLiau4PHcPG6dz7VLX0w/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


作者：DFINITY 高级研究员和工程师 Joachim Breitner

翻译：Catherine

来源：DFINITY公众号
##### [原文链接](https://mp.weixin.qq.com/s/mwpOqT5Ja50N0tDHRXdmHg)