---
summary: "3C 数码电子（充电宝 / 充电器 / 耳机 / 线材 / 外设）Amazon 图片结构骨架。覆盖 A+ 9 模块 + 主图 6 模块 + 出图 prompt 模板 + 风险清单。"
---

# 3C 数码电子类 · Amazon 图片结构骨架

_沉淀自 Anker Power Bank（20K, 87W, Built-In USB-C Cable）完整 15 张素材。_

## 适用范围

3C 数码配件与小型电子产品：

| 子品类 | 典型产品 | 核心卖点轴 |
|---|---|---|
| 移动电源 | 充电宝 / 无线充电宝 | mAh + W + 内置线 + 协议 |
| 充电头 | GaN 充电器 / 多口桌面充 | W + 口数 + GaN + 折叠脚 |
| 充电线材 | USB-C / Lightning / 数据线 | W + 长度 + 弯折次数 + MFi |
| 蓝牙耳机 | TWS / 头戴 / 运动耳机 | 续航 + 驱动 + ANC + 防水 |
| 键鼠外设 | 三模键盘 / 静音鼠标 | 连接 + DPI + 续航 + 静音 |
| 智能配件 | 手表 / 手环 / 音箱 | 续航 + 健康指标 + 防水 |

> 处理任意 3C 子品类时，先读本文，按"主卖点轴"映射到对应模块，最后用本文末「适配模板」做品类定制。

---

## 通用风格（Anker 风为基准，可品牌替换）

### 调色板

| 角色 | 颜色 | 用途 |
|---|---|---|
| 品牌主色 | `#0098E5`（Anker 蓝 / 科技蓝）| headlines、ribbon、icon、强调 |
| 产品色 | `#000000` 黑或 `#FFFFFF` 白 | 产品本身（充电宝 / 充电器主色）|
| 背景 | `#FFFFFF` 纯白 | 主图 + A+ 大量留白 |
| 辅色 | `#F5F5F5` 浅灰 | 表格底、卡片底 |
| 正文文字 | `#1A1A1A` 近黑 | 副标题、脚注 |
| 数据强调 | `#0098E5` 蓝 | 百分数、功率、容量数字 |

### 字体与排版

- **字体**：sans-serif（Inter / Helvetica 风），headlines 600 weight，副标题 400-500
- **headline 结构**：三段式 / 四段式（"Full-Speed. Cable-Ready. Every Device."），每段以 `.` 分隔
- **副标策略**：型号 + 关键 3 spec（"Anker Power Bank (20K, 87W, Built-In USB-C Cable)"）
- **数据优先**：每个 headline 都跟一个可量化卖点（W / mAh / % / 次 / °F / in / oz）

### 视觉语言

- **干净 + 大量留白**：产品放在白底，靠留白做高级感
- **真实 lifestyle 场景**：机场候机厅、酒店大堂、咖啡馆、家里桌面 → 比纯摆拍有人味
- **对比锚点**：充电宝与水瓶、咖啡杯、手机堆叠做"等价比较"
- **图标化**：功能列表用扁平 icon（电池、闪电、Type-C、飞机、盾牌）

---

## A+ 9 模块结构

> 画布统一 1792×1024 (16:9)，Pillow 后处理 resize 到 970×H。

### M1 · Hero + Badge + 5-Features（顶部主视觉）

**位置**：A+ 第 1 块——消费者首先看到，必须有冲击力

| 元素 | 内容 |
|---|---|
| 顶部 ribbon（左上）| "World's NO.1 Mobile Charging Brand" / "Editor's Choice" / "Best Seller" 类（第三方品牌必须替换文案）|
| 主标题（蓝、大号）| 三段式："Full-Speed. Cable-Ready. Every Device." |
| 副标题（黑）| 型号 + 关键 spec："Anker Power Bank (20K, 87W, Built-In USB-C Cable)" |
| 主图 | 产品 + 周边设备白底图（MacBook + iPhone + 充电宝连着内置线）|
| 底部 5 个 icon + 文案 | Built-In USB-C Cable / 1 USB-C Port / 1 USB A Port / Huge Capacity 20000mAh / Total 87W Output |

