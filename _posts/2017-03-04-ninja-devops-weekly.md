---
layout: post
title:  "DevOpsWeekly#15 AWS S3故障分析, Uncle bob: TDD有损架构? Google开源Python命令行生成工具, 面试时HR问现在收入该怎么回答?"
date:   2017-03-04 13:00:00 +0800
categories: weekly
tags: devops
---


## [**AWS S3 故障分析: Summary of the Amazon S3 Service Disruption in the Northern Virginia (US-EAST-1) Region**](https://aws.amazon.com/cn/message/41926/)
  
  AWS的工程师在移除一部分billing prcoess用到的servers, 不小心输入了错误的指令, 导致很多服务器被移除. 更详细的报告可以点击标题看到(目前只有英文版), 酷壳陈皓老师也写了一篇博客: [AWS 的 S3 故障回顾和思考](http://coolshell.cn/articles/17737.html).


## [**Uncle Bob: TDD Harms Architecture**](http://blog.cleancoder.com/uncle-bob/2017/03/03/TDD-Harms-Architecture.html)

 TDD会对架构带来负面影响吗? 随着TestCase的不断增多, 修改一行production code可能会需要随着修改很多test, test越多, production code修改越麻烦. 小编的确也遇到过这样的系统. Uncle Bob的观点: 如果在设计的时候不考虑设计原则, 譬如Open-Closed, DependencyInversion等原则, 如果不把测试作为系统的一部分,`you will damage your design and architecture – TDD or no TDD.`
 文中引用了之前的一些讨论/视频, 有兴趣的读者可以仔细阅读. 


## [**Google开源Python命令行生成工具: Introducing Python Fire, a library for automatically generating command line interfaces**](http://developers.googleblog.com/2017/03/introducing-python-fire-library-for.html)

  Google开源了其自用的Python命令行生成工具, 举例:
  ```python
    import fire

    class Calculator(object):
    """A simple calculator class."""

    def double(self, number):
        return 2 * number

    if __name__ == '__main__':
        fire.Fire(Calculator)
  ```
  用法:
  ```bash
    python calculator.py double 10  # 20
    python calculator.py double --number=15  # 30
 ```

  在[NinjaDevOps Weekly 20161226](https://ninjadevops.com/weekly/2016/12/26/ninja-devops-weekly.html)小编曾提到过 [命令行神器 Click 简明笔记](https://funhacks.net/2016/12/20/click/), 有需要的读者也可以参考[Comparing Python Command-Line Parsing Libraries - Argparse, Docopt, and Click](https://realpython.com/blog/python/comparing-python-command-line-parsing-libraries-argparse-docopt-click/#conclusion)


## [**你确定吗?**](https://m.signalvnoise.com/are-you-sure-ae4ae0ef72a7#.ta5qnfmjq)

  如何设计人性化的软件? 不断弹出需要用户确认的信息:"你确定要进行**操作吗?"　Basecamp的Designer AdamStoddard认为:　如果操作可能会出现用户不想要的结果，那应该提供一个优雅的undo操作．`If you’re trying to make considerate software, don’t ask your user if they’re sure. Assume they’re competent humans who mean what they intend. If the action is potentially destructive, give them a way to gracefully recover if they change their mind (undo/redo, archive states, auto-save drafts, etc).`


## [**(中文)职场话题: HR 电面问现在月薪怎么办**](https://www.v2ex.com/t/341859)

  面试前/面试中, HR问现在的薪水时该怎么办? 其实小编每次也想问HR能出多少, 但是往往都是被HR套进去, 不知不觉就拖了自己的底. 这篇帖子是v2ex上网友们的讨论.


