---
layout:     post
title:      "创想三维（Creality）产品研究报告"
subtitle:   "创想三维（Creality）产品业务布局及核心技术"
date:       2026-08-27
author:     "Arvin"
header-img: "img/in-post/3D%20printer/creality_tables/post-creality-hg.jpg"
header-mask: 0.3
tags:
    - 3D 打印机
    - 3D printer
---

## 一、公司概况

![表格 01](/img/in-post/3D%20printer/creality_tables/table_01.png)

### 名字由来

"创想三维"（Creality）—— 取 "Creative Reality" 之意，寓意将创意变为现实。公司英文名 Creality 为 Creative + Reality 的合成词，体现"让创意成为现实"的使命。

### 业务版图

创想三维已从单一 3D 打印机制造商发展为 **AI 驱动的消费级创意平台**，业务涵盖：

```
创想三维（Creality Group）
├── 3D 打印设备（FDM + 光固化）
├── 3D 扫描仪（CR-Scan 系列）
├── 激光雕刻机（Falcon 系列）
├── 耗材与配件（Hyper PLA RFID、CFS 供料系统）
├── 软件平台（Creality Cloud、Creality Print）
└── 跨境电商（Nexbie 平台）
```


## 二、发展历程与里程碑

![表格 02](/img/in-post/3D%20printer/creality_tables/table_02.png)

> 💡 创想三维的发展轨迹体现了典型的深圳硬创路径：**低价爆品 → 全球化渠道 → 品类扩张 → 生态平台 → 资本市场**。早期以 Ender-3 奠定全球渠道基础，中期以 K 系列追赶 Bambu Lab 的高速/多色浪潮，近期以 SPARKX 子品牌和 AI 功能寻求差异化。


## 三、产品线全景

截至 2026 年 6 月，创想三维拥有 **八大产品线**：

```
旗舰级（K2 系列）      高性能级（K1 系列）      经典入门（Ender 3 V3）    入门多色（Hi/SPARKX）
─────────────────────────────────────────────────────────────────────────────────────
K2 Plus  (350³)  →    K1 Max    (300³)    →    E3 V3 Plus (300³) →    Hi Combo   (260³)*
K2 Pro   (300³)  →    K1C       (220³)    →    E3 V3 KE   (220³) →    SPARKX i7  (260³)
K2       (260³)  →    K1        (220³)    →    E3 V3 SE   (220³) →
                      K1 SE     (220³)    →    E3 V3      (220³) [经典]
* Hi Combo 已在部分区域下架

大尺寸（Ender 5）      特殊用途（CR）          光固化（HALOT）
───────────────────────────────────────────────────────────
Ender 5 Max (400³) →  CR-30 (∞ 传送带) →  HALOT-Mage
Ender 5 S1  (220³)                             HALOT-Sky
                                                HALOT-Ray

另外：3D 扫描仪（CR-Scan 系列）、激光雕刻机（Falcon 系列）
```
![](/img/in-post/3D%20printer/creality_tables/business%20overview.png)

![表格 03](/img/in-post/3D%20printer/creality_tables/table_03.png)

## 四、各系列产品详解

### 🔹 K2 系列 — 旗舰级（封闭式 CoreXY） {#41-k2-系列--旗舰级封闭式-corexy}

K2 系列是创想三维 2024–2025 年推出的旗舰产品线，代表公司最高技术水平，全部支持 CFS 多色打印。

#### K2 Plus（旗舰中的旗舰）
![表格 04](/img/in-post/3D%20printer/creality_tables/table_04.png)

> 🏆 K2 Plus 获得 **2025 Red Dot 设计奖**。

#### K2 Pro
![表格 05](/img/in-post/3D%20printer/creality_tables/table_05.png)

#### K2
![表格 06](/img/in-post/3D%20printer/creality_tables/table_06.png)

> 💡 K2 系列是创想三维"高端化"战略的核心。虽然定价仅为 Bambu Lab 同类产品的 60–80%，但硬件配置（尤其是 K2 Plus 的 350°C 喷嘴 + 350³ 体积 + 主动腔室加热）在纸面上已经超越了 X2D/H2D 的部分规格。然而，软件生态（Creality Print vs Bambu Studio）和社区模型库（Creality Cloud vs MakerWorld）仍是主要短板。


### 🔹 K1 系列 — 高性能级（封闭式 CoreXY） {#42-k1-系列--高性能级封闭式-corexy}

K1 系列是创想三维 2023 年推出的首款 CoreXY 高速产品线，对标 Bambu Lab X1/P1 系列。2025 年可通过 CFS 升级套件支持多色打印。

