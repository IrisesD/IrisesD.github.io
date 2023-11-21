---
layout: post
title: Hackergame 2023 Writeup
date: 2023-11-20 17:00:00-0500
description: 记录参加Hackergame 2023的经历以及题解
tags: hackergame
categories: experience
giscus_comments: false
related_posts: true
related_publications: false
---
以前一直有听过Hackergame，但一直没参加。这次正好看到群友在讨论，便怀着好奇的心态点开，结果就一发不可收拾了。（确实有意思）
由于参加的时候人还在美国，所以上分时间和大家都错开了hhh。
在申请季一边干活、准备文书，一边抽时间打Hackergame的经历确实很难忘。
最终成绩也还是不错，总排名30，校内排名第6，勉强挤进了二等奖，作为一个第一次参加hg，以前也没有类似经历的新手来说感觉还不错。
下面是题解：

#### Hackergame 启动
签到题，首先打开界面

随便录制一段音频提交，发现url变成了：
```
https://cnhktrz3k5nc.hack-challenge.lug.ustc.edu.cn:13202/?similarity=
```
直接修改url为：
```
https://cnhktrz3k5nc.hack-challenge.lug.ustc.edu.cn:13202/?similarity=100
```
提交获取flag：
```
flag{W3!COme-T0-hackeR94Me-anD-3NJoY-H@CKIN9-Z0z3}
```

#### 猫咪小测

> 1. 想要借阅世界图书出版公司出版的《A Classical Introduction To Modern Number Theory 2nd ed.》
应当前往中国科学技术大学西区图书馆的哪一层？（30 分）

直接打开图书馆网站，检索馆藏分布

不难发现，外文书库在12楼，因此答案为`12`

> 2. 今年 arXiv 网站的天体物理版块上有人发表了一篇关于「可观测宇宙中的鸡的密度上限」的论文，请问论文中作者计算出的鸡密度函数的上限为 10 的多少次方每立方秒差距？（30 分）

Google搜索:宇宙中鸡的数量密度上限

在排名第一的[知乎回答](https://www.zhihu.com/question/20337132/answer/3023506910)中可以找到答案`23`

> 3. 为了支持 TCP BBR 拥塞控制算法，在编译 Linux 内核时应该配置好哪一条内核选项？

直接问一下ChatGPT就行，得到答案`CONFIG_TCP_CONG_BBR`

> 4. 🥒🥒🥒：「我……从没觉得写类型标注有意思过」。在一篇论文中，作者给出了能够让 Python 的类型检查器 MyPY mypy 陷入死循环的代码，并证明 Python 的类型检查和停机问题一样困难。请问这篇论文发表在今年的哪个学术会议上？（20 分）

Google搜索`MyPY Python type checking halt problem`，找到[论文](https://drops.dagstuhl.de/storage/00lipics/lipics-vol263-ecoop2023/LIPIcs.ECOOP.2023.44/LIPIcs.ECOOP.2023.44.pdf)，得到答案`ECOOP`

#### 更深更暗
打开题目界面，点击检查，即可找到flag

#### 旅行照片 3.0
我超，盒！
开盒题感觉还是很有意思的。

线索首先在拉面店的图片中，从图上的肩带可以看出，学长将要去参加STATPHYS28，这个是最大的突破口
Google搜索STATPHYS28，在官方主页中点击Banquet：
https://statphys28.org/banquet.html

可以找到题目1、5的信息，结合文字描述可以得到答案：
> 1、你还记得与学长见面这天是哪一天吗？（格式：yyyy-mm-dd）

```
2023-08-10
```

> 5、学长当天晚上需要在哪栋标志性建筑物的附近集合呢？（请用简体中文回答，四个汉字）

```
安田讲堂
```

之后看第二题：

> 2、在学校该展厅展示的所有同种金色奖牌的得主中，出生最晚者获奖时所在的研究所缩写是什么？

很明显是Nobel Prize奖章，搜索奖章上名字可以知道学校为东京大学，然后找最年轻的获奖者即可
https://en.wikipedia.org/wiki/Takaaki_Kajita
答案是`ICRR`

> 3、帐篷中活动招募志愿者时用于收集报名信息的在线问卷的编号（以字母 S 开头后接数字）是多少？

Googl搜索图片得到该地点为上野公园。搜索`上野公園 2023年8月10`

在网站中可以找到志愿者报名表格链接https://ws.formzu.net/dist/S495584522/
得到答案
```
S495584522
```

> 4、学长购买自己的博物馆门票时，花费了多少日元？

文字信息提到学长看到志愿者招募活动是在"马路对面"，首先打开google map搜索上野恩賜公園 噴水広場。

可知提到的博物馆为东京国立博物馆。稍加搜索可知，门票对大学生免费，学长是东京大学学生，因此答案为`0`.

> 6、进站时，你在 JR 上野站中央检票口外看到「ボタン＆カフリンクス」活动正在销售动物周边商品，该活动张贴的粉色背景海报上是什么动物（记作 A，两个汉字）？ 在出站处附近建筑的屋顶广告牌上，每小时都会顽皮出现的那只 3D 动物是什么品种？（记作 B，三个汉字）？（格式：A-B）

首先Google搜索`ボタン&カフリンクス jr 上野`，找到相关信息：https://plaza.rakuten.co.jp/ayumilife/diary/202308110000/。 得到A为熊猫。
接着搜索`3d動物廣告 JR`，得到B为秋田犬.
答案 `熊猫-秋田犬`

-- TO BE UPDATED