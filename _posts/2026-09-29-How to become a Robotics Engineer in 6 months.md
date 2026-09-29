---
layout:     post
title:      "How to become a Robotics Engineer in 6 months (RESOURCES)"
subtitle:   "如何在六个月内成为一名机器人工程师（含资源）"
date:       2026-08-31 12:13
author:     "Paul Graham Author、Arvin 译 "
header-img: "img/in-post/bgimg/post-think-bg.jpg"
header-mask: 0.3
tags:
    - Learn
    - Robot
---

**推荐语**

最近 Microduck 爆火，除了其可爱的形态和动作招人爱之外，背后是 Hugging Face 为全球开发者提供了开发智能具身机器人的低门槛入口和平台。

然后看到 X 上 [Ronin](https://x.com/DeRonin_ "Twitter") 的这篇文章，觉得挺好，所以翻译分享给大家。

---

# How to become a Robotics Engineer in 6 months (RESOURCES)

Robotics is the least crowded high-value skill in tech right now  
机器人学是目前科技领域中最不拥挤的高价值技能

The problem is that almost nobody knows where to start, because the field looks like five fields stacked on top of each other  
问题在于，几乎没有人知道从哪里开始，因为这个领域看起来像是五个领域叠在一起

Some people start with a university robotics textbook and quit at the chapter on rotation matrices  
有些人从大学机器人教材开始，读到旋转矩阵那一章就放弃了

Some buy an Arduino kit, blink an LED, and never build the second thing  
有些人买了 Arduino 套件，点亮了 LED，就再也没有做第二件事

Some jump straight into ROS 2 tutorials without knowing what a PWM signal is, then wonder why nothing works on real hardware  
有些人直接跳进 ROS 2 教程，却不知道什么是 PWM 信号，然后纳闷为什么真实硬件上什么都跑不起来

Others go the opposite way and learn only machine learning, which means they can train a policy but cannot make a motor turn  
还有人走完全相反的路，只学机器学习，结果能训练策略，却连让电机转起来都做不到

The result is usually the same: months of scattered effort and no working robot to show anyone  
结果通常都一样：几个月零散努力，却没有任何可以展示给别人的能工作的机器人

If your goal is to become a robotics engineer, you do not need a mechanical engineering degree and you do not need to derive the dynamics of a seven-link arm by hand  
如果你的目标是成为一名机器人工程师，你不需要机械工程学位，也不需要亲手推导七连杆机械臂的动力学

You need to be able to make physical things do what you tell them to, reliably, and then prove it  
你需要的是能够让物理物体可靠地按你说的去做，然后证明这一点

**That means learning how to:**  
**这意味着要学会：**

- read a schematic, wire a circuit, and debug it with a multimeter  
  读原理图、接线、用万用表调试
- program a microcontroller to drive motors and read sensors in real time  
  编程微控制器实时驱动电机并读取传感器
- design and manufacture your own mechanical parts  
  设计和制造自己的机械零件
- build robots the way companies build them, in ROS 2, with simulation  
  像公司一样用 ROS 2 和仿真构建机器人
- close a control loop and know why it oscillates when it does  
  闭环控制，并知道为什么它会振荡
- teach a robot a task from demonstrations instead of hand-coding it  
  通过示范而不是手写代码教机器人完成任务
- ship a portfolio that survives three follow-up questions in an interview  
  做出能在面试中经受住三个追问的作品集

This guide is a **practical 6-month roadmap**, and it assumes you are starting from zero electronics knowledge  
这份指南是一份**实用的 6 个月路线图**，假设你从零电子知识起步

Every single section has resources, a focus list, and a practical task that leaves you with something real, because a robotics portfolio is made of things that moved, not courses you finished  
每一个部分都有资源、重点清单和能留下真实成果的实践任务，因为机器人作品集是由会动的东西组成的，而不是你完成了哪些课程

It also has hardware costs and where to order from, at three budget tiers, so you can follow this whether you are in San Francisco or somewhere AliExpress takes six weeks to reach  
它还包含硬件成本和订购渠道，分三个预算档次，所以无论你在旧金山还是阿里快递要六周才到的地方，都能跟着走

This one runs to nearly **12,000 words with over 100 linked resources and 27 practical projects**, so bookmark it and come back to it month by month rather than trying to read it in one sitting  
这篇文章将近**12000 字，包含超过 100 个链接资源和 27 个实践项目**，所以请收藏它，按月回来看，而不是试图一次读完

Every price and every link in here was checked against the vendor or the official docs in September 2026, and where the widely-quoted numbers did not survive checking I have said so instead of repeating them  
这里的每一个价格和每一个链接都在 2026 年 9 月对照供应商或官方文档核对过，如果广泛引用的数字经不起核对，我会直接说明，而不是重复它们

**Important!!!**  

While writing this article, I realized the most important skill is being able to explain hard technical things in simple words  
写这篇文章时，我意识到最重要的技能是能用简单的话解释困难的技术问题

So I created my personal YouTube channel where I am going to record videos about AI & Robotics engineering  
所以我创建了个人 YouTube 频道，准备录制关于 AI 与机器人工程的视频

If you really love my content on X and want to become Advanced in these two disciplines FOR FREE, then  
如果你真的喜欢我在 X 上的内容，并想**免费**在这两门学科上进阶，那么

Follow me:  

[https://www.youtube.com/@deronin_23](https://www.youtube.com/@deronin_23)

It would mean a lot to me. I want this to be genuinely useful, and to keep making more of the content that gets so much positive feedback on X ❤️  
这对我意义重大。我希望这些内容真正有用，并继续制作更多在 X 上获得大量正面反馈的内容 ❤️

**Now let's start reading the article ⬇️**  

## Why robotics and not AI engineering  
## 为什么选择机器人学而不是 AI 工程

Everyone in your timeline is an AI engineer now, and that is the whole problem  
你的时间线上现在人人都是 AI 工程师，这正是问题所在

You cannot build a moat out of what a subagent does at 3am for pennies  
你无法用一个子代理凌晨三点用几分钱做的事情来构建护城河

Robotics is the opposite, for reasons that are structural rather than fashionable:  
机器人学则完全相反，原因是结构性的而非时髦的：

- the models already work, what is missing is someone who can put them in a body  
  模型已经能工作，缺的是能把它们装进身体的人
- you cannot scrape the physical world, someone has to move a real machine to create the data  
  你无法爬取物理世界，必须有人去移动真实机器才能产生数据
- there is no Stack Overflow answer for why your gripper keeps slipping  
  没有 Stack Overflow 能回答为什么你的夹爪一直打滑
- a robot falling over is not a problem you can hand to a subagent  
  机器人摔倒不是你可以扔给子代理的问题
- nobody clones your robot over a weekend  
  没人能在一个周末克隆你的机器人

AI engineering is crowded and robotics is empty  
AI 工程拥挤，机器人学空旷

## What a robotics engineer actually does  
## 机器人工程师实际在做什么

A lot of people hear "robotics engineer" and imagine someone designing a humanoid from scratch  
很多人听到“机器人工程师”就想象有人从零设计人形机器人

In reality the job splits into specialisms, and you pick one and stay literate in the rest:  
实际上工作会分成多个专长，你选一个深入，同时对其余保持了解：

- perception and computer vision  
  感知与计算机视觉
- controls and state estimation  
  控制与状态估计
- motion planning and manipulation  
  运动规划与操作
- robot learning  
  机器人学习
- embedded and firmware  
  嵌入式与固件
- simulation  
  仿真
- systems and integration  
  系统与集成
- deployment and operations  
  部署与运维

I read live job listings from Figure and Skild, and the same four requirements appear in every single one:  
我阅读了 Figure 和 Skild 的实时招聘信息，每一条都出现相同的四个要求：

- C++ and Python, both, not one or the other  
  C++ 和 Python，两者都要，不是二选一
- experience on real hardware, since simulation-only does not qualify you as senior  
  真实硬件经验，因为仅有仿真无法成为资深
- depth in one specialism and literacy across the rest  
  在一个专长上有深度，并对其余保持素养
- debugging named as a skill in its own right  
  调试被单独列为一项技能

Notice what is not on that list: a specific degree  
注意列表上没有的东西：特定学位

That is why this roadmap is built around making things work rather than studying theory, and why every section below ends with something you have to build  
这就是为什么这份路线图围绕“让东西真正工作”而不是“学理论”构建，也是为什么下面每个部分都以你必须动手做的东西结尾

Keep whatever is paying you while you do it, treat this as two or three hours a day, and the six months are designed to be run that way  
一边保留现有收入，一边每天投入两三个小时，六个月就是按这个节奏设计的

⏩---------------------------------------------------------------------⏪

## Month 1: Electronics, the bench, and the tools you build everything with  
## 第 1 个月：电子学、工作台，以及你用来构建一切的工具

Your goal this month: be able to read a schematic, build a circuit that works, and find the fault when it does not  
本月目标：能读懂原理图，搭建能工作的电路，并在出故障时找到问题

Almost every roadmap skips this and starts at Arduino, which is why so many people can copy a wiring diagram but cannot fix anything when it breaks  
几乎所有路线图都跳过这部分直接从 Arduino 开始，所以很多人对着接线图能抄，但一坏就修不了

Robotics is the one software field where the bug is sometimes a loose wire, a sagging battery or a motor drawing more current than your regulator can supply, and you will never diagnose those if you do not understand the electrical layer underneath  
机器人学是唯一一个软件领域，bug 有时可能是松动的线、电压下降的电池，或者电机电流超过稳压器能力，如果你不理解底层电气层，就永远无法诊断这些问题

### What to learn  
### 要学什么

### 1. Electronics fundamentals  
### 1. 电子学基础

You need Ohm's law, voltage dividers, what a capacitor does, how a transistor switches, and how to read a schematic  
你需要欧姆定律、分压器、电容的作用、晶体管如何开关，以及如何读原理图

You do not need to design an op-amp from first principles  
你不需要从第一性原理设计运放

**How to learn it:**  
**如何学习：**

Start in a simulator before you spend a single dollar, because you can wire things wrong at zero cost and actually see why they failed  
先从仿真器开始，一分钱都不用花，因为你可以零成本接错线，并真正看到为什么失败

The most common beginner mistake is watching hours of video without ever building the circuit, so build every example as you go, even in the simulator  
初学者最常见的错误是看几个小时视频却从不搭建电路，所以边学边搭每一个例子，哪怕是在仿真器里

**Resources:**  

**1. Falstad Circuit Simulator (free, in-browser)**  

Link:  
[https://www.falstad.com/circuit/](https://www.falstad.com/circuit/)

Animated electron flow and live voltage colouring, so you actually watch current move instead of imagining it, which is the fastest way to build intuition  
动画电子流和实时电压着色，让你真正看到电流流动而不是靠想象，这是建立直觉最快的方式

**2. Tinkercad Circuits (Autodesk, free with account)**  

Link:  
[https://www.tinkercad.com/circuits](https://www.tinkercad.com/circuits)

The only simulator that gives you a virtual breadboard, a virtual Arduino and a virtual multimeter together, so it catches your wiring mistakes before you own any parts  
唯一同时提供虚拟面包板、虚拟 Arduino 和虚拟万用表的仿真器，能在你拥有任何零件之前就抓住你的接线错误

**3. All About Circuits, "Lessons in Electric Circuits" (free)**  

Link:  
[https://www.allaboutcircuits.com/textbook/](https://www.allaboutcircuits.com/textbook/)

A complete open-licensed EE textbook in six volumes, and this is your reference when a video hand-waves something you need to actually understand  
六卷完整开源许可的电子工程教材，当视频含糊带过你需要真正理解的内容时，它就是你的参考书

**4. Afrotechmods Tutorials (free)**  

Link:  
[https://afrotechmods.com/tutorials/](https://afrotechmods.com/tutorials/)

Short, fast, funny videos sorted into beginner, intermediate and advanced, and the right choice if you bounce off lecture-format teaching  
短小、快速、有趣的视频，按初级、中级、高级分类，如果你不喜欢讲座式教学，这是正确选择

**5. Make: Electronics, 3rd edition, Charles Platt ($29.99)**  

Link:  
[https://www.makershed.com/products/make-electronics-3rd-edition-print](https://www.makershed.com/products/make-electronics-3rd-edition-print)

The best single paper book for someone who has never held a multimeter, built around deliberately destroying components to learn their limits  
对从未拿过万用表的人来说最好的纸质书，围绕故意毁坏元件来学习其极限而构建

**What to focus on:**  

- Ohm's law and voltage dividers until they are automatic  
  欧姆定律和分压器，直到它们变成本能
- Current draw, and why a motor stalling browns out your microcontroller  
  电流消耗，以及为什么电机堵转会让微控制器电压下降
- Reading a schematic, including the symbols you will meet constantly: resistor, capacitor, diode, transistor, ground, Vcc  
  读原理图，包括你经常会遇到的符号：电阻、电容、二极管、晶体管、地、Vcc
- Pull-up and pull-down resistors, because you will use them every week  
  上拉和下拉电阻，因为你每周都会用到
- What a decoupling capacitor is and why every IC needs one  
  什么是去耦电容，以及为什么每个 IC 都需要一个
- Battery chemistry basics: LiPo cell counts, C ratings, and why you never leave a LiPo charging unattended  
  电池化学基础：LiPo 电芯数量、C 倍率，以及为什么永远不要让 LiPo 充电时无人看管

**Practice task:** build a voltage divider in Falstad, calculate the output voltage by hand, then confirm it in the simulator. Then build a transistor switch that turns an LED on from a logic-level input, since that is the exact circuit that will later let a 3.3V microcontroller pin control something that needs more current than the pin can supply  
**实践任务：** 在 Falstad 中搭建分压器，用手算出输出电压，再在仿真器中确认。然后搭建一个晶体管开关，用逻辑电平输入点亮 LED，因为这正是后续让 3.3V 微控制器引脚控制需要更大电流器件的电路

### 2. The bench, the tools, and what everything costs  
### 2. 工作台、工具以及所有东西的成本

This is the section that decides whether you actually start, so here is the honest budget  
这是决定你是否真正开始的部分，所以给出诚实的预算

**Tier 0, $ 0**Falstad, Tinkercad and All About Circuits, so that you learn Ohm's law and dividers before spending anything. Genuinely do this first  
**0 档，$0** Falstad、Tinkercad 和 All About Circuits，先学会欧姆定律和分压器再花任何钱。真的先做这个

**Tier 1, roughly $45 to $60.** A starter kit and a multimeter. Every kit below is solderless, so you need no iron yet  
**1 档，大约 $45 到 $60。** 入门套件和万用表。下面所有套件都是免焊的，所以暂时不需要烙铁

**Tier 2, roughly $110 to $160.** Add a soldering iron, solder, side cutters, wire strippers, helping hands, perfboard and extra passives  
**2 档，大约 $110 到 $160。** 增加烙铁、焊锡、斜口钳、剥线钳、辅助夹、万用板和额外无源元件

**Tier 3, roughly $200 to $300.** Add a bench power supply, better meter, desoldering pump, storage drawers and a robot chassis kit  
**3 档，大约 $200 到 $300。** 增加台式电源、更好的万用表、吸锡器、收纳抽屉和机器人底盘套件

**Verified kit prices, September 2026:**  
**已核实套件价格（2026 年 9 月）：**

**1. Elegoo UNO R3 Super Starter Kit ($42.99)**

Link:  
[https://www.elegoo.com/products/elegoo-uno-r3-super-starter-kit](https://www.elegoo.com/products/elegoo-uno-r3-super-starter-kit)

The best value pick and the kit most beginner courses target, with a pre-soldered LCD, power module and a 22-lesson PDF  
性价比最高的选择，也是大多数入门课程针对的套件，带预焊 LCD、电源模块和 22 课 PDF

**2. Elegoo UNO Basic Starter Kit ($19.99)**

Link:  
[https://www.elegoo.com/products/elegoo-uno-basic-starter-kit](https://www.elegoo.com/products/elegoo-uno-basic-starter-kit)

The cheapest real entry point if money is genuinely tight, with an Uno clone and basic passives  
如果钱真的很紧，这是最便宜的真实入门点，带 Uno 克隆板和基础无源元件

**3. SparkFun Inventor's Kit v4.1.2 ($99.95)**  

Link:  
[https://www.sparkfun.com/sparkfun-inventor-s-kit-v4-1-2.html](https://www.sparkfun.com/sparkfun-inventor-s-kit-v4-1-2.html)

The best curriculum of any kit, 16 circuits across 5 projects ending in a working robot, and the free guide is readable even if you buy a cheaper kit  
所有套件中最好的课程，16 个电路跨越 5 个项目，最终做出能工作的机器人，即使买更便宜的套件，免费指南也很好读

**4. Adafruit digital multimeter 9205B+ ($17.50)**  
**4. Adafruit 数字万用表 9205B+（$17.50）**

Link:  
[https://www.adafruit.com/product/2034](https://www.adafruit.com/product/2034)

Volts, current to 20A, continuity, resistance and capacitance, which is everything you need for years  
电压、电流到 20A、通断、电阻和电容，这是你未来几年需要的一切

**5. Pinecil V2 soldering iron ($25.99 community, $35.99 retail)**  
**5. Pinecil V2 烙铁（社区价 $25.99，零售 $35.99）**

Link:  
[https://pine64.com/product/pinecil-smart-mini-portable-soldering-iron/](https://pine64.com/product/pinecil-smart-mini-portable-soldering-iron/)

A real temperature-controlled iron for the price of a toy one, USB-C powered, takes standard TS100 and Hakko T12 tips  
真正的温控烙铁，价格却只相当于玩具级，USB-C 供电，兼容标准 TS100 和 Hakko T12 烙铁头

**Where to order, and the honest guidance:**  
**订购渠道，以及诚实建议：**

- **AliExpress** is cheapest by a wide margin, often 3 to 10 times less, but shipping runs 2 to 6 weeks and there is no support when a board arrives dead  
  **阿里国际站**便宜得多，经常便宜 3 到 10 倍，但运费 2 到 6 周，板子到了是坏的也没售后
- **Amazon** is mid-priced and fast, and the right place for your first kit  
  **亚马逊**中等价格且快，是买第一个套件的正确地方
- **Elegoo direct** ships from regional warehouses in about a week  
  **Elegoo 官网**从区域仓库发货，大约一周
- **Adafruit** and **SparkFun** cost more and are worth it early, because every product page links a full tutorial and their support is real  
  **Adafruit** 和 **SparkFun** 更贵，但早期值得，因为每个产品页都链接完整教程，售后是真的
- **Seeed Studio** and **DFRobot** ship worldwide from China at low-to-mid prices  
  **Seeed Studio** 和 **DFRobot** 从中国发全球，价格中低
- **DigiKey** and **Mouser** are for exact parts by specification with genuine datasheets, not for kits  
  **DigiKey** 和 **Mouser** 是按规格买精确零件并提供真数据手册的地方，不是买套件
- **Pololu** ships internationally and is the best source for motors and drivers  
  **Pololu** 国际发货，是电机和驱动器最好的来源

For your first order, pay the premium and buy from Amazon or Elegoo direct so you are building within days instead of sulking for a month. Once you know what a 10k resistor is for, order everything from AliExpress  
第一次订购，多花点钱从亚马逊或 Elegoo 官网买，这样几天内就能开始做，而不是生闷气等一个月。等你知道 10k 电阻是干什么的之后，再从阿里国际站订所有东西

**Practice task:** buy a kit and a multimeter, then measure things. Measure the voltage of a battery, the resistance of five random resistors and check them against the colour bands, then use continuity mode to find a deliberately broken wire you make yourself. This sounds trivial and it is the single skill that will save you the most hours over the next six months  
**实践任务：** 买一套件和万用表，然后去测量。测电池电压、五个随机电阻的阻值并对照色环检查，再用通断档找一根你故意弄断的线。这听起来微不足道，却是未来六个月最能帮你节省时间的单一技能

### 3. Soldering  
### 3. 焊接

At some point a jumper wire will not be good enough, and a robot that shakes itself apart mid-demo is not a portfolio piece  
总有一天跳线不够用，而演示中自己抖散的机器人不是作品集

**Resources:**  

**1. Adafruit Guide to Excellent Soldering (free)**  
**1. Adafruit 优秀焊接指南（免费）**

Link:  
[https://learn.adafruit.com/adafruit-guide-excellent-soldering](https://learn.adafruit.com/adafruit-guide-excellent-soldering)

Iron selection, joint technique, photographs of every common failure, and safety, and it is the reference everyone in the industry points to  
烙铁选择、焊点技巧、每种常见失败的照片，以及安全，这是行业内所有人指向的参考

**2. SparkFun: How to Use a Multimeter (free)**  
**2. SparkFun：如何使用万用表（免费）**

Link:  
[https://learn.sparkfun.com/tutorials/how-to-use-a-multimeter](https://learn.sparkfun.com/tutorials/how-to-use-a-multimeter)

Voltage, resistance, current and continuity explained properly, including what to do when you blow the fuse, which you will  
正确解释电压、电阻、电流和通断，包括当你烧断保险丝时该怎么办（你会烧断的）

**What to focus on:**  

- Tinning the tip and keeping it clean  
  给烙铁头镀锡并保持清洁
- Heating the joint, not the solder  
  加热焊点，而不是焊锡
- Recognising a cold joint by sight  
  用肉眼识别虚焊
- Through-hole first, surface-mount much later  
  先通孔，贴片很久以后再说
- Using flux, which fixes most problems beginners blame on the iron  
  使用助焊剂，它能解决大多数初学者怪到烙铁头上的问题

**Practice task:** solder header pins onto a cheap breakout board, then test every pin with continuity mode, and do the whole thing three times. Then desolder one and resolder it, because removing components badly is how most beginners destroy boards  
**实践任务：** 给便宜的扩展板焊排针，然后用通断档测试每一个引脚，整件事做三遍。然后拆下一个再重焊，因为拆件拆得差是大多数初学者毁掉板子的原因

### 4. Python, the terminal and Git  

You will use all three every single week from here to month six, so get them out of the way now  
从这里到第 6 个月，你每周都会用到这三样，所以现在先解决它们

**Resources:**  

**1. CS50P: Introduction to Programming with Python (Harvard, free)**  
**1. CS50P：Python 编程导论（哈佛，免费）**

Link:  
[https://cs50.harvard.edu/python/](https://cs50.harvard.edu/python/)

More rigorous than most beginner courses, with problem sets and a final project, and the structure is what makes people finish it  
比大多数入门课程更严谨，有习题集和最终项目，正是这种结构让人能坚持完成

**2. Python for Everybody (Coursera, free to audit)**  

Link:  
[https://www.coursera.org/specializations/python](https://www.coursera.org/specializations/python)

The gentlest starting point if CS50P feels too steep, taught by one of the most beginner-friendly instructors online  
如果 CS50P 感觉太陡，这是最温和的起点，由网上最对初学者友好的讲师之一授课

**3. The Missing Semester of Your CS Education (MIT, free)**  
**3. The Missing Semester of Your CS Education（MIT，免费）**

Link:  
[https://missing.csail.mit.edu/](https://missing.csail.mit.edu/)

Shell, scripting, and the command-line fluency that university courses skip, and robotics runs on the command line  
Shell、脚本，以及大学课程跳过的命令行熟练度，而机器人学就运行在命令行上

**4. Learn Git Branching (free, interactive)**  

Link:  
[https://learngitbranching.js.org/](https://learngitbranching.js.org/)

The best visual tool for understanding branches and merges, which is the part of Git that confuses everyone  
理解分支和合并最好的可视化工具，这正是 Git 让所有人困惑的部分

**What to focus on:**  

- Python: functions, classes, file I/O, JSON, virtual environments, pip  
  Python：函数、类、文件 I/O、JSON、虚拟环境、pip
- Terminal: cd, ls, grep, running scripts, environment variables, ssh  
  终端：cd、ls、grep、运行脚本、环境变量、ssh
- Git: init, add, commit, push, branches, and writing a README someone can follow  
  Git：init、add、commit、push、分支，以及写出别人能跟着做的 README

**Practice task:** from today, every project you build lives in a GitHub repo with a README that has a photo, a wiring description and a one-paragraph explanation of what broke and how you fixed it. That last part is what makes a repo look like engineering instead of a tutorial  
**实践任务：** 从今天起，你做的每个项目都放在 GitHub 仓库里，README 要有照片、接线描述，以及一段解释“什么坏了、你怎么修的”。最后这部分才是让仓库看起来像工程而不是教程的关键

### Month 1 Milestone  

By the end of this month you should be able to:  
到本月末你应该能够：

- Read a schematic and build the circuit it describes on a breadboard  
  读懂原理图并在面包板上搭建它所描述的电路
- Calculate whether a resistor value is right before you plug it in  
  在插入之前就能算出电阻值是否合适
- Find a short, a break or a dead component with a multimeter  
  用万用表找到短路、断路或损坏的元件
- Solder a clean through-hole joint and check it electrically  
  焊出一个干净的通孔焊点并用电学方法检查
- Write a Python script, run it from the terminal, and push it to GitHub  
  写一个 Python 脚本，从终端运行并推送到 GitHub
- Explain out loud why a motor stalling can reset your microcontroller  
  能口头解释为什么电机堵转会让微控制器复位

⏩---------------------------------------------------------------------⏪

## Month 2: Microcontrollers, motors and sensors, and your first moving robot  
## 第 2 个月：微控制器、电机和传感器，以及你的第一个会动的机器人

Your goal this month: build a robot that moves, senses its environment, and corrects itself  
本月目标：做出一个能移动、能感知环境并能自我纠正的机器人

This is the month robotics stops being theory, and it is also the month where most of the fundamental skills of the whole field first appear in miniature  
这个月机器人学不再是理论，也是整个领域大多数基本技能首次以微型形式出现的月份

A line-following robot is a closed control loop with sensor input, actuator output and a tuning problem, which is exactly what a humanoid is, only smaller and cheaper to break  
循线机器人就是一个有传感器输入、执行器输出和调参问题的闭环控制，这正是人形机器人的本质，只是更小、更便宜、更容易坏

### What to learn  

### 1. Arduino  

Start on Arduino rather than ESP32, because the ecosystem is enormous and every tutorial in existence targets it  
先从 Arduino 开始而不是 ESP32，因为生态系统巨大，现有所有教程都针对它

You will move to ESP32 within weeks, and nothing you learn here is wasted  
几周内你就会转到 ESP32，这里学的东西一点都不会浪费

**Resources:**  

**1. Paul McWhorter, Arduino Lessons (free)**  
**1. Paul McWhorter，Arduino 课程（免费）**

Link:  
[https://toptechboy.com/arduino-lessons/](https://toptechboy.com/arduino-lessons/)

Over 100 lessons taught slowly with homework at the end of each one, and the single best fit for a true beginner who has failed at Arduino before  
超过 100 课，讲得慢，每课末尾有作业，对之前失败过的真初学者来说是最佳选择

**2. Arduino Built-in Examples (official, free)**  

Link:  
[https://docs.arduino.cc/built-in-examples/](https://docs.arduino.cc/built-in-examples/)

Runnable sketches already inside your IDE, which is the fastest route from "installed" to "something moved"  
IDE 里已经有可运行的 sketch，是从“安装完成”到“有东西动起来”最快的路径

**3. Arduino Official Docs, Learn section (official, free)**  

Link:  
[https://docs.arduino.cc/learn/](https://docs.arduino.cc/learn/)

The authoritative reference for digital and analog IO, PWM, I2C, SPI and UART, best used as lookup rather than as a course  
数字与模拟 IO、PWM、I2C、SPI 和 UART 的权威参考，最好当查阅手册而不是当课程用

**4. Arduino Project Hub (free)**  

Link:  
[https://projecthub.arduino.cc/](https://projecthub.arduino.cc/)

Over 6,000 projects with wiring and code, and this is where you go when tutorials end and you need something to build  
超过 6000 个带接线和代码的项目，教程结束后你需要东西可做时就来这里

**What to focus on:**  

- digitalWrite, digitalRead, analogRead and analogWrite, and what PWM actually is  
  digitalWrite、digitalRead、analogRead 和 analogWrite，以及 PWM 到底是什么
- Interrupts, and why polling a button in a loop eventually fails you  
  中断，以及为什么在循环里轮询按钮最终会失败
- I2C and SPI: how to wire them and how to read a sensor datasheet to find the address  
  I2C 和 SPI：如何接线，以及如何读传感器数据手册找到地址
- Serial debugging, which will be your primary tool for months  
  串口调试，这将是你未来几个月的主要工具
- Non-blocking timing with millis() instead of delay(), because delay() will ruin every robot you build  
  用 millis() 做非阻塞计时而不是 delay()，因为 delay() 会毁掉你做的每一个机器人

**Practice task:** build a reaction-timer game. An LED fires after a random delay, a button stops the clock, and the time in milliseconds prints to serial. It uses interrupts, debouncing and non-blocking timing, and it has a score, which makes it demonstrable in fifteen seconds of video  
**实践任务：** 做一个反应时间游戏。LED 在随机延迟后亮起，按钮停止计时，毫秒时间打印到串口。它使用中断、防抖和非阻塞计时，还有分数，十五秒视频就能演示

### 2. ESP32  

The ESP32 is where you go the moment you want WiFi, Bluetooth, more processing power or two cores, and it is cheaper than an Arduino Uno  
一旦你想要 WiFi、蓝牙、更强处理能力或双核，就该上 ESP32，而且它比 Arduino Uno 还便宜

Buy an **ESP32-S3** as your main board, which is the most capable current variant, and one classic ESP32 so that older tutorial code runs unmodified  
买一块 **ESP32-S3** 作为主控板（当前最强变体），再买一块经典 ESP32，这样旧教程代码可以不改直接跑

**Resources:**  

**1. Random Nerd Tutorials, Getting Started with ESP32 (free)**  

Link:  
[https://randomnerdtutorials.com/getting-started-with-esp32/](https://randomnerdtutorials.com/getting-started-with-esp32/)

The highest-signal free tutorial library anywhere for this chip, with a specific fix for nearly every beginner failure mode, and a 250+ project index alongside it  
这个芯片上信号最高的免费教程库，几乎对每种初学者失败模式都有具体修复方法，旁边还有 250+ 项目索引

**2. ESP-IDF Programming Guide (Espressif official, free)**  

Link:  
[https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html](https://docs.espressif.com/projects/esp-idf/en/stable/esp32/get-started/index.html)

The only source of truth once you outgrow the Arduino layer, covering the real toolchain, menuconfig and the build system  
一旦你超出 Arduino 层，这是唯一真相来源，涵盖真正的工具链、menuconfig 和构建系统

**3. Arduino ESP32 Core documentation (Espressif official, free)**  

Link:  
[https://docs.espressif.com/projects/arduino-esp32/en/latest/](https://docs.espressif.com/projects/arduino-esp32/en/latest/)

Espressif's own docs for the Arduino layer, and the bridge that makes "Arduino versus ESP-IDF" a spectrum rather than a fork in the road  
乐鑫自己对 Arduino 层的文档，也是让“Arduino 对 ESP-IDF”变成连续光谱而不是分叉路口的桥梁

**4. DroneBot Workshop ESP32 hub (free)**  

Link:  
[https://dronebotworkshop.com/esp32-2/](https://dronebotworkshop.com/esp32-2/)

Long-form, wiring-diagram-heavy tutorials with written articles mirroring every video, covering ESP-NOW, OTA updates and low-power modes  
长篇、接线示意图丰富的教程，每段视频都有对应文字文章，涵盖 ESP-NOW、OTA 更新和低功耗模式

**Board prices, verified:**  

- ESP32-S3-DevKitC-1, 8MB flash, **$15.95** at Adafruit  
  ESP32-S3-DevKitC-1，8MB flash，Adafruit **$15.95**  
  Link: [https://www.adafruit.com/product/5312](https://www.adafruit.com/product/5312)
- Classic ESP32 Dev Board, **$15.00** at Adafruit  
  经典 ESP32 开发板，Adafruit **$15.00**  
  Link: [https://www.adafruit.com/product/3269](https://www.adafruit.com/product/3269)
- Seeed XIAO ESP32-C3, **$4.99**, for when you need something tiny  
  Seeed XIAO ESP32-C3，**$4.99**，需要小巧时用  
  Link: [https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html](https://www.seeedstudio.com/Seeed-XIAO-ESP32C3-p-5431.html)
- Generic ESP32 clones on AliExpress run roughly $4 to $9, which is unverified but is the well-known street range  
  阿里国际站上的通用 ESP32 克隆大约 $4 到 $9，未核实但是众所周知的市场价格区间

**Decision framework:**  
**决策框架：**

- **Arduino framework** for speed to a working robot, with the largest library ecosystem  
  **Arduino 框架**：最快做出能工作的机器人，库生态最大
- **ESP-IDF** when you need real control over tasks, cores, power and timing  
  **ESP-IDF**：需要真正控制任务、核心、电源和时序时
- **MicroPython** for fast sensor experimentation, but not for a balancing loop, since garbage collection pauses will wreck your timing  
  **MicroPython**：快速做传感器实验，但不适合平衡环，因为垃圾回收暂停会毁掉你的时序

**Practice task:** build something that could not exist on an Arduino Uno. Serve a web page from the ESP32 that shows live sensor readings and has buttons that drive a servo, then access it from your phone on the same network. This teaches WiFi, HTTP handling and asynchronous work at the same time  
**实践任务：** 做一件 Arduino Uno 上不可能存在的东西。让 ESP32 提供一个网页，显示实时传感器读数，并有按钮驱动舵机，然后从同一网络的手机访问。这同时教你 WiFi、HTTP 处理和异步工作

### 3. Motors, drivers and actuation  
### 3. 电机、驱动器和执行

This is where electronics stops being abstract, because motors draw real current and behave badly  
这里电子学不再抽象，因为电机真正耗电流，而且行为很差

Four types matter, and you should understand all four by the end of the month  
有四种重要类型，到月底你应该全部理解

**Brushed DC gearmotor**: cheap, needs an H-bridge, and has no position feedback unless you add an encoder. The default for a first rover  
**有刷直流减速电机**：便宜，需要 H 桥，没有位置反馈除非加编码器。第一台小车的默认选择

**Hobby servo**: an internal closed loop with roughly 180 degrees of travel and no feedback out  
**舵机**：内部闭环，大约 180 度行程，没有向外反馈

**Smart serial bus servo**: daisy-chained, with position, velocity and current feedback and a 12-bit magnetic encoder. This is what modern low-cost arms use  
**智能串行总线舵机**：可菊花链，带位置、速度和电流反馈以及 12 位磁编码器。现代低成本机械臂用的就是它

**Stepper**: open-loop absolute positioning with high holding torque  
**步进电机**：开环绝对定位，保持力矩大

**Resources:**  

**1. DroneBot Workshop, Controlling DC Motors with the L298N (free)**  
**1. DroneBot Workshop，用 L298N 控制直流电机（免费）**

Link:  
[https://dronebotworkshop.com/dc-motors-l298n-h-bridge/](https://dronebotworkshop.com/dc-motors-l298n-h-bridge/)

DC motor theory, PWM, H-bridge internals and three complete sketches, ending in a joystick-driven robot car  
直流电机理论、PWM、H 桥内部结构和三个完整 sketch，最终做出摇杆控制的小车

**2. SparkFun TB6612FNG Hookup Guide (free)**  
**2. SparkFun TB6612FNG 接线指南（免费）**

Link:  
[https://learn.sparkfun.com/tutorials/tb6612fng-hookup-guide/all](https://learn.sparkfun.com/tutorials/tb6612fng-hookup-guide/all)

Pinout, wiring and library for the driver you should actually use, with the reasoning for why  
你真正应该用的驱动器的引脚定义、接线和库，以及为什么要用它的理由

**3. DroneBot Workshop, Stepper Motors with Arduino (free)**  
**3. DroneBot Workshop，Arduino 步进电机（免费）**

Link:  
[https://dronebotworkshop.com/stepper-motors-with-arduino/](https://dronebotworkshop.com/stepper-motors-with-arduino/)

Unipolar versus bipolar, microstepping, NEMA sizing, and four demos across three different drivers  
单极 vs 双极、微步进、NEMA 尺寸，以及三种不同驱动器上的四个演示

**4. SimpleFOC documentation (open source, free)**  

Link:  
[https://docs.simplefoc.com/](https://docs.simplefoc.com/)

The clearest free explanation of field-oriented control anywhere, and the affordable on-ramp to brushless motors when you get there  
任何地方对磁场定向控制最清晰的免费解释，也是你将来进入无刷电机时最平价的入口

**Hardware, verified prices:**  

- Adafruit DRV8833 motor driver, **$5.95**, the cheapest good driver on the list  
  Adafruit DRV8833 电机驱动，**$5.95**，列表上最便宜的好驱动  
  Link: [https://www.adafruit.com/product/3297](https://www.adafruit.com/product/3297)
- SparkFun TB6612FNG breakout, **$14.77**, the correct default replacement for the L298N  
  SparkFun TB6612FNG 扩展板，**$14.77**，L298N 的正确默认替代品  
  Link: [https://www.sparkfun.com/sparkfun-motor-driver-dual-tb6612fng-1a.html](https://www.sparkfun.com/sparkfun-motor-driver-dual-tb6612fng-1a.html)
- Pololu gearmotor with encoder assembly, **$19.95 each**, with the encoder wiring already solved  
  Pololu 带编码器的减速电机组件，**每个 $19.95**，编码器接线已经解决  
  Link: [https://www.pololu.com/product/3675](https://www.pololu.com/product/3675)
- Pololu A4988 stepper driver carrier, **$8.95**  
  Pololu A4988 步进驱动载板，**$8.95**  
  Link: [https://www.pololu.com/product/1182](https://www.pololu.com/product/1182)
- FeeTech STS3215 smart servo, 12V, 30 kg·cm, **$31.71** at RobotShop, which is the servo used in the open-source SO-101 arm  
  FeeTech STS3215 智能舵机，12V，30 kg·cm，RobotShop **$31.71**，开源 SO-101 机械臂用的就是它  
  Link: [https://www.robotshop.com/products/feetech-12v-30kgcm-magnetic-encoding-servo-sts3215](https://www.robotshop.com/products/feetech-12v-30kgcm-magnetic-encoding-servo-sts3215)

**What to memorize:** the L298N is in every tutorial and you should not use it. It is an obsolete bipolar-transistor H-bridge that drops about 2V across its output stage, gets hot and wastes your battery. Learn it because the tutorials use it, then switch to the TB6612FNG or DRV8833  
**要记住的：** L298N 出现在每个教程里，但你不应该用它。它是过时的双极晶体管 H 桥，输出级压降约 2V，会发热并浪费电池。先学会它因为教程用它，然后换成 TB6612FNG 或 DRV8833

**Practice task:** drive one DC motor forward and backward at five different speeds using PWM, then add an encoder and write a function that turns the wheel exactly one full revolution regardless of battery voltage. The second half is your first real closed loop, and it is much harder than it sounds  
**实践任务：** 用 PWM 让一个直流电机以五种不同速度正转和反转，然后加编码器，写一个函数让轮子不管电池电压如何都准确转一整圈。后半部分是你的第一个真正闭环，比听起来难得多

### 4. Sensors and reading the physical world  
### 4. 传感器与读取物理世界

**Resources:**  

**1. Adafruit BNO085 9-DoF IMU guide (free)**  

Link:  
[https://learn.adafruit.com/adafruit-9-dof-orientation-imu-fusion-breakout-bno085/overview](https://learn.adafruit.com/adafruit-9-dof-orientation-imu-fusion-breakout-bno085/overview)

Covers an IMU that does sensor fusion on-chip and hands you a quaternion, which is the "buy your way out of the maths" option  
介绍一个芯片内做传感器融合并直接给你四元数的 IMU，这是“花钱绕过数学”的选项

**2. Kalman and Bayesian Filters in Python, Roger Labbe (free, CC-BY)**  

Link:  
[https://rlabbe.github.io/Kalman-and-Bayesian-Filters-in-Python/](https://rlabbe.github.io/Kalman-and-Bayesian-Filters-in-Python/)

Jupyter notebooks with runnable code and solved exercises covering g-h, discrete Bayes, KF, EKF, UKF and particle filters, and it is the best free filtering education that exists  
带可运行代码和已解习题的 Jupyter 笔记本，覆盖 g-h、离散贝叶斯、KF、EKF、UKF 和粒子滤波，是现有最好的免费滤波教育

**3. MathWorks, Understanding Sensor Fusion and Tracking (free)**  
**3. MathWorks，理解传感器融合与跟踪（免费）**

Link:  
[https://www.mathworks.com/videos/series/understanding-sensor-fusion-and-tracking.html](https://www.mathworks.com/videos/series/understanding-sensor-fusion-and-tracking.html)

Six short parts from "what is sensor fusion" to fusing IMU and GPS for pose, and the right conceptual overview before you touch code  
从“什么是传感器融合”到融合 IMU 和 GPS 求位姿的六个短部分，是你动手写代码前正确的概念概览

**Sensor prices, verified:**  

- HC-SR04 ultrasonic, **$3.95**, cheap obstacle detection with a wide cone and poor performance on soft surfaces  
  HC-SR04 超声波，**$3.95**，便宜的障碍检测，锥角大，软表面上表现差
- VL53L0X time-of-flight laser, **$14.95**, a much narrower 35-degree cone and no double-imaging problems  
  VL53L0X 飞行时间激光，**$14.95**，锥角窄得多（35 度），没有双像问题
- MPU-6050 6-DoF IMU, **$12.95**, the cheap classic where you do the fusion yourself, which is the point  
  MPU-6050 6 自由度 IMU，**$12.95**，便宜的经典款，你自己做融合，这正是重点
- BNO085 9-DoF IMU, **$29.50**, fusion on-chip with a UART mode built for robotics  
  BNO085 9 自由度 IMU，**$29.50**，芯片内融合，带专为机器人设计的 UART 模式
- Pololu magnetic encoder pair, **$8.95**, for adding odometry to motors that lack it  
  Pololu 磁编码器对，**$8.95**，给没有编码器的电机加里程计
- RPLIDAR C1 360-degree lidar, **$69.00** at DFRobot, newer and cheaper than the classic A1  
  RPLIDAR C1 360 度激光雷达，DFRobot **$69.00**，比经典 A1 更新更便宜

**Beginner tip:** for a balancing robot, write a complementary filter before you write a Kalman filter. It is four lines, angle = a * (angle + gyro * dt) + (1 - a) * accelAngle with a around 0.98, and it works. Graduate to Kalman when you understand why the complementary filter fails  
**初学者提示：** 做平衡机器人时，先写互补滤波再写卡尔曼滤波。就四行：angle = a * (angle + gyro * dt) + (1 - a) * accelAngle，a 大约 0.98，它能工作。等你理解为什么互补滤波会失败时，再升级到卡尔曼

**Practice task:** mount an IMU on a board, print the pitch angle to serial, hold the board perfectly still and watch the number drift anyway. Now add a complementary filter and watch that drift disappear, which is the single most important lesson in state estimation and it took you twenty minutes  
**实践任务：** 把 IMU 装在板上，把俯仰角打印到串口，把板子完全静止握住，看数字还是会漂移。现在加互补滤波，看漂移消失。这是状态估计中最重要的一课，而且只花了你二十分钟

### 5. Your first two robots  

These two projects together teach more than any course will  
这两个项目合在一起教的东西比任何课程都多

**Line-following robot.** Quality build roughly **$105**, budget build roughly **$38**  
**循线机器人。** 高质量版大约 **$105**，预算版大约 **$38**

Bill of materials, quality: ESP32-S3 $15.95, Pololu Romi chassis kit $39.95, TB6612FNG driver $14.77, QTR-8RC reflectance array $12.95, batteries and holder about $12, wiring and headers about $10  
高质量物料清单：ESP32-S3 $15.95，Pololu Romi 底盘套件 $39.95，TB6612FNG 驱动 $14.77，QTR-8RC 反射阵列 $12.95，电池和支架约 $12，接线和排针约 $10

Budget version: generic ESP32 about $6, 2WD acrylic chassis about $12, DRV8833 $5.95, five TCRT5000 sensors about $3, batteries about $6, wiring about $5  
预算版：通用 ESP32 约 $6，2WD 亚克力底盘约 $12，DRV8833 $5.95，五个 TCRT5000 传感器约 $3，电池约 $6，接线约 $5

**Self-balancing robot.** Quality build roughly **$134**, budget build roughly **$62**  
**自平衡机器人。** 高质量版大约 **$134**，预算版大约 **$62**

Bill of materials, quality: ESP32 $15.95, two gearmotor-with-encoder assemblies $39.90, TB6612FNG $14.77, MPU-6050 $12.95, printed or laser-cut chassis about $10, LiPo and charger and wheels about $30, misc about $10  
高质量物料清单：ESP32 $15.95，两个带编码器的减速电机组件 $39.90，TB6612FNG $14.77，MPU-6050 $12.95，打印或激光切割底盘约 $10，LiPo 和充电器与轮子约 $30，杂项约 $10

**Practice task for the month:** build the line follower first, tune it with a P controller, then add the D term and watch the oscillation disappear, filming both versions. The video of a badly tuned robot next to the same robot tuned properly is one of the most persuasive things a beginner can put in a portfolio, because it proves you understand the loop rather than having copied a gain  
**本月实践任务：** 先做循线机器人，用 P 控制器调参，再加 D 项看振荡消失，把两个版本都拍下来。一个调得差的机器人旁边放同一个调好的机器人，这种视频是初学者作品集里最有说服力的东西之一，因为它证明你理解环而不是抄了个增益

Then build the balancer, which will not work at all until your filter and your loop timing are both correct, and that frustration is the point  
然后做平衡器，在滤波器和环时序都正确之前它根本不会工作，而这种挫折正是重点

### Month 2 Milestone  

By the end of this month you should be able to:  
到本月末你应该能够：

- Drive a motor at a controlled speed and know the difference between PWM duty and actual RPM  
  以受控速度驱动电机，并知道 PWM 占空比和实际 RPM 的区别
- Read an encoder and close a position loop around it  
  读编码器并围绕它闭环位置
- Wire and read an I2C sensor from its datasheet without a tutorial  
  不看教程，只根据数据手册接线和读取 I2C 传感器
- Fuse accelerometer and gyroscope data into a stable angle estimate  
  把加速度计和陀螺仪数据融合成稳定的角度估计
- Explain what P, I and D each do by describing what your robot did when you changed them  
  通过描述你改变它们时机器人的表现，解释 P、I、D 各自做什么
- Show two working robots on GitHub with wiring, code and a written account of what broke  
  在 GitHub 上展示两个能工作的机器人，带接线、代码和“什么坏了”的书面记录

⏩---------------------------------------------------------------------⏪

## Month 3: Mechanical design, CAD and manufacturing your own parts  
## 第 3 个月：机械设计、CAD 以及制造自己的零件

Your goal this month: design a part in CAD, manufacture it, and have it fit  
本月目标：在 CAD 中设计一个零件，制造它，并让它能装上

This is the month that separates people who assemble kits from people who build robots  
这个月把“拼套件的人”和“造机器人的人”分开了

Every robot you build after this will contain parts that exist only because you designed them, and being able to go from an idea to a physical bracket in an afternoon changes what projects are possible for you  
之后你做的每一个机器人都会包含只因为你设计才存在的零件，而能在一个下午从想法变成实体支架，会改变你能做的项目范围

### What to learn  

### 1. CAD  

Pick one tool and go deep rather than sampling all of them  
选一个工具深入，而不是每个都浅尝

Decision framework:  
决策框架：

- **Onshape Free** if you are happy designing in public. It runs in a browser, works on any machine including a Chromebook, and its assembly and mate system behaves the way robot joints actually behave. The catch is real: **every document is public** on the free tier  
  **Onshape Free**：如果你愿意公开设计。它在浏览器运行，任何机器包括 Chromebook 都能用，装配和配合系统的行为方式就像真实机器人关节。代价是真的：**免费层每一个文档都是公开的**
- **Fusion Personal** if you want CAM and 3D-print integration later. Free on a renewable 3-year term for non-commercial use under $1,000 a year of revenue, but with limited import and export file types  
  **Fusion Personal**：如果你以后想要 CAM 和 3D 打印集成。非商业使用且年收入低于 1000 美元可免费续期 3 年，但导入导出文件类型有限
- **FreeCAD** if you are somewhere cloud CAD or card payment is a problem, or you object to a licence that can be revoked. Version 1.1 landed in March 2026 and it is genuinely usable now  
  **FreeCAD**：如果你所在地方云 CAD 或刷卡有问题，或者你反对可被撤销的许可证。1.1 版 2026 年 3 月发布，现在真的可用了
- **SOLIDWORKS for Makers** at **$48/year** if you want the industry-standard tool, with the caveat that native files are watermarked and will not open in commercial SOLIDWORKS  
  **SOLIDWORKS for Makers** 每年 **$48**：如果你想要行业标准工具，但注意原生文件带水印，在商业版 SOLIDWORKS 里打不开

**Resources:**  

**1. Onshape Learning Center, Fundamentals: CAD (free with account)**  

Link:  
[https://learn.onshape.com/learning-paths/onshape-fundamentals-cad](https://learn.onshape.com/learning-paths/onshape-fundamentals-cad)

The only free structured CAD curriculum that ends in a credential you can put on a CV, and it ships a dedicated robotics-competition track  
唯一免费结构化的 CAD 课程，结束时有可放简历的证书，还专门有机器人竞赛轨道

**2. Product Design Online, Learn Autodesk Fusion in 30 Days (free)**  
**2. Product Design Online，30 天学会 Autodesk Fusion（免费）**

Link:  
[https://productdesignonline.com/learn-autodesk-fusion-360-in-30-days-official-course/](https://productdesignonline.com/learn-autodesk-fusion-360-in-30-days-official-course/)

Thirty modelled objects in thirty days, which is the fastest route from never having opened CAD to confident parametric sketching  
30 天做 30 个模型，是从从未打开过 CAD 到自信参数化草图的最快路径

**3. MangoJelly Solutions FreeCAD tutorials (free)**  

Link:  
[https://www.youtube.com/@MangoJellySolutions](https://www.youtube.com/@MangoJellySolutions)

The best FreeCAD teacher for makers, organised as short targeted lessons rather than one monolithic course  
对创客最好的 FreeCAD 老师，以短而针对性强的课程组织，而不是一个大块课程

**4. Protolabs Network, Design for 3D printing (free)**  

Link:  
[https://www.hubs.com/knowledge-base/design-for-3d-printing/](https://www.hubs.com/knowledge-base/design-for-3d-printing/)

The design-for-manufacture half of CAD: wall thickness, orientation, tolerances, supports, snap-fits, and when to use STL versus 3MF versus STEP  
CAD 中面向制造的一半：壁厚、方向、公差、支撑、卡扣，以及何时用 STL、3MF 还是 STEP

**What to focus on:**  

- Fully constrained sketches, because an under-constrained sketch will move when you edit it later and ruin your day  
  完全约束的草图，因为欠约束的草图以后编辑时会动，毁掉你的一天
- Parametric design driven by variables, so changing one dimension updates the whole part  
  由变量驱动的参数化设计，改一个尺寸整个零件都会更新
- Assemblies and mates that mirror real joints: revolute, slider, fixed  
  镜像真实关节的装配和配合：旋转、滑动、固定
- Designing around hardware you actually own, starting from the servo's datasheet dimensions  
  围绕你实际拥有的硬件设计，从舵机数据手册尺寸开始
- Exporting STEP for sharing and STL for printing, and knowing the difference  
  导出 STEP 用于分享、STL 用于打印，并知道区别

**Practice task:** model a bracket that holds the exact servo you bought, with correctly sized screw holes and a shaft clearance, from the manufacturer's datasheet drawing rather than by eye. Then print it and see if it fits, which it probably will not the first time, and that failure is the lesson  
**实践任务：** 根据制造商数据手册图纸（而不是靠眼睛）建模一个固定你所买舵机的支架，螺丝孔尺寸正确，轴有间隙。然后打印看能不能装上，第一次大概装不上，这种失败才是课程

### 2. 3D printing  

Verified printer prices, September 2026:  
已核实打印机价格（2026 年 9 月）：

- Creality Ender-3 V3 SE, **$199**  
  Creality Ender-3 V3 SE，**$199**  
  Link: [https://store.creality.com/products/ender-3-v3-se-3d-printer](https://store.creality.com/products/ender-3-v3-se-3d-printer)
- Bambu Lab A1 mini, **$219.99**  
  Bambu Lab A1 mini，**$219.99**  
  Link: [https://www.bestbuy.com/product/bambu-lab-a1-mini-3d-printer-silver/CZTZV9ZGGV](https://www.bestbuy.com/product/bambu-lab-a1-mini-3d-printer-silver/CZTZV9ZGGV)
- Bambu Lab A1, **$299.99**, with the 256mm bed you will want for larger brackets  
  Bambu Lab A1，**$299.99**，带你做大支架时会想要的 256mm 热床  
  Link: [https://www.bestbuy.com/product/bambu-lab-a1-3d-printer-silver/CZW2ZH33H4](https://www.bestbuy.com/product/bambu-lab-a1-3d-printer-silver/CZW2ZH33H4)
- Creality K1C, **$369**, enclosed and hardened for carbon-fibre filaments  
  Creality K1C，**$369**，封闭并硬化喷嘴，适合碳纤维耗材  
  Link: [https://store.creality.com/products/k1c-3d-printer](https://store.creality.com/products/k1c-3d-printer)
- Bambu Lab P1S, **$799**, enclosed CoreXY for ABS and ASA  
  Bambu Lab P1S，**$799**，封闭 CoreXY，适合 ABS 和 ASA  
  Link: [https://us.store.bambulab.com/products/p1s](https://us.store.bambulab.com/products/p1s)

**Filament, and when to use each:**  

- **PLA and PLA+** for prototype brackets, jigs, and the SO-101 arm itself, which specifies PLA+ at 15% infill and 0.2mm layers. Stiffest of the easy materials, and it creeps under sustained load and softens around 55 to 60°C  
  **PLA 和 PLA+**：原型支架、治具，以及 SO-101 机械臂本身（规定用 PLA+、15% 填充、0.2mm 层高）。易用材料中最硬，持续负载下会蠕变，55-60°C 左右软化
- **PETG** for the default real robot part: chassis plates, gearbox housings, servo mounts, anything that must survive a drop. Tough with far better layer adhesion than PLA, and stringy  
  **PETG**：默认真实机器人零件：底盘板、齿轮箱外壳、舵机安装座，任何必须扛得住摔的东西。比 PLA 韧得多，层间附着力好得多，但容易拉丝
- **ABS and ASA** for parts near hot motors and for outdoor rovers, and they warp badly without an enclosure  
  **ABS 和 ASA**：靠近热电机的零件和户外小车，没有封闭腔会严重翘曲
- **Nylon** for gears and cable guides, and it is easier to order than to print  
  **尼龙**：齿轮和线缆导向，订购比打印容易
- **Carbon-fibre filled** for stiff structural links, and it needs a hardened nozzle because it is abrasive  
  **碳纤维填充**：刚性结构连杆，因为磨料性强需要硬化喷嘴
- **TPU** for feet, bumpers and compliant gripper fingers  
  **TPU**：脚、保险杠和柔顺夹爪手指

**Resources:**  

**1. OrcaSlicer Calibration wiki (free)**  

Link:  
https://github.com/OrcaSlicer/OrcaSlicer/wiki/Calibration

Temperature, flow, pressure advance, retraction and tolerance calibration in a recommended running order, and it is the most useful slicing document for anyone who wants parts that fit  
温度、流量、压力推进、回抽和公差校准，按推荐顺序执行，是任何想做出能装上零件的人最有用的切片文档

**2. Teaching Tech 3D Printer Calibration (free, interactive)**  

Link:  
[https://teachingtechyt.github.io/calibration.html](https://teachingtechyt.github.io/calibration.html)

A printer-agnostic interactive walkthrough that takes you through every calibration in sequence  
与打印机无关的交互式走查，按顺序带你完成每一个校准

**3. CNC Kitchen (free)**  

Link:  
[https://www.youtube.com/@CNCKitchen](https://www.youtube.com/@CNCKitchen)

Instrumented, repeatable strength tests on infill, walls, threaded inserts and orientation, which is where print orientation stops being folklore and starts being data  
对填充、壁、螺纹嵌件和方向进行仪器化、可重复的强度测试，让打印方向从民间传说变成数据

**4. Clearance and Tolerance 3D Printer Gauge (free STL)**  
**4. 间隙与公差 3D 打印机量规（免费 STL）**

Link:  
[https://www.printables.com/model/57067-clearance-and-tolerance-3d-printer-gauge](https://www.printables.com/model/57067-clearance-and-tolerance-3d-printer-gauge)

Print this once and you know your machine's real clearance for press fits and sliding fits, which every bracket and bearing seat you design afterwards depends on  
打印一次，你就知道机器对过盈配合和滑动配合的真实间隙，之后你设计的每一个支架和轴承座都依赖它

If you cannot buy a printer:  
如果你买不起打印机：

- **Fab Labs** worldwide, roughly 2,875 of them, searchable by country  
  全球 **Fab Labs**，大约 2875 个，可按国家搜索  
  Link: [https://fablabs.io/labs](https://fablabs.io/labs)
- **Public library makerspaces**, free or near-free in much of the US  
  **公共图书馆创客空间**，美国很多地方免费或几乎免费  
  Link: [https://action.everylibrary.org/how_to_find_a_makerspace_near_you](https://action.everylibrary.org/how_to_find_a_makerspace_near_you)
- **Craftcloud** compares quotes across a network spanning 95 countries and routes to a manufacturer near you, which is the right choice outside the US and EU  
  **Craftcloud** 比较覆盖 95 个国家的网络报价，并路由到你附近的制造商，美国和欧盟以外是正确选择  
  Link: [https://craftcloud3d.com/](https://craftcloud3d.com/)
- **JLC3DP** starts at $1.00 per part for MJF nylon and FDM, with 3-day builds  
  **JLC3DP** MJF 尼龙和 FDM 每件从 $1.00 起，3 天出件  
  Link: [https://jlc3dp.com/](https://jlc3dp.com/)

**The honest economics:** an SO-101 arm needs roughly 1kg of PLA+, which is about $20 to $25 of filament on your own machine against $30.99 for a ready-printed set. A printer does not pay for itself on one build. It pays for itself on iteration, because the tenth revision of a gripper finger costs 40 cents and 25 minutes at home, against $8 and a week from a service  
**诚实经济学：** 一个 SO-101 臂大约需要 1kg PLA+，自己机器上耗材约 $20 到 $25，而现成打印套件 $30.99。一台打印机不会靠一次构建回本。它靠迭代回本，因为夹爪手指的第十次修改在家只要 40 美分和 25 分钟，服务商则要 $8 和一周

**Practice task:** print the tolerance gauge, write down your machine's actual clearance numbers, then design and print a two-part snap-fit enclosure for your ESP32 that closes without glue. Iterate until it clicks properly. This is the loop that all mechanical design is made of  
**实践任务：** 打印公差量规，记下机器的真实间隙数字，然后设计和打印一个两件式卡扣 ESP32 外壳，不用胶水就能合上。迭代直到它咔嗒一声合好。这就是所有机械设计的循环

### 3. Actuators, transmissions and why robots are hard  
### 3. 执行器、传动以及为什么机器人很难

Understanding gear reduction, backlash and torque density is what separates a robot that works in a video from a robot that works repeatedly  
理解减速比、间隙和扭矩密度，才能把“视频里能工作的机器人”和“能反复工作的机器人”分开

**What to focus on:**  

- Gear ratios and the trade between speed and torque  
  齿轮比以及速度与扭矩的权衡
- Backlash, and why it destroys position accuracy in a way software cannot fully fix  
  间隙，以及为什么它以软件无法完全修复的方式毁掉位置精度
- Bearing selection and preload  
  轴承选择与预紧
- Belt versus gear versus direct drive  
  皮带 vs 齿轮 vs 直接驱动
- Why a cheap servo's plastic gearset is the first thing to fail on any arm  
  为什么便宜舵机的塑料齿轮组是任何机械臂上最先坏的东西

**Practice task:** design and print a simple planetary or cycloidal reducer for a NEMA17 stepper or a hobby motor, and accept that the first one will be bad. Measure the backlash by holding the output and rocking it, then redesign to reduce it. Reference builds are on Instructables and Hackaday if you want a starting geometry  
**实践任务：** 为 NEMA17 步进或舵机设计和打印一个简单的行星或摆线减速器，接受第一个会很差。握住输出端晃动测量间隙，然后重新设计减小它。如果你想要起始几何，Instructables 和 Hackaday 上有参考构建  
Link: [https://www.instructables.com/OpenCycloid-3D-printed-Open-Source-Robotic-Actuato/](https://www.instructables.com/OpenCycloid-3D-printed-Open-Source-Robotic-Actuato/)

### 4. Build a real robot arm  
### 4. 建造一个真实的机械臂

This is the capstone of the month, and it is the single best hardware purchase in this entire roadmap  
这是本月的压轴项目，也是整份路线图中最好的一笔硬件投资

The **SO-101** is an open-source 5-DOF arm plus gripper from TheRobotStudio and Hugging Face, designed to be built as a leader and follower pair so you can hand-guide one and have the other mirror it  
**SO-101** 是 TheRobotStudio 和 Hugging Face 的开源 5 自由度机械臂加夹爪，设计成主从对，你可以手引导一个，另一个镜像跟随

That teleoperation setup is what lets you record demonstrations, which is what month six is built on  
这种遥操作设置让你可以记录示范，而第 6 个月正是建立在此之上

Official bill of materials, verified in the repo: **$229.88 US** for a leader and follower pair, **$121.94** for a single follower arm, excluding 3D printing  
官方物料清单（仓库已核实）：主从一对 **$229.88 美元**，单个从臂 **$121.94**，不含 3D 打印  
Link: https://github.com/TheRobotStudio/SO-ARM100

**Where to buy, verified prices:**  
**购买渠道（已核实价格）：**

- Seeed Studio SO-ARM101 Pro servo kit, **$277.99**, motors and control boards without printed parts  
  Seeed Studio SO-ARM101 Pro 舵机套件，**$277.99**，电机和控制板，无打印件  
  Link: [https://www.seeedstudio.com/SO-ARM101-Low-Cost-AI-Arm-Kit-Pro-p-6427.html](https://www.seeedstudio.com/SO-ARM101-Low-Cost-AI-Arm-Kit-Pro-p-6427.html)
- Seeed Studio printed parts set, **$30.99**, if you have no printer  
  Seeed Studio 打印件套装，**$30.99**，如果你没有打印机  
  Link: [https://www.seeedstudio.com/SO-ARM101-3D-printed-Enclosure-p-6428.html](https://www.seeedstudio.com/SO-ARM101-3D-printed-Enclosure-p-6428.html)
- Robonine SO-ARM101 complete kit, **$349.00**, shipping from Delaware  
  Robonine SO-ARM101 完整套件，**$349.00**，从特拉华发货  
  Link: [https://robonine.com/shop/so-arm101-black-robotic-arm-kit/](https://robonine.com/shop/so-arm101-black-robotic-arm-kit/)
- WowRobo via OpenELAB, **$325.99** printed parts plus servos, **$419.99** unassembled full kit, **$489.99** fully assembled  
  WowRobo 通过 OpenELAB，打印件加舵机 **$325.99**，未组装完整套件 **$419.99**，全组装 **$489.99**  
  Link: [https://openelab.com/products/wowrobo-robotics-so-arm101-diykit](https://openelab.com/products/wowrobo-robotics-so-arm101-diykit)

**Cheaper alternatives at every tier:**  
**每个档次的更便宜替代：**

- **$0**: everything in the LeRobot stack runs in MuJoCo simulation before hardware exists, which is the answer if you cannot import anything  
  **$0**：LeRobot 栈里所有东西在硬件存在前都能在 MuJoCo 仿真里跑，如果你什么都进不来，这就是答案
- **$50 to $80**: the EEZYbotARM MK2, free STLs, built from MG996R hobby servos and printed parts. It teaches linkage kinematics rather than servo-bus protocols  
  **$50 到 $80**：EEZYbotARM MK2，免费 STL，用 MG996R 舵机和打印件做。它教连杆运动学而不是舵机总线协议  
  Link: [https://www.thingiverse.com/thing:1454048](https://www.thingiverse.com/thing:1454048)
- **$122**: a single SO-101 follower arm if you print the parts yourself. You lose teleoperation and keep the entire software path  
  **$122**：自己打印零件的单个 SO-101 从臂。你失去遥操作但保留完整软件路径
- **$199.99**: Hiwonder xArm 1S, the cheapest arm with intelligent bus servos that report position and voltage  
  **$199.99**：Hiwonder xArm 1S，带能报告位置和电压的智能总线舵机的最便宜机械臂  
  Link: [https://www.hiwonder.com/products/xarm-1s](https://www.hiwonder.com/products/xarm-1s)

**Practice task:** build the SO-101, calibrate every servo, and teleoperate the follower with the leader. Then design and print your own gripper fingers to replace the stock ones, in TPU, and test them on three objects of different shapes. The arm is the platform for months five and six, and the custom fingers are the part that proves you can design as well as assemble  
**实践任务：** 组装 SO-101，校准每一个舵机，用主臂遥操作从臂。然后用 TPU 设计和打印自己的夹爪手指替换原装的，在三个不同形状的物体上测试。这个臂是第 5、6 个月的平台，定制手指证明你既能设计也能组装

### Month 3 Milestone  
### 第 3 个月里程碑

By the end of this month you should be able to:  
到本月末你应该能够：

- Model a part from a datasheet in CAD with fully constrained sketches  
  根据数据手册在 CAD 中用完全约束草图建模零件
- State your printer's real clearance numbers from measurement rather than guesswork  
  用测量而不是猜测说出打印机的真实间隙数字
- Design a part specifically for FDM, accounting for orientation, overhangs and layer adhesion  
  专门为 FDM 设计零件，考虑方向、悬垂和层间附着
- Choose PLA, PETG, ABS or TPU for a given part and justify it  
  为给定零件选择 PLA、PETG、ABS 或 TPU 并说明理由
- Explain what backlash is and demonstrate it on something you built  
  解释什么是间隙，并在你做的东西上演示它
- Show a working robot arm you assembled, calibrated and modified with your own parts  
  展示一个你组装、校准并用自己零件改装过的能工作的机械臂

⏩---------------------------------------------------------------------⏪

## Month 4: ROS 2, simulation, and building robots the way companies do  
## 第 4 个月：ROS 2、仿真，以及像公司一样构建机器人

Your goal this month: build a robot in ROS 2, simulate it, and make it map a room and navigate autonomously  
本月目标：在 ROS 2 中构建机器人，仿真它，让它建图并自主导航

Everything up to now was you building robots your way  
到目前为止都是你用自己的方式造机器人

ROS 2 is how the industry builds them, and it is the single most requested skill in robotics job listings  
ROS 2 是行业造机器人的方式，也是机器人招聘中被要求最多的单一技能

The best part of this month is that **you can do all of it with no hardware at all**, on a normal laptop, with no NVIDIA GPU. Say that to yourself twice, because the belief that robotics requires expensive equipment is the main reason people never start  
本月最好的部分是：**你可以完全不需要硬件**，在普通笔记本上、没有 NVIDIA GPU 就能全部完成。对自己说两遍，因为“机器人学需要昂贵设备”的信念是人们永远不开始的主要原因

### What to learn  
### 要学什么

### 1. Which ROS 2 to install, and the ROS 1 trap  
### 1. 该装哪个 ROS 2，以及 ROS 1 陷阱

ROS 2 releases every May. Even years are LTS with five years of support, odd years get about eighteen months  
ROS 2 每年 5 月发布。偶数年是 LTS，支持五年；奇数年大约十八个月

As of September 2026 the picture is:  
截至 2026 年 9 月情况是：

- **Lyrical Luth**, released May 2026, EOL May 2031, targets Ubuntu 26.04. The current LTS  
  **Lyrical Luth**，2026 年 5 月发布，EOL 2031 年 5 月，目标 Ubuntu 26.04。当前 LTS
- **Jazzy Jalisco**, released May 2024, EOL May 2029, targets Ubuntu 24.04  
  **Jazzy Jalisco**，2024 年 5 月发布，EOL 2029 年 5 月，目标 Ubuntu 24.04
- **Kilted Kaiju**, EOL 31 December 2026. Do not start here  
  **Kilted Kaiju**，EOL 2026 年 12 月 31 日。不要从这里开始
- **Humble Hawksbill**, EOL May 2027. Legacy  
  **Humble Hawksbill**，EOL 2027 年 5 月。遗留

**Start on Jazzy.** Lyrical is newer and is what you would pick for a new production project, but as of now almost every course, book and YouTube series still targets Jazzy, and it has more than two and a half years of support left. Move to Lyrical once your tutorial stack catches up  
**从 Jazzy 开始。** Lyrical 更新，新生产项目你会选它，但目前几乎所有课程、书籍和 YouTube 系列仍针对 Jazzy，而且它还有两年半以上支持。等你的教程栈跟上后再转到 Lyrical

**ROS 1 is dead.** Noetic reached end of life on 31 May 2025 and there is no successor. Enormous amounts of highly-ranked tutorial content is ROS 1, so learn to recognise it instantly: if you see catkin_make, roscore, rosrun, rospy or XML-only launch files, close the tab. ROS 2 uses colcon build, has no master, and uses ros2 run and Python launch files  
**ROS 1 已死。** Noetic 在 2025 年 5 月 31 日到达生命周期终点，没有继任者。大量高排名教程内容是 ROS 1，所以要学会立刻识别：如果你看到 catkin_make、roscore、rosrun、rospy 或纯 XML 启动文件，关掉标签页。ROS 2 用 colcon build，没有 master，用 ros2 run 和 Python 启动文件

### 2. ROS 2 core concepts  
### 2. ROS 2 核心概念

**Resources:**  

**1. Official ROS 2 Tutorials (free)**  

Link:  
[https://docs.ros.org/en/jazzy/Tutorials.html](https://docs.ros.org/en/jazzy/Tutorials.html)

The canonical reference, structured exactly around nodes, topics, services, actions, parameters, launch files, tf2 and URDF. It is reference-grade rather than pedagogy, so pair it with video  
权威参考，完全围绕节点、话题、服务、动作、参数、启动文件、tf2 和 URDF 结构化。它是参考级而非教学级，所以要搭配视频

**2. The Construct (free tier, paid from €39.97/month)**  

Link:  
[https://www.theconstruct.ai/](https://www.theconstruct.ai/)

Everything runs in a browser-based ROS environment with simulated robots, which removes the single biggest friction point for beginners: no Ubuntu dual-boot, no install weekend, no GPU. The free tier includes three complete courses  
一切都在基于浏览器的 ROS 环境中运行，带仿真机器人，消除了初学者最大的摩擦点：无需 Ubuntu 双系统、无需安装周末、无需 GPU。免费层包含三门完整课程

**3. Edouard Renard, ROS 2 for Beginners, Level 1 (Udemy, roughly $10 to $20 on sale)**  

Link:  
[https://www.udemy.com/course/ros2-for-beginners/](https://www.udemy.com/course/ros2-for-beginners/)

Thirteen hours in both Python and C++ covering nodes, packages, topics, services, custom interfaces, parameters and launch files. Never pay list price, Udemy discounts almost permanently  
十三小时，Python 和 C++ 都有，覆盖节点、包、话题、服务、自定义接口、参数和启动文件。永远不要付标价，Udemy 几乎一直打折

**4. Articulated Robotics, Josh Newans (free)**  

Link:  
[https://articulatedrobotics.xyz/tutorials/](https://articulatedrobotics.xyz/tutorials/)

The best free end-to-end narrative anywhere: design a robot, write the URDF, simulate it, add ros2_control, put it on a Raspberry Pi with a lidar, then SLAM and navigate. Uniquely good on ros2_control, which almost every other resource fumbles  
任何地方最好的免费端到端叙述：设计机器人、写 URDF、仿真、加 ros2_control、放到带激光雷达的树莓派上，然后 SLAM 和导航。在 ros2_control 上特别好，其他资源几乎都搞砸

**5. MOGI-ROS, a full university course (free, Apache 2.0)**  

Link:  
https://github.com/orgs/MOGI-ROS/repositories

A real semester-length syllabus on ROS 2 Jazzy with Gazebo Harmonic, running from pub/sub through URDF, sensors, navigation and MoveIt 2 arms, with working code for every week  
真正的学期长度大纲，ROS 2 Jazzy + Gazebo Harmonic，从 pub/sub 到 URDF、传感器、导航和 MoveIt 2 机械臂，每周都有可运行代码

**6. Automatic Addison (free)**  

Link:  
[https://automaticaddison.com/tutorials/](https://automaticaddison.com/tutorials/)

Recipe-style guides organised by distro, and notable for already carrying Lyrical tracks alongside Jazzy. This is where you go for "how do I write an action in Jazzy" rather than a full course  
按发行版组织的菜谱式指南，值得注意的是已经同时有 Lyrical 和 Jazzy 轨道。你来这里找“如何在 Jazzy 写 action”而不是完整课程

**What to focus on:**  

- Nodes, topics, services and actions, and knowing which of the three a given problem needs  
  节点、话题、服务和动作，以及知道给定问题需要三者中的哪一个
- Custom message and service definitions  
  自定义消息和服务定义
- Parameters and YAML config files  
  参数和 YAML 配置文件
- Launch files in Python, and passing arguments and remapping topics  
  Python 启动文件，以及传参和重映射话题
- colcon workspaces and package layout  
  colcon 工作空间和包布局
- ros2 bag for recording and replaying, which is how you debug anything that only fails occasionally  
  ros2 bag 用于录制和回放，这是调试偶尔才失败的东西的方法

Honest gap worth naming: **DDS and QoS settings are covered badly by every resource I could find.** No course does it well. When you hit mysterious "my topic publishes but nothing receives" problems, the answer is almost always a QoS mismatch, and you will be reading the official Concepts pages rather than a tutorial  
值得诚实指出的空白：**DDS 和 QoS 设置在我能找到的所有资源里都讲得很差。** 没有课程讲得好。当你遇到神秘的“话题发布了但没人收”问题时，答案几乎总是 QoS 不匹配，你得去读官方 Concepts 页面而不是教程

**Practice task:** build a multi-node system with no robot and no simulator at all. A sensor publisher, a processing node, a service-based configuration node and a parameterised aggregator, with your own custom .msg and .srv, wired together in a Python launch file that takes arguments. Record it with ros2 bag and replay it. This costs nothing and it proves you understand the graph rather than that you can run turtlesim  
**实践任务：** 做一个完全没有机器人和仿真器的多节点系统。一个传感器发布者、一个处理节点、一个基于服务的配置节点和一个参数化聚合器，用你自己的自定义 .msg 和 .srv，在接受参数的 Python 启动文件里连在一起。用 ros2 bag 录制并回放。这零成本，证明你理解图而不是只会跑 turtlesim

### 3. URDF, TF and describing a robot  
### 3. URDF、TF 以及描述机器人

**Resources:**  

**1. Articulated Robotics, Coordinate Transforms for Robotics (free)**  

Link:  
[https://articulatedrobotics.xyz/category/coordinate-transforms-for-robotics](https://articulatedrobotics.xyz/category/coordinate-transforms-for-robotics)

A dedicated series on frames and transforms, which is the concept that blocks most people's understanding of URDF  
专门讲坐标系和变换的系列，这是阻碍大多数人理解 URDF 的概念

**2. Edouard Renard, Level 2: TF, URDF, RViz, Gazebo (Udemy, roughly $10 to $20 on sale)**  

Link:  
[https://www.udemy.com/course/ros2-tf-urdf-rviz-gazebo/](https://www.udemy.com/course/ros2-tf-urdf-rviz-gazebo/)

The single best URDF resource, covering xacro macros, robot_state_publisher, RViz configuration and Gazebo plugins, ending in a mobile base with an arm on it  
最好的单一 URDF 资源，覆盖 xacro 宏、robot_state_publisher、RViz 配置和 Gazebo 插件，最终做出带机械臂的移动底盘

**3. Official URDF tutorial with robot_state_publisher (free)**  

Link:  
[https://docs.ros.org/en/jazzy/Tutorials/Intermediate/URDF/Using-URDF-with-Robot-State-Publisher-cpp.html](https://docs.ros.org/en/jazzy/Tutorials/Intermediate/URDF/Using-URDF-with-Robot-State-Publisher-cpp.html)

The canonical walkthrough, available in both C++ and Python variants  
权威走查，有 C++ 和 Python 两个版本

**Common issues to learn:**  

- Confusing joint_state_publisher with robot_state_publisher. Fix: the first invents joint positions, the second computes transforms from them  
  混淆 joint_state_publisher 和 robot_state_publisher。修复：前者发明关节位置，后者从它们计算变换
- Missing inertial tags. Fix: your robot explodes or sinks through the Gazebo floor without them, so always include mass and inertia  
  缺少惯性标签。修复：没有它们机器人会爆炸或沉入 Gazebo 地板，所以永远包含质量和惯性
- A missing static transform to the lidar frame. Fix: this causes more beginner SLAM failures than any algorithm problem  
  缺少到激光雷达坐标系的静态变换。修复：这比任何算法问题导致的初学者 SLAM 失败都多
- Writing 400 lines of XML by hand. Fix: use xacro macros from day one  
  手写 400 行 XML。修复：从第一天就用 xacro 宏

**Practice task:** design your own robot in xacro, not TurtleBot. A differential-drive base, a sensor mast and a two-DOF pan-tilt head, with correct inertias and separate collision and visual geometry. Drive the joints with joint_state_publisher_gui and view the full TF tree in RViz. A screenshot of your own robot in RViz is the most legible signal in a beginner portfolio  
**实践任务：** 用 xacro 设计你自己的机器人，不是 TurtleBot。差速驱动底盘、传感器桅杆和两自由度云台头，带正确惯性和分离的碰撞与视觉几何。用 joint_state_publisher_gui 驱动关节，在 RViz 看完整 TF 树。你自己的机器人在 RViz 里的截图是初学者作品集中最清晰的信号

### 4. Simulation  
### 4. 仿真

The Gazebo naming history confuses everyone, so here it is cleanly  
Gazebo 命名历史让所有人困惑，所以这里干净说明

Gazebo Classic, versions 1 to 11, reached end of life in January 2025. It was rewritten and briefly called Ignition Gazebo, then renamed back to plain Gazebo in an announcement in April 2022, with every ign command becoming gz. If a tutorial types roslaunch gazebo_ros or ign gazebo, it is out of date  
Gazebo Classic 1 到 11 版在 2025 年 1 月到达生命周期终点。它被重写并短暂叫 Ignition Gazebo，然后在 2022 年 4 月公告中改回普通 Gazebo，所有 ign 命令变成 gz。如果教程写 roslaunch gazebo_ros 或 ign gazebo，它过时了

Current releases are named alphabetically: Fortress, Garden, Harmonic, Ionic, Jetty  
当前版本按字母命名：Fortress、Garden、Harmonic、Ionic、Jetty

**Install the version paired with your ROS 2 distro or you will fight build errors:** Humble pairs with Fortress, **Jazzy pairs with Harmonic**, Kilted with Ionic, Lyrical with Jetty  
**安装与你的 ROS 2 发行版配对的版本，否则你会和构建错误斗争：** Humble 配 Fortress，**Jazzy 配 Harmonic**，Kilted 配 Ionic，Lyrical 配 Jetty

**Resources:**  

**1. Gazebo documentation and tutorials (free)**  

Link:  
[https://gazebosim.org/docs/latest/getstarted/](https://gazebosim.org/docs/latest/getstarted/)

Building your own robot, moving it, SDF worlds, sensors, and spawning a URDF  
构建自己的机器人、移动它、SDF 世界、传感器，以及生成 URDF

**2. MuJoCo (free, open source)**  

Link:  
[https://mujoco.readthedocs.io/en/stable/overview.html](https://mujoco.readthedocs.io/en/stable/overview.html)

The fastest and most accurate contact dynamics available, CPU-first so it needs no GPU, and it is the research standard for locomotion and manipulation learning  
可用最快最准确的接触动力学，以 CPU 优先所以不需要 GPU，是运动和操作学习的研究标准

**3. NVIDIA Isaac Sim (free download)**  

Link:  
[https://docs.isaacsim.omniverse.nvidia.com/6.0.0/installation/requirements.html](https://docs.isaacsim.omniverse.nvidia.com/6.0.0/installation/requirements.html)

Photoreal simulation and synthetic data generation, and read that requirements link before getting excited: the **minimum is an RTX 4080 with 16GB VRAM**, and data-centre cards without RT cores such as the A100 and H100 are not supported at all  
照片级仿真和合成数据生成，兴奋前先读那个需求**最低是带 16GB VRAM 的 RTX 4080**，没有 RT 核心的数据中心卡如 A100 和 H100 完全不支持

Decision framework:  
决策框架：

- **Learn Gazebo first**, because it is the only simulator natively wired into ROS 2 and it runs on the laptop you already own  
  **先学 Gazebo**，因为它是唯一原生接入 ROS 2 的仿真器，而且在你已有的笔记本上就能跑
- Go to **MuJoCo** when you want reinforcement learning or locomotion, and it still needs no GPU  
  想做强化学习或运动时去 **MuJoCo**，它仍然不需要 GPU
- Go to **Isaac Sim or Isaac Lab** only when you have the RTX hardware and a specific reason  
  只有当你有 RTX 硬件和具体理由时才去 **Isaac Sim 或 Isaac Lab**
- Skip **PyBullet**, which has had no release since 2022 and whose maintainers closed the issue tracker  
  跳过 **PyBullet**，它从 2022 年起就没有发布，维护者关闭了 issue 追踪器
- Watch **Genesis** but do not build a portfolio on it yet, since v1.0 is fresh and it has no ROS 2 integration  
  关注 **Genesis** 但暂时不要用它做作品集，因为 v1.0 还新，而且没有 ROS 2 集成

**Practice task:** put your xacro robot from the last section into Gazebo, add a lidar plugin and a camera plugin, and build a custom SDF world with obstacles for it to sit in. Confirm the sensor data appears on ROS 2 topics and renders in RViz  
**实践任务：** 把上一节的 xacro 机器人放进 Gazebo，加激光雷达插件和相机插件，建一个带障碍物的自定义 SDF 世界让它坐在里面。确认传感器数据出现在 ROS 2 话题上并在 RViz 渲染

### 5. ros2_control  

This is the topic most self-taught candidates have never touched, which makes it the fastest way to differentiate yourself  
这是大多数自学候选人从未碰过的话题，也因此是最快让你脱颖而出的方式

**Resources:**  

**1. ros2_control documentation (free)**  

Link:  
[https://control.ros.org/rolling/index.html](https://control.ros.org/rolling/index.html)

Where URDF meets actuation: hardware interfaces, controller manager, and the <ros2_control> tags that go in your xacro  
URDF 与执行相遇的地方：硬件接口、控制器管理器，以及放进 xacro 的 <ros2_control> 标签

**2. Articulated Robotics, ros2_control on real hardware (free)**  

Link:  
[https://articulatedrobotics.xyz/tutorials/mobile-robot/applications/ros2_control-real/](https://articulatedrobotics.xyz/tutorials/mobile-robot/applications/ros2_control-real/)

The only resource that walks the simulation-to-real-hardware transition properly  
唯一正确走仿真到真实硬件过渡的资源

**Practice task:** add <ros2_control> tags to your robot, configure diff_drive_controller and joint_state_broadcaster through YAML, and drive it in Gazebo with keyboard teleop. Then write an action server that drives a commanded distance and reports progress, with feedback and cancellation. Actions plus ros2_control in one project is a genuinely strong portfolio piece  
**实践任务：** 给机器人加 <ros2_control> 标签，通过 YAML 配置 diff_drive_controller 和 joint_state_broadcaster，用键盘遥操作在 Gazebo 驱动它。然后写一个动作服务器，驱动指定距离并报告进度，带反馈和取消。动作 + ros2_control 在一个项目里是真正强的作品集作品

### 6. SLAM and navigation  

**Resources:**  

**1. Nav2 Getting Started (free)**  

Link:  
[https://docs.nav2.org/rolling/getting_started/index.html](https://docs.nav2.org/rolling/getting_started/index.html)

Launches Nav2 in simulation in under five minutes, with a pre-configured VS Code dev container that removes all install pain  
五分钟内在仿真中启动 Nav2，带预配置的 VS Code 开发容器，消除所有安装痛苦

**2. Nav2 Tutorials (free)**  

Link:  
[https://docs.nav2.org/rolling/tutorials/](https://docs.nav2.org/rolling/tutorials/)

Covers SLAM, keepout zones, speed limits, collision monitoring, docking, GPS navigation, and writing your own planner, controller or behaviour-tree node  
覆盖 SLAM、禁区、速度限制、碰撞监控、对接、GPS 导航，以及写自己的规划器、控制器或行为树节点

**3. SLAM Toolbox (free, open source)**  

Link:  
https://github.com/SteveMacenski/slam_toolbox

The currently supported ROS 2 SLAM library, with synchronous, asynchronous, lifelong and localization-only modes, and multi-robot support  
当前支持的 ROS 2 SLAM 库，有同步、异步、终身和仅定位模式，以及多机器人支持

**4. RTAB-Map for ROS 2 (free, open source)**  

Link:  
https://github.com/introlab/rtabmap_ros

Appearance-based RGB-D and stereo SLAM with loop closure, for when you have a depth camera rather than a lidar, or want a 3D map  
基于外观的 RGB-D 和立体 SLAM，带闭环，适合你有深度相机而不是激光雷达，或想要 3D 地图时

**What to focus on:**  

- The difference between mapping and localizing, and when to switch SLAM Toolbox into localization mode  
  建图和定位的区别，以及何时把 SLAM Toolbox 切到定位模式
- Odometry quality, because SLAM Toolbox needs it and a smeared map is almost always an odometry problem rather than an algorithm problem  
  里程计质量，因为 SLAM Toolbox 需要它，模糊的地图几乎总是里程计问题而不是算法问题
- Costmap tuning: inflation radius, obstacle layers, and the local versus global split  
  代价地图调参：膨胀半径、障碍层，以及局部与全局的划分
- Behaviour trees, which is how Nav2 orchestrates everything and the part beginners fail to grasp  
  行为树，这是 Nav2 编排一切的方式，也是初学者抓不住的部分

Hardware for real SLAM, three tiers:  
真实 SLAM 的硬件，三档：

- **$0**: Gazebo with a simulated lidar. Do the entire SLAM and Nav2 curriculum here first  
  **$0**：Gazebo 带仿真激光雷达。先在这里完成整个 SLAM 和 Nav2 课程
- **$250 to $450**: DIY: RPLIDAR C1 at $69, a Raspberry Pi 4 or 5, a differential-drive base with encoders, a motor driver and a battery. Most learning per dollar, and the most yak-shaving  
  **$250 到 $450**：DIY：RPLIDAR C1 $69，树莓派 4 或 5，带编码器的差速底盘、电机驱动和电池。每美元学到最多，也最折腾
- **$300 to $535**: a ready platform. Hiwonder MentorPi M1 from **$299.99** runs ROS 2 Humble on a Pi 5 with lidar and a depth camera. Waveshare's UGV Rover ROS 2 kit at **$534.99** splits a Pi host and an ESP32 real-time controller, which is how real robots are actually architected  
  **$300 到 $535**：现成平台。Hiwonder MentorPi M1 从 **$299.99** 起，在 Pi 5 上跑 ROS 2 Humble，带激光雷达和深度相机。Waveshare UGV Rover ROS 2 套件 **$534.99**，分离 Pi 主机和 ESP32 实时控制器，这才是真实机器人的架构方式  
  Link: [https://www.hiwonder.com/products/mentorpi-m1](https://www.hiwonder.com/products/mentorpi-m1)  
  Link: [https://www.waveshare.com/ugv-rover-ros2-kit.htm](https://www.waveshare.com/ugv-rover-ros2-kit.htm)

**Practice task:** run SLAM Toolbox in your Gazebo world, teleop around it, save the map, then switch to localization mode and send Nav2 goals from RViz. Tune the costmaps until it stops clipping corners. Then screen-record it. A video of a robot autonomously navigating a map it built itself is the most compelling artifact a self-taught roboticist can produce  
**实践任务：** 在你的 Gazebo 世界里跑 SLAM Toolbox，遥操作转一圈，保存地图，然后切到定位模式，从 RViz 发送 Nav2 目标。调代价地图直到它不再切角。然后录屏。一个机器人自主导航它自己建的地图的视频，是自学机器人工程师能产出的最有说服力的作品

### Month 4 Milestone  
### 第 4 个月里程碑

By the end of this month you should be able to:  
到本月末你应该能够：

- Write ROS 2 nodes in both Python and C++ that use topics, services and actions  
  用 Python 和 C++ 写使用话题、服务和动作的 ROS 2 节点
- Describe your own robot in xacro with correct frames, inertias and collision geometry  
  用 xacro 描述自己的机器人，带正确坐标系、惯性和碰撞几何
- Simulate that robot in Gazebo with working lidar and camera sensors  
  在 Gazebo 中仿真该机器人，带能工作的激光雷达和相机传感器
- Configure ros2_control and drive the robot through a controller rather than raw commands  
  配置 ros2_control 并通过控制器而不是原始命令驱动机器人
- Build a map with SLAM Toolbox and navigate autonomously with Nav2  
  用 SLAM Toolbox 建图并用 Nav2 自主导航
- Diagnose a broken TF tree, which is the most common failure in the entire stack  
  诊断坏掉的 TF 树，这是整个栈中最常见的失败

⏩---------------------------------------------------------------------⏪

## Month 5: The maths that makes robots actually work  
## 第 5 个月：让机器人真正工作的数学

Your goal this month: understand and implement the control and perception underneath everything you have built  
本月目标：理解并实现你之前构建的一切之下的控制和感知

Up to now you have used libraries that did the hard parts for you  
到目前为止你一直在用库帮你做困难的部分

This month is where you learn what they were doing, because the difference between someone who can configure Nav2 and someone who can fix Nav2 when it misbehaves is exactly this material  
这个月你学习它们在做什么，因为能配置 Nav2 的人和能在它行为异常时修好它的人的区别，正是这些材料

You do not need all of it at research depth. You need working fluency in control, enough kinematics to reason about an arm, and enough vision to get 3D information out of a camera  
你不需要全部达到研究深度。你需要控制上的工作流利度、足够推理机械臂的运动学，以及足够从相机得到 3D 信息的视觉

### What to learn  

### 1. Control theory, starting with PID  
### 1. 控制理论，从 PID 开始

You already tuned a PID controller by feel in month two. Now learn why it worked  
你在第 2 个月已经凭感觉调过 PID 控制器。现在学习它为什么有效

**Resources:**  

**1. Understanding PID Control, MATLAB Tech Talks with Brian Douglas (free)**  
**1. Understanding PID Control，Brian Douglas 的 MATLAB Tech Talks（免费）**

Link:  
[https://www.mathworks.com/videos/series/understanding-pid-control.html](https://www.mathworks.com/videos/series/understanding-pid-control.html)

Seven parts covering what PID is, integrator windup, derivative filtering, tuning, and manual versus automatic tuning. The fastest route from zero to a controller that works this week  
七部分，覆盖 PID 是什么、积分饱和、微分滤波、调参，以及手动 vs 自动调参。从零到本周能工作的控制器最快路径

**2. Brian Douglas, Control System Lectures (free)**  
**2. Brian Douglas，控制系统讲座（免费）**

Link:  
[https://www.youtube.com/@BrianBDouglas/playlists](https://www.youtube.com/@BrianBDouglas/playlists)

Intuition-first explanations across PID, state space, robust control and drone control, and the best fit for someone with no formal controls course behind them  
以直觉优先的解释，覆盖 PID、状态空间、鲁棒控制和无人机控制，最适合没有正式控制课程背景的人

**3. The Fundamentals of Control Theory, Brian Douglas (free, Creative Commons)**  
**3. The Fundamentals of Control Theory，Brian Douglas（免费，知识共享）**

Link:  
[https://engineeringmedia.com/books](https://engineeringmedia.com/books)

The written companion to the videos, and a coherent narrative rather than scattered lessons  
视频的文字伴侣，是连贯叙述而不是零散课程

**4. Control Bootcamp, Steve Brunton (free)**  

Link:  
[https://www.youtube.com/playlist?list=PLMrJAkhIeNNR20Mz-VpzgfQs5zrYi085m](https://www.youtube.com/playlist?list=PLMrJAkhIeNNR20Mz-VpzgfQs5zrYi085m)

Thirty-nine videos and the right entry point to state space, controllability, observability, LQR and the Kalman filter  
三十九个视频，进入状态空间、可控性、可观性、LQR 和卡尔曼滤波的正确入口

**5. Feedback Systems, Åström and Murray (free PDF)**  

Link:  
[https://fbswiki.org/wiki/index.php/Feedback_Systems:_An_Introduction_for_Scientists_and_Engineers](https://fbswiki.org/wiki/index.php/Feedback_Systems:_An_Introduction_for_Scientists_and_Engineers)

The rigorous textbook, released free by Princeton University Press, for when you want the proper version without paying  
严谨教材，普林斯顿大学出版社免费发布，想要正式版本又不想付钱时用

**What to focus on:**  

- What each of P, I and D physically does, and the failure mode of each  
  P、I、D 各自物理上做什么，以及各自的失败模式
- Integrator windup, and why your arm slams when it comes off a limit  
  积分饱和，以及为什么手臂离开限位时会猛撞
- Why the derivative term amplifies sensor noise and needs filtering  
  为什么微分项放大传感器噪声并需要滤波
- Steady-state error, and when an integrator is the fix versus when gravity compensation is the fix  
  稳态误差，以及何时用积分器修复、何时用重力补偿修复
- Feedforward, which is the cheapest performance improvement most people never add  
  前馈，大多数人从未加的最便宜性能提升

**Practice task:** take the balancing robot from month two and implement three controllers on the same hardware: P only, PD, then PID with feedforward. Log the step response of each to a CSV, plot all three, and write up which one you would ship and why. That plot is worth more in an interview than any certificate  
**实践任务：** 拿第 2 个月的平衡机器人，在同一硬件上实现三个控制器：仅 P、PD，然后带前馈的 PID。把每个的阶跃响应记录到 CSV，画出三个，并写明你会发货哪一个以及为什么。那张图在面试里比任何证书都值钱

### 2. State space, LQR and MPC  
### 2. 状态空间、LQR 和 MPC

**Resources:**  

**1. Understanding Model Predictive Control, MATLAB Tech Talks (free)**  
**1. Understanding Model Predictive Control，MATLAB Tech Talks（免费）**

Link:  
[https://www.mathworks.com/videos/series/understanding-model-predictive-control.html](https://www.mathworks.com/videos/series/understanding-model-predictive-control.html)

Seven parts from why to use MPC through adaptive and nonlinear variants, and how to make it run fast enough to be real  
七部分，从为什么用 MPC 到自适应和非线性变体，以及如何让它跑得足够快以成为现实

**2. Underactuated Robotics, Russ Tedrake, MIT (free)**  

Link:  
[https://underactuated.csail.mit.edu/index.html](https://underactuated.csail.mit.edu/index.html)

This is where control theory becomes robotics: pendulums, cart-poles, walking, running and humanoids, with dynamic programming, LQR, Lyapunov analysis and trajectory optimisation. Free notes, free PDF and lecture videos  
控制理论变成机器人学的地方：摆、小车倒立摆、走路、跑步和人形，带动态规划、LQR、李雅普诺夫分析和轨迹优化。免费笔记、免费 PDF 和讲座视频

**What to focus on:**  

- Representing a system as state, input and output rather than a transfer function  
  把系统表示为状态、输入和输出而不是传递函数
- Why LQR is just a principled way of choosing gains  
  为什么 LQR 只是选择增益的原则性方法
- What MPC buys you, which is constraints, and what it costs, which is compute  
  MPC 给你带来什么（约束），以及它的代价（计算）
- Underactuation, and why a robot with fewer actuators than degrees of freedom needs completely different thinking  
  欠驱动，以及为什么执行器少于自由度的机器人需要完全不同的思考

**Practice task:** implement LQR for a simulated cart-pole in Python, then implement the same thing with a hand-tuned PID and compare how each handles a disturbance. Tedrake's notes give you the model, so you are implementing rather than deriving  
**实践任务：** 在 Python 中为仿真小车倒立摆实现 LQR，然后用手调 PID 做同样的事，比较它们如何处理扰动。Tedrake 的笔记给你模型，所以你是在实现而不是推导

### 3. Kinematics and dynamics  
### 3. 运动学与动力学

**Resources:**  

**1. Modern Robotics, Kevin Lynch, Northwestern (free book, code and videos)**  

Link:  
[http://hades.mech.northwestern.edu/index.php/Modern_Robotics](http://hades.mech.northwestern.edu/index.php/Modern_Robotics)

The free preprint of the standard textbook, plus companion libraries in Python, MATLAB and Mathematica and full video lectures. It uses screw theory and product-of-exponentials rather than DH parameters, which is cleaner and now the industry norm  
标准教材的免费预印本，加上 Python、MATLAB 和 Mathematica 的配套库以及完整讲座视频。它用螺旋理论和指数积而不是 DH 参数，更干净，现在是行业规范

**2. Modern Robotics Specialization (Coursera, free audit available)**  

Link:  
[https://www.coursera.org/specializations/modernrobotics](https://www.coursera.org/specializations/modernrobotics)

The same material as a structured six-course sequence with assessment, if you need deadlines to finish things  
同样材料，结构化为六门课序列带评估，如果你需要截止日期才能完成事情

**3. Robotics Toolbox for Python, Peter Corke (free, MIT)**  

Link:  
https://github.com/petercorke/robotics-toolbox-python

Forward kinematics, Jacobians, numerical IK, trajectory generation and fifty-plus real robot models including Franka and UR, so you learn by running code against real arms  
正运动学、雅可比、数值 IK、轨迹生成以及五十多个真实机器人模型包括 Franka 和 UR，所以你通过针对真实手臂跑代码来学习

**4. QUT Robot Academy, Peter Corke (free)**  

Link:  
[https://robotacademy.net.au](https://robotacademy.net.au/)

Over 200 video lessons of under ten minutes each, labelled by prerequisite level, and the best source of short atomic explanations of DH parameters, Jacobians and pose representation  
超过 200 个每段不到十分钟的视频课，按先修水平标注，是 DH 参数、雅可比和位姿表示短小原子解释的最佳来源

**What to focus on:**  

- Homogeneous transforms and composing them, which is the language of everything  
  齐次变换以及组合它们，这是一切的语言
- Forward kinematics, which is easy, and inverse kinematics, which is not  
  正运动学（容易）和逆运动学（不容易）
- The Jacobian, and what a singularity physically means when your arm suddenly cannot move sideways  
  雅可比，以及当你的手臂突然不能侧向移动时奇异点在物理上意味着什么
- Workspace limits, and joint limits versus reachability  
  工作空间限制，以及关节限制 vs 可达性
- Trajectory generation, and why you interpolate in joint space sometimes and Cartesian space other times  
  轨迹生成，以及为什么有时在关节空间插值、有时在笛卡尔空间插值

**Practice task:** compute the forward kinematics of your SO-101 arm by hand from its link lengths, then verify against the Robotics Toolbox. Then write a numerical IK solver that moves the end effector to a commanded XYZ, and watch what it does near a singularity. Feeling the arm lose a degree of freedom is what makes the concept stick  
**实践任务：** 根据连杆长度手算 SO-101 臂的正运动学，然后用 Robotics Toolbox 验证。再写一个数值 IK 求解器，让末端执行器移到命令的 XYZ，观察它在奇异点附近做什么。感觉手臂失去一个自由度才是让概念牢记的关键

### 4. Perception and computer vision  
### 4. 感知与计算机视觉

**Resources:**  

**1. FREE OpenCV Bootcamp (OpenCV.org official, free)**  

Link:  
[https://courses.opencv.org/courses/course-v1:OpenCV+Bootcamp+CV0/about](https://courses.opencv.org/courses/course-v1:OpenCV+Bootcamp+CV0/about)

The official two-to-three hour course from OpenCV themselves, covering image manipulation, filtering, edge detection, tracking and the DNN module. Start here rather than a paid course  
OpenCV 自己官方两到三小时课程，覆盖图像操作、滤波、边缘检测、跟踪和 DNN 模块。从这里开始而不是付费课程

**2. OpenCV Camera Calibration tutorial (official docs, free)**  

Link:  
[https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html](https://docs.opencv.org/4.x/dc/dbb/tutorial_py_calibration.html)

The canonical walkthrough with full Python code, from chessboard corners to undistortion to re-projection error. Every robotics engineer must be able to do this from memory  
权威走查，带完整 Python 代码，从棋盘角点到去畸变到重投影误差。每个机器人工程师都必须能从记忆中做这件事

**3. Cyrill Stachniss lectures, University of Bonn (free)**  

Link:  
[https://www.ipb.uni-bonn.de/online-training-robotics/](https://www.ipb.uni-bonn.de/online-training-robotics/)

Full university lecture recordings on mobile sensing, photogrammetry and SLAM, and the best free source on the geometric side: projective geometry, bundle adjustment, EKF and graph SLAM  
移动传感、摄影测量和 SLAM 的完整大学讲座录像，几何方面最好的免费来源：射影几何、光束法平差、EKF 和图 SLAM

**4. Open3D point cloud tutorials (free)**  

Link:  
[https://www.open3d.org/docs/release/tutorial/geometry/pointcloud.html](https://www.open3d.org/docs/release/tutorial/geometry/pointcloud.html)

Voxel downsampling, normal estimation, ICP registration, plane segmentation and clustering, with far less friction than PCL for anyone already in Python  
体素下采样、法线估计、ICP 配准、平面分割和聚类，对已经在用 Python 的人来说摩擦远小于 PCL

**What to focus on:**  

- Camera intrinsics and distortion, and doing a real calibration with a printed chessboard  
  相机内参和畸变，以及用打印棋盘做真实标定
- Pinhole projection, and the difference between image coordinates and world coordinates  
  针孔投影，以及图像坐标与世界坐标的区别
- Depth from stereo versus structured light versus time-of-flight  
  立体 vs 结构光 vs 飞行时间得到深度
- Point cloud basics: downsampling, plane fitting to find a table, clustering to find objects on it  
  点云基础：下采样、平面拟合找桌子、聚类找桌上的物体
- Why lighting changes break vision pipelines that worked yesterday  
  为什么光照变化会毁掉昨天还能工作的视觉管道

**Practice task:** calibrate an actual camera with a printed chessboard, save the intrinsics, then write a script that detects a coloured object and estimates its position in 3D relative to the camera. Then move the lighting and watch it fail, and fix it. That failure-and-fix write-up is portfolio material  
**实践任务：** 用打印棋盘标定真实相机，保存内参，然后写脚本检测彩色物体并估计它相对相机的 3D 位置。然后移动灯光看它失败，再修复。这种失败与修复的书面记录是作品集材料

### 5. Manipulation and MoveIt 2  

**Resources:**  

**1. MoveIt 2 Getting Started (free, open source)**  
**1. MoveIt 2 入门（免费，开源）**

Link:  
[https://moveit.picknik.ai/main/doc/tutorials/getting_started/getting_started.html](https://moveit.picknik.ai/main/doc/tutorials/getting_started/getting_started.html)

The official entry point, and the docs recommend Jazzy on Ubuntu 24.04 for the smoothest experience  
官方入口，文档推荐 Ubuntu 24.04 上的 Jazzy 以获得最流畅体验

**2. Pick and Place with MoveIt Task Constructor (free)**  

Link:  
[https://moveit.picknik.ai/main/doc/tutorials/pick_and_place_with_moveit_task_constructor/pick_and_place_with_moveit_task_constructor.html](https://moveit.picknik.ai/main/doc/tutorials/pick_and_place_with_moveit_task_constructor/pick_and_place_with_moveit_task_constructor.html)

The most useful manipulation tutorial in ROS 2, teaching how to decompose a task into stages and implement grasp generation, IK and collision management  
ROS 2 中最有用的操作教程，教你如何把任务分解成阶段并实现抓取生成、IK 和碰撞管理

**3. Robotic Manipulation, Russ Tedrake, MIT (free)**  

Link:  
[https://manipulation.csail.mit.edu/](https://manipulation.csail.mit.edu/)

Twelve chapters connecting hardware, kinematics, perception, grasping, planning and control into one coherent stack, and it now teaches model-based and learned approaches together, which is exactly how the industry now works  
十二章把硬件、运动学、感知、抓取、规划和控制连成一个连贯栈，现在同时教基于模型和基于学习的方法，这正是行业现在的工作方式

**4. Contact-GraspNet, NVIDIA (free code)**  

Link:  
https://github.com/NVlabs/contact_graspnet

Six-DOF grasp generation in cluttered scenes from a depth map, and the standard baseline for learned grasping  
从深度图在杂乱场景中生成六自由度抓取，是学习抓取的标准基线

**Practice task:** get MoveIt 2 planning motions for a simulated arm, add collision objects to the planning scene, and execute a pick and place. Then make it fail by placing an obstacle in the only viable path and observe how the planner behaves. Understanding planner failure is more valuable than watching it succeed  
**实践任务：** 让 MoveIt 2 为仿真机械臂规划运动，在规划场景中加入碰撞物体，执行拾取放置。然后在唯一可行路径上放障碍物让它失败，观察规划器如何表现。理解规划器失败比看它成功更有价值

### Month 5 Milestone  
### 第 5 个月里程碑

By the end of this month you should be able to:  
到本月末你应该能够：

- Implement and tune a PID controller and explain every term from measured data  
  实现并调 PID 控制器，并根据测量数据解释每一项
- Describe a system in state space and implement LQR on a simulated plant  
  用状态空间描述系统并在仿真对象上实现 LQR
- Compute forward kinematics by hand and solve IK numerically  
  手算正运动学并用数值方法解 IK
- Explain what a singularity is by pointing at a robot doing it  
  通过指着一个正在发生的机器人解释什么是奇异点
- Calibrate a camera and turn a pixel into a 3D position  
  标定相机并把像素变成 3D 位置
- Plan and execute a collision-free pick and place in MoveIt 2  
  在 MoveIt 2 中规划并执行无碰撞拾取放置

⏩---------------------------------------------------------------------⏪

## Month 6: Robot learning, specialisation, and becoming hireable  
## 第 6 个月：机器人学习、专精，以及变得可被雇佣

Your goal this month: pick one direction, build a portfolio piece in it, and start applying  
本月目标：选一个方向，在其中做出作品集作品，并开始申请

You now have the whole stack: electronics, embedded, mechanical, ROS 2, control and perception  
你现在有了完整栈：电子、嵌入式、机械、ROS 2、控制和感知

This month has two halves. The first is the frontier, which is teaching robots from demonstrations rather than programming them. The second is turning everything you have built into something that gets you hired  
这个月有两半。第一半是前沿：通过示范而不是编程教机器人。第二半是把你构建的一切变成能让你被雇佣的东西

**Part one:** modern robot learning  

This is the part of robotics that changed completely in the last two years, and it is the reason there is so much capital in the field  
这是过去两年完全改变的机器人学部分，也是这个领域有大量资本的原因

### 1. LeRobot  

LeRobot is Hugging Face's PyTorch library for real-world robotics, and it is the open hub the whole low-cost robot-learning world has converged on  
LeRobot 是 Hugging Face 的真实世界机器人 PyTorch 库，是整个低成本机器人学习世界汇聚的开放中心

The workflow is: teleoperate, record, train, deploy. You drive the robot by hand, demonstrations are saved as synchronised video and action data, a policy learns to imitate them, then it runs on its own  
工作流是：遥操作、记录、训练、部署。你用手驱动机器人，示范被保存为同步的视频和动作数据，策略学习模仿它们，然后它自己运行

**Resources:**  

**1. LeRobot documentation (free)**  

Link:  
[https://huggingface.co/docs/lerobot/index](https://huggingface.co/docs/lerobot/index)

The main docs, covering the full pipeline and every supported robot  
主文档，覆盖完整管道和每一个支持的机器人

**2. LeRobot repository (free, Apache 2.0)**  

Link:  
https://github.com/huggingface/lerobot

Over 26,000 stars, and the place to read how the policies are actually implemented  
超过 26000 星，阅读策略实际如何实现的地方

**3. Hugging Face Robotics Course (free, no hardware required)**  

Link:  
[https://huggingface.co/learn/robotics-course/unit0/1](https://huggingface.co/learn/robotics-course/unit0/1)

Runs entirely on simulated environments and public datasets, so you can do the whole thing before buying anything. Roughly 30 to 45 minutes per unit  
完全在仿真环境和公共数据集上运行，所以你可以在买任何东西之前做完整件事。每单元大约 30 到 45 分钟

**4. SO-101 setup guide (free)**  

Link:  
[https://huggingface.co/docs/lerobot/so101](https://huggingface.co/docs/lerobot/so101)

The exact port-finding, motor-setup, calibration and recording commands for the arm you built in month three  
你在第 3 个月建的机械臂的精确端口查找、电机设置、校准和记录命令

**What to focus on:**  

- The record-train-deploy loop end to end, on your own arm  
  在自己的臂上端到端的记录-训练-部署循环
- Dataset quality, because a policy trained on sloppy demonstrations is a sloppy policy  
  数据集质量，因为在马虎示范上训练的策略就是马虎策略
- ACT, which the docs recommend as the starting policy, and why predicting chunks of future actions works better than predicting single steps  
  ACT（文档推荐的起始策略），以及为什么预测未来动作块比预测单步更好
- Diffusion Policy, which represents the policy as a denoising process and reported a 46.9% average improvement over prior methods across twelve tasks  
  Diffusion Policy，把策略表示为去噪过程，在十二个任务上报告平均比先前方法提升 46.9%

**Practice task:** record 50 demonstrations of a single simple task on your SO-101, such as picking up a cube and dropping it in a bin, train an ACT policy, and deploy it. It will work maybe half the time. Then record 50 more demonstrations covering the failure cases and retrain. Document the success rate before and after. That number, and the fact that you measured it, is the portfolio piece  
**实践任务：** 在你的 SO-101 上记录 50 次单一简单任务的示范，比如拿起方块丢进箱子，训练 ACT 策略并部署。它可能一半时间能工作。然后再记录 50 次覆盖失败案例的示范并重新训练。记录前后的成功率。那个数字，以及你测量了它这一事实，就是作品集作品

### 2. Vision-language-action models  
### 2. 视觉-语言-动作模型

These are the foundation models of robotics, and knowing which ones you can actually run matters  
这些是机器人学的基础模型，知道哪些你真正能跑很重要

- **π₀, π₀-FAST and π₀.₅** from Physical Intelligence, **Apache 2.0, weights open**, pretrained on 10,000+ hours of robot data. The repo warns honestly that these were developed for their own robots and transfer is not guaranteed  
  Physical Intelligence 的 **π₀、π₀-FAST 和 π₀.₅**，**Apache 2.0，权重开放**，在 10000+ 小时机器人数据上预训练。仓库诚实警告这些是为他们自己的机器人开发的，迁移不保证  
  Link: https://github.com/Physical-Intelligence/openpi
- **OpenVLA**, 7B parameters, **fully open**, trained on 970,000 robot episodes from Open X-Embodiment, and the best-documented open VLA to read the code of  
  **OpenVLA**，70 亿参数，**完全开放**，在 Open X-Embodiment 的 97 万机器人片段上训练，是读代码最好文档化的开放 VLA  
  Link: [https://openvla.github.io/](https://openvla.github.io/)
- **GR00T N1.7** from NVIDIA, code Apache 2.0 with **weights under the NVIDIA Open Model License**, which is a distinction often reported wrongly. Needs 16GB+ VRAM for inference  
  NVIDIA 的 **GR00T N1.7**，代码 Apache 2.0，**权重在 NVIDIA Open Model License 下**，这个区别经常被错误报告。推理需要 16GB+ VRAM  
  Link: https://github.com/Nvidia/Isaac-GR00T
- **SmolVLA** from Hugging Face, compact and designed for affordable hardware, which is the right one to fine-tune on an SO-101 rather than reaching for a 7B model  
  Hugging Face 的 **SmolVLA**，紧凑且为平价硬件设计，是在 SO-101 上微调的正确选择，而不是去碰 70 亿模型  
  Link: [https://huggingface.co/lerobot/smolvla_base](https://huggingface.co/lerobot/smolvla_base)
- **RT-2** from Google DeepMind is historically important and **has no public weights**, so study the paper and use one of the above for practice  
  Google DeepMind 的 **RT-2** 历史上重要，**没有公开权重**，所以研究论文并用上面其中一个练习

### 3. Reinforcement learning for robotics  
### 3. 机器人强化学习

**Resources:**  

**1. MuJoCo Playground (free, Apache 2.0)**  

Link:  
https://github.com/google-deepmind/mujoco_playground

GPU-accelerated environments for locomotion, manipulation and vision tasks with four Colab tutorials, and far easier to get running than the alternatives. Start here  
用于运动、操作和视觉任务的 GPU 加速环境，带四个 Colab 教程，比替代品容易跑得多。从这里开始

**2. NVIDIA Isaac Lab (free, BSD-3)**  

Link:  
https://github.com/isaac-sim/IsaacLab

Sixteen robot models and thirty-plus pre-built training environments, integrating RSL RL, skrl, RL Games and Stable Baselines. The industry standard for legged and humanoid sim-to-real, and it needs the RTX hardware from month four  
十六个机器人模型和三十多个预构建训练环境，集成 RSL RL、skrl、RL Games 和 Stable Baselines。腿式和人形仿真到现实的行业标准，需要第 4 个月的 RTX 硬件

**3. CS 285, Deep Reinforcement Learning, Sergey Levine, UC Berkeley (free)**  

Link:  
[https://rail.eecs.berkeley.edu/deeprlcourse](https://rail.eecs.berkeley.edu/deeprlcourse)

The best RL course available, and Levine is a robotics researcher so the framing is robotics-native throughout, covering imitation learning, policy gradients, actor-critic, model-based and offline RL  
可用最好的 RL 课程，Levine 是机器人研究员，所以整个框架都是机器人原生的，覆盖模仿学习、策略梯度、actor-critic、基于模型和离线 RL

**Practice task:** train a quadruped locomotion policy in MuJoCo Playground from one of the Colab tutorials, then change the reward function and observe how the gait changes. You do not need hardware and you do not need a GPU beyond what Colab gives you free  
**实践任务：** 从 Colab 教程之一在 MuJoCo Playground 训练四足运动策略，然后改变奖励函数观察步态如何变化。你不需要硬件，也不需要超过 Colab 免费提供的 GPU

**Part two:** pick a direction  

Three directions genuinely exist. Pick one, and let the other two stay at literacy level  
三个方向真正存在。选一个，让另外两个保持素养水平

**Direction 1: Robot learning and embodied AI**  
**方向 1：机器人学习与具身 AI**

Best if you want the frontier companies and the highest ceiling  
如果你想要前沿公司和最高天花板，这是最好的

Focus on: LeRobot, VLA fine-tuning, imitation learning, RL, simulation, PyTorch  
重点：LeRobot、VLA 微调、模仿学习、RL、仿真、PyTorch

This is the highest-paid track and also the most competitive, and it is where a real dataset you collected yourself is worth more than any credential  
这是最高薪赛道也最竞争，也是你自己收集的真实数据集比任何证书都更值钱的地方

**Direction 2: Autonomy and mobile robotics**  

Best if you want the largest number of available jobs  
如果你想要最多可用工作，这是最好的

Focus on: ROS 2, Nav2, SLAM, perception, sensor fusion, C++  
重点：ROS 2、Nav2、SLAM、感知、传感器融合、C++

Controls engineer and field service engineer together are over 20% of all robotics postings, and this direction serves both  
控制工程师和现场服务工程师合起来占所有机器人岗位超过 20%，这个方向服务两者

**Direction 3: Embedded, mechatronics and integration**  
**方向 3：嵌入式、机电一体化与集成**

Best if you want to work immediately, including as a contractor  
如果你想立刻工作（包括作为承包商），这是最好的

Focus on: firmware, motor control, real-time systems, PLCs, functional safety, system integration  
重点：固件、电机控制、实时系统、PLC、功能安全、系统集成

This is the least glamorous and the most consistently employable, and it is where the technician-to-engineer path actually runs. Note that **66% of robotics projects report delays caused by certification**, so functional safety knowledge is a genuine and underserved specialism  
这是最不风光但最持续可雇佣的，也是技术员到工程师路径真正运行的地方。注意 **66% 的机器人项目报告因认证导致延误**，所以功能安全知识是真正且供给不足的专长

### 4. Your portfolio  

I looked at what recruiters in this field actually say they screen for, and the pattern is consistent  
我看了这个领域招聘人员实际说他们筛选什么，模式是一致的

**High signal:**  
**高信号：**

- GitHub repos with **logged metrics and a commit history that shows iterative debugging**, not a finished demo dropped in one commit  
  带**记录指标和显示迭代调试的提交历史**的 GitHub 仓库，而不是一次提交丢进的完成演示
- **Evidence of real-robot deployment** with reliability data, not simulation only  
  **真实机器人部署证据**带可靠性数据，而不是仅仿真
- Public datasets on the LeRobot Hub, where there are already tens of thousands of community datasets  
  LeRobot Hub 上的公共数据集，那里已经有数万社区数据集
- Contributions to the packages employers depend on: ROS 2 core, Nav2, MoveIt, Isaac Lab, LeRobot  
  对雇主依赖的包的贡献：ROS 2 核心、Nav2、MoveIt、Isaac Lab、LeRobot
- Systems integration work joining sensors to actuators to planning to control, with video and clear documentation  
  把传感器到执行器到规划到控制连起来的系统集成工作，带视频和清晰文档

**Red flags they name explicitly:**  

- Still on end-of-life ROS 1 with no migration evidence  
  仍在生命周期结束的 ROS 1 且没有迁移证据
- Claimed projects that cannot survive three follow-up questions  
  声称的项目经不起三个追问
- A pure deep-learning background with no kinematics or embodiment understanding  
  纯深度学习背景却没有运动学或具身理解
- Tutorial completion certificates, which are weighted far below real contributions  
  教程完成证书，权重远低于真实贡献

**Practice task:** take your three best projects and rewrite their READMEs. Each one needs a video at the top, a wiring or architecture diagram, the actual numbers you measured, and a section titled "what broke and how I fixed it". That last section is the single highest-value thing in a self-taught portfolio, because it is the part that cannot be faked from a tutorial  
**实践任务：** 拿你最好的三个项目重写它们的 README。每一个顶部需要视频、接线图或架构图、你测量的实际数字，以及一个标题为“什么坏了以及我怎么修的”的部分。最后这个部分是自学作品集中单一最高价值的东西，因为它是无法从教程伪造的部分

### 5. Interviews  
### 5. 面试

Robotics interviews are not software interviews, and leetcode is a much weaker predictor here  
机器人面试不是软件面试，leetcode 在这里预测力弱得多

Expect: inverse kinematics questions, PID and feedback loops, sensor fusion and Kalman filters, SLAM concepts, path planning including RRT, and C++ versus Python trade-offs  
预期：逆运动学问题、PID 和反馈环、传感器融合和卡尔曼滤波、SLAM 概念、包括 RRT 的路径规划，以及 C++ vs Python 权衡

Expect also, at good companies: a **simulation-based debugging exercise** where they hand you a MuJoCo or Isaac scene with a deliberately broken controller, a ROS 2 architecture problem scoped to the real job, and a long conversation about a specific past failure and how you diagnosed it  
在好公司还预期：**基于仿真的调试练习**，他们给你一个故意弄坏控制器的 MuJoCo 或 Isaac 场景、一个针对真实工作的 ROS 2 架构问题，以及关于一个具体过去失败和你如何诊断的长时间对话

Glassdoor has 1,721 robotics engineer interview questions on file from 877 companies if you want to read real examples  
Glassdoor 有来自 877 家公司的 1721 个机器人工程师面试问题，如果你想读真实例子  
Link: [https://www.glassdoor.com/Interview/robotics-engineer-interview-questions-SRCH_KO0,17.htm](https://www.glassdoor.com/Interview/robotics-engineer-interview-questions-SRCH_KO0,17.htm)

**Practice task:** have someone interrogate you about your own repo for twenty minutes. Not the concepts, your specific code. Why that gain, why that sensor, what happens if the battery sags, what did you try before this worked. If you cannot answer three levels deep, the project is not ready to be on your CV  
**实践任务：** 让别人就你自己的仓库拷问你二十分钟。不是概念，是你的具体代码。为什么那个增益、为什么那个传感器、电池电压下降会怎样、在这个工作之前你试了什么。如果你不能答到三层深度，这个项目还不适合放简历

### Month 6 Milestone  

By the end of this month you should be able to:  
到本月末你应该能够：

- Record a demonstration dataset and train a policy that runs on your own hardware  
  记录示范数据集并训练在自己硬件上运行的策略
- Explain the difference between behaviour cloning, ACT and diffusion policy  
  解释行为克隆、ACT 和扩散策略的区别
- Name which VLA models have open weights and which do not  
  说出哪些 VLA 模型有开放权重、哪些没有
- State which of the three directions you are pursuing, and why  
  说出你正在追求三个方向中的哪一个，以及为什么
- Show three portfolio projects with video, metrics and a documented failure analysis  
  展示三个带视频、指标和文档化失败分析的作品集项目
- Answer three levels of follow-up questions about any line of your own code  
  能回答关于你自己代码任何一行的三层追问
