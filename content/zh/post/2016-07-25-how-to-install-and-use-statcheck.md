---
id: 508
title: 如何安装与使用statcheck工具包
date: 2016-07-25T07:38:54+08:00
author: hcp4715
layout: post
guid: http://huchuanpeng.com/?p=508
permalink: /2016/07/25/how-to-install-and-use-statcheck/
categories:
  - methodology
  - 方法
tags:
  - methodology
  - stats
  - 可重复性
  - reproducibility
---

2016.09.23更新：statcheck的作者发布了一个[manual](http://rpubs.com/michelenuijten/202816).

2016.10.21更新：statcheck发布了[在线版](http://statcheck.io/).

7月23号，psych sci的主编在自己的twitter上发推说目前psych. sci.正在测试使用statcheck工具包。

![insert pic 1](/img/Lindsay_tw.png)

对于不少人来说这可能并不奇怪，因为这个工具包早就已经公布出来，能够快速地检查一篇论文中统计量是否有错误，比如F值与后面的p值是对应。这个软件的好处在于它可以检查出由于手动输入造成的错误。一经发布，得到了广大的好评。

statcheck的官网：https://mbnuijten.com/statcheck/；这个页面有教大家如何安装，当然还有另一个教大家如何使用的[博客](http://daniellakens.blogspot.co.uk/2015/10/checking-your-stats-and-some-errors-we.html)（需要翻墙）

以下是我在window 10下面进行安装和测试的结果。

第一：下载R和Rstudio，并且安装好；

第二：下载 Xpdf 并且解压（下载地址：http://www.foolabs.com/xpdf/download.html），可以选择把这个解压后的文件移动到一个存放软件程序的路径（比如我就是C:/Programfiles/xpdf）。

第三：将Xpdf添加到系统的environmental variable里，右击 this pc（此电脑）-> Properties -> Advanced system settings -> environmental variable. 在User variable 里编辑Path，如果没有Path, 自己新建一个，把Xpdf的路径放进去。

（第二步和第三步就是安装Xpdf，其功能是将pdf转化为txt进行读取，具体安装可以看这个[pdf](https://mbnuijten.files.wordpress.com/2013/08/manualinstallationxpdflakens.pdf)）

安装好了之后，打开Rstudio，安装statcheck这个工具包（>>后面接的是代码，如果复制的话，不要把>>也复制到R里去了）：

    # install and load statcheck
    if(!require(statcheck)){install.packages("statcheck")}
&nbsp;

然后打开这个工作，使用它来检查：

    library(statcheck)
    checkPDF(&#8220;C:/Users/Daniel/statcheck/Zhang2015.pdf&#8221;)

如何一切正确的话，你的Rstudio里就出输出检查出来的结果，比如：

![insert pic 2](/img/statcheck.png)

值得一提的是，并不是所有的pdf都能够读出统计值 ，至少我看了两篇APA的文档可能就无法进行检查。

如果对statcheck本身有兴趣，可以查看一下[原文](https://mbnuijten.files.wordpress.com/2013/01/nuijtenetal_2015_reportingerrorspsychology1.pdf)。

为了避免麻烦，我直接把Xpdf的winow版本和Lakens提供安装英文手册使用云盘共享，链接：http://pan.baidu.com/s/1kVrpWzX 密码：rpe4；下载statcheck压缩包即可。