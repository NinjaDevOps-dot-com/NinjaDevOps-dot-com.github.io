---
layout: post
title:  "DevOpsWeekly#17 神经网络训练是一种编程吗? 微软Flow, 免费的自动化服务; 如何完败你的写代码面试? 该选择哪种FeatureBranch工作方式? DNS原理入门"
date:   2017-03-18 14:00:00 +0800
categories: weekly
tags: devops
---

### [**Uncle Bob: 神经网络训练是一种编程吗?**](http://blog.cleancoder.com/uncle-bob/2017/03/16/DrCalvin.html)
  
  Uncle bob最近写了一篇博客回应[Grady Booch(UML设计者之一)](https://en.wikipedia.org/wiki/Grady_Booch)在twitter上的提问"How does the presence of neural nets impact the dev lifecycle?":
   训练神经网络是一种编程吗? 目前来说不是, 更像一种'黑科技', 它的背后可能有科学, 但这种科学还不是很严格. 
 
  > Is training a neural net programming? The answer to that, at least at the moment, is clearly “No”. Training neural nets is something of a black art. There may be a science behind it; but that science is not particularly rigorous yet.
  Training a neural net is nothing like programming. It is not the enumeration of transitions into a finite state machine. Rather, it is an attempt to find enough events to present to the neural network, and a corresponding attempt to measure how appropriately the neural net behaves. And it is that last measurement that is the most fraught with uncertainty and danger.

  Grady Booch最近在TED有过一次关于AI的演讲, 有兴趣的读者可以点此观看: [Don't fear superintelligent AI
](https://www.ted.com/talks/grady_booch_don_t_fear_superintelligence)


### [**Microsoft Flow: 免费的自动化服务**](https://flow.microsoft.com/en-us/pricing/)
  ```python
  if 超过10天没有写博客:
        发邮件给我, 提醒我写点什么.
  ```
  [如果我超过时间没更新博客, 请提醒我!](https://flow.microsoft.com/en-us/blog/fotw-remind-to-post/)
  如果你喜欢/需要类似的自动化服务, 你也许应该尝试IFFT/Zapier, 
  微软于2016年推出了Flow服务, 该服务类似于IFFT/Zapier,帮助用户自动化集成外部应用/服务. 譬如当设定的RSS有更新时, 自动发布到Twitter跟Facebook, 然后再call一个http服务, 之后再发邮件通知流程执行完毕等等. 

  免费配额: 750次运行/月. 


### [**如何完败你的写码面试 How NOT to succeed in your 45-minute coding interview**](https://dev.to/fahimulhaq/how-not-to-succeed-in-your-45-minute-coding-interview)
  
  本文列举了面试中的典型错误: 
  
  1. 花太多时间谈论目前正在做的工作/项目. 应该简洁直白的切中要点, 把握好面试中的时间. 在面试前, 考虑以下问题, 并给出一两句话的简短回答: 1. 你正在做什么项目? 2. 该项目中最挑战的部分? 3. 在过去6个月中你碰到的最难解决的bug? 
  2. 没了解清楚问题就下手. 譬如给你一个linked-list, 是要逆序, 还是要逆序打印? 
  3. 因为紧张, 没有想清楚解决方案就仓促的开始编码
  4. 试图随便先写一点代码到墙上. 应该花点时间把问题想清楚, 如果对方要一个O(1)的解决方案, 如果你做不到, 那基本上就是被拒.
  5. 你没有测试你的代码. 用一个例子来验证你的代码, 在对方指出问题之前发现问题. 
  **Bonus**: 问面试官你做的怎么样? 虽然这不会对结果造成影响, 但这回让你的面试官觉得尴尬(如果是要拒你的话?)

### [**FeatrureBranch: 该选择怎样的工作方式?**](https://martinfowler.com/bliki/FeatureBranch.html)
  
  2009年MartinFowler关于FeatureBranch的博客, 在使用Distributed Version Control Systems (DVCS)时, 该采取怎样的流程保证多人同时开发并减少merge的痛苦? 本文对比多种分支管理/合并方式, 结论:
  - 对于纪律严明的团队, 使用DVSC + CI
  - 对于稍微乱一些的团队, 恐怕DVSC会误导人们使用长生命周期的branch. 集中化的VCS并不鼓励branch, 会要求成员尽早的提交代码. 


### [**[中文]DNS原理入门**](http://www.ruanyifeng.com/blog/2016/06/dns.html)

  读读阮一峰老师的DNS原理入门, 通俗易懂. 
  

---
**插播广告**
如果您乐于贡献, 欢迎你每周抽出时间来为所有读者推荐富有营养的文章, 您可以通过以下方式推荐您的内容及点评:
 - 提交[gitbug issue](https://github.com/NinjaDevOps-dot-com/NinjaDevOps-dot-com.github.io/issues)
 - Email: info at ninjadevops.com