**画布**：970 × 600+（比 fashion 的 500 略高，因为有底部 icon 条）

### M2 · Quick Charge Speed 速度对比

| 元素 | 内容 |
|---|---|
| 居中 headline（蓝）| "Fast Charging for All" |
| 左侧产品图 | 充电宝连 iPhone + MacBook，"Total 87W / Single-Port 65W Max" |
| 右侧白面板 | "30-Minute Quick Charge" + 4 张设备卡：大号 % + ⚡ + 设备图 + 设备名 |
| 典型 4 卡 | iPhone 15 Pro 58% / Samsung S24 Ultra 66% / MacBook Air 52% / Steam Deck 24% |
| 脚注 | "Note: Data based on internal lab testing." |

**画布**：970 × 500

### M3 · Built-In Cable Recharge 内置线卖点

| 元素 | 内容 |
|---|---|
| 左图 | lifestyle 静物——产品在木桌、窗边、绿植背景（柔光）|
| 右侧 headline（蓝）| "Effortlessly Quick with Built-In Cable" |
| 副标（黑）| "Fully Recharged in 1 H 30 Min" |
| 脚注 | "Note: For optimal speed, use a charger with 65W output or more (not included). Data based on internal lab testing." |

**画布**：970 × 400

### M4 · Capacity Ecosystem 容量生态

| 元素 | 内容 |
|---|---|
| 左图 | 俯拍——产品居中 + 4-6 设备环绕（手机 / iPad / 笔记本 / 手表 / 耳机）|
| 右侧 headline（蓝）| "Huge 20,000mAh Capacity" |
| 副标（黑）| "Full Power, Zero Worries" |

**画布**：970 × 450

### M5 · Multi-Device 3-Photo 多设备充电

| 元素 | 内容 |
|---|---|
| 居中 headline（蓝）| "Built-In USB-C for All Your Devices" |
| 3 张白底图横排 | 分别接手机、平板、笔记本，每张左上角电池 icon + ⚡ |
| 脚注 | "Note: Use a Lightning cable (not included) to charge iPhone 14 models and earlier." |

**画布**：970 × 400

### M6 · Compatibility List 兼容清单

| 元素 | 内容 |
|---|---|
| 居中 headline（蓝）| "One Power Bank, Every Device" |
| 白面板左栏 | "Laptops and Tablets:" + 5-6 个设备缩略图 + 设备名（MacBook Air/Pro, iPad Air/Pro, Dell, Lenovo, HP）|
| 白面板右栏 | "Phones and Others:" + 6-8 个设备（iPhone 12-15, Samsung S22-S24, Switch, Steam Deck, Apple Watch, AirPods）|
| 右侧外缘 | 2 张产品角度照堆叠 |

**画布**：970 × 500

### M7 · Durability Lab Data 耐用性数据

| 元素 | 内容 |
|---|---|
| 居中 headline（黑、粗）| "Built-In Cable. Built to Last." |
| 左图 | 天平秤——产品 vs 标准水瓶（强调重量等价）|
| 右侧白面板 | "Built-In Cable Engineered for 10,000+ Cycles*" + "Designed for 5,000+ Bends" + 线缆特写 |
| 脚注 | "Note: Data based on internal lab testing." |

**画布**：970 × 400

### M8 · Travel: Airline 航空场景

| 元素 | 内容 |
|---|---|
| 左图 | 商务人士在机场候机厅用笔记本 + 手机 + 充电宝（飞机舷窗背景）|
| 右侧 headline（蓝）| "Boost Your Productivity with Rapid Charging" |
| 圆形 icon | ✈ + ✓ — "Airline-Approved" |

**画布**：970 × 400

### M9 · Travel: Vacation 度假场景

| 元素 | 内容 |
|---|---|
| 左图 | 度假场景（海边 / 泳池 / 度假酒店），用户用 iPad + 充电宝 |
| 右侧 headline（蓝）| "Keep the Energy Up on Vacation" |

**画布**：970 × 400

---

## 主图（Main）+ 副图（Sub）6 模块

> 主图必须 1:1 (1000×1000)；副图 1:1 或 4:5 (1000×1250)。

