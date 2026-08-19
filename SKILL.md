---
name: ss-art-prompt-image
description: 电商套图提示词工作台 — 只把用户的输入（产品/平台/风格/数量）转换成可直接复制的 AI 生图提示词，不执行任何生图动作、不调用任何生图工具。覆盖 Amazon、Shopify、TikTok Shop、淘宝/天猫/京东/拼多多、1688、Shopee（虾皮）、Ozon、Lazada、Coupang 等电商平台。输出提示词后由用户自行粘贴到任意生图工具生成。触发词：多平台套图、做套图、电商主图、平台套图、电商图片、海外套图、listing 套图、提示词、生图提示词、Amazon 套图、Shopify 套图、TikTok Shop 套图、淘宝套图、1688 套图、Shopee 套图、Ozon 套图、套图案例、套图案例展示。需要做任何一个电商平台的套图、listing 主副图、A+/详情页、活动海报并只想要提示词时使用。
agent_created: true
---

# 电商套图提示词工作台（ss-art-prompt-image）

本 skill 只做一件事：**把你的输入变成高质量的生图提示词**，然后提示你拿去生图。它不生成、不调用、不执行任何图像生成动作。**只覆盖电商平台套图**

原有的 `ss-amazon-image-generation` / `shopify-image-generator` / `tiktok-shop-image` / `china-commerce-image-prompt-generator` / `1688-image-prompt-generator` / `ozon-image-prompt-generator` 已经把各自的平台逻辑写到了非常细的程度，本 skill 不是替代它们，而是把它们汇总到一个总线入口：

- **一个入口**：所有电商平台套图问题都在这里接。
- **自动路由**：识别用户提到的平台/品类/关键词，加载对应的 `references/platforms/{platform}.md` 子模块。
- **统一工作流**：先识别平台与品类 → 再识别图片角色 → 再选风格 → 输出确认稿 → 用户确认 → 输出提示词。
- **只出提示词**：确认稿通过后，只输出可复制的提示词，**不生成任何图片**，并提示用户自行去生图工具生成。
- **缺啥补啥**：补齐原 skill 漏掉的 Shopee（虾皮）、Lazada、Coupang。

## 使用方法

### 方式 1：标准提问格式（推荐）

直接按下面字段提问，字段能省则省，缺的我会自动补全并先跟你确认：

```text
平台：{Amazon / Shopify / TikTok Shop / 淘宝 / 京东 / 拼多多 / 1688 / Shopee / Ozon / Lazada / Coupang}
产品：{产品名 + 品类，如"女装 V领灯笼袖连衣裙"}
地区：{目标市场，如 美国 / 巴西 / 墨西哥 / 英国 / 德国 / 日本 / 俄罗斯 / 新加坡 / 马来西亚 / 韩国 / 中国}
套图要求：{主图 x 张 + 副图 x 张 + 详情页 x 张，如"主图 1 张 + 副图 4 张 + 详情页 6 段"}
规格：{尺码 / 材质 / 颜色 / 参数 / 卖点，如"冰丝面料、UPF50+、3 色可选"}
风格：{可选，如"Phone UGC 镜自拍 / 高级棚拍 / 参数解释型 / 大字海报"}
```

#### 示例 1：单平台

```text
平台：TikTok Shop
产品：女装 V 领灯笼袖抽绳腰连衣裙
地区：美国
套图要求：主图 5 张 + 详情页 5 张
规格：碎花/几何印花、收腰、长款、Boho Maxi
风格：Phone UGC 镜自拍 + 街拍
```

#### 示例 2：最简提问（其余我自动补）

```text
平台：Shopee
产品：3C 磁吸充电宝 10000mAh
地区：新加坡
套图要求：主图 1 + 副图 4
```

#### 示例 3：跨平台

```text
产品：女包
套图要求：Amazon 主图 1 + Shopify PDP 6 段 + TikTok Shop 详情页 4 张
```

#### 示例 4：套图案例展示

```text
套图案例展示：TikTok Shop 连衣裙 / Shopify 户外 / Amazon 家具 各 3 张
```

模型会自动识别平台并加载对应 `references/platforms/{platform}.md` + 子目录完整 reference。

### 方式 2：跨平台对比 / 案例库

