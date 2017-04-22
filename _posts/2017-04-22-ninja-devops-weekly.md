---
layout: post
title:  "DevOpsWeekly#22 程序员如何自学成才, Netflix的容器进化之路, Flaky test是哪来的? 没有“小”的变更, 用合伙人关系取代面试"
date:   2017-04-22 17:22:57 +0800
categories: weekly
tags: devops
---

### [**程序员如何自学成才 Learning without a mentor: how to become an expert programmer on your own**](https://codewithoutrules.com/2017/04/17/learning-without-a-mentor/?utm_source=ninjadevops)

在没有导师的情况下，程序员如何自学成才? 如果你感到困惑, 觉得这些一切都比你想象的困难, 这说明你正在学习. 如果迫使自己学习并进步? **Teaching**: 迫使自己深入思考i; **Switching jobs**: 不管是在公司内部调动还是跳槽, 都能让你跳出来学习. 

### [**Netflix的Docker容器进化之路 The Evolution of Container Usage at Netflix**](http://techblog.netflix.com/2017/04/the-evolution-of-container-usage-at.html?utm_source=ninjadevops)

Netfix大量使用EC2, 就在上周, 通过自家平台`Titus`, 启动了100万个instance. 在高峰时, 会运行500个`EC2 r3.8xl`(32个vCPU, 244GiB内存)应付batch job, 运算量约等于16,000个核 + 120 TB内存



### [**Google Testing：Flaky test是哪来的？**](http://testing.googleblog.com/2017/04/where-do-our-flaky-tests-come-from.html?utm_source=ninjadevops)

测试越大，越不稳定:
> We need to be more careful before we decide to write large tests. Think about what code you are testing and what a minimal test would look like. And we need to be careful as we write large tests. Without additional effort aimed at preventing flakiness, there's is a strong likelihood you will have flaky tests that require maintenance. 


### [**没有“小”的变更 There are no small changes**](https://blog.intercom.com/there-are-no-small-changes/?utm_source=ninjadevops)

看起来很小很简单的变更，往往牵扯到很多细节。


### [**用合伙人关系取代面试 Eliminating the Job Interview via Partnership**](http://www.daedtech.com/eliminating-job-interview-partnership/?utm_source=ninjadevops)

需要招人时, 选择"合伙人",  不再需要邀请陌生人来面试. 譬如: 与其一次性支付的referral bonus, 不如改为按月支付被推荐人薪水的2%. 这样一来, 的确会有一种合伙人的感觉. 如果没有长期的打算, referral bonus按月拿的话, 也没有很多. 给公司推荐越好的员工, 拿到的奖金就越多, 而且是越来越多, 就会长期在公司留下来.
