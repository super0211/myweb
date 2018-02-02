---
title: 街机游戏模拟器 MAME 是一款怎样的软件？有哪些特色？
tags: []
date: 2018-02-02 11:01:40
---

MESS和MAME合并了，现在叫做MAME Software List。现在MAME已经不光是街机硬件模拟器了，而且还有着许多最完美的家用机模拟核心，比如FC/MD/PS/N64等等。AMIGA和C64等古董微机也可以模拟了。

这个模拟器的主要主旨是“将街机/家用机/古董PC的硬件文档化（用编程语言）”。也就是说，要完全的、原原本本的、一步一步的将硬件原本的特性、操作还原出来。而不是用某些取巧的HACK来达到“能玩”的效果。

对MAME来说，“完美的诠释原硬件”要比“能玩”两个字重要得多。由于这个宗旨，MAME极少使用各种优化，最多就是一些SIMD Intrinsic，甚至为了考虑跨平台移植性，连这种东西也很少。硬件加速更是完全不被支持。原硬件有3D绘图/3D加速功能？用C语言软件实现！绝对不会借用任何硬件加速功能。

当然，现在的MAME支持D3D/OGL输出，并且支持各种Shader来增强画质。但那毕竟只是在内核部分用软件方式渲染完全部画面之后输出图片而已。Shader的作用也只是锦上添花，比如模拟一下CRT的效果。游戏本身是绝对不会经过D3D或者OGL进行绘图的。

结果就是，只要MAME的“支持状态”里面写着“正常工作（Working）”，那就意味着你可以得到和原机完全相同的体验。当然，输入设备的不同等问题则是另一回事。但是软件上做到了完全的、完美的再现原始基板、游戏、主机etc。但是运行效率则完全没有保证。比如MAME的N64的RDP核心是最完美的RDP核心之一。不像主流N64模拟器那样，需要对每一个游戏一一编写微代码。MAME的RDP核心完全再现了N64原本RDP芯片的可编程特性，可以响应所有的指令。但是速度非常、非常的慢。我把我的5960x超冒烟了4.5G，也只能有不到20帧的速度。

所以MAME不会像其他一些以“能玩”为主要目标的模拟器那样，由于各种Hack的存在，同一款硬件大多数游戏基本完美，一部分有些毛病，但是基本不太影响玩这种情况。Working就是完美、绝对不会出现“有些毛病”，只要是这个硬件的都会完全正常运作。Partial通常意味着一些部分没有实现，可以有一些期待，Not Working就是不能玩、有关键部分没有被实现——不排除有些游戏能启动，但是毕竟不被支持。

另外还有一点，早年MAME本身是命令行程序。所以各种GUI和整合GUI版本如雨后春笋般到处出现，其中不乏有做的非常不错的。比如MAMEPlus，MAME XT等等。但是现在MAME本身已经内建一套GUI了（依然可以通过命令行使用），所以各路GUI和整合GUI版本纷纷下马，不再继续开发了。由于这套GUI的操作并非基于Windows的操作习惯，对于习惯了以前那套GUI的人来说是一件憾事，初次上手或许也会有些困难。

总之，MAME是一款模拟器，总之是将硬件文档化，特色是完美模拟各种硬件、但是效率非常低。功能非常强大，但是上手可能有些困难。

来源：知乎 www.zhihu.com

作者：[pig-10](http://www.zhihu.com/people/pig_10?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=author)

【知乎日报】千万用户的选择，做朋友圈里的新鲜事分享大牛。
        [点击下载](http://daily.zhihu.com?utm_source=rssyanwenzi&utm_campaign=tuijian&utm_medium=rssnormal)

此问题还有 [9 个回答，查看全部。](http://www.zhihu.com/question/265689338/answer/299031244?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=title)

                延伸阅读：

[在游戏中，你见过哪些富有创意的技能？](http://www.zhihu.com/question/22099262?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=title)

[街机相对于其它电子游戏有何特点？](http://www.zhihu.com/question/20438290?utm_campaign=rss&utm_medium=rss&utm_source=rss&utm_content=title)