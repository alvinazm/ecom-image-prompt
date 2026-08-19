---
summary: "家具（电脑桌 / 书桌 / 收纳柜 / 学习桌）类 Amazon 图片结构骨架。覆盖主副图 7 模块 + A+ 复合长图 + 出图 prompt 模板 + 风险清单。沉淀自 47'' Computer Desk With Fabric File Drawers Cabinet 完整 8 张素材。"
---

# 家具（电脑桌 / 书桌 / 收纳） · Amazon 图片结构骨架

_沉淀自 **47 Inch Computer Desk With Fabric File Drawers Cabinet**（黑橡木纹桌面 + 金属支架 + 3 层布抽屉 + 侧挂袋 + RGB 游戏场景）完整 8 张素材：A+ 复合长图 ×1 + 主图 2000×2000 ×1 + 副图 6 张。源码图存放在 `references/sources/furniture_47_desk/`。_

## 适用范围

家具品类里「**电脑桌 / 书桌 / 游戏桌 / 学习桌 / 化妆桌 / 收纳柜 / 文件柜**」一类 Amazon Listing。这一类的共同特征：

| 子品类 | 典型产品 | 核心卖点轴 |
| --- | --- | --- |
| 电脑桌 / 游戏桌 | 47'' 电脑桌 / L 型桌 / 升降桌 | 尺寸 + 抽屉数 + 承重 + 多功能 + 风格 |
| 书桌 / 学习桌 | 学生桌 / 简约书桌 / 折叠桌 | 尺寸 + 抽屉 + 易组装 + 安全圆角 |
| 化妆桌 | 带镜化妆桌 / 梳妆台 | 镜 + LED + 抽屉 + 风格 |
| 收纳柜 / 文件柜 | 布抽屉柜 / 文件柜 / 书架 | 层数 + 单格尺寸 + 承重 + 折叠 |
| 多功能桌 | 带书架 / 带打印机架 / 带侧挂袋 / 带充电口 | 一体化 + 节省空间 |

> 处理家具子类时，先读本文，按"核心卖点轴"映射到对应模块，最后用本文末「适配模板」做品类定制。

---

## 通用风格（47'' 桌为基准，可品牌替换）

### 调色板

| 角色 | 颜色 | 用途 |
| --- | --- | --- |
| **品牌主色（teal）** | `#3BB7AF`（teal/青绿，标准 ~`#2EBDB4`–`#43C6B7` 之间）| pill 标签底色、headline banner、icon stroke、维度数字、品牌强调 |
| 品牌主色副调 | `#5BCFC8` 浅 teal | 渐变、阴影、辅助 highlight |
| 产品色 | `#1A1A1A` 近黑 / 木纹深棕 | 桌面 + 金属架 + 抽屉 |
| 背景 | `#FFFFFF` 纯白 | 主图 + A+ 全部模块（大留白） |
| 辅色 | `#F5F5F5` 浅灰 | 表格底、卡片底 |
| 正文文字 | `#1A1A1A` 近黑 | 副标、脚注、说明段 |
| 数据强调 | `#3BB7AF` teal | 尺寸数字、容量数字、关键 spec |
| 装饰灰色 | `#888888` 中灰 | "Good waterproof effect" 类次要描述 |

### 字体与排版

- **字体方向**：clean modern sans-serif（Inter / Helvetica / Roboto 风），headline 字重 600-700，副标 400-500。**不要**用衬线体或手写体（家具不像服装/美妆需要品牌温度）
- **headline 结构**：
  - Banner 风："Product Dimensions" / "3-Tier Fabric Drawers" / "Removable Storage Function"——白字大写 + teal 实底矩形
  - Inline 风："Reversible Drawers Unit & Easy Installation" / "Adjustable File Drawer for Different Sizes Files"——teal 字 + teal 小图标 + 细线分隔
- **文字策略**：AI 直接出字适合大字、短句、teal pill 标签、4-6 个英文单词以内的标题；尺寸数字、参数表、密集说明段必须用 Pillow 后期确定性排版叠字
- **数字策略**：所有尺寸数字用 teal 色 + 紧贴标注线，像 "46.6"" / "19.7"" / "29.5"" 这种带双引号的 imperial 标注是这套风格的识别度

