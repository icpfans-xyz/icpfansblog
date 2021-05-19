---
title: "在互联网计算机上达成共识"
date: 2021-05-18T9:40:24+06:00
# post thumb
images:
  - "images/post/dynamic/5-18.png"
#author
author: "ICPFans"
# description
description: "在互联网计算机上达成共识"
# Taxonomies
categories: ["Dfinity","进展"]
tags: ["Dfinity","进展"]
type: "featured" # available type (regular or featured)
draft: false
---

<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>
<br>

<center>
<video id="video" height=380 width=680 controls="" preload="none" poster="http://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzPbK8zEeG5tg4LRBGc3PDBRX2pRE1pP94GdAibTMEWJOnb9czejibe94dvmBguhVz0qBpBOKRicdEiciaA/0?wx_fmt=jpeg">
      <source id="mp4" src="http://mpvideo.qpic.cn/0bf2omaamaaalmakrpl6nrpva46dazzqabqa.f10003.mp4?dis_k=098a4828140d2379f86a8203f72b0d52&amp;dis_t=1621327588&amp;spec_id=MzU1ODA4MjE5Ng%3D%3D1621327588&amp;vid=wxv_1552653654439084035&amp;format_id=10003" type="video/mp4">
</video>
</center>

<br>

安全性和可靠性对于互联网计算机的愿景至关重要。互联网计算机是一个扩展公共互联网功能的区块链计算平台，因此它可以托管软件，从而使下一代dapp和开放式互联网服务成为可能。



互联网计算机由世界各地数据中心中通过互联网计算机协议（ICP）进行通信的计算机提供动力。通过这种方式的协作，这些机器形成了一个虚拟的互联网计算机，该虚拟互联网计算机允许开发人员以安全可靠的方式编写和部署称为容器的软件。



“安全”是指容器的状态只会根据容器的规则进行更改，并且不能被篡改，“可靠”是指容器不会突然停止运行。



互联网计算机使用一种新颖的共识协议来实现这些特性：不同的机器或副本必须就要处理的输入和以什么顺序达成共识，以使它们保持一致的状态。每一款软件都是由世界各地的许多机器执行的，而不仅仅是一个机器；大多数机器共同定义了软件的真实状态。



如果某些单个副本报告状态被篡改，存在连接问题甚至是恶意的，只要大多数副本正确执行软件，这都不会有所作为。



另外，我们希望互联网计算机能够扩展，这意味着我们可以在平台上以容器的形式运行越来越多的分散式应用程序。为了实现此可扩展性要求，我们将容器分成较小的组，每个组在我们称为子网的网络上运行。



子网由世界各地许多不同的副本提供动力，并且它们都执行在该子网上运行的容器。不同子网中的容器也可以安全地通信。我们总是可以向互联网计算机添加子网，从而增加其容量。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83RBnYzfvwOkLIuInVh2EWbEfTbPPYBQaxPicu85F08viaWeLyalNice7Tg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>

<center><font color=#FFA900>为什么共识很重要<font></center>



只要大多数计算机都能正常运行，任何数量的副本就可能不可用或具有恶意，而不会影响子网的正确状态。这种使用复制获得安全性的方法需要共识协议。子网必须处理不同的消息，即从用户到容器以及从容器到容器的消息。



而且，它们都必须以相同的顺序处理相同的消息，以便所有副本始终以相同的状态结束-但是为子网提供动力的每个副本实际上可能会以不同的顺序看到消息。我们使用共识协议，以便为子网提供动力的所有节点都可以同意要处理的消息的顺序。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83cicUW9A2j43x7HC5MOy2gEJgmjJbD6unor0K5urE7yLZzg2U7wbOIpQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


我们将通过使用区块链达成共识。子网应处理的消息被分组在一起，并放置在区块中，其中每个区块都指向前一个区块，从而形成了一个区块链。当所有副本都在区块链上达成共识时，就可以实现安全性，从而对要执行的消息进行排序。



更确切地说，我们想要我们所谓的“安全性”-也就是说，如果两个诚实的副本认为他们在某个点上都同意区块链，那么实际上他们在那个点上必须拥有相同的区块链观点。



其次，我们要“活跃”，这意味着区块链在不断增长，我们在越来越多的区块上达成共识，并不断处理其他消息。



第三，我们想要所谓的“有效性”，这意味着所有区块和区块中的消息实际上都是有效的。例如，这可确保发送方正确签名了区块中的所有消息。



这里的困难在于，即使为子网提供动力的某些节点可能出现故障、脱机甚至是恶意活动，我们也要保持这三个属性。更准确地说，只要子网中少于三分之一的节点处于脱机或恶意状态，我们就希望所有这些属性都能够保留。