![表格 07](/img/in-post/3D%20printer/creality_tables/table_07.png)

**K1 系列核心技术特点**：
- **CoreXY 结构**：全系采用 CoreXY 构型，刚性铝合金框架
- **双齿轮直驱挤出机**：32 mm³/s 最大流量，兼容 PLA/ABS/PA/PC/碳纤维材料
- **AI 功能**（K1 Max/K1C）：AI LiDAR 首层检测、AI 摄像头炒面检测/异物检测/延时摄影
- **双风扇散热**：打印头风扇 + 18W 辅助腔室风扇
- **自动调平**：应变式传感器 + 双 Z 轴独立电机（K1 Max 为 LiDAR 辅助测平）
- **CFS 升级**：2025 年推出 **K1 系列 CFS 升级套件**（含外部切刀+缓冲器），可将多色功能赋予 K1 全系

> ⚠️ K1 系列发布初期曾面临挤压机堵塞、热端散热不足等问题，2024–2025 年通过硬件迭代（陶瓷加热块、快拆喷嘴）部分解决。作为创想三维的首代 CoreXY 产品，软件适配度和开箱体验不及 Bambu Lab 同期竞品。

### 🔹 Ender 3 V3 系列 — 经典入门级 {#43-ender-3-v3-系列--经典入门级}

Ender 3 系列是创想三维的"传奇产品线"，自 2018 年发布以来累计销售超百万台。2024 年全面升级为 V3 代。

![表格 08](/img/in-post/3D%20printer/creality_tables/table_08.png)

**Ender 3 V3 三大升级方向**：
1. **高速化**：从 50 mm/s → 250–600 mm/s（KE/Plus 支持 Klipper 固件 + 输入整形）
2. **刚性提升**：从 V 型槽轮 → 线性导轨（SE/KE/Plus），大幅减少维护
3. **智能化**：全系自动调平、彩色触摸屏（KE/Plus）、断料检测

> 💡 Ender 3 V3 Plus 是该系列最具竞争力的一款：300³ 级别大尺寸 + 600 mm/s 高速 + 直驱挤出 + $299 定价，是打印农场批量部署的热门选择。


### 🔹 Hi 系列 — 入门多色（开放式） {#44-hi-系列--入门多色开放式}

Hi 系列是创想三维 2025 年推出的入门级多色打印产品线，以 CFS 为核心卖点切入低价市场。

#### Hi Combo
![表格 09](/img/in-post/3D%20printer/creality_tables/table_09.png)

> ⚠️ Hi Combo 定位尴尬——SPARKX i7 在更低的价格点提供了更好的 AI 功能，而 K2 系列在高端提供了更完整的体验。在 SPARKX i7 发布后，Hi Combo 被迅速边缘化。

### 🔹 SPARKX i7 — AI 入门级（开放式） {#45-sparkx-i7--ai-入门级开放式}

SPARKX 是创想三维 2026 年推出的全新子品牌，定位 AI 驱动的入门级 3D 打印机，i7 是首款产品。

![表格 10](/img/in-post/3D%20printer/creality_tables/table_10.png)

> 🆕 SPARKX i7 直接对标 Bambu Lab A1 mini/A1。以更低价格（$259/$369 vs A1 的 $299/$449）提供 AI 功能，是 2026 年入门多色市场最具性价比的选择之一。

### 🔹 Ender 5 系列 — 大尺寸 {#46-ender-5-系列--大尺寸}

![表格 11](/img/in-post/3D%20printer/creality_tables/table_11.png)

> 💡 Ender 5 Max 是全球最大尺寸的量产消费级 3D 打印机之一，400³ mm 的打印体积特别适合 cosplay 道具、大型装饰件、批量打印小件。

### 🔹 CR 系列 — 特殊用途 {#47-cr-系列--特殊用途}

![表格 12](/img/in-post/3D%20printer/creality_tables/table_12.png)

CR 系列定位特殊应用场景。CR-30（又名 3DPrintMill）是全球首款量产传送带打印机，可沿 Z 轴无限连续打印（理论上）。

### 🔹 HALOT 系列 — 光固化（树脂） {#48-halot-系列--光固化树脂}

创想三维在光固化领域拥有完整的产品矩阵，是消费级 LCD 光固化市场的主要玩家之一。

![表格 13](/img/in-post/3D%20printer/creality_tables/table_13.png)

> 注：光固化产品线非本报告重点，此处仅简要列出。完整产品信息请参考创想三维官方渠道。

## 五、配件与生态系统

### 5.1 供料与配件 {#51-供料与配件}

### CFS（Creality Filament System）供料系统

CFS 是创想三维对标 Bambu Lab AMS 的多色/多材料供料系统。