### 视觉语言

- **干净 + 大量留白**：产品放在白底，靠留白做高级感（与 3C Anker 风同源）
- **真实 lifestyle 场景**：卧室窗边 + 椅子 + RGB 灯条 + 摆件 + 地毯 → 比纯摆拍有人味
- **细线标注**：尺寸图全部用 1px 浅灰引导线 + teal 数字 + 末端小尖头
- **胶囊 pill**：teal 圆角矩形 + 白字 600 weight 居中（典型尺寸：宽 auto × 高 ~50px，圆角 25px）
- **扁平 icon**：3-5px teal 描边、纯线稿、不要渐变——「Books / Wallet / Files / Laptop」「Waterproof / Structural / Leg Pads」都是这种处理
- **3-grid callout**：功能图常用 1 大 + 2 小 或 2×2 网格 + pill 标签贴角
- **横向多模块堆叠**：build quality 这类多卖点常拆成 3 行横条，每行 image-left + text-right 交替

---

## 主副图 7 模块结构（Listing 上半部分）

> 画布统一 1792×1024 (16:9) 生图成功率最高，再用 Pillow resize 到目标模块尺寸裁切到位。本套的 7 张图：

### 模块总览

| # | 模块名 | 页面位置 | 画布 | 最终尺寸 | 模块目标 |
| --- | --- | --- | --- | --- | --- |
| M0 | Main Hero 主图 | `main-image` | 2000×2000 | 2000×2000 | 搜索曝光第一眼 + 白底产品 |
| S1 | Room Lifestyle 卧室场景 | `gallery-secondary`（2nd） | 1792×1024 → 2000×1500 | 2000×1500 (4:3) | 真实使用场景 + 风格锚点 |
| S2 | Product Dimensions 尺寸图 | `gallery-secondary`（3rd） | 1792×1024 → 2000×1700 | 2000×1700 (约 7:6) | 关键 spec + 购买决策 |
| S3 | File Drawer 3-Callout 文件抽屉 | `gallery-secondary`（4th） | 1792×1024 → 2000×1800 | 2000×1800 | 文件收纳功能证明（3 卖点） |
| S4 | 3-Tier Drawers + Icons 三层抽屉 | `gallery-secondary`（5th） | 1792×1024 → 2000×1800 | 2000×1800 | 收纳容积 + 4 种物品适配 |
| S5 | Removable Storage 侧挂袋 | `gallery-secondary`（6th） | 1792×1024 → 2000×1700 | 2000×1700 | 配件功能 + 桌面扩展 |
| S6 | Build Quality Stack 做工堆叠 | `gallery-secondary`（7th） | 1792×1024 → 2000×2300 或 970×逐行 | 2000×2300 | 工艺/材质/结构三段证据 |

> **画布规则**：本套大量使用 4:3 / 7:6 / 9:10 一类"略高"竖向矩形而非纯方，因为家具需要"地面 + 上方空间"或"产品 + 上方装饰/标注"。后续要复用到其它家具子品类时，主图仍强制 2000×2000 方形，副图可按模块需要选 4:3 / 3:4 / 9:16。

---

### M0 · Main Hero 主图

**版式**：纯白背景 #FFFFFF + 桌面产品正面/3/4 角 + 配件摆放

**关键元素**
- 桌面整体可见（含抽屉、侧挂袋、桌腿）
- 桌面上自然摆放 1-2 件日常物品（显示器、键盘、Switch、智能音箱）
- 抽屉开 1-2 个露出内容（相机、书、文件）
- 投影 / 阴影非常轻（避免主图加杂元素被判违规）