在下面的示例中，我们将经常使用四个节点，这意味着如果其中最多一个是恶意的，我们应该满足这些属性。在创世时，互联网计算机将使用更大的子网，这些子网可以容忍多个损坏的副本。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83hoYpO3RBZzm9WoNBNrP3td0ceZhMiceYNJaN0DVALOHGHTTKIBPLVGw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


我们将放大到单个子网，并了解如何使用区块链达成共识，但是请务必记住，互联网计算机由许多子网组成，因此由许多区块链组成。我们将通过在对等八卦网络之上构建一个共识协议。



我们经常会说副本将“发送此消息”。就是说，我们的意思是我们使用八卦网络与子网上的其他副本交换消息。我们还将只关注消息的顺序，我们协议的其他部分将处理这些消息。



重要的是要注意，我们选择根据互联网计算机的需求来设计共识协议。我们正在尝试针对吞吐量、延迟和协议简单性进行优化。我们的协议包含四个主要部分：



+ 首先，我们有区块制作。这部分创建候选区块，我们可以在其中构建区块链。



+ 第二，我们有公证。这部分负责识别有效的区块，我们可以在其中构建有效的区块链。



+ 第三，我们有随机信标。随机信标将为我们提供一些随机性，可用于进一步增强协议。



+ 最后，我们有最终性。它将告诉我们我们何时真正达成协议。



<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>

<center><font color=#FFA900>区块链制作<font></center>



子网上的副本可以充当区块制造者，提出一个扩展链的区块。它将具有一些可用消息，这些消息应由在此子网上运行的容器处理。



它可能有一个达到一定高度（例如29）的区块链。它收集等待处理的消息，将它们分组为一个区块，并通过在此八卦网络上将其发送到其他副本来建议对区块链进行扩展。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83ibUQM1gqlxEamkkYzRJZLic6M3DAmJ30MP8Aic2zPQFNwiajPzOfdzaWZw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



重要的是要记住，即使某些参与者实际上行为不当，我们也希望该协议能够正常工作。



这意味着我们不能选择一个单一的区块制造者来扩展区块链，因为这个区块制造者实际上可能是恶意的，而且我们可能会被困住，这将损害我们的活力。因此，我们必须有许多副本充当块制造者。



<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>

<center><font color=#FFA900>公正<font></center>




出于相同的原因，这些整体提议实际上可能是无效的。为了解决这个问题，我们有一个经过公证的流程，该流程可以轮流工作，并且每轮都确保我们至少有一个可以扩展区块链的有效区块。



例如，假设副本1具有经过公证的区块链，高度一直到29。如果现在看到一个区块将区块链扩展到高度30，它将验证该区块。



如果副本1看到此区块有效，则可能在其上放置一个加密签名，我们将其称为“公证份额”。公证份额将发送到其他副本和子网，表示副本1认为这是一个好区块。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83Jan6rDBPMSo5nFpEUhoWrUichicX60pibXN1B9XAKQUr7reTMbP0L12MA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)

也许副本3和副本4也可能在同一区块上创建公证份额。让我们定义四个副本中的三个是足够的批准。请注意，在这种情况下，四分之三是我们希望获得的最高批准百分比，即使其中一项说明出现问题或脱机，协议也应取得进展。



我们将这三个公证份额合并为一个虚拟制品，我们将其称为公证，这意味着区块30已公证。公证人现在将进入下一个回合，并开始在31号高度寻找区块。



对于这些公证份额，我们使用称为多重签名的特殊签名。多重签名具有一个不错的属性，它允许将同一条消息上的许多签名压缩为一个恒定大小的签名，以证明所有节点都对该消息进行了签名。



这意味着，即使我们有一个包含许多公证人的非常大的子网，该公证工作仍将是一个很小的工件。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83os6yyia4Tu7I7VmPO3Yome3zkayk6lnvgY0ibWOLrgt5mmlic8TnvmRzw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


公证并不总是像刚才描述的那样工作。副本可能会看到有效的区块，并在该区块上创建公证共享。但是，现在可能会看到另一个候选区块处于相同高度，这也是有效的。



如果副本只对其中一个区块进行签名，我们实际上可能会陷入困境，因为一些公证人可能支持一个区块，而其他公证人则支持另一个区块，而任何一个公证人都不会获得足够的批准。



为了满足活性，公证人现在将实际对两个区块进行签名，并确保至少其中一个将以这种方式进行公证。这意味着我们可以在一个高度上获得多个经过公证的区块。



