---
id: 612
title: 当我们谈“可重复性”的时候我们在谈什么？
date: 2016-08-15T03:01:22+08:00
author: Chuanpeng Hu
layout: post
guid: http://huchuanpeng.com/?p=612
permalink: /2016/08/15/four_layers_of_reproducibility/
categories:
  - Methodology
tags:
  - reproducibility
  - 可重复性
---
此文是我在自己的微信公众号上的一篇文章，本意是在记录一下自己对于可重复性（reproducibility）的理解。原文见<a href="http://mp.weixin.qq.com/s?__biz=MzA4NzAwOTk1Mw==&mid=2649293732&idx=1&sn=8e6a158bfbf579a378ddc9f6d17373f7#rd" target="_blank">这里</a>。欢迎关注Open Science 公众号(ID: OpenScience).

最近看到了讨论科研中可重复性问题的<a href="http://library.fora.tv/2016/08/06/the_replication_crisis" target="_blank">视频</a>（不仅是心理学），其中Brian Nosek提到了可重复性(reproducibility)的几层含义(23:45&#8217;到25:30&#8242;)。我觉得非常有意思，这也是我们在讨论可重复性时因为篇幅的限制而未讨论的问题[见引文]，所以正好在展开说一下。

这个视频是一次关于<a href="http://mp.weixin.qq.com/s?__biz=MzA4NzAwOTk1Mw==&mid=2649293695&idx=1&sn=ae2226c695702122957f3f7ccd0f22f6&scene=21#wechat_redirect" target="_blank">可重复危机</a>的讨论。在这个视频中，Brian谈到了四层不同的reproducibility，以下是我自己对这四层的可重复性的理解，建议看原视频（点击原文链接可观看）：

第一层：再现原论文中的结果。即使用相同的数据，相同的分析方法，是否能够得到相同的结果。这一层是最容易实现的，基本上只要公开数据和分布方法，我们就可以得到跟原论文一样的结果。但从目前科研界的主流做法来看，这一点并没有那么容易实现，因为大家基本上只是发表论文，并不公开原始数据，也不公开分析数据的过程。也正是由于不需要公开数据分析的过程，不少研究者靠GUI，手动点击完成数据分析（比如SPSS和Excel）。这样造成的后果就是，论文发表之后，作者本人也不一定记得自己当时是如何分析的了。所以从这个角度来，目前许多关于可重复性问题的解决方案，是在试图解决这个问题，比如Rmarkdown的使用；

第二层：再现原论文中的结论。也就是说，仍然使用原论文的数据，告诉你研究的问题和假设，让你去分析，看看你是否能够得到相同的结果和结论。这一点上就比较有意思了。理论上讲，各种方法应该得到相同的结果，但实际上，Brian他们目前正在做的一个研究显示并非如此：招募世界范围内不同的研究者，给他们一批数据和研究假设，让他们采用自己擅长的方法去分析。结果不同研究小组分析的结果差异很大，因此结论也不尽相同。从这个角度来讲，研究者在数据分析的过程中，自由度还是太大，可操作的空间太大，于是数据最终可能是朝着符合研究者预期的方向得到结果；

第三层：使用与原论文相同的方法和材料，看看是否能够得到原论文的结果。前段时间Replication Project: Psychology所做的工作是这一层的重复。这种重复也叫做直接重复(direct replication)。当然，直接重复面临着不少的批评，因为直接重复的过程中，可能会忽略不少的细节，有可能这些细节才是关键的，而原研究者甚至都没有意识到。所以不少研究者发现自己对其他人的研究进行直接重复时，即使失败，也会不立刻怀疑原研究，而是首先从自己的研究过程找问题。但是仅仅看论文确实是很难精确复制原实验的过程，这个问题Brian在视频中也说了；

第四层：使用与原论文不同的材料和方法，仍然得到原论文的结论。我理解的这个就是心理学中常用的概念重复（conceptual replication）。比如为了证明刻板印象启动是有效的，第一个实验启动老年的刻板印象，第二个启动婴儿的刻板印象，第三个启动嬉皮士的刻板印象，都发现了与刻板印象一致的行为表现，于是证明了刻板印象启动是有效的（婴儿和嬉皮士是我瞎编的）。这种方法在过去的研究中经常出现，Stapel也说他的结论被conceptual replicated。这个意义上的重复也是重复，但可能没有直接重复那么能力有力地证明原研究的效应确实是存在的。

这四层可重复性还只是一种观点，还可以讲方法可重复性、结果可重复性、推论可重复性等，可以参考 Goodman, S. N., Fanelli, D., & Ioannidis, J. P. A. (2016)在Science Translational Medicine上对这个问题的讨论。

此外，关于reproducibility，这个概念最早是由做计算和统计这一块的人提出的，由于他们的工作涉及到海量的运算，可能有大量的代码和脚本，一个人是否能用使用代码完全再现另一个分析，就是最原始的reproducibility的意思。这是我对Roger Peng在Coursera上关于reproducible research一课上讲到内容的理解（如果有误，那得怪我）。对这个问题感兴趣的话，可以上coursera上免费注册和学习这个课程：https://www.coursera.org/learn/reproducible-research。

最后的最后，reproducibility并不是心理学这个领域特有的问题，比如Science在2011年讨论reproducibility的时候，完全跟心理学没有关系：http://science.sciencemag.org/content/334/6060。

参考文献：

Goodman, S. N., Fanelli, D., & Ioannidis, J. P. A. (2016). What does research reproducibility mean? Science Translational Medicine, 8(341), 341ps312-341ps312. doi:10.1126/scitranslmed.aaf5027

胡传鹏, 王非, 过继成思, 宋梦迪, 隋洁, 彭凯平. (2016). 心理学研究的可重复性问题：从危机到契机. 心理科学进展, 24(9), 1504–1518 doi:10.3724/SP.J.1042.2016.01504