### Main 1 · Hero + Big Number 主 KV

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "Simultaneous Fast Charging" |
| 副标（黑）| "Full-Speed Charging for iPhone, Samsung, and More" |
| 中部超大蓝字 | "87W" |
| 中心 hero | 充电宝同时连 iPhone 和 MacBook |
| 右下文字 | "Single-Port 65W Max / Charge a 14" MacBook Pro to 50% in 40 Min" |

**画布**：1000 × 1000（1:1 严格）

### Main 2 · Quick Charge Cards 速度卡组

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "Cable-Ready Fast Charging" |
| 副标（黑）| "30-Minute Quick Charge" |
| 4 张白底卡 2×2 | 大号 % + ⚡ + 设备图 + 设备名 |
| 底部 photo | 充电宝在木桌上充电的静物图 |
| 底部 banner | "Fully Recharged in 1 H 30 Min at 65W" |

**画布**：1000 × 1300（4:5 竖版）/ 也可 1:1

### Main 3 · Capacity Counts 容量次数

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "20,000mAh Unlimited Power" |
| 4 列充电次数表 | iPhone 15 Pro 4 / Galaxy S24 Ultra 3 / MacBook Air 1.2 / Steam Deck 0.8（Charges）|
| 中部 hero | 产品 + 4 设备环绕俯拍 |
| 圆形 icon | ✈ + ✓ — "Airline-Approved" |

**画布**：1000 × 1300

### Main 4 · Durability Cycles 耐用次数

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "Built-In Cable Engineered to Last" |
| 巨大蓝字 + 小字 | "10,000+" + "Band Lifespan*" |
| 中心产品大图 | 产品竖直旋转 5°，USB-C 线展开 |
| 左下 2 个 icon | "11 lb Pull Resilience" / "5,000 Bends and Twists" |
| 脚注 | "*Data based on internal lab testing." |

**画布**：1000 × 1300

### Main 5 · Safety Features 安全特性

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "Charge Anywhere. Power All Your Devices." |
| 2 张 lifestyle 横排 | 机场办公 + 桌面办公 |
| 中部 headline（蓝）| "Enhanced Safety Features" |
| 副标（黑）| "864,000 Temperature Checks per Day" |
| 中心产品 + 尺寸标注 | 6.2 in / 2.9 in / 1.0 in |
| 两侧 icon | 15.5 oz / 6.2 × 2.9 × 1.0 in |

**画布**：1000 × 1500

### Main 6 · Weight Comparison 重量对比

| 元素 | 内容 |
|---|---|
| 顶部 headline（蓝）| "About the Weight of a Standard Water Bottle" |
| 大图 | 天平秤——产品在左托盘，标准矿泉水瓶在右托盘（视觉等价 ≈ 15.5 oz）|
| 中部 icon + 数字 | "15.5 oz" |
| 尺寸标注 | 6.2 in 高、2.9 in 宽、1.0 in 厚 |

**画布**：1000 × 1300

---

## 出图提示词模板（标准 8 字段格式）

```
品类：<3C 子品类>
页面位置：<a-plus / main / sub>
画布：1792×1024 (16:9) [A+] / 1024×1024 (1:1) [main] / 1024×1280 (4:5) [sub]
文字策略：
  - 主标题：<文案>
  - 副标题：<文案>
  - 角标 / ribbon：<文案>
  - 脚注：<文案>
模块目标：<一句话核心卖点>
提示词：
[完整英文 prompt]
风险检查：
  - 第三方品牌 logo：Apple / Samsung / Anker / iPhone / MacBook / Steam Deck / Nintendo Switch → 用 generic 描述
  - 数据 claim：W / mAh / % / 次必须基于真实 SKU 检测报告
  - "Airline-Approved" / "TSA-Compliant" 需 UN38.3 / FAA / 民航局认证
```

### 完整示例：M1 Hero+Badge+5-Features