<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>

<center><font color=#FFA900>随机信标<font></center>



区块制造者和公证人可以识别有效的区块，但是我们尚未达成共识，因为在每个高度上可能都有多个经过公证的区块-因此，我们所看到的可能看起来像是由许多有效区块组成的树。



为了最终在区块链上达成协议，我们将通过在协议中添加一些内容：随机信标，来减少每轮获得的经过公证的区块数量。在每个高度，我们都有一个看起来像是虚拟的随机数，我们称其为随机信标，这是一个不可预测的值。



副本可能在高度29处有一个随机信标，并且当第二十九轮的公证过程完成时，它决定是时候创建下一个随机信标了。它将在先前的随机信标值（我们称为随机信标份额）上创建一个特殊签名。这是我们通过八卦网络共享的另一个工件。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83lCK3cUXMrd7qoShqxlWseOUALgLv6rsljVu0Hzcqx2Bbo0xSWbXibjg/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


如果现在获得另一个随机信标份额，则可以合并这些份额以构造下一个随机信标值。我们通过使用特殊签名（即阈值BLS签名）来做到这一点。它们具有独特的特殊属性，这意味着哪个副本参与构建值并不重要。



但是，它们也是不可预测的，因为副本无法自行构造该值。这些阈值BLS签名需要特殊的密钥材料，其中各方之间共享密钥，我们通过称为非交互式分布式密钥生成的协议进行了设置。



现在我们有了这种常见的随机性，我们将使用它来对每一轮的区块制造者进行排名。



例如，使用我们在第23轮中创建的随机信标，我们将在第24轮中对区块制造者进行排名。在第24轮中，我们可以同意副本1是最高优先级的区块制造者（即，排名为0的区块制造者）。



当然，我们仍然需要回退，因为副本1可能无法正常工作。例如，副本4可能会被选为第1级区块制造者，这是第一个后备者。如果这不起作用，则副本3是第2级区块制造者。



最后，副本2是不得已的方法。由于随机信标具有共同的随机性，因此所有复制品均同意区块制造者的这种排序。


