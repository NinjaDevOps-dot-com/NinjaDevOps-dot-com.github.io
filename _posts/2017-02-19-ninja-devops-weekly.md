
---
layout: post
title:  "DevOpsWeekly#13 Instapaper事故分析, 码农的义务, 在stack overflow远程工作,Google Testing Blog:Discomfort as a Tool for Change, 采访Agile Manifesto co-author Martin Fowler"
date:   2017-02-19 17:00:00 +0800
categories: weekly
---

- [**Instapaper事故分析: Instapaper Outage Cause & Recovery**](https://medium.com/making-instapaper/instapaper-outage-cause-recovery-3c32a7e9cc5f#.i1k13dx2g)

    Instapaper使用基于Amazon的Relational Datbase Service(RDS)的MySQL, 事故原因是由于2TB文件大小限制: `"The table 'bookmarks' is full"`, RDS console并没警告信息. 宕机之后试着备份并转移数据,但耗时太久. 于是花6小时新建一个"limited access"的instance, 此时已宕机31小时. 由于缺少应对此类紧急情况的计划, 他们并不清楚备份并恢复数据库需要多久. 一开始的估计是6~8小时, 但后来发现需要好几天. 最后一个Aamazon的工程师mount了一个ext4的文件系统到处问题的数据库服务器上,resync了之前的ext3文件, 8小时候一个基于ext4的数据库恢复成功. Action items:
  - 设计一个更好的流程来应对此类事故,并上报问题到Pinterest的Reliability Engineering team
  - 测试数据库备份!


- [**码农的义务**](https://dev.to/steliosvoskos/the-obligation-of-a-software-developer)
 
    16年的时候我们讨论过[什么样的人才算高级程序员](http://ninjadevops.com/weekly/2016/12/17/ninja-devops-weekly.html), 最近刚好又看到这篇, 不做翻译, 直接摘抄:
  
  - Find the best solution and not a solution
  - Do not write code you do not trust
  - Learn how to say No. But also learn to negotiate.
  - Respect your team members
  - Enhance an implementation. Do not criticise it.


- [**在stack overflow远程工作 - What it Means to be a Remote-First Company**](http://www.stackoverflow.blog/code-for-a-living/what-it-means-to-be-a-remote-first-company)

    stack overflow大概有300多名员工, 其中有85名是remote woker. 开会都是戴耳机google
     hangouts `face-to-face`, 大量使用Slack, Hangouts, 以及自内部的chat工具. chat也被认为是异步/asynchronous的. 公司会给remote woker提供设备, 譬如Herman Miller的椅子, Steelcase的可调整高度的桌子, Macbook, 外接显示器等等. 公司也会给一些钱用来支付"home office"花销, 譬如网络. 公司有活动时, 也会受到相应的礼物. 


- [**Google Testing Blog:Discomfort as a Tool for Change**](https://testing.googleblog.com/2017/02/discomfort-as-tool-for-change.html)

    Google Drive的一个SETI(Software Engineer, Tools and Infrastructure)写的关于解决Product-Wide问题的文章:
     - Hard-to-use APIs
     - Big, slow releases
    解决方案:
     - Incentivizing easy-to-use APIs 通过创建测试环境, 并与engineering team leads一起创建[Fakes](https://testing.googleblog.com/2013/07/testing-on-toilet-know-your-test-doubles.html)测试, 让engineering尽快获得反馈, 并帮助Management设计engineer team的绩效考核目标. 
     - Fast, small releases: less coupling between systems, bettwe/more automated testing, fater feedback.


- [**博客: 采访Agile Manifesto co-author Martin Fowler**](http://www.stitcher.com/podcast/the-agile-uprising-podcast/e/manifesto-coauthor-interview-martin-fowler-49106530?autoplay=true)

    iTunes Podcasts可以搜索"The Agile Uprising Podcast"