用户说 `多平台套图案例 / 套图案例展示 / 各平台套图 / 跨平台对比`，进入「跨平台套图案例库」分支，参考 `references/platforms/_case-gallery.md`。

### 方式 3：明确触发某一个子 skill

如果你只想用旧逻辑，可以继续用原 skill 名（`$ss-amazon-image-generation` / `$shopify-image-generator` 等），本 skill 不覆盖它们。本 skill 只是统一入口。

## 总工作流（适用于所有平台）

不管哪个平台，套图任务默认走下面 6 步：

1. **识别平台与站点**：Amazon / Shopify / TikTok Shop / 淘宝 / 1688 / Shopee / Ozon / Lazada / Coupang 等；以及所在国家/地区（如 Amazon US/UK/DE/JP，TikTok Shop US/BR/MX/UK/SEA 等）。
2. **识别品类与图片角色**：女装/3C/家居/美妆/母婴/茶器/眼镜/工具/食品/包装礼盒 等；产品图/参考图/竞品图/参数图/工厂图 等。
3. **加载对应平台模块**：先读入口 `references/platforms/{platform}.md` 获取平台定位、平台硬规则和路由表，再**必读路由表指向的** `references/platforms/{platform}/` 子文件（如 `fashion.md`、`3c.md`、`furniture.md`、各类目 `*-main-sub-detail-logic.md`、`ozon-cover-layouts.md`、`greenwood-style-pack.md` 等）。**品类/图类型的具体规则以子文件为唯一事实源**，入口文件不承载执行细节。
4. **确认套图风格**：套图风格未确定时，先给 2-4 个可选风格方向让用户选；用户说"直接做"可跳过。
5. **输出确认稿**：每张图给出页面位置/画布尺寸/文字策略/模块目标/prompt/风险检查，等待用户确认。
6. **输出图片提示词 + 文案**：用户确认后，按平台规则输出每张图的完整提示词（见下方「通用输出格式」）；如要做完整 Listing（Amazon/Shopify），同时输出文案。**本 skill 只产出提示词，不执行任何生图动作。**

## 生图衔接（只出提示词，提示用户自己生图）

> **SOP 铁律：本 skill 只出提示词，不生成图。** 无论用户是否一开始就说"直接生成"，都只按「总工作流」第 5 步把每张图的完整提示词（含图片描述/产品/卖点/场景/文案/风格/构图/比例/字体）写出来给用户，**不调用任何生图工具（如 ss-art-image-gen 等）**。

1. **默认行为**：确认稿通过后，直接交付完整提示词，并明确提示"请把上面的提示词复制到你的生图工具中生成图片"；本 skill 到此结束，不自动生图。
2. **如何生图**：由用户自行把提示词粘贴/复制到任意外部生图工具（如 ss-art-image-gen、Midjourney、即梦 等）去生成，本 skill 不负责执行。
3. **尺寸标注**：提示词里保留各平台比例（`1:1` / `3:4` / `9:16` / `16:9` 等）作为生图参考，方便用户粘贴到任意生图工具。

## 平台路由表

| 触发词 / 平台 | 入口文件 | 完整 references 目录 |
|---|---|---|
| Amazon / 亚马逊 / 主图白底 / A+ / 长图 | `references/platforms/amazon.md` | `amazon/`（fashion.md、3c.md、3c-anker.md、furniture.md + sources 图片） |
| Shopify / 独立站 / DTC / GreenWood | `references/platforms/shopify.md` | `shopify/`（fashion / ugc-fashion / 3c / furniture / greenwood-style-pack / **tea-tool / tea-tool-ugc**） |
| TikTok Shop / TK Shop / 美区 / 巴西 / 墨西哥 | `references/platforms/tiktok-shop.md` | `tiktok-shop/`（3c.md、case-dress-maxi-puff-sleeve.md、ugc-fashion.md） |
| 淘宝 / 天猫 / 京东 / 拼多多 | `references/platforms/taobao-jd-pdd.md` | `taobao-jd-pdd/`（apparel / cosmetics ×2 / oral-care） |
| 1688 / 工厂 / 批发 / 源头店 | `references/platforms/1688.md` | `1688/`（main-sub / detail-page / spec-parameter / factory-trust / campaign-poster） |
| Shopee / 虾皮 / SG / MY / TW / BR / ID / TH / VN / PH | `references/platforms/shopee.md` | 新增（无原 skill，规则已内联） |
| Ozon / 俄罗斯 / EAC / GOST / 俄文 | `references/platforms/ozon.md` | `ozon/`（general-layouts / cover-layouts / fashion-layouts / xiaomi-3c / Hillsusu-desk） |
| Lazada / 来赞达 / 东南亚 B2C | `references/platforms/lazada.md` | 新增（无原 skill，规则已内联） |
| Coupang / 韩国 / 火箭配送 | `references/platforms/coupang.md` | 新增（无原 skill，规则已内联） |