**风险检查硬要求**
- 背景必须纯白 #FFFFFF，不能有渐变、地板、阴影线
- 不能有文字 / logo / 边框 / 促销角标
- 不能放未包含物（卖的桌不含显示器的，画面里的显示器只能算"暗示使用"，不能喧宾夺主）
- 产品须占画面主面积 ≥85%

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：main-image
画布：2000×2000（直接生成 1792×1024 后 Pillow 居中裁方）
文字策略：无字（主图绝不放字）
模块目标：搜索曝光第一眼 + 白底产品清晰
提示词：
Studio product photography, pure white background #FFFFFF, a 47-inch black
computer desk with three black fabric drawers on the right side and a hanging
storage bag on the left. The desk surface shows a computer monitor, RGB keyboard,
mouse, Nintendo Switch and a smart speaker. Two fabric drawers are pulled halfway
out showing camera and books inside. Shot at three-quarter angle slightly above
eye level, soft even studio lighting with no harsh shadow, product fills 90% of
frame, sharp focus, no text no logo no watermark, photorealistic.
风险检查：背景纯白 / 无字 / 无竞品对比 / 无夸大 claim / 显示器键盘等为场景道具不需真实包含
```

---

### S1 · Room Lifestyle 卧室场景

**版式**：真实卧室角落全景——窗边 + 窗帘 + 椅子 + 装饰 + RGB 灯条 + 地毯

**关键元素**
- 完整 setup：桌 + 椅 + 侧置书架 + 装饰品（手办、霓虹灯、挂画）
- RGB 三角色块灯在墙上做氛围
- 自然光从窗户进，营造真实生活感
- 椅子要展示出 ergonomic / gaming / office 调性

**适配**
- 学习桌：换成书桌 + 椅子 + 台灯 + 书架场景
- 化妆桌：换成卧室 + 梳妆台 + 镜前灯 + 化妆品场景
- 收纳柜：换成衣帽间 + 玄关 + 客厅角落

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×1500
文字策略：场景图不放文字（卖点留给 S2-S6）
模块目标：真实使用场景 + 风格锚点（gaming / home office / 多功能）
提示词：
Interior photography, a real bedroom corner with a 47-inch black wood-grain
computer desk next to a window. A grey ergonomic gaming chair with footrest in
front of the desk. On the desk: a gaming monitor displaying an MSI Championship
poster, RGB mechanical keyboard, mouse, ring light, Nintendo Switch and a small
figurine. To the left of the desk a 4-tier black metal shelf with manga, action
figures and a digital clock showing "X:01". Above the desk RGB triangular wall
lights glow pink and blue, a small floating shelf with anime figures on the right
wall, a soft grey curtain on the left window. Light wooden floor with a grey
rug under the chair. Soft warm afternoon light, no text, no logo, no watermark,
photorealistic, 4:3 aspect ratio.
风险检查：墙面装饰不出现第三方 IP logo（手办不画特写品牌）；rgb 灯不抢镜；窗外景深自然
```

---

### S2 · Product Dimensions 尺寸图

**版式**：白底 + 桌子 3/4 角度 + teal banner 顶标 "Product Dimensions" + 浅灰标注线 + teal 双引号尺寸数字 + 3 icon 顶部 badge（Heavy Duty / Environment / 3 Drawers）

**关键元素**
- 顶部 banner：teal 实底矩形（约 200px 高）+ 白字 48-60pt "Product Dimensions"
- 桌体 3/4 透视，方便同时展示长、宽、高
- 标注线：1px #CCCCCC 浅灰
- 数字：teal #3BB7AF + 字重 600 + 带 inch 符号 ("") — 例 `46.6"` `19.7"` `29.5"`
- 单独模块的「抽屉」或「关键部件」可再单独拆出尺寸小图
- 顶部三 badge：图标 + 文字（如 "Heavy Duty Metal Design" / "Environment all protection" / "3 Fabric Drawers"）

