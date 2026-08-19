# GreenWood Style Pack — 户外/家居生活独立站 28 张套图

> 已验证的「深绿 + 米白 + 自然木色」户外生活视觉系统 + 28 张独立站全站装修 SOP。原型来自公众号「小野火 跨境好家伙」2026-07-28 文章《跨境独立站装修SOP标准版28张【更新】》的椅子测品套图（HaoJH OUTDOOR LIVING 户外 HDPE 长椅）。本 pack 把其结构、字体、配色、图标固化成可换产品的参数化模具。
> 区别于本 skill 的纯产品图流程（main/gallery/PDP/variant/banner）：GreenWood 解决的是**整个独立站装修**——从社媒获客到品牌故事，全链路 28 张，且强制统一视觉系统。

### GW.1 视觉系统（必须贯穿全 28 张）

**色彩体系（sacred palette）**

| 角色 | 色值 | 使用位置 |
|------|------|----------|
| 品牌深绿 | `#2F4F3A` / `rgb(47,79,58)` | Logo、标题、按钮、信息面板、底部 benefit bar、弧形分隔 |
| 米白/奶油白 | `#F5F5F0` / `rgb(245,245,240)` | 背景、卡片、留白区 |
| 纯白 | `#FFFFFF` | 白底产品主图、规格表背景 |
| 自然木色/米色 | `#D4C4A8` | 露台地板、编织地毯、花盆、暖调和过渡 |
| 黑/深灰 | `#1A1A1A` | 正文、小字 |
| 点缀黄/橙 | 仅星星评价、强调小标 | 小面积使用，禁止大面积铺色 |

色彩纪律：每屏只允许「深绿 + 米白 + 木色 + 产品本色 + 中性色」，**随机撞色会打破 GreenWood 氛围**。

**字体与排版**
- 字体：现代无衬线（Montserrat / Inter / Helvetica 系），标题粗重、正文细。每屏 ≤ 2 种字体。
- 标题：超大号、左对齐或居中，常用首字母大写或全大写。
- 信息层级固定：`主标题 → 副标题 → 4 个圆形图标+说明 → 底部深绿 benefit bar`。
- 布局习惯：左文右图 / 左图右文交替；**深绿色弧形或斜切面板**分隔图文（GreenWood 招牌动作）；每屏底部统一一条深绿 benefit bar；圆角卡片、轻阴影、留白多。

**图标系统**：全部使用**圆形线框图标**（细描边、单色深绿），统一风格：防水、UV 防护、低维护、环保可回收、耐用、舒适、可折叠、全球配送等。禁止实心彩色图标、禁止 emoji 堆砌。

**图像与场景**
- 产品：同一单品贯穿 28 张，固定 3/4 侧视角，确保品牌一致性（换产品时只换主体，角度逻辑保留）。
- 场景：海滩、露台、花园、草坪；光线明亮、阴影柔和；绿植 / 编织元素 / 白色建筑点缀。
- 人物：仅在品牌/B2B 模块出现，走「真实团队 + 专业」路线（穿品牌 POLO、工厂/展厅背景）。
- 细节：水滴、螺丝、扶手、靠背等微距图增强材质信任。

**尺寸规格**（28 张只有三种画幅）

| 画幅 | 尺寸 | 数量 | 典型模块 |
|------|------|------|----------|
| 方形 | 1080 × 1080 | 17 | 社媒、A+、产品图、品牌页 |
| 宽屏 | 1080 × 608 | 10 | Hero Banner、分类页、功能页 |
| 竖屏 | 1080 × 1440 | 1 | 三场景生活方式长图 |

### GW.2 28 张结构总览

| 模块 | 张数 | 画幅 | 对应原案例图 | 用途 |
|------|------|------|--------------|------|
| A 社媒/获客 | 2 | 1方+1宽 | 01, 02 | 社媒互动卡、邮件订阅弹窗 |
| B 网站功能页 | 3 | 宽 | 03, 13, 31 | 空购物车、404、Contact Us |
| C Hero Banner | 8 | 7宽+1竖 | 09,10,14,20,22,25,30,33 | 首页轮播、分类入口、促销 |
| D 产品详情/A+ | 10 | 方 | 04,05,06,08,11,12,15,16,17,27 | 卖点、参数、细节、对比、开箱、认证 |
| E 品牌/B2B | 5 | 3方+2宽 | 21,23,24,28,29 | 团队、Logo、时间线、定制、工厂 |
| **合计** | **28** | — | — | 覆盖独立站全链路 |