![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83M0FtFCZz59Te7TtqQxV9YXuRCISd1tMEQRIaibicFBGJkNsTYibvVoTeQ/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


现在，我们将使用该区块制造者排名来进一步增强公证行为。更准确地说，当公证人进入回合时，它将启动一个计时器。在计时周期开始时，它只是希望由第0级区块制造者为该区块创建公证份额。



只有在一定时间后失败，公证人才会退回到第一级区块制造者的区块提案中。再经过一段预设的时间后，它将进一步下降到2级或3级区块制造者。



通过使公证人考虑到制造者的排名，我们的目标是减少每轮获得的经过公证的公证件的数量。让我们看一个例子：副本1在第30轮中，它收到一个有效的高度建议为30的区块建议，但它只是排名1的区块制造者。



它要等待，因为它尚不愿意对等级1的区块进行签名。如果一切顺利，它现在可能会从第0级区块制造者那里收到一个区块建议。现在，公证人在此区块上而不是在等级1区块上创建公证份额。



如果足够多的其他公证人都这样做，那么只有等级0的区块会被完全公证。在这种情况下，我们实际上减少了经过公证的区块数。这使我们更加接近共识。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83OW1PyPiapzUvicVJIh4pOEgkmp3iaibBnJ6gfHIDld2KnX83O3CxPRxG2g/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



现在，在某些回合中我们可能仍然有多个经过公证的区块，但希望在大多数回合中，我们仅从第0级区块制造者那里获得一个经过公证的区块。实际上，如果只有一位公证人，那么我们实际上已经达成协议。



这是因为每一轮中必须有一个有效的公证区块链，并且如果只有一个候选区块，那么经过该点的每一条链都必须经过该区块。因此，实际上必须商定该区块所隐含的链。



<center>
<img width = '73' height ='43' src ="https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPv13Yhx8f5HJdwqvg2haiahIxicsicYmwiczfL8icRSkwiaMDaRlXa0EWLOoItTxEum6jIap192uvV6W4g/640?wx_fmt=png"/>
</center>

<center><font color=#FFA900>最终性<font></center>





因此，挑战仍然存在：我们如何知道我们已经达成协议？复制品如何知道它们可以接受链？一种选择是让副本仅等待一段时间，并假设在此时间段之后它将看到所有已公证的区块，并且如果仅一个高度的公证区块，则认为该链是同意达到这个高度。



但这是一种非常冒险的方法。也许网络无法正常运行，实际上还有其他一些我们尚未看到的经过公证的模块。这意味着如果我们没有等待足够长的时间，则可能会违反安全属性。



这使我们处于非常困难的境地。我们希望快速达成协议，以便子网对用户做出响应，但是与此同时，我们知道需要等待很长时间才能保证安全性。



我们通过使用不同的机制来遵守协议来避免这种折衷。我们有一个单独的异步完成过程，可以帮助我们检测何时达成协议。请记住，公证人会创建公证份额，直到他们看到一个区块被完全公证，然后他们才进入下一轮。



现在，我们将让公证人分享一些有关他们公证的区块的信息，这将有助于我们达成协议。更准确地说，如果公证人没有为该轮在该轮收到的第一个经过公证的区块以外的区块创建任何公证份额，它将创建另一种类型的签名，我们称之为最终份额。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu833FqsqYoH9gUZicrQUT8jofyJHB9O43xxdKSByIRgMtfePR6ef65gRCA/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



副本1的高度30区块上的最终份额从本质上讲意味着副本1没有公证签署除此高度以外的任何高度30区块。这是另一个将散布到其余子网的工件。如果足够多的副本还为同一区块创建最终份额，那么我们可以将它们聚合为一个终结。



每当我们在区块上看到这样的最终确定时，我们都知道我们可以信任区块链，因为最终确定证明了在那个高度上没有其他经过公证的区块可以存在。



如果网络运行良好，这意味着我们实际上可以很快在区块上达成协议，因为我们可以快速创建这些最终份额并在区块链上达成协议。



此外，我们没有受到网络攻击的风险。即使网络运行不正常，我们也知道我们仍然是安全的，因为我们仅依赖签名，而不依赖于已经看到所有消息的假设。



完全完成意味着只要子网的少于三分之一的节点损坏，就不能存在其他经过公证的区块。



让我们深入理论，看看为什么在具有四个节点的情况下实际上是这种情况。我们知道，如果完成一个区块，则意味着三个公证人在此区块上创建了最终份额，因为我们有四个节点。



我们假设其中最多有一个已损坏，但这仍然意味着我们可以确定至少有两个副本是诚实的，并在该区块上创建了最终份额。我们也知道，诚实的副本只有在未在该高度复制任何其他区块的情况下，才会创建这样的最终份额。



![avatar](https://mmbiz.qpic.cn/mmbiz_png/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83vJ5icycJamQjgiaONF5v6W2QXuDTU0ZHb5J3c5MT6KJT9xDNr2q6l9Pw/640?wx_fmt=png&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)



这意味着，在此高度上，两个副本没有为最终确定的区块以外的任何区块创建公证份额。我们也知道，公证需要三份公证份额。这意味着必须参与三个副本才能达到目标，但是子网上只有四个副本。



此外，我们说过其中的两个肯定不会对任何其他区块进行公证，这只剩下两个副本。而且两个还不足以达到这个公证阈值3，因此可以得出结论，即最终确定意味着在那个高度上没有其他经过公证的区块。



这是基于少于三分之一的副本已损坏的假设。上面的演示使用了一个子网大小，其中四个副本最多包含一个已损坏的副本，但是只要“f”小于a，就可以轻松地将相同的参数扩展到“f”个已损坏的“n”个副本，只要“f”小于“n”的三分之一。



总而言之，我们有一个由四个部分组成的共识协议。区块制造者创建候选区块以扩展区块链。我们有一个公证过程，可确保识别出有效的区块。



然后，我们添加一个随机信标，用于对区块制造者进行排名，并减少每轮获得的经过公证的区块数量。



最后，我们使用异步终结机制，该机制使我们知道何时真正同意区块链，而不必完全依赖网络假设。



这个共识协议使我们能够在子网内使用复制，从而实现了互联网计算机所需要的安全性和可靠性。



请继续关注更多发布，详细介绍互联网计算机背后的技术。



开始在sdk.dfinity.org上构建并加入我们的开发者社区forum.dfinity.org。



![avatar](https://mmbiz.qpic.cn/mmbiz_jpg/JUK5MT24wzPeMe8lxJW1Nhk4GrpCuu83Bv35JIdslaDKDWHdnQZW3iatUZeiajo1sJ2YvFxxH1zYS5GFget7AMVg/640?wx_fmt=jpeg&tp=webp&wxfrom=5&wx_lazy=1&wx_co=1)


作者：DFINITY工程（共识）经理Manus Drijvers

翻译：Catherine


来源：DFINITY公众号
##### [原文链接](https://mp.weixin.qq.com/s/S-gzFhELzFCrVU2Ly-7Uyg)