#### 工作原理

```
┌────────────────────────────────────────────────────┐
│              CFS 主机                               │
│  ┌─────────┐ ┌─────────┐ ┌─────────┐ ┌───────────┐ │
│  │ Slot 1  │ │ Slot 2  │ │ Slot 3  │ │ Slot 4  │ │ │
│  │ RFID识别│ │ RFID识别 │ RFID识别 │    RFID识别 │   │
│  └────┬────┘ └────┬────┘ └────┬────┘ └────┬────┘   │
│       │           │           │           │        │
│       └───────────┴─────┬─────┴───────────┘        │
│                         │                          │
│                   自动切换+退料                     │
│                         │                          │
│                   密封防潮仓                        │
│               (内置干燥剂 / 温湿度显示)              │
└─────────────────────────┬──────────────────────────┘
                          │ CAN 总线
                          ▼
               ┌──────────────────┐
               │   3D 打印机       │
               │ (K2/K1/Hi/SPARKX)│
               └──────────────────┘
```

#### CFS 产品线

![表格 14](/img/in-post/3D%20printer/creality_tables/table_14.png)

#### CFS 核心特性

1. **RFID 自动识别**：使用创想三维 RFID 耗材时，系统自动读取材料类型、颜色、打印参数，无需手动设置
2. **自动续料**：耗材耗尽时自动切换到同类型同色备用卷
3. **密封防潮**：内置干燥剂仓 + 温湿度 LCD 显示屏，湿度超标报警
4. **自动颜色映射**：与 Creality Print 切片软件通信，按颜色匹配耗材槽位

### 耗材体系

![表格 15](/img/in-post/3D%20printer/creality_tables/table_15.png)

> ⚠️ CFS 兼容耗材限制：TPU（95A 及更软）、潮湿 BVOH/PVA、变形纸板卷轴不兼容。

### 5.2 软件与云平台 {#52-软件与云平台}

### Creality Print — 切片软件

Creality Print 是创想三维自主研发的桌面端切片软件，最新版本 6.3+。

![表格 16](/img/in-post/3D%20printer/creality_tables/table_16.png)

### Creality Cloud — 云平台与社区

![表格 17](/img/in-post/3D%20printer/creality_tables/table_17.png)

#### Creality Cloud 核心功能矩阵

```
Creality Cloud / Print
├── 打印
│   ├── 远程控制（多台打印机管理）
│   ├── 手机切片（FlowSlicer / FlowPrint PAD 版）
│   ├── 一键 3MF 打印
│   └── 延时视频
├── 创作
│   ├── AI 建模中心（MakeNow — 文生 3D/图生 3D）
│   ├── AI 搜索（图像搜索 + 语义搜索）
│   └── AI 上传助手（自动标签/分类/描述）
├── 社区
│   ├── Maker Verified 认证模型库
│   ├── 积分与激励机制
│   └── Nexbie 电商（2025 年 8 月上线）
└── 第三方兼容
    ├── OrcaSlicer 项目上传
    ├── 外部文件导入（微信/WhatsApp/Telegram）
    └── 多平台数据同步
```

### 竞品平台对比

![表格 18](/img/in-post/3D%20printer/creality_tables/table_18.png)

> 💡 Creality Cloud 在功能丰富度上（尤其是 AI 建模和第三方兼容性）实际上已超越 MakerWorld，但在社区活跃度、模型质量和用户粘性方面仍有明显差距。

## 六、产品对比矩阵

### FDM 打印机横向对比（2026 年 6 月在售主力机型）

![表格 19](/img/in-post/3D%20printer/creality_tables/table_19.png)

> \* K1 系列需要 CFS 升级套件才能支持多色打印，K2/Hi/SPARKX 原生支持。

### 与 Bambu Lab 主力机型对比

![表格 20](/img/in-post/3D%20printer/creality_tables/table_20.png)

## 七、技术特色与核心优势

### 核心技术矩阵

![表格 21](/img/in-post/3D%20printer/creality_tables/table_21.png)

### 技术深度分析

#### 1. FOC 闭环电机系统

创想三维在高端产品线（K2、Hi Combo）采用 FOC（Field-Oriented Control，磁场定向控制）步进伺服电机：

```
传统开环步进           FOC 闭环步进伺服
    │                      │
    │ 指令脉冲              │ 指令位置+速度+电流
    ▼                      ▼
┌─────────┐          ┌─────────────┐
│ 步进驱动器│          │ FOC 控制器    │
│ (无反馈) │          │ (电流/位置反馈)│
└────┬────┘          └──────┬──────┘
     │ 失步不感知              │ 实时补偿
     ▼                       ▼
  步进电机              步进伺服电机
                         (编码器反馈)
```