> 原案例：HaoJH OUTDOOR LIVING 户外 HDPE 长椅（2-seater / loveseat / outdoor bench）。换产品时只替换 `{product}` / `{brand}` / `{material}` / `{scenes}` 等占位符。

### GW.3 SOP 流程（沿用本 skill 的确认式节奏）

1. **锁定产品与品牌**：提取产品类型、材质、颜色、核心卖点、品牌名（⚠ 品牌名必须全局一致，原案例曾出现 `GreenWood Living` 与 `HaoJH` 不一致的 bug）。
2. **确认 GreenWood 风格**：展示「深绿+米白+木色 / 左文右图 / 圆弧面板 / 底部 benefit bar / 圆形线框图标」套系摘要，确认是否沿用。用户说「直接做 / 继续」则跳过等待。
3. **逐模块输出 prompts**：严格按 A→B→C→D→E 顺序，每屏 prompt 显式声明「沿用上文 GreenWood 视觉系统（背景/主色/字体/卡片/图标/光影/产品锚点）」。
4. **主动提示扩展**：28 张完成后，问是否要加促销 Banner / 广告图 / 节日专题（不编造价格折扣，未提供时用 "New Arrival / Limited Time / Seasonal" 等泛化文案）。

### GW.4 逐图 Prompt 模板（参数化，可直接复制进生图工具）

> 占位符：`{product}` `{brand}` `{material}` `{color}` `{scenes}`（如 Porch/Garden/Beach）`{benefits}`（4 个卖点）`{keywords}`（如 2-seater / loveseat）。
> 风格前缀固定加：`GreenWood visual system: deep forest green #2F4F3A + cream #F5F5F0 + natural wood #D4C4A8, modern sans-serif, rounded cards, circular line icons, soft bright outdoor light.`

**A 社媒/获客（2 张）**

A1 社媒互动卡（方形 1080×1080）：
```text
Generate a social-media engagement card for {brand}, 1080x1080 square. GreenWood visual system. Left: "CONNECT WITH US" headline in bold Montserrat, a round QR code placeholder, and 4 circular line icons with labels: {benefits}. Right: a clean lifestyle photo of {product} on a {scenes} deck. Deep green #2F4F3A panel behind text, cream background, rounded cards, soft bright light. No watermark.
```

A2 邮件订阅弹窗（宽屏 1080×608）：
```text
Generate an email-capture popup banner for {brand}, 1080x608 wide. GreenWood visual system. Left: "GET 10% OFF YOUR FIRST ORDER" headline + email input field mockup + subscribe button in deep green. Right: {product} in a bright {scenes} scene. Cream background, circular line icons, rounded corners, consistent with GreenWood set. No real prices except the stated 10% OFF.
```

**B 网站功能页（3 张，均宽屏 1080×608）**

B1 空购物车页：
```text
Generate an empty-cart page hero, 1080x608 wide. GreenWood visual system. Soft, non-disappointing tone: "YOUR CART IS EMPTY" in deep green, a gentle illustration of {product}, and a bottom benefit bar with 4 circular icons: {benefits}. Cream background, rounded cards.
```

B2 404 页：
```text
Generate a 404 error page, 1080x608 wide. GreenWood visual system. "OOPS — PAGE NOT FOUND" with a tasteful product showcase of {product} on the right, deep green accents, bottom benefit bar. Turn the error into a brand moment.
```

B3 Contact Us 页：
```text
Generate a Contact Us page hero, 1080x608 wide. GreenWood visual system. Left: contact info block (email / phone / address placeholders) in deep green panel. Right: {product} with a subtle map background. Cream, rounded cards, circular line icons.
```

**C Hero Banner（8 张：7 宽屏 + 1 竖屏）**

