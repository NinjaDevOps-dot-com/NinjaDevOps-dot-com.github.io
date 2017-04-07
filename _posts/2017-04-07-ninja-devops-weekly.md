---
layout: post
title:  "DevOpsWeekly#20 Google是如何提高代码质量的? DigitalOcean的宕机报告, Python很慢,但我不介意, Java Annotated 4月版, Jenkins发布新版UI"
date:   2017-04-07 23:00:00 +0800
categories: weekly
tags: devops
---


## [**Google是如何提高代码质量的? Code Health: Google's Internal Code Quality Efforts**](https://testing.googleblog.com/2017/04/code-health-googles-internal-code.html)

几年前, 一群Googler成立了`Code Health`小组. 
>  What we cared about was the processes and practices of software engineering in full—any aspect of how software was written that could influence the readability, maintainability, stability, or simplicity of code. We liked the analogy of having "healthy" code as covering all of these areas.

这个Google-wide Code Health Group维护Google的`code review guidelines`, 编写内部文档, 组织讲座等等. 除了这个Central的小组之外, 很多产品/团队也会他们自己的`Code Health`小组. 


## [**DigitalOcean的宕机报告**](https://www.digitalocean.com/company/blog/update-on-the-april-5th-2017-outage/)

4月5日, DigitalOcean的control panel及API宕机4小时56分钟. 事故起因: 测试程序不慎用了生产环境的credentials.
> The root cause of this incident was a engineer-driven configuration error. A process performing automated testing was misconfigured using production credentials. 

事故发生后, DigitalOcean花了4个小时恢复数据.　有网友评论`I think someone's in trouble!`, DO员工Andrew Starr-Bochicchio回复: 
> People will always make mistakes, it's in our nature. The main lesson here is about the system, not that an individual made an error.

相信多数人在自己的职业生涯中都会犯几次类似的错误, 不小心删除了备份, 清空了数据库? 没关系, 吸取教训, 继续前进, 做一个更好的engineer :)


## [**Python很慢, 但我不介意 Yes, Python is Slow, and I Don’t Care**](https://hackernoon.com/yes-python-is-slow-and-i-dont-care-13763980b5a1)

一篇关于Python的文章, 作者分享了很多务实的观点: `Optimize your most expensive resource.`, `It’s more important to get stuff done than to make it go fast.`
 - 优化最昂贵的资源, 是你, 而不是电脑
 - 选择那些可以帮你提高开发速度的语言/框架/架构, 不要仅仅因为运行的快而选择某一门语言
 - 如果有performance issue: 找出bottleneck
 - bottleneck往往既不是CPU也不是Python
 - 如果Python是bottleneck, 而且你已经尝试了优化算法等, 尝试转向Cython/C
 - Go back to enjoying getting things done quickly


## [**Java Annotated Monthly – April 2017**](https://blog.jetbrains.com/idea/2017/04/java-annotated-monthly-april-2017/)

IntelliJ发布本月的[Java Annotated Monthly](https://blog.jetbrains.com/idea/2017/04/java-annotated-monthly-april-2017/), 涵盖Java生态圈里的新鲜事. 推荐Java/Android 程序员阅读. 


## [**Jenkins正式发布新版UI Getting Started with Blue Ocean**](https://jenkins.io/blog/2017/04/05/welcome-to-blue-ocean/)

主要的新功能:
 - 可视化Pipeline
 - Pipeline编辑器

![jenkins-blue-ocean](https://jenkins.io/doc/book/resources/blueocean/intro/new-pipeline-box.png)
