--- 
layout: post
title: 嵌套评论的问题及向Japhia,邓肯致歉
wordpress_id: 152
wordpress_url: http://ISayMe.com/?p=152
date: 2011-05-30 11:05:44 +08:00
tags: [Apology, PhilNa2, 点滴]
---
写这篇文章之前,首先要对[Japhia](http://japhia.info)以及[邓肯]http://dengken.name()两位朋友表示抱歉,因为我的一时小聪明,而连累到两位使用philna2主题的朋友.具体原因请往下看

从前两天换回philna2后,一直就有点小问题.在侧边栏上的最新评论,当我点击链接进入文章页的时候,会在文章页找不到评论,
具体的表现是什么呢?

是这样的,假如文章评论是分页的形式,侧边栏上的最新评论按找文章页的正常情况下是在第二页或者是第三页,但是侧边栏上的链接显示的是第一页.
经过我检查,是因为嵌套评论的原因.

philna2本身不支持嵌套评论,也不能使用willinkan大师的邮件回复通知代码.
原因就是,philna2在回复评论的时候不对此条评论的parent值做任何设置.如果有parent值,wordpress就会认为此条评论是对某条评论的回复.

当初在看自由的风 博客时,自由的风博主曾讲到了 修复了philna2使用willinkan的邮件回复通知不能在前台发邮件的问题.
按照他的思路,我把我用的philna2.js修改了一下,使philna2使用邮件回复通知代码的时候,可以在前台发邮件.本以为是个好事.但是却犯了个错误.

现在的情况是 每次回复别人的评论的时候都会给此条评论指定parent值,因此,即使在后台选择不嵌套评论,还是会有parent值向wordpress说明此条评论是某条评论的回复.所以侧边栏在寻找最新评论的时候,依旧把这条评论以及他的父评论算作一条.因此就会出现第20+条评论的链接仍然会显示在第一页,但是由于在后台设置不嵌套,所以就找不到了. 你听明白否?我表达能力有限.

当然如果你设置的是 不分页显示评论 或者设置的每一页的评论数足够大 就没有任何问题.仍然能从侧栏上的链接正确找到评论

说的不是很清楚,但是我明白是怎么回事.
由于我发给Japhia以及邓肯童鞋的philna2.js文件是我修改后的文件,因此可能就会出现这样的问题.但是我看到在两位童鞋的博客上还没有出现太大的问题.邓肯童鞋貌似没有分页显示评论,而Japhia童鞋每篇文章的评论比较少以及设置的每页评论数可能比较大,还没有出现这个问题.

但是出现问题就要解决.麻烦 Japhia以及邓肯童鞋将你们的philna2.js文件发给我,我负责帮你们修改好,对于以前的那些评论如果出现了这样的问题我表示非常抱歉,希望没对你们造成什么影响.实在是抱歉~

本人邮箱 lwnet90[AT]gmail.com