**规范**
- 数字必须可读 ≥ 24px，不要 14px 这样的小字
- 标注线交叉处要断开避免视觉乱
- 抽屉单独拆图时，也要带尺寸（`13.5" x 13.5" x 6.1"` 这种）

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×1700
文字策略：teal banner 标题 + teal 双引号尺寸数字 + 1px 浅灰标注线
模块目标：关键 spec + 购买决策
提示词：
Amazon product specifications diagram on pure white background. A 47-inch
black wood-grain computer desk shown at three-quarter perspective.
Top: a teal #3BB7AF full-width banner (about 200px tall) with white bold
sans-serif text "Product Dimensions". Below the banner three feature badges
in a row: weight icon + "Heavy Duty Metal Design", recycle icon + "Environment
all protection", three-drawer icon + "3 Fabric Drawers".
Around the desk, thin light grey 1px annotation lines point to each dimension
with teal #3BB7AF bold text including inch symbols: 46.6" length, 19.7" width,
15.1" deep area, 29.5" total height, 18.9" side bag depth, 31.5" under-desk
clearance, 12.4" back-to-front depth, 3.9" leg, with the drawer stack
measurements 6.3" + 6.3" + 12" / 13.5" width labelled on the right. Two
separate drawer renderings at the bottom: the small drawer 13.5" x 13.5" x
6.1" and the file drawer 13.5" x 18.8" x 11.2", each with teal dimension
labels. Clean technical-product photography aesthetic, photorealistic, no
other text.
风险检查：尺寸数字必须和 listing spec 一致；标注线不要穿插打架；teal 是 #3BB7AF 不要漂
```

---

### S3 · File Drawer 三段功能 callout

**版式**：白底 + 顶部 inline 标题（teal 文件柜图标 + teal "Adjustable File Drawer for Different Sizes Files" + 细线分隔）+ 主图（file drawer 装彩色文件夹实物）+ 右上 / 右下两个 pill callout（"Legal/Letter/A4 Size" / "Storage Cabinet"）

**关键元素**
- 顶部 inline 标题风格：teal 小 icon（文件柜 / 抽屉 / 文件夹线性 svg 感）+ 加粗 teal 标题 + 灰色细线分隔条
- 大图占左 60%，3 个抽屉实物 + 彩色文件夹
- pill callout：teal 实底 + 白字 500 weight，圆角矩形，可贴角
- 箭头 / chevron `>` `>` `>`：teal 渐变，做"调节方向"暗示

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×1800
文字策略：teal inline 标题 + 2 个 teal pill callout + teal chevron 箭头
模块目标：文件收纳功能证明（3 卖点）
提示词：
Amazon product feature infographic on pure white background. A vertical photo
of a black fabric file drawer pulled out, filled with colorful hanging folders
in red, orange, yellow, green, blue, purple. Above the photo: a small teal
filing-cabinet icon + teal bold text "Adjustable File Drawer for Different
Sizes Files" + a thin teal underline.
Overlaid on the photo a teal #3BB7AF rounded pill label "Adjustable Rod" at
top-left with three teal chevron arrows pointing right beneath it. To the
right of the main photo a top inset image showing folders in red/yellow/blue
with a teal pill label "Legal/Letter/A4 Size". Below that a second inset image
of the drawer open with a camera, magazine and game cases inside, labelled
"Storage Cabinet" in a teal pill.
Clean editorial photography aesthetic, no other text, photorealistic.
风险检查：文件夹颜色明亮不喧宾夺主；pill 文字不超 8 个词；chevron 方向暗示"调节"
```

---

### S4 · 3-Tier Drawers + Icons 三层抽屉

**版式**：白底 + 顶部 teal banner "3-Tier Fabric Drawers" + teal 副标 "Spacious storage space for organization / Practical design keeps your space tidy" + 左侧 icon 列（Books / Wallet / Files / Laptop）+ 右侧产品大图（3 个抽屉拉出，1 个装相机和杂志，2 个装文件夹和书）

