# 跨平台套图案例展示库

当用户说「套图案例展示」「看套图案例」「做几组套图案例」「出 3 套跨平台套图」时，加载本文件。目标是产出**多平台套图示范**，让用户直观看到不同平台调性、版式、卖点承接方式，而不是直接出实际商品图。

## 用法

```text
做套图案例展示 — TikTok Shop 连衣裙 / Shopify 户外 / Pinterest 宠物 各 3 张
```

或：

```text
出 3 套跨平台套图案例：Amazon 女装 + 1688 工厂 + Shopee 东南亚
```

模型根据用户指令生成对应的「案例卡片」：每张案例卡列出平台、品类、张数、风格、每张图的画面描述和提示词骨架，**不调用生图工具、不执行任何生图动作**（即使用户说"生成图片"，也只交付提示词，由用户自行粘贴到生图工具生成）。

## 案例库结构（持续积累）

每张案例卡按以下骨架输出：

```markdown
## 案例 {N}：{平台名} · {品类} · {数量} 张 · {风格}

### 平台定位
- 主战场 / 主流量入口：
- 关键合规：
- 主语言：
- 视觉调性：

### 套图结构
| 张数 | 类型 | 比例 | 模块目标 | 风格关键词 |
|---|---|---|---|---|

### 每张图要点
#### G1. {图类型}
- 画面：
- 产品：
- 卖点：
- 场景：
- 文案策略：
- 提示词骨架（{几行描述}）：

#### G2. ...
（重复）

### 视觉签名
（这一套图的"一眼识别度"特征：背景/主色/字体/卡片/图标/光影/产品锚点/模特姿势 等）

### 不能照抄
（品牌 / 价格 / 活动 / logo / 平台 UI 等）

### 复用建议
（什么品类适合复刻这种结构）
```

## 默认预置案例

为方便用户快速查看，本 skill 默认预置以下案例（后续可扩展）：

1. **Amazon · 时尚女装（V 领 + 灯笼袖 + 抽绳腰 + 荷叶边碎花）** — 6+6 套图范本（白底主图 + 场景正侧背 + 详情页主题大场景 + 3 圆框细节 callout + UGC 买家秀 + 尺码虚线标注图）。完整复盘见 `references/platforms/tiktok-shop/case-dress-maxi-puff-sleeve.md`。
2. **Shopify · 户外家具家居（GreenWood Style Pack）** — 28 张独立站全站装修（社媒获客 + 网站功能页 + Hero Banner + 产品详情 + 品牌/B2B）。完整规则见 `references/platforms/shopify/greenwood-style-pack.md`。
3. **TikTok Shop · 美区连衣裙** — Phone UGC 镜自拍 + 街拍 + 咖啡店 + 详情页尺寸/洗护。完整复盘见 `references/platforms/tiktok-shop/ugc-fashion.md`。
4. **Ozon · 时尚女装** — 大俄文标题封面 + 卖点副图 + 细节 callout + 场景。完整规则见 `references/platforms/ozon/ozon-fashion-layouts.md`。
5. **Shopee · SG 女装 / 3C** — 平台卡首图 + 副图 + 详情页。参考 `references/platforms/shopee.md`。
6. **1688 · 工厂 / 工具 / 包装礼盒** — 主图 + 白底图 + 规格图 + 工厂实力图 + 包装发货图。完整规则见 `references/platforms/1688/1688-main-sub-image-logic.md` + `references/platforms/1688/1688-factory-trust-logic.md`。
7. **Coupang · 3C 韩文大字海报** — 火箭配送 + 韩文大字 + 多 SKU。参考 `references/platforms/coupang.md`。
8. **Lazada · 东南亚 3C / 家居** — 多语言 + 3C 卖点图。参考 `references/platforms/lazada.md`。


## 用户自定义案例

用户可说：

```text
套图案例展示：自己挑 3 个平台 + 3 个品类，出一组案例
```

模型自动从电商平台中挑选 3 个组合，输出 3 张案例卡。

```text
套图案例展示：Amazon / Shopify / TikTok Shop 都做一组女装套图
```

模型自动针对女装品类，按 3 个平台各自的规则出 3 套对照。

## 扩展约定

新增案例时，在对应平台的**子目录**新建案例文件（命名规范 `{品类}-{风格}.md`，如 `tiktok-shop/3c.md`），并在本文件 `_case-gallery.md` 加一行索引、在平台入口文件的路由表加一行引用。**不要**往入口文件里追加案例章节。
