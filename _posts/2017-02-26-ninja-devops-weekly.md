---
layout: post
title:  "DevOpsWeekly#14 第一个SHA1 collision被发现, 在Uber的那一年, 函数式编程入门, 程序员需要大学文凭吗?"
date:   2017-02-26 17:00:00 +0800
categories: weekly
---

### [**SHA1 collision已被发现: Announcing the first SHA1 collision**](https://security.googleblog.com/2017/02/announcing-first-sha1-collision.html)

SHA1不够安全已经不是什么新闻. 2014年9月, google security blog就发表过关于逐渐淡出'SHA-1'的文章: [Gradually sunsetting SHA-1](https://security.googleblog.com/2014/09/gradually-sunsetting-sha-1.html). 
    小编所在的公司也早已停用使用SHA1的certificate, 但SHA1仍旧是被普遍使用的技术: 数字签名, GIT, SVN, 等等
    两天前, Google与CWI宣布他们发现第了一个SHA1 collision, 同时发布了[两个不同的PDF文件](https://shattered.it/), 但是他们有相同的SHA1.

如果你或者你的项目还在使用基于SHA1的数字签名, 是时候review并且fix SHA1带来的潜在威胁了. 


### [**到底该如何推出Vim? How the hell do I exit: A beginner's guide to Vim**](https://getintodevops.com/blog/how-the-hell-do-i-exit-a-beginners-guide-to-vim)

0起点的新手Vim指南. 


### [**在Uber的那一年 Reflecting On One Very, Very Strange Year At Uber**](https://www.susanjfowler.com/blog/2017/2/19/reflecting-on-one-very-strange-year-at-uber)

女员工在公司受到上司性骚扰该怎么办? HR可能并不会帮你. 作者亲身经历的一年, 最终以离职结束那奇葩的经历. 紧接着techCrunch有文章指出, [还有一些其他的技术公司也没能处理好性骚扰](https://techcrunch.com/2017/02/20/uber-is-not-the-only-tech-company-that-mishandles-sexual-harassment-claims/?ncid=rss)
    后来Uber召开了all-hands, 称他们将会了解错误并且fix it. 
    
    > Change doesn’t usually happen without a catalyst. I hope that by taking the time to understand what’s gone wrong and fixing it we can not only make Uber better but also contribute to improvements for women across the industry.


### [**函数式编程入门教程**(中文)](http://www.ruanyifeng.com/blog/2017/02/fp-tutorial.html)

阮一峰老师深入浅出的介绍functional programing


### [**程序员需要一张大学文凭吗? Do Developers Need College Degrees?**](http://www.stackoverflow.blog/code-for-a-living/do-developers-need-college-degrees)

答案是: 不一定. 
