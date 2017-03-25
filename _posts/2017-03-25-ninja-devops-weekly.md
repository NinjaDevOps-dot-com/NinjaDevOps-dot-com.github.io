---
layout: post
title:  "DevOpsWeekly#18 Stack Overflow发布2017程序员调查结果; 如何成为一个更好的程序员? 正确的对用户密码进行加密; 配置管理是一种反模式"
date:   2017-03-25 15:00:00 +0800
categories: weekly
tags: devops
---

### [**Stack Overflow发布2017程序员调查结果**](http://stackoverflow.com/insights/survey/2017/)

超过6万4千名程序员参与了此次调查，有很多有趣的发现. 譬如: 有56.5%的受访者认为自己工资过低; 有13.1%的人表示他们在积极的找工作, 有75.2%的人表示他们会考虑新的工作机会. 
> Only 13.1% of developers are actively looking for a job. But 75.2% of developers are interested in hearing about new job opportunities.

90%的受访者表示他们是自学成才(Self-taught); 72.6%的受访者认为自己是Webdeveloper, 62.5%的受访者使用JavaScript, 有73.9%的SysAdmin/DevOps表示他们使用JavaScript.

详细的报告请阅读: [Developer Survey Results 2017](http://stackoverflow.com/insights/survey/2017/), 同时Stack Overflow也有一期关于调查结果的播客: [Podcast #105: The Wait is Over! Developer Survey 2017 results are in.](https://stackoverflow.blog/2017/03/22/podcast-105-wait-developer-survey-2017-results/)

  
### **如何成为一个更好的程序员**

关于这个话题, 小编要推荐两篇文章: 

 - [**How I Became a Better Programmer**](http://jlongster.com/How-I-Became-Better-Programmer)

    干货甚多, 翻译几条, 与君共勉:
  
    - 找到能激励你的人, 但不要盲从他们.
    - 即使你是新人, 也不要低估自己的工作.
    - 新技术层出不穷, 不要疲于奔命. 多数都是老调重弹, 革命性的创新并不是每年都有.
    - 忽略皮毛, 譬如新的语法, 新的library APIs, 配置build工具等等.
    - 深入了解以往的研究结果, 譬如阅读[Papers We Love GitHub repo](https://github.com/papers-we-love/papers-we-love).
    - 做点有挑战的事情. 譬如, 写一个compiler.

 - [**Turning Tech Hobbies into Side Hustle**](http://www.daedtech.com/turning-tech-hobbies-into-side-hustle/)
  
    四年前立下雄心壮志要学习某某语言, 结果到如今只是"从入门到放弃". 怎样高效的学习一门新技术? 找到动机 e.g. `help who and do what`. 找到潜在用户, 然后做成一个side hustle.

    文中提到的另一篇关于程序员修炼的文章: [Sharpening the Saw](https://blog.codinghorror.com/sharpening-the-saw/)
  

### [(中文) **如何正确对用户密码进行加密？**](http://www.infoq.com/cn/articles/how-to-encrypt-the-user-password-correctly)
    
还记得[2011年的CSDN密码泄露事件](http://www.csdn.net/article/2011-12-21/309505)么? 用户密码到底该以哪种形式存储? 像曾经的CSDN那样明文存储吗? 

一起来读一读InfoQ翻译的[如何正确对用户密码进行加密？](http://www.infoq.com/cn/articles/how-to-encrypt-the-user-password-correctly)
英文原文: [Salted Password Hashing - Doing it Right](https://crackstation.net/hashing-security.htm)


### [**配置管理是一种反模式 Configuration Management is an Antipattern**](https://hackernoon.com/configuration-management-is-an-antipattern-e677e34be64c#.swhue3t7y)

谁来负责维护Configuration? Ops? Dev? 总有那么几台机器因为各种原因而没有接收到最近的更新, 怎么办?　try/catch + monitoring tool? 

  > configuration management promises that you’ll know the complete state of your infrastructure, but it never works that way.

**解决方案 - immutable infrastructure**: 先build一个base image, 然后安装具体的app, build成为包含具体app的image. 然后部署这些image.

  > Your base image should have the latest security updates as well as any base infrastructure packages that are run platform-wide. Things like your monitoring packages, or your service discovery. Now, you could use a configuration management tool to build your base image, but you could also use OS packages and a little python to install and configure your base image.

  > Once you have that base image, you install your application and its dependencies on the base image using your standard package manager (like apt-get or yum). If you have your dependencies configured in your package correctly, this is basically one step.
    
  > You compile that into a new application specific image, push that to all your was regions, and viola! Immutable infrastructure!
