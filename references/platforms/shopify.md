---
summary: Shopify 独立站主图/副图/PDP/变体图/促销 Banner SOP（含 GreenWood Style Pack 28 张全站装修）
read_when: 用户提到 Shopify、独立站、DTC、品牌官网、Premium DTC、Aesop/Apple/Herman Miller 调性、GreenWood、户外家具家居 Shopify 装修、茶具、紫砂壶、Yixing、茶器、文人茶室、紫砂 zisha、宜兴、茶宠、茶台、石茶盘
---

# Shopify 套图子模块

> 本文是 Shopify 入口索引：只含平台定位、平台硬规则和路由。类目的完整规则以 `shopify/` 子目录为**唯一事实源**，做具体类目时必读对应子文件。

## 平台定位

为 **premium DTC brands** 服务的套图 SOP。不是 marketplace 商品图，而是 Aesop / Apple / Herman Miller 级别的视觉系统。

## 平台硬规则：美学原则（最高级，贯穿所有类目）

1. **Less is always more.** Negative space 是 feature。
2. **Typography is brand architecture.** 每个字体、字号、字重、tracking、颜色都承载品牌意义。每张图最多 2 个字体。
3. **Lighting is the invisible brand.** 柔和阴影、定向光、轮廓光、控制反差。
4. **Color palette is sacred.** 2-3 主色 + 产品色 + 中性色。
5. **No clutter, no badges, no stacked sale tags, no urgency stickers.**
6. **Scene context must elevate, not distract.** 编辑感、策展感、博物馆感。
7. **Coherence is luxury.** 一套图必须像 DNA 一样贯穿。
8. **Reference the best, copy nobody.** 参考 Apple / Aesop / Rimowa / Herman Miller，但不复刻。

## 平台级 SOP 要点

- 完整流水线按业务位置：Main / Gallery → PDP / Description → Variant → Promo Banner →（GreenWood 全站装修）。
- **PDP 必须先定义一套连续视觉系统，再分屏输出**；本 skill 只交付可复制提示词，不执行生图。
- 图片角色不清晰时，先按 `_sop-common.md` 第 0 步判断产品图 / 参考图 / 竞品图 / 规格图，不要把参考图的商品当成客户产品。
- 完成后主动提示：是否继续变体图 / 活动海报。

## 默认套图结构（用户未指定类目时）

| 类型 | 业务位置 | 默认数量 | 比例 | 任务 |
|---|---|---|---|---|
| Main Image | 搜索结果 / 列表页 | 1 | 1:1 | 抢点击 |
| Gallery Images | 详情页图库第 2-6 张 | 4-6 | 1:1 / 3:4 | 解释功能/细节/场景/规格 |
| PDP / Description | 详情页长图 / 分段 | 6-8 屏 | 3:4 / 9:16 | 建立购买理由 |
| Variant Images | 颜色/尺码选择 | 2/variant | 1:1 | 白底看色 + 模特看效果 |
| Promo Banners | 季节/大促/广告 | 1-4 | 1:1 / 3:4 / 9:16 / 16:9 | 主题氛围 |

## 路由表（类目 → 必读子文件）

| 类目 | 必读文件 | 调性 |
|---|---|---|
| 服装 / 鞋包 / 配饰 | `shopify/fashion-main-sub-image-logic.md` | 模特 + 真实场景，多角度 |
| UGC / social-native fashion | `shopify/ugc-fashion-main-sub-image-logic.md` | 8 张（4 UGC Scene + 4 Phone-UGC） |
| 3C / 数码配件 | `shopify/3c.md` | Apple playbook：暗调高级 + 科技 DNA |
| 家具 / 家居 | `shopify/furniture-main-sub-detail-logic.md` | 建筑室内 |
| 户外 / 园艺 / 阳台（全站装修 28 张） | `shopify/greenwood-style-pack.md` | GreenWood Style Pack |
| 茶器 / 茶具（暗调禅意） | `shopify/tea-tool.md` | Aesop × 野兽派 |
| 茶器 / 茶具（文人茶室 UGC，9 张参考图在 `shopify/tea-tool-ugc/`） | `shopify/tea-tool-ugc.md` | 冷灰素墙 + 石茶台 + 自然光 |
| 化妆品 / 护肤 / 美妆个护 | `taobao-jd-pdd/cosmetics-main-sub-image-logic.md` + `taobao-jd-pdd/cosmetics-detail-page-logic.md` | 包装色系高级棚拍 |
| 口腔护理 | `taobao-jd-pdd/oral-care-main-sub-detail-logic.md` | 临床信任 + 功效 |

## 茶具双路线选择（重要）

茶具类目有两条并列视觉路线，**默认根据「产品价位 + 目标人群」路由；客户没指定时先问一句：「暗调高级感（Premium）还是浅色文人感（UGC）？」**，再走对应文件。两份文件独立维护，不要混用。

| 路线 | 必读文件 | 适合 |
|---|---|---|
| 暗调禅意（Premium DTC） | `shopify/tea-tool.md` | 高端礼盒、海外 DTC、商务礼品 |
| 文人茶室 UGC（自然光） | `shopify/tea-tool-ugc.md` | 中端日常、内外贸通用、禅意素雅风 |

## 维护约定

- 类目规则只写入 `shopify/` 子目录文件（美妆/口腔护理在 `taobao-jd-pdd/`）；本入口只维护路由和平台级规则。
- 茶具两条路线保持独立文件，不要合并。
- 原 `shopify-image-generator` skill 更新时，同步对应 `shopify/{类目}.md`。
- 用户提供新的 9 张 UGC 参考图时，按角色拆解并更新 `shopify/tea-tool-ugc.md` 的 slot map。
