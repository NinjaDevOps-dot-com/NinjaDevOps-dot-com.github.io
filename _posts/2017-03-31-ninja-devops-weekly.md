---
layout: post
title:  "DevOpsWeekly#19 如何让你的简历脱颖而出, InfrastructureAsCode, 听StackOverflow员工讲他的经历, ThoughtWorks发布新一期的技术雷达, SaaS型初创企业安全101"
date:   2017-03-31 23:00:00 +0800
categories: weekly
tags: devops
---

### [**如何让你的简历脱颖而出 Getting Your Résumé Read**](https://www.joelonsoftware.com/2004/01/26/getting-your-resume-read/)
  
这是[Stack Overflow CEO Joel Spolsky](https://www.joelonsoftware.com/about-me/)在2014年写的一篇关于求职简历的文章. 

 - 简历是通向面试的途径, 公司会收到大量简历, 你需要保证你的简历足够完美, 才能够赢得面试
 - 如果你觉得自己不够格, 不要应聘. 如果一份工作写明"暑期实习", 那就不要诉求一份全职工作
 - 注意标点及拼写! 只要是逗号, 后面一定要有一个空格. "I", 要大写!
 - 校对简历的每一个细节, 并且让别人帮你校对
 - 为要申请的工作单独写Cover letter. 
 
 更多建议, 请[阅读原文](https://www.joelonsoftware.com/2004/01/26/getting-your-resume-read/). 


### [**InfrastructureAsCode**](https://martinfowler.com/bliki/InfrastructureAsCode.html)

 使用代码定义机器/网络等基础设施. 具体实践:
  - 使用定义文件(Definition Files), 如:　Ansible playbooks, Vagrantfile
  - 自我表达的系统及流程 Self-documented systems and processes, 而不是文档里的指示步骤.
  - 为所有文件提供版本控制
  - 持续测试系统及流程, 使用Deployment Pipelines来对基础设施应用Continuous Delivery
  - 偏好小的改变, 基础设置变化越大, 风险越高, 问题也越不容易发现
  - 保持服务持续可用. 采用BlueGreenDeployment/ParallelChange等技术, 在保证服务可用的情况下, 快速发布小规模更新. 

 这些方法有很多好处, 譬如: 
  - 可以让我们快速启动新环境, 安全的销毁就环境
  - 保证所有环境都是一致的
  - 降低风险, 更安全的发布更新.


### (播客)[**Stack Exchange Engineering with Nick Craver**](https://scaleyourcode.com/interviews/interview/31)

Nick Craver是一名就职于Stack Exchange的工程师, 在工作中他扮演多重角色: developer, site reliability engineer, system administrator, database administrator, architect, network guy, data center guy，等等. 相信很多读者都读过他的博客, 例如:[Stack Overflow: How We Do Deployment](https://nickcraver.com/blog/2016/05/03/stack-overflow-how-we-do-deployment-2016-edition/)．

最近一期的ScaleYourCode采访了他, 感兴趣的读者可以从中听到他在Stack Overflow的工作经历:
> I told myself JavaScript and JQuery weren't well covered, so I "went nuts" on it and answered six thousand or so questions a year. That made Atwood take notice of what I was doing. I got hired and didn't know JavaScript whatsoever.

播客全长: 66分钟, 可通过[网页, iTunes, 以及Stitcher收听](https://scaleyourcode.com/interviews/interview/31). 也推荐阅读文字版, 大量干货.


### (英文/中文)[**ThoughtWorks发布新一期的技术雷达 Technology Radar Vol.16**](https://www.thoughtworks.com/radar)

本期亮点: 

 - The growing importance of Conversational UI.
 - Intelligence as a Service promises to deliver AI for all.
 - Why Developer Experience is becoming critical.
 - Rise of the Platforms.
 - The pervasiveness of Python.

新增加的"推荐"项目: 平台: `Linux Security Modules`, 工具: `fastlane`, 语言: `Python 3`, `ReactiveX`等. 

访问网页版/PDF:[thoughtworks.com/radar](https://www.thoughtworks.com/radar).  直达[简体中文PDF](https://assets.thoughtworks.com/assets/technology-radar-vol-16-cn.pdf)


 ### (英文/中文)[**SaaS型初创企业安全101 Security 101 for SaaS startups**](https://github.com/forter/security-101-for-saas-startups)
 
 这是一篇写给SaaS型初创企业的安全建议, 按照初创企业的成长阶段, 罗列了应该需要注意的安全事项. 本作品发布于Github, 值得一读. 
 
 - 英文原文: [Security 101 for SaaS startups](https://github.com/forter/security-101-for-saas-startups)
 - 中文翻译: [SaaS型初创企业安全101](https://github.com/forter/security-101-for-saas-startups/blob/chinese/readme.md)