```
品类：移动电源
页面位置：a-plus
画布：1792×1024 (16:9)，生成后 Pillow resize 到 970×600
文字策略：
  - 左上 ribbon：World's NO.1 Mobile Charging Brand 徽章
  - 主标题（蓝 #0098E5）：Full-Speed. Cable-Ready. Every Device.
  - 副标题：Anker Power Bank (20K, 87W, Built-In USB-C Cable)
  - 底部 5 icon：Built-In USB-C Cable / 1 USB-C Port / 1 USB A Port / 20000mAh / 87W Output
模块目标：品牌露出 + 5 大卖点一眼锚定
提示词：
Amazon A+ Content module, 970px-wide flat editorial layout. Top-left: blue ribbon badge
"World's NO.1 Mobile Charging Brand" in #0098E5. Center top: large blue #0098E5 sans-serif
bold headline "Full-Speed. Cable-Ready. Every Device." with black subtitle "Anker Power Bank
(20K, 87W, Built-In USB-C Cable)". Center hero: a black rectangular power bank with built-in
USB-C cable connecting it to a silver laptop and a black smartphone, all on pure white
background, soft studio light, slight top-down 3/4 angle. Bottom strip: 5 circular blue
outline icons evenly spaced — Built-In USB-C Cable / 1 USB-C Port / 1 USB A Port / Huge
Capacity 20000mAh / Total 87W Output, each with one-line caption below. Clean Anker
editorial style, no extra text, no third-party logos.
风险检查：
  - "World's NO.1" 是 superlative，必须有 Counterpoint / IDC 等第三方报告支撑；否则改 "Best-Selling"
  - 笔记本 / 手机 logo 不能复刻 Apple / Samsung；用 generic 银色笔电 + 黑色手机
  - 20000mAh / 87W 必须按真实 SKU 标签
```

---

## 风险检查清单（3C 重点）

| 风险项 | 触发场景 | 处理 |
|---|---|---|
| Apple 设备 logo | A+ M2/M4/M5/M6 + Main 1/2/3 | 用 generic 银色金属笔电 + 黑色手机，禁复刻 Apple logo |
| Samsung / Galaxy logo | 同上 | 同上 |
| Anker 品牌 logo | 所有模块左上 ribbon | 用户品牌可保留；第三方品牌必须替换 |
| "World's NO.1" 类 superlative | M1 ribbon | 必须有 Counterpoint / IDC 报告，否则改 "Best-Selling" |
| 容量数据 (mAh) | M1/M2/M4/M6 + Main 3 | 100% 按真实 SKU 标签——亚马逊 Capacity Claim 政策硬红线 |
| 充电功率 (W) | M1/M2 + Main 1 | 按真实协议（PD 3.1 / QC 5 / SCP），写实验室实测值，不夸大 |
| 充电次数 | Main 3 | 电池容量 ÷ 设备电池容量计算，注明 "based on internal lab testing" |
| 充电速度 % | M2 + Main 1/2 | 必须有 OEM 报告（30-min 测试），配脚注 |
| "Airline-Approved" | M8 + Main 3 | UN38.3 + < 100Wh（民航局 100Wh 上限）|
| 安全特性（temp checks）| Main 5 | 不能虚构数字（864,000/day 来自 Anker 公开 spec）|
| 重量 / 尺寸 | M7 + Main 5/6 | 实测数据，不能 P 图美化 |
| "5,000+ Bends" / "10,000+ Cycles" | M7 + Main 4 | 实验室数据，必须有 OEM 检测报告支撑 |

---

## Pillow 后处理

| 输出类型 | 建议生图尺寸 | 目标尺寸 | 处理 |
|---|---|---|---|
| A+ 模块 | 1792×1024 | 970×H 等比 | resize，宽度锁 970 |
| Main 主图 | 1024×1024 | 1000×1000 | resize，1:1 严格 |
| Sub 副图 4:5 | 1024×1280 | 1000×1250 | resize |
| Sub 副图 1:1 | 1024×1024 | 1000×1000 | resize |

**统一后处理代码**：

```python
from PIL import Image
img = Image.open(path).convert("RGB")
w, h = img.size
target_w = 970  # A+；主图/副图改成 1000
new_h = round(h * target_w / w)
img.resize((target_w, new_h), Image.LANCZOS).save(out_path)
```

---

## 适配其他 3C 子品类

### 充电器（GaN 充电头）