**关键元素**
- banner 文字：白底白字 + teal 实底 + 左对齐，圆角或直角都行（本套是右上圆角的"招牌"）
- 副标双行：用深灰 400 weight
- icon 列：teal 描边 3px 线性 icon + 下标灰色 "Books/Wallet/Files/Laptop" 标签
- 大图抽屉内容丰富：相机、车模、杂志、文件夹、日历、书——证明容量

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×1800
文字策略：teal banner + teal 副标 + icon 列 + 产品大图
模块目标：收纳容积 + 4 种物品适配
提示词：
Amazon product feature graphic on pure white background.
Top: a teal #3BB7AF banner with white bold sans-serif "3-Tier Fabric Drawers"
and a small cabinet icon, plus a subtitle in smaller white text "Spacious
storage space for organization / Practical design keeps your space tidy".
Left column: four teal line-art icons stacked vertically with grey labels
"Books", "Wallet", "Files", "Laptop" — icon style uniform 3px stroke.
Right two-thirds: a high-resolution photo of a 47-inch black desk with all
three fabric drawers pulled out. Top drawer shows a silver toy car, magazine
and headphones. Middle drawer shows a blue folder, a small calendar card, a
stack of books with white covers. Bottom drawer shows photo cards and small
electronics.
Clean, light, organized, lots of white space, photorealistic, no other text.
风险检查：4 个 icon 风格必须统一；banner 文字别超 6 个英文词；抽屉内容物真实可信
```

---

### S5 · Removable Storage 侧挂袋

**版式**：白底 + 左侧 teal icon（带 dotted border 的方框，暗示"可拆"）+ teal 标题 "Removable Storage Function" + 灰色副标 "Have Larger Desktop Space" + 右侧产品图（侧挂袋装笔记本、Switch、马克笔、卷笔袋，桌面上还有 Switch 和智能音箱）

**关键元素**
- icon：虚线边框方块（暗示"模块化 / 可拆卸"）—— 这是 47'' 桌的核心差异化
- 标题与副标分两行，标题 teal 600 weight，副标灰 400 weight
- 产品图要展示侧挂袋挂在桌侧面 + 桌面上还有空间放其它东西（"省桌面空间"叙事）

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×1700
文字策略：teal icon 虚线框 + teal 标题 + 灰色副标
模块目标：配件功能 + 桌面扩展（差异化卖点）
提示词：
Amazon product feature graphic on pure white background.
Left side: a teal line icon of a dotted-border square (suggesting a detachable
module), followed by teal bold text "Removable Storage Function" and a smaller
grey text "Have Larger Desktop Space".
Right side: a high-resolution photo crop of the left edge of the 47-inch black
computer desk, showing a black fabric hanging storage bag attached to the desk
side, filled with notebooks, a Nintendo Switch case, a marker holder, a soft
pencil pouch. Above the desk edge a sliver of monitor with red wallpaper is
visible; on the desk surface a small smart speaker glowing pink-blue and a
Nintendo Switch console. The composition emphasizes how the side bag frees up
the main desk surface.
Clean white background, soft studio lighting, photorealistic, no other text.
风险检查：虚线框 icon 必须传达"可拆"含义；侧挂袋的位置和实物一致
```

---

### S6 · Build Quality Stack 工艺堆叠

**版式**：白底 + 3 行横条 / 或 1 列 3 段——每段 image-left product photo + text-right（teal line icon + teal 标题 + 灰色副标）

**3 段内容**
1. **Waterproof / 防水** — 桌面水珠特写 / 水洒桌面不渗 + droplet icon
2. **Enhanced Structural / 结构加强** — 桌腿金属支架/角铁特写 + bracket icon
3. **Adjustable Leg Pads / 调节脚垫** — 桌脚螺丝垫特写 + leveling icon

**关键元素**
- 每段同尺寸、同节奏、同字体方向
- icon 用极简线性 teal stroke（不超过 4px）
- 标题 teal 600，副标灰 400
- 产品图是真实特写，不是 3D 渲染

**适配**
- 收纳柜：换成层板 / 折叠 / 抽屉滑轨 3 段
- 化妆桌：换成镜 / LED / 抽屉 3 段
- 学习桌：换成安全圆角 / 易擦桌面 / 高度调节 3 段

**prompt 模板**
```text
品类：47" 电脑桌
页面位置：gallery-secondary
画布：1792×1024 → resize 2000×2300（3 段横条堆叠，每段 ~770 高）
文字策略：每段 teal icon + teal 标题 + 灰色副标
模块目标：工艺/材质/结构三段证据
提示词：
Amazon product feature infographic on pure white background, three horizontal
rows stacked vertically.
Row 1: left half shows extreme close-up of a water droplet on the black
wood-grain desktop surface with light reflections; right half shows a teal
droplet line icon + teal bold text "Waterproof" + smaller grey text "Good
waterproof effect".
Row 2: left half shows the heavy-duty metal corner bracket under the desk
where leg meets frame; right half shows a teal bracket line icon + teal bold
text "Enhanced Structural" + smaller grey text "Heavy Duty Metal Design".
Row 3: left half shows close-up of the adjustable leg pad at the bottom of
the desk foot; right half shows a teal leveling-icon of a leg with horizontal
screw + ground symbol + teal bold text "Adjustable Leg Pads" + smaller grey
text "Suitable for uneven ground".
All text and icons in teal #3BB7AF, body in clean sans-serif, clean technical
aesthetic, no other text, photorealistic.
风险检查：3 段节奏一致；icon 尺寸一致；产品特写真实不 3D；副标不要超过 5 个英文词
```