## 通用原则（适用于所有平台）

1. **先识别，再选风格**：平台和品类不对，风格选对也没用。
2. **客户/卖家图优先**：参考/竞品图只用于风格、构图、信息层级参考，不照抄商品主体、品牌、文案、价格、活动。
3. **默认直接出完整成图**：用户没明确说"无字/留白/后期排版"时，详情图、参数图、活动图默认让 AI 直接生成完整画面和排版。
4. **不编造数据**：价格、优惠、起订量、库存、认证、销量、成分百分比、防晒指数 等都不允许凭空写，除非用户提供。
5. **套图连贯性优先**：同一套图沿用背景、主色、字体、卡片、图标、道具、光影和产品锚点，不要每张换一套审美。
6. **合规底线**：禁止夸大（"best / #1 / 100% / 治百病"）、禁止平台 UI（价格、星星、收藏、平台 logo）、禁止未经授权品牌 logo / 二维码 / 联系方式 / 车牌 / 平台 UI。
7. **本地化**：图片内文字 / 文案 / 模特气质 / 场景 / 单位制 必须符合目标市场，巴西葡语 / 俄语西里尔 / 韩文 Hangul / 东南亚本地语言。
8. **默认按平台规则而不是通用规则**：Ozon 不要做亚马逊白底；Shopee 不要直接照搬淘宝重文字海报；Coupang 用韩文大字。优先按 `references/platforms/{platform}.md` 走。

## 通用输出格式

所有平台输出提示词时按下面格式（具体平台可能微调，但骨架一致）：

```markdown
## {ID}. {图片类型} - {用途}
图片描述：{画面内容}
产品：{产品名 + 展示方式}
核心信息/卖点：{只表达一个核心信息点}
场景：{该平台类目适配场景}
图片文案：{无文字 / 直接生成中文文案：xxx / 直接生成英文 / 俄文 / 韩文 / 葡语...}
风格：{该平台电商审美 + 用户指定/参考反推风格}
构图：{主体占比、视角、信息层级}
比例：{1:1 / 3:4 / 9:16 / 16:9 / 970x600 / 750px 宽长图}
字体：{根据平台语言指定}
提示词：
```text
{可直接复制给 AI 生图工具的完整提示词}
```
合规检查：{该图风险点}
```

## 何时不使用本 skill

- 纯文案（不涉及图）：走对应文案类 skill。
- 单张海报/品牌大片：使用具体平台的 image generation skill。
- 视频脚本/分镜：使用 video 类 skill（`ss-art-prompt-video`）。
- 对标图复刻提示词：使用 `ss-art-prompt-clone`。
- 用户明确指定其他套图 skill（如 `humanizer-zh`、`detail-page-planner` 等）：继续用原 skill。

## 子模块文件清单

### 入口文件（平台定位 + 硬规则 + 路由表；不含品类执行细节）

- `references/platforms/amazon.md`
- `references/platforms/shopify.md`
- `references/platforms/tiktok-shop.md`
- `references/platforms/taobao-jd-pdd.md`
- `references/platforms/1688.md`
- `references/platforms/shopee.md`
- `references/platforms/ozon.md`
- `references/platforms/lazada.md`
- `references/platforms/coupang.md`

### 完整 references 目录（品类/图类型规则的唯一事实源；从原 skill 原样搬入，内容不精简）