- **核心卖点**：W + 口数 + GaN III + 折叠脚
- **A+ 顺序建议**：M1 Hero+GaN → M2 多口同时充 → M3 体积对比（vs 传统充电器）→ M4 兼容设备 → M5 旅行场景
- **主图核心**：65W / 100W 大字 + 笔电+手机双充电 hero
- **替换模块**：M2 Quick Charge % 卡组保留；M3 改为 "GaN Tech"；M4 改为多口设备图；M7 耐用性改为温控 / 安全

### 蓝牙耳机（TWS）

- **核心卖点**：续航（H）+ 驱动单元（mm）+ ANC 降噪深度（dB）+ 防水（IPX）
- **A+ 顺序建议**：M1 Hero+ANC → M2 续航 → M3 音质 → M4 佩戴场景 → M5 防水 → M6 兼容（设备配对）→ M7 耐用（跌落 / 弯折盒）
- **主图核心**：ANC / 续航 H / 通话清晰度 三选一
- **替换模块**：M2 Quick Charge % 卡组 → 续航 H 数表；M3 充电 → "Charged in 10 Min for 5 H Play"

### 数据线（USB-C / Lightning）

- **核心卖点**：W 承载 + 长度（ft / m）+ 弯折次数 + MFi 认证
- **A+ 顺序建议**：M1 Hero+MFi → M2 弯折测试 → M3 充电速度 → M4 兼容设备 → M5 长度选项 → M6 收纳场景
- **主图核心**：100W / 6ft / 30,000 bends 三选一
- **替换模块**：M3 Built-In Cable → "Built to Last 30,000 Bends"；M4 Capacity → 长度对比 / 多设备

### 键盘 / 鼠标

- **核心卖点**：连接（2.4G + BT 5.1 + 有线三模）+ DPI + 续航 + 静音
- **A+ 顺序建议**：M1 Hero+三模 → M2 多设备切换 → M3 续航 → M4 静音声 → M5 桌面场景
- **主图核心**：3 台设备同时切换 hero + DPI 大字
- **替换模块**：M2 Quick Charge % → 续航 H 数表；M3 Built-In Cable → "Tri-Mode Connectivity"；M7 Durability → 击键寿命（5000 万次）

### 智能手表 / 手环

- **核心卖点**：续航（H）+ 健康指标（血氧 / 心率 / 睡眠）+ 防水（5ATM）+ 表盘数量
- **A+ 顺序建议**：M1 Hero+续航 → M2 健康监测 → M3 运动模式 → M4 防水 → M5 表盘 → M6 兼容
- **主图核心**：14 天续航 + AMOLED 大屏 + 100+ 运动模式 三选一
- **替换模块**：M3 Built-In Cable → "14-Day Battery"；M4 Capacity → 多运动模式表

### 智能音箱

- **核心卖点**：音质（W）+ 麦克风数 + 智能助手 + 防水（户外款）
- **A+ 顺序建议**：M1 Hero+音质 → M2 360° 环绕声 → M3 语音助手 → M4 智能家居联动 → M5 户外场景
- **主图核心**：360° sound + 多房间联动 hero

---

## 与 fashion.md 的关键差异

| 维度 | fashion（服装鞋帽）| 3c（数码配件）|
|---|---|---|
| 背景 | 杂志感白底 + 米金色 | 极简纯白 + 科技蓝 |
| 主标题 | 手写体品牌 + serif 粗体 | sans-serif 全大写 + 数字强调 |
| 模块数 | 6 模块 | A+ 9 + 主图 6 |
| 卖点轴 | 版型 / 面料 / 场景 | 容量 / 功率 / 速度 / 兼容 |
| 数据形式 | 主观描述（"soft / breathable"）| 客观数据（W / mAh / % / 次）|
| 风险侧重点 | 版型漂移 / 身材夸大 / 第三方 IP（Luke's Diner）| 容量虚标 / Apple logo / "World's NO.1" superlative |
| 文案语气 | lifestyle / 时尚杂志 | 科技 / 工程参数 |

---

_This file is part of the `ss-amazon-image-generation` skill. Read alongside `references/fashion.md` for full coverage of clothing and 3C electronics categories. Update when new sub-categories emerge._