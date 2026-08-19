---
summary: Amazon 套图主图/副图/A+/详情页长图 SOP（含完整 Listing 双交付）
read_when: 用户提到 Amazon 套图、亚马逊主图白底、A+、Product Description 长图、listing 上架素材、品类包含服装/3C/家具/美妆等
---

# Amazon 套图子模块

> 本文是 Amazon 入口索引：只含平台定位、平台硬规则和路由。品类/图类型的完整规则以 `amazon/` 子目录为**唯一事实源**，做具体品类时必读对应子文件。

## 平台定位：先页面位置，再品类

Amazon 至少有 4 类不同图片面，先判断做哪一类，再进品类规则：

1. `main-image` — 第一张主图，搜索结果可见。优先合规：白底、无字、无 logo、无卖点贴片。
2. `gallery-secondary` — 顶部图库第 2-N 张。服装/裤子/童装/宠物服饰/鞋类优先 `3:4` 竖版。
3. `a-plus` — 下方 A+ / From the brand / Product Description 模块。常用 `970x600`、`970x300`、`300x300`、`300x400`、`600x180`。
4. `long-description` — 把多个 A+ 风格模块竖向拼成一张长图。`970px` 宽，分段生成后拼接。

> A+ / 长图的模块级画布规则（如 1792×1024 生成再裁切）见 `amazon/fashion.md`、`amazon/3c.md`、`amazon/furniture.md` 等子文件的「画布规则」。

## 平台硬规则（不随品类变化）

### 文字策略

- `main-image`：不放文字、logo、角标、卖点图形、边框。
- `gallery-secondary`：可以有短文字，建议 1 个标题 + 3 个以内短标签。
- `a-plus` / `long-description`：可有文字；生产级做法"先生成无字画面，再设计叠字"；AI 直接出字只适合大字短句少量标签。
- 尺码表 / 成分表 / 护理图标 / 密集参数表：不要依赖 AI 直接画字，应该后期确定性排版。
- 提示词里含文字时必须明确字体方向（clean bold sans-serif / modern condensed sans-serif 等）。

### 合规底线

- 主图显示真实售卖产品；纯白背景 `#FFFFFF`；无文字、logo、水印、边框、促销角标、拼图、小窗、道具。
- 主图产品占画面主要面积，清楚锐利。
- 副图和 A+ 可以有场景和文字，但不能做虚假、无法证明、医疗化、竞品对比、促销式 claim。
- 童装、宠物用品、健康相关日用品，claim 要更保守。

### Listing 双交付（生图 + 文案）

用户说"做 listing / 生成 listing / 上架素材 / 图文一起出" → 触发双交付：

```text
【Listing 文案】
站点：
标题：
5点描述：
  1. ...
  2. ...
  3. ...
  4. ...
  5. ...
商品说明：
后台关键词：
```

## 默认套图结构（用户未指定品类时）

| 模块 | 页面位置 | 默认尺寸 | 作用 |
|---|---|---|---|
| 1 | `main-image` | 2000x2000 | 白底清晰展示实际产品 |
| 2 | `gallery-secondary` | 3:4 竖版 1500x2000 或 1800x2400 | 正面/整体/上身 |
| 3 | `gallery-secondary` | 3:4 | 背面/侧面/另一角度 |
| 4 | `gallery-secondary` | 3:4 / 1:1 | 细节特写 |
| 5 | `gallery-secondary` | 3:4 / 1:1 | 尺寸/尺码/容量/安装 |
| 6 | `gallery-secondary` | 3:4 / 1:1 | 场景图 |
| 7 | `a-plus` | 970x600 起 | 品牌/功能/详情页模块 |
| 8 | `long-description` | 970 宽 | 多模块竖向拼接长图 |

## 路由表（品类 → 必读子文件）

| 品类 / 任务 | 必读文件 |
|---|---|
| 服装 / 鞋 / 帽（A+ 6 模块、主副图、尺码） | `amazon/fashion.md` |
| 3C 数码（充电宝/充电器/耳机/线材/外设，Anker 基准结构） | `amazon/3c.md` |
| 3C 品牌风格详版（Anker 风） | `amazon/3c-anker.md` |
| 家具（电脑桌/书桌/收纳柜/文件柜） | `amazon/furniture.md` |
| 参考图（furniture_47_desk 完整 8 张源图） | `amazon/sources/furniture_47_desk/` |
| 女装长裙棚拍案例（V 领灯笼袖碎花度假裙 6+6） | `tiktok-shop/case-dress-maxi-puff-sleeve.md` |

> `amazon/3c.md` 与 `amazon/3c-anker.md` 内容相同（同骨架），按是否点名 Anker 风格选择；若确认冗余可合并为一个文件。

## 维护约定

- 品类规则只写入 `amazon/` 子目录文件；本入口只维护「页面位置判断、平台硬规则、默认套图结构、路由表」。
- 新增/重命名子文件时，同步更新上方路由表。