---

## A+ 复合长图结构（基于 970 宽长图）

本套 A+ 是 **1 张整张长图**，宽 970 / 高 3000+，自上而下拆 4 个逻辑段。用户下次做类似家具 A+ 时按这个结构切片：

### 4 段结构

| # | 段名 | 视觉 | 卖点点 |
| --- | --- | --- | --- |
| A+1 | Hero Room Scene 全场景主图 | 整图宽 970、约 1000-1100 高，单图卧室全景 | 整体调性 + 风格锚点 |
| A+2 | Reversible Drawers Unit 主功能 + 3-callout | 970 × 约 900-1000，标题 + 段落 + 主图 + 3 个 teal pill | 可逆抽屉 + 安装方式 |
| A+3 | Fabric File Cabinet 描述段 | 970 × 约 400-500，标题 + 段落 + 1 张抽屉图 | 文件抽屉功能描述 |
| A+4 | 3-Column Icon Grid 三卖点网格 | 970 × 约 700-800，3 列 icon + 标题 + 段落 | 易组装 / 防水 / 抽屉 |

### 各段细节

#### A+1 · Hero Room Scene（A+ 顶部主图）

- 整张宽的全景卧室场景图——window + chair + shelf + desk + RGB + decor
- 这一张承担 80% 的"A+ 调性"，决定整套风格走向
- **不需要叠加文字**（品牌标题由 A+2 处理）

#### A+2 · Reversible Drawers Unit 主功能 + 3-callout

- 顶部 inline 标题：`Reversible Drawers Unit & Easy Installation`（深灰 700 weight，不带 banner）
- 下方段落："The table with reversible design, try this two installation methods (left or right) according to the workplace, so maximize the small space."
- 中央主图：file drawer 装彩色文件夹实物
- 右 / 右下两个 teal pill callout：`Adjustable Rod` / `Legal/Letter/A4 Size` / `Storage Cabinet`

#### A+3 · Fabric File Cabinet 描述段

- 左 inline 标题：`Fabric File Cabinet`（深灰 700 weight）
- 下方段落："One versatile file cabinet keep everything well organized and easily accessible. Two small drawers offers storage solution to home office supplies. The adjustable file drawer is suitable for hanging legal size or letter size files, It is also a storage cabinet."
- 右 / 右下放一张抽屉内容图（相机、文件夹、书）

#### A+4 · 3-Column Icon Grid 三卖点网格

- 3 列等宽（每列 300 宽），间距 35
- 每列顶部：teal 描边线性 icon（不带 banner）
- 每列下：深灰 700 标题 + 灰色段落 + 1 张产品小图
- 3 列内容：
  1. **Easy Assembly & Storage Capacity** — 桌面 + 抽屉 + 段落实物图
  2. **Waterproof Desktop & Stable & Adjustable Leg Pads** — 桌腿 + 角铁特写图
  3. **3 Fabric Drawers** — 3 个抽屉拉出图

### A+ 长图分段 prompt 模板

> 长图不建议一次性生 3000 高，分段生成更可控：

