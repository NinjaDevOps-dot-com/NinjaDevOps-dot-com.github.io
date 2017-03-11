---
layout: post
title:  "DevOpsWeekly#16 Google云计算的永久免费计划, 程序员招聘趋势, 播客-采访敏捷宣言的作者们, 老板应该保护员工的时间, 持续集成认证"
date:   2017-03-11 13:00:00 +0800
categories: weekly
tags: devops
---

### [**Google云计算增强了免费项目, 并推出永久免费计划**](https://cloud.google.com/free/)

  $300的免费点卡 + 永久免费项目. 永久免费项目包括了:
  
  - GAE: 28 Instance hours per day
  - GCE: [f1 micro instance](https://cloud.google.com/compute/pricing#sharedcore)(0.2 vCPU, 0.6GB Memory ~$2.56) per month, 包含30GB的 HDD
  - Google Cloud Storage: 5GB
 
除此之外还有的服务, 譬如图像识别, 声音识别, 自然语言处理, Build container, private Git repository等等. 
当然免费项目也有一些限制, 譬如区域, 配额等等. 
更多更多可访问: [https://cloud.google.com/free/](https://cloud.google.com/free/)

当然现在其他的微型instance价格也是越来越低, 但永久免费的这些项目的确是不错的开始. 


### [**2017程序员招聘趋势 Developer Hiring Trends in 2017**](https://stackoverflow.blog/2017/03/09/developer-hiring-trends-2017/)

  stack overflow通过分析其Jobs服务的200家企业的招聘数据, 得出了今年的最新趋势. 增长最快的关键词: 
  ReactJS, Docker, Ansible, Apache Spark, SysAdmin, QA, Azure, DevOps, Go, Automated Test. 高需求(肉多狼少)的: backend web/cloud, iOS, Android, and DBA/SQL.
  
  更多的数据/图表可访问[stack overflow博客](https://stackoverflow.blog/2017/03/09/developer-hiring-trends-2017/)
  
  
### [**播客: 采访敏捷宣言作者 Manifesto Co-Author Interview: Ken Schwaber, Stephen Mellor, Martin Fowler**](http://www.stitcher.com/podcast/the-agile-uprising-podcast)

  最近The Agile Uprising Podcast采访了Martin Fowler, Stephen Mellor, Ken Schwaber等敏捷宣言的作者, 每次采访都少于60分钟, 推荐.
  - [Stitcher订阅: The Agile Uprising Podcast](http://www.stitcher.com/podcast/the-agile-uprising-podcast)
  - [iTunes订阅: The Agile Uprising Podcast](https://itunes.apple.com/us/podcast/the-agile-uprising-podcast/id1163230424?mt=2)
  

### [**Manager的工作目标之一: 保护团队的时间及注意力 protecting team’s time and attention**](https://m.signalvnoise.com/give-40-take-0-dddf5ffb2aaa#.fmiizvkf6)
  
 在工作里, 我们的时间难免的被打碎. 在公司里有过连续4小时不被打扰的经历吗? 如果有过, 是什麽时候? (小编有过, 大概是在每次新工作开始的前几天吧). 有一些老板/manager会觉得员工应该时刻为公司待命, 想想那些在下班后收到的邮件, 短信, 甚至电话. 这将会让透支员工经历, 并且可能导致员工离职. 本文并举例为什么[在Basecamp他们没有status update meetings](https://m.signalvnoise.com/status-meetings-are-the-scourge-39f49267ca90#.f6fkp9jji), 他们认为: 一群人在一起逐个说自己所得事情是意见浪费时间的事情. 
   > A manager’s job is to protect their team’s time and attention.
  
  对Basecamp感兴趣的读者还可以继续阅读: [What six weeks of work looks like](https://m.signalvnoise.com/what-six-weeks-of-work-looks-like-69289221e80d#.zg3rdqitn)
  

### [**持续集成认证 - ContinuousIntegrationCertification**](https://martinfowler.com/bliki/ContinuousIntegrationCertification.html)  

  1. 所有developer每天都会commit到"shared mainline"(而不是某个feature branch)
  2. 每次commit都会trigger 自动build, test
  3. 如果build/test 失败, 问题会在10分钟内解决掉. 
  
  只有跑在每个人天天commit的"shared mainline"上的CI才是真正的CI. 跑在FeatureBranch上的所谓CI是` Daemonic Continuous Integration`, 因为这并不能带来期望的效果. 每个人的code based都不应该在明显偏离其他人的, CI意味着整个团队了解目前code的真实状态, 避免big risky的merge, 在需要重构的时候就大胆重构. [阅读Martin Fowler的原文.](https://martinfowler.com/bliki/ContinuousIntegrationCertification.html)

---

**插播广告**
如果您乐于贡献, 欢迎你每周抽出时间来为所有读者推荐富有营养的文章, 您可以通过以下方式推荐您的内容及点评:
 - 提交[gitbug issue](https://github.com/NinjaDevOps-dot-com/NinjaDevOps-dot-com.github.io/issues)
 - Email: info at ninjadevops.com