![表格 22](/img/in-post/3D%20printer/creality_tables/table_22.png)

> 💡 创想三维的 FOC 方案与拓竹的 PMSM 伺服挤出机在目标上一致（闭环挤出控制），但 PMSM 在采样频率（20 kHz）和推力峰值（8.5 kg）上有绝对优势。FOC 步进伺服可视为"够用"的铁氧体方案。

#### 2. AI 流量校准 vs 涡流传感器流量补偿

创想三维采用 **视觉方案**，拓竹采用 **电磁方案**：

![表格 23](/img/in-post/3D%20printer/creality_tables/table_23.png)

两种方案各有优劣。视觉方案的优势在于可复用摄像头硬件实现多重 AI 功能（监控+校准），但实时性不如电磁方案。创想三维的 AI 积累（来自 Creality Cloud 的海量打印数据）如果能和摄像头数据形成闭环，长期潜力值得关注。

#### 3. AI LiDAR 首层检测

K1 Max 搭载的 AI LiDAR 采用与拓竹 Micro LiDAR 类似的激光三角测量原理：

此 Lidar 为奥比中光提供的线激光

```
工作流程：
打印首层 → LiDAR 扫描表面 → 生成点云高度图 → AI 分析平整度
    → 自动补偿 Z 偏移 → 确保首层完美贴合
```

与拓竹 X1C Micro LiDAR 的区别：
- 拓竹 LiDAR 精度 7 μm，仅在打印前校准阶段工作（非实时）
- 创想三维 LiDAR 精度 50 μm，仅在首层扫描
- 拓竹 X1C 已于 2026 年 3 月 EOL，LiDAR 技术路线被涡流传感器取代

## 八、市场定位与竞争格局

### 市场地位

![表格 24](/img/in-post/3D%20printer/creality_tables/table_24.png)

>根据公开数据整理，不代表权威数据

### 竞争格局总览（2026 年）

![表格 25](/img/in-post/3D%20printer/creality_tables/table_25.png)

## 九、客户群体

### 用户画像

![表格 26](/img/in-post/3D%20printer/creality_tables/table_26.png)

## 附录：Sources

### 官方来源
- [创想三维官网](https://www.creality.com)
- [Creality Wiki](https://wiki.creality.com)
- [Creality Store（产品对比）](https://store.creality.com/pages/compare)
- [Creality Cloud](https://www.crealitycloud.com)
- [港交所招股说明书（03388.HK）](https://www.hkex.com.hk)

### 行业媒体
- [Tom's Hardware — Creality Hi Combo Review](https://www.tomshardware.com/3d-printing/creality-hi-combo-review)
- [Tom's Hardware — Bambu Lab Overtakes Creality](https://www.tomshardware.com/3d-printing/bambu-lab-overtakes-creality-as-the-worlds-top-selling-budget-3d-printer-brand)
- [3DPrint.com / CONTEXT Market Data](https://3dprintingindustry.com)
- [CNX Software — Falcon A1 Pro Review](https://www.cnx-software.com/2026/02/15/creality-falcon-a1-pro-review)
- [3Druck.com — SPARKX i7 发布](https://3druck.com/en/printers-and-products/answer-to-bambu-lab-creality-presents-the-sparkx-i7)
- [3Druck.com — Creality Cloud 7.3](https://3druck.com/en/programs/creality-cloud-7-3-slicing-via-smartphone-and-more-open-platform-55157234/)
- [KrASIA — Creality HK IPO Analysis](https://kr-asia.com/crealitys-hong-kong-listing-bid-lays-bare-its-retreat-in-consumer-3d-printing)

### 财经/分析
- [南方财经网 — 创想三维 IPO 报道](https://m.sfccn.com)
- [证券时报 — 拓竹战群狼](https://www.stcn.com/article/detail/3609058.html)
- [证券时报 — 增收不增利](https://www.stcn.com/article/detail/3684551.html)
- [澎湃新闻 — 创想三维深度分析](https://m.thepaper.cn/newsDetail_forward_33271863)
- [雪球 — 创想三维 vs 拓竹 2026 对比](https://xueqiu.com/4051442683/373724131)
- [南极熊 — TCT 亚洲展 创想三维](https://www.nanjixiong.com/thread-174136-1-1.html)

### 社区/评测
- [什么值得买 — K2 Pro vs K2 Plus 选购](https://post.smzdm.com/p/ae6po394/)
- [Reddit r/Creality](https://reddit.com/r/Creality)
- [Reddit r/3Dprinting](https://reddit.com/r/3Dprinting)