```text
品类：47" 电脑桌
页面位置：a-plus（长图分段）
画布：每段 1792×1024（16:9），生成后 Pillow resize 到 970×该段高，再竖向拼接
文字策略：teal banner / pill / inline + 深灰段落 + 灰色脚注；统一 clean sans-serif
模块目标：A+4 段结构（Hero / Reversible Drawers / Fabric File Cabinet / 3-Column Icons）
提示词（每段独立一段）：
[段 1] Interior photography, wide-angle 47-inch black computer desk in a real
bedroom corner with a window, grey curtain, RGB triangular wall lights pink and
blue, a grey ergonomic gaming chair with footrest, side metal shelf with
manga and action figures, soft warm afternoon light, no text no logo.
[段 2] White background infographic. Top: bold dark-grey text "Reversible
Drawers Unit & Easy Installation" + paragraph "The table with reversible
design..." (≤25 words). Center photo: black fabric drawer pulled out filled
with colorful hanging folders. Overlay three teal #3BB7AF rounded pill labels:
"Adjustable Rod", "Legal/Letter/A4 Size", "Storage Cabinet".
[段 3] White background. Left: bold dark-grey text "Fabric File Cabinet" +
paragraph "One versatile file cabinet keep everything well organized..."
(≤40 words). Right: a square photo of an open black fabric drawer containing
a camera, hanging files, magazines.
[段 4] White background, three equal columns separated by 35px gutters.
Column 1: teal line icon + bold dark text "Easy Assembly & Storage Capacity"
+ paragraph (≤30 words) + small square photo of the desktop with accessories.
Column 2: teal line icon + bold dark text "Waterproof Desktop & Stable &
Adjustable Leg Pads" + paragraph (≤40 words) + small photo of desk leg and
corner bracket. Column 3: teal line icon + bold dark text "3 Fabric Drawers"
+ paragraph (≤25 words) + small photo of three drawers pulled out.
All text in teal #3BB7AF headlines, #1A1A1A body, #888888 secondary. Clean
sans-serif Inter/Helvetica style. Photorealistic product photos. No other
text.
风险检查：
- 段落总字数 ≤200，过长用 Pillow 后期确定性排版
- 4 段风格统一（teal pill / icon / 字体方向一致）
- 标注线/箭头只在需要处出现
- 第三方 IP 角色（手办 / 海报）必须抽象化或替换成无品牌
```

---

## 关键风格参数（全局统一）

| 参数 | 值 |
| --- | --- |
| 品牌主色 | `#3BB7AF` teal（pill / banner / icon / 关键数字） |
| Headline 字色 | `#3BB7AF`（teal 实底矩形上的 white）+ inline 用 `#1A1A1A` |
| Body 字色 | `#1A1A1A` |
| Secondary 字色 | `#888888` |
| 字体方向 | clean modern sans-serif（Inter / Helvetica） |
| 标注线 | `#CCCCCC` 1px |
| 背景 | `#FFFFFF` 纯白（主图 + A+ 全模块） |
| 构图 | 白底 + 真实产品特写 / 卧室全景 + teal pill + 1px 浅灰标注线 |
| Pill 样式 | `#3BB7AF` 实底 + 白字 500 weight，圆角 50%（胶囊），内边距 12px 水平 / 8px 垂直 |
| Icon 样式 | teal #3BB7AF 描边 3px，线性，无填充 |
| Banner 样式 | `#3BB7AF` 实底矩形 + 白字 600-700 weight，圆角可选 |
| 数字策略 | teal + 双引号 + inch/imperial（家具美国主战场），例 `46.6"`, `29.5"` |

> 同一套图使用同一套 teal 颜色和字体规则，避免每张图风格漂移。

---

## 风险检查（家具特化）

- **主图合规底线**：纯白 #FFFFFF + 无文字 + 无 logo + 无边框 + 无促销角标 + 无参照物（不要放 person / hand / 比例尺暗示）
- **床 / 桌 / 柜承重 / 寿命 claim**：避免 "lifetime warranty" / "forever durable" / "supports 500 lbs" 这类无实证数据，替换成 "supports up to X lbs" / "heavy-duty metal frame" 这种可证明的
- **儿童相关 claim**：如果产品可能用于儿童场景，必须查 CPSIA / ASTM F2057（小储物柜抗倾倒），ant-tip strap 必备
- **甲醛 / 环保 claim**：避免 "zero VOC" / "100% formaldehyde free"，除非有 CARB Phase 2 / EPA TSCA Title VI 认证
- **第三方 IP**：卧室场景里的手办 / 海报 / 屏幕内容（MSI 标志、《英雄联盟》角色等）必须抽象化或替换为通用形象，否则容易触发商标投诉
- **尺寸标注一致性**：S2 的尺寸数字必须和 listing bullet / description 完全一致，避免"买家买的和图不一致"投诉
- **AI 直接出字风险**：尺寸数字、参数密集段、备注脚注 → Pillow 后期确定性排版。AI 适合的是 banner、pill 标签、标题、短 callout
- **多张图产品色不一致**：M0 / S1 / S2 / S3 / S4 / S5 / S6 桌体颜色必须严格一致（同一木纹 / 同一抽屉布纹 / 同一金属质感），否则视觉割裂
- **场景道具**：显示器、Switch、智能音箱、相机、车模等是 lifestyle 道具，不是包含物。如果 listing 没有标 "with monitor"，主图绝不放
- **退货成本**：家具品类退货率普遍 10-15%（比 3C 服装低但运费高），S2 尺寸图必须准确降低退货