- `references/platforms/amazon/` — `fashion.md` / `3c.md` / `3c-anker.md` / `furniture.md` / `sources/`（8 张参考图）
- `references/platforms/shopify/` — `fashion-main-sub-image-logic.md` / `ugc-fashion-main-sub-image-logic.md` / `3c.md` / `furniture-main-sub-detail-logic.md` / `greenwood-style-pack.md` / `tea-tool.md` / **`tea-tool-ugc.md`**（含 9 张主图参考 + 3×3 montage）
- `references/platforms/tiktok-shop/` — `3c.md` / `case-dress-maxi-puff-sleeve.md` / `ugc-fashion.md`
- `references/platforms/taobao-jd-pdd/` — `apparel-main-sub-image-logic.md` / `cosmetics-main-sub-image-logic.md` / `cosmetics-detail-page-logic.md` / `oral-care-main-sub-detail-logic.md`
- `references/platforms/1688/` — `1688-main-sub-image-logic.md` / `1688-detail-page-logic.md` / `1688-spec-parameter-logic.md` / `1688-factory-trust-logic.md` / `1688-campaign-poster-logic.md`
- `references/platforms/ozon/` — `ozon-general-layouts.md` / `ozon-cover-layouts.md` / `ozon-fashion-layouts.md` / `xiaomi-3c.md` / `Hillsusu-desk.md`

### 公共文件

- `references/platforms/_sop-common.md` — 通用 SOP（输入识别、风格确认、输出格式、合规清单）
- `references/platforms/_sop-brief-template.md` — 参考图拆解简报模板
- `references/platforms/_case-gallery.md` — 跨平台套图案例展示库

### 生图方式

- 本 skill **只产出提示词，不内置也不调用任何生图脚本**（`ss-art-image-gen` 等外部生图工具均不在本 skill 执行范围内）。提示词确认后即交付，并提示用户自行复制到外部生图工具生成。详见「生图衔接」规则。

## 与其他套图 skill 的关系

本 skill 是电商套图提示词"总入口"，**不删除** 任何已有套图 skill。同时，为了让你在本 skill 内就能独立跑完整流程，**原 skill 的 references 已经完整内联进来**（一个字节不丢）。入口文件与子目录**分层运行**：入口只做路由 + 平台硬规则，品类/图类型的具体规则以子目录为唯一事实源，内容不重复、不需要双向同步：

| 已有 skill | 原 skill 是否保留 | 在本 skill 中的位置 |
|---|---|---|
| `ss-amazon-image-generation` | 保留 | 入口 `amazon.md` + 完整 `amazon/`（含 8 张参考图） |
| `shopify-image-generator` | 保留 | 入口 `shopify.md` + 完整 `shopify/`（7 个 reference，含 `tea-tool` 暗调禅意 + `tea-tool-ugc` 文人茶室双路线） |
| `tiktok-shop-image` | 保留 | 入口 `tiktok-shop.md` + 完整 `tiktok-shop/`（3 个 reference） |
| `china-commerce-image-prompt-generator` | 保留（已 disable） | 入口 `taobao-jd-pdd.md` + 完整 `taobao-jd-pdd/`（4 个 reference） |
| `1688-image-prompt-generator` | 保留（已 disable） | 入口 `1688.md` + 完整 `1688/`（5 个 reference） |
| `ozon-image-prompt-generator` | 保留 | 入口 `ozon.md` + 完整 `ozon/`（5 个 reference） |
| `shopee` | 缺，本 skill 补齐 | `shopee.md`（规则内联） |
| `lazada` | 缺，本 skill 补齐 | `lazada.md`（规则内联） |
| `coupang` | 缺，本 skill 补齐 | `coupang.md`（规则内联） |

## 快速示例

### 例 1：单平台

```text
平台：TikTok Shop
国家：美国
品类：女装（V 领 + 灯笼袖 + 抽绳腰）
张数：5 张主图 + 5 张详情页
风格：TikTok Phone UGC（镜自拍 + 街拍）
```

→ 自动加载 `references/platforms/tiktok-shop.md`，按其 5+5 套图规则出确认稿。

### 例 2：跨平台

```text
同一件女包，要做 Amazon 主图 + Shopify PDP + TikTok Shop 详情页。
```

→ 依次加载 amazon.md / shopify.md / tiktok-shop.md，按各平台规则并行出提示词。

### 例 3：套图案例展示

```text
做套图案例展示 — 看下 TikTok Shop 连衣裙、Shopify 户外、Amazon 家具各 3 张。
```

→ 加载 `references/platforms/_case-gallery.md`，输出案例展示清单。