C1 分类入口 Banner（宽屏）：
```text
Generate a category hero banner for {brand}, 1080x608 wide. GreenWood visual system. Left deep green curved info panel with headline "{keywords} Collection" + product series nav chips. Right: {product} on a {scenes} with bright sky. Bottom benefit bar with 4 circular icons.
```

C2 三场景生活方式长图（竖屏 1080×1440 — 唯一竖屏）：
```text
Generate a vertical 3-scene lifestyle image, 1080x1440. GreenWood visual system. Three stacked scenes: Porch / Garden / Beach, each showing {product} in that setting, separated by deep green arc dividers. Bottom: 4 circular benefit icons {benefits}. Cream background, soft natural light. This is the richest image of the set.
```

C3–C8 多角度 Hero（宽屏，文案轮换）：
```text
Generate a homepage hero banner, 1080x608 wide. GreenWood visual system. {product} as first focal point on a bright {scenes}, headline emphasizing "{keywords}" (rotate angles: comfort / durability / weatherproof / easy-care / space-saving across C3-C8). Deep green curved panel, bottom benefit bar, circular line icons. Copy variants only — keep same visual DNA.
```
> C8 可改为春季促销版：`headline "SPRING SALE — 20% OFF {keywords}"`，其余视觉不变（价格仅当用户提供才写具体数字）。

**D 产品详情/A+（10 张，均方形 1080×1080）**

D1 评价引用卖点：
```text
Generate a testimonial benefit image, 1080x1080. GreenWood visual system. 5 gold stars + a short review quote placeholder + {product} photo. Deep green headline "LOVED BY {scenes} OWNERS". Cream card, rounded, circular icons.
```

D2 规格参数表：
```text
Generate a spec sheet image, 1080x1080. GreenWood visual system. Clean table: dimensions + material ({material}) + weight + load capacity (use placeholders), with 4 circular line icons. White/cream background, deep green headers, Montserrat.
```

D3 三栏 A+：
```text
Generate a 3-column A+ module, 1080x1080. GreenWood visual system. Left: dimension diagram of {product}; middle: spec table; right: detail close-up. Deep green section dividers, cream background, circular icons, consistent typography.
```

D4 白底主图 + 5 图标（最接近 Amazon 主图）：
```text
Generate a white-background product hero, 1080x1080. Pure white background, {product} centered 3/4 view, 5 circular line icons with labels {benefits} arranged along the bottom in deep green. Crisp e-commerce photography, no clutter. (This is the only near-Amazon frame in the set.)
```

D5 认证与售后：
```text
Generate a certification & warranty image, 1080x1080. GreenWood visual system. Badge row (ISO / CE / SGS placeholders) + "1-YEAR WARRANTY" headline. Deep green panel, cream background, circular icons.
```

D6 材质细节网格：
```text
Generate a material-detail grid, 1080x1080. GreenWood visual system. 6 close-up cells: UV resistance / waterproof / low maintenance / stainless steel parts / armrest / structure + a water-drop test micro shot. Deep green labels, cream grid, consistent icons.
```

D7 人体工学细节：
```text
Generate an ergonomics detail image, 1080x1080. GreenWood visual system. Callouts on backrest / armrest / seat / frame of {product}, plus a bottom material macro (wood-grain or woven texture). Deep green annotations, cream background.
```

D8 型号对比表：
```text
Generate a model comparison table, 1080x1080. GreenWood visual system. Rows: 2FT / 4FT / 5FT / Foldable 4FT (replace with {product} variants), columns: size / seats / weight / foldable. Deep green header, cream cells, Montserrat, rounded cards.
```

D9 认证墙：
```text
Generate a certification wall, 1080x1080. GreenWood visual system. Grid of certificates: SGS / TÜV / CTI / ISO9001 / ISO14001 / CE (placeholders). Deep green frame, cream background, uniform badge style.
```

D10 开箱体验：
```text
Generate an unboxing experience image, 1080x1080. GreenWood visual system. 3-step assembly icons (1. Open / 2. Assemble / 3. Enjoy) + parts list + packaging photo of {product}. Deep green steps, cream background, circular icons.
```

**E 品牌/B2B（3 方 + 2 宽）**