---

## 后处理（Pillow 标准化）

生图模型常返回非精确像素。交付前用 Pillow 把每张 1792×1024 裁切 / resize 到目标模块尺寸：

```python
from PIL import Image

# 主图（注意方形居中裁）
im = Image.open("M0_gen.png").convert("RGB")
w, h = im.size
side = min(w, h)
im = im.crop(((w-side)//2, (h-side)//2, (w+side)//2, (h+side)//2))
im = im.resize((2000, 2000), Image.LANCZOS)
im.save("M0_main_2000x2000.png")

# 副图按比例
im = Image.open("S2_gen.png").convert("RGB")
im = im.resize((2000, 1700), Image.LANCZOS)
im.save("S2_dimensions_2000x1700.png")

# A+ 长图分段后竖向拼接
from PIL import Image as PI
chunks = [PI.open(f"aplus_seg{i}.png").convert("RGB").resize((970, h), PI.LANCZOS)
          for i, h in enumerate([1000, 950, 450, 750])]
total_h = sum(c.height for c in chunks)
canvas = PI.new("RGB", (970, total_h), (255,255,255))
y = 0
for c in chunks:
    canvas.paste(c, (0, y)); y += c.height
canvas.save("aplus_composite_970x3150.png")
```

---

## 子品类适配模板

| 子品类 | 主图调整 | 副图调整 | A+ 调整 |
| --- | --- | --- | --- |
| 电脑桌 / 游戏桌（本套基准）| 3/4 角 + 显示器键盘 | 见 7 模块 | 见 4 段 |
| 书桌 / 学习桌 | 正面 + 文具 | S1 换成小孩写作业场景；S5 改成带书架/桌灯 | A+4 三卖点改为安全圆角 / 易擦桌面 / 高度可调 |
| 升降桌 | 侧面 + 显示升降机构 | S2 改成升降范围；S6 改成电机 / 承重 / 防夹 | A+4 三卖点改为电机 / 记忆档位 / 承重 |
| 化妆桌 | 正面 + 镜 | S1 换成卧室 + 梳妆镜前灯；S5 改成首饰收纳 | A+4 三卖点改为镜面 / LED / 抽屉分类 |
| 收纳柜 / 文件柜 | 正面 + 多抽屉 | S1 换成衣帽间；S3 改成文件 / 衣物分类；S5 改成折叠 | A+4 三卖点改为层数 / 折叠 / 防倾倒 |
| 多功能桌 | 3/4 + 一体化 | S1 改成组合（打印机架 / 充电口 / 书架） | A+4 三卖点改为一体化 / 节省空间 / 多功能 |

---

## 用户偏好（Sungw override）

- 用户要成品图时，默认直接出图文一体创意，不默认"留白后叠加文字"或"后期叠字"，除非用户明确要求可编辑 / 无字背景。
- 图中需要文字时，文案要短、大、可读；把确切文案作为 verbatim text 写进 prompt，指定统一 clean sans-serif 字体方向，要求不要多余字。
- 生图后必须 Pillow 标准化到精确模块尺寸再交付 / 拼接（A+ 用 970 宽分段竖拼）。
- 家具 S2 尺寸图是**最关键**的一张副图（影响退货率），数字必须 100% 与 listing 一致，AI 直接画的尺寸数字不可信，重要数字走 Pillow 后期叠字。