E1 团队品牌故事（方形）：
```text
Generate a brand-story image, 1080x1080. GreenWood visual system. A small team wearing {brand} polo shirts sitting together on {product} in a bright {scenes}. Warm, authentic, "real team" vibe. Deep green logo corner, cream background.
```

E2 Logo（方形）：
```text
Generate a brand logo mark, 1080x1080. GreenWood visual system. Circular emblem with {product} silhouette inside + wordmark "{brand} OUTDOOR LIVING" in Montserrat. Deep green on cream. Clean, scalable.
```

E3 品牌时间线（方形，可宽屏）：
```text
Generate a brand timeline image. GreenWood visual system. Horizontal timeline 2010 → 2024+ with milestone nodes (founded / first factory / global shipping / eco-material). Deep green line, cream nodes, circular icons, consistent typography.
```

E4 B2B 定制服务（方形）：
```text
Generate a B2B custom-service one-pager, 1080x1080. GreenWood visual system. 5-step flow: Consultation → Design → Sample → Production → Delivery, with circular line icons and deep green connectors. Cream background, "OEM / ODM WELCOME" headline.
```

E5 关于我们/工厂（宽屏 1080×608）：
```text
Generate an about-us / factory hero, 1080x608 wide. GreenWood visual system. Left: team + factory + showroom photos collage; right: {product} + {brand} OUTDOOR LIVING wordmark. Deep green panel, cream background. ⚠ Brand name must match E2 exactly — do not introduce a second brand name.
```

### GW.5 生成「不一样的」套图（产品替换规则）

GreenWood 是模具，换产品时只动以下占位符，视觉系统不动：

| 占位符 | 说明 | 示例 |
|--------|------|------|
| `{product}` | 核心单品 | 户外长椅 → 露台秋千 → 园艺收纳柜 |
| `{brand}` | 品牌名（全局唯一） | HaoJH / 你的品牌 |
| `{material}` | 主体材质 | HDPE / 实木 / 铝合金 / 藤编 |
| `{color}` | 产品本色 | 深绿 / 原木 / 石墨灰 |
| `{scenes}` | 生活场景 | Porch / Garden / Beach / Balcony |
| `{benefits}` | 4 个卖点（圆形图标） | 防水/UV/低维护/耐用 |
| `{keywords}` | 标题关键词 | 2-seater / loveseat / storage |

换品类提示：从「户外家具」扩到「家居园艺 / 阳台生活 / 庭院设备」都适用；若换到完全非生活场景的工业品，需先与用户确认是否仍套 GreenWood（深绿生活调性可能不匹配）。

### GW.6 禁忌清单

- ❌ 品牌名在套图里出现两个版本（原案例 `GreenWood Living` vs `HaoJH` 的 bug，必须避免）。
- ❌ 把 28 张做成互不相关的独立海报——必须共享背景/主色/字体/卡片/图标/光影/产品锚点。
- ❌ 使用纯白底 Amazon 高对比风替代 GreenWood 生活调性（除 D4 单张白底主图外）。
- ❌ 随机撞色、实心彩色图标、emoji 堆砌、满屏促销贴纸。
- ❌ 编造具体价格、折扣金额、销量、认证编号（未提供时用占位符或泛化文案）。

### GW.7 输出格式

每图按以下结构输出（中文说明 + 英文 prompt）：

```markdown
# {ID}. {模块} - {用途}
视觉描述：{该图展示什么}
产品：{product} + 展示方式
核心卖点：{每图仅 1 个核心卖点}
画幅：{1080×1080 / 1080×608 / 1080×1440}
风格：GreenWood 视觉系统（深绿+米白+木色 / 圆弧面板 / 底部 benefit bar / 圆形线框图标）
Prompt：
```text
{可直接复制进生图工具的英文 prompt}
```
```

### GW.8 参考来源

- 原型结构来自公众号「小野火 跨境好家伙」2026-07-28 文章《跨境独立站装修SOP标准版28张【更新】》的椅子测品套图。
- 本地分析存档：不随 skill 分发（34 张原图 + 结构拆解仅存在于原作者本机，不引用外部路径）。
