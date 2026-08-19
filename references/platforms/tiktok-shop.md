---
summary: TikTok Shop 多国套图 SOP（Phone UGC + 信息详情 + 参数解释型）
read_when: 用户提到 TikTok Shop / TK Shop / 美区/巴西/墨西哥/英国/欧洲/东南亚 TK Shop 主图或详情页
---

# TikTok Shop 套图子模块

> 本文是 TikTok Shop 入口索引：只含平台定位、平台硬规则和路由。案例与品类范本的完整规则以 `tiktok-shop/` 子目录为**唯一事实源**。

## 核心判断：两种模式 + 一种信息图

1. **模式 A：TK 原生 UGC 场景图**（主图/相册默认）
   - **默认 Phone UGC**（手机拍摄质感：镜自拍 / 对镜自拍 / 朋友手机抓拍 / 咖啡店自拍，竖版 3:4，自然手机相机色调，不过度修图、不棚拍、不杂志大片）
   - 其次才考虑摄像 UGC（手持相机/微单拍摄，更清晰但仍保持达人随手感）
2. **模式 B：Amazon 式信息详情图**（尺寸/测量/面料/细节/洗护）
3. **模式 C：参数解释型卖点信息图**（车品/工具/家居/电子配件/户外等功能型产品）

## 硬规则

- **确认优先**：参考套图必须先输出确认稿，不直接生图。
- **本地化优先**：巴西葡语 / 墨西哥西语 / 英美英 / 东南亚本地语言；模特、场景、季节、单位制匹配目标市场。
- **默认直出完整图**：除非明确"后期排版/无字底图/留白"，否则默认直接生成可用成图。
- **文字少而清楚**：每张图 1 个短标题 + 2-5 个短标签；避免密集段落。
- **禁止小字密集排版**：默认改成大字模块/图标标签版。
- **主图/纯场景图/无文案图**：`no embedded text, no letters, no numbers, no typography`。
- **信息图/参数图**：默认直接带少量目标市场语言短标题和参数。
- **不写绝对化、医疗化、夸大化**：`best / #1 / guaranteed / 100%` 禁止。
- **不生成品牌、竞品、平台 UI、二维码、联系方式、水印**。

## 上传图片后的必问项

- 没指定国家/地区 → 问"目标国家/地区是哪里？"。
- 没指定套图风格 → 问"这套图想走什么风格？"，可选方向：
  - TikTok Phone UGC 手机原生风（默认推荐）
  - Amazon 信息详情风
  - 美式街拍/通勤风
  - 居家镜自拍风
  - 简洁高级棚拍风
  - 参数解释型卖点信息图
  - 甜酷/辣妹/度假/运动休闲等

## 工作流

1. 分析产品和参考图。
2. 识别目标市场。
3. 判断是否有参考套图。
4. 输出确认稿（参考套图映射 + 拟生成张数 + 每张提示词）。
5. 确认套图风格。
6. 选择模式（A/B/C）。
7. 选择比例：主图/Phone UGC `3:4`；详情页/PDP 信息图 `3:4` 优先；视频封面/广告 `9:16`。
8. 生成提示词（中文用于解释，prompt 默认英文）。
9. 等待用户确认后交付可复制提示词，由用户自行生图。

## 默认套图结构

### 用户只说"生成头 5 个"时

1. `1:1` 主图：模特正面全身/半身，真实场景，无字。
2. `1:1` 场景试穿：镜自拍或街拍。
3. `1:1` 版型图：侧面/背面/走动。
4. `1:1` 细节图：面料、蕾丝、领口、袖口、下摆。
5. `1:1` 平铺/搭配图：单品和配饰自然摆放。

> 实际越来越多 TK 套图改用 `3:4` 竖版以贴近手机滑屏，按用户/参考图优先。

### 完整详情页（8 张）

1. `1:1` 商品卡首图
2. `1:1` 主图相册-场景试穿
3. `1:1` 主图相册-版型展示
4. `1:1` 主图相册-面料/细节
5. `3:4` 详情页-简化尺码/尺寸说明图
6. `3:4` 详情页-测量说明图
7. `3:4` 详情页-洗护/面料说明图
8. `3:4` 详情页-搭配/包装/售后说明图

### 功能型产品参数解释型（6 张或 1 张 2x3）

1. 尺寸/规格
2. 材质/结构
3. 核心功能效果
4. 安装/使用步骤
5. 折叠/收纳/包装
6. 适配范围/使用场景

## 国家/地区市场风格

| 国家/地区 | 语言 | 模特/场景 | 单位 | 禁忌 |
|---|---|---|---|---|
| 美国 | English | 明亮卧室/公寓镜子/步行街/咖啡店 | inch | 医疗化、夸大、平台 UI |
| 巴西 | Brazilian Portuguese | 明亮公寓/城市街区/海滨度假 | cm | 同上 |
| 墨西哥 | Mexican Spanish | 城市街区/家居/通勤 | cm | 同上 |
| 英国 | British English | 街区/通勤/室内自然光 | cm | 同上 |
| 法国 | French | 优雅街区/公寓 | cm | 同上 |
| 德国 | German | 极简家居/办公 | cm | 同上 |
| 越南 | Vietnamese | 热带家居/出行 | cm | 同上 |
| 泰国 | Thai | 室内/热带 | cm | 同上 |
| 马来西亚 | Malay / English | 热带都市 | cm | 同上 |

## 模式提示词重点

### 模式 A：TK 原生 UGC 场景图

- `realistic phone-captured UGC fashion photography`
- `phone mirror selfie / front-facing phone selfie / friends phone snap`
- `natural daylight` / `warm indoor phone camera light`
- `{local market} casual home / street / coffee shop / apartment mirror / everyday lifestyle scene`
- `authentic try-on photo, unpolished creator content, slight phone camera color tone, no studio lighting`
- 避免：`professional studio lighting` / `glossy magazine shoot` / `over-retouched`

### 模式 B：Amazon 式信息详情图

- `clean ecommerce detail infographic`
- `clear readable localized short labels`
- `flat lay garment measurement layout with simple callouts`
- `neutral background`
- `Amazon-style product detail page image, complete ready-to-use layout`

### 模式 C：参数解释型提示词重点

- `clean TikTok Shop {local market} ecommerce infographic`
- `2x3 grid parameter explanation collage`
- `realistic product photography with clean callout boxes`
- `clear readable {local market} selling-point text`
- `dimension arrows, icons, layer cutaway, installation steps`
- `no brand logo, no watermark, no QR code, no TikTok UI`

## 路由表（案例/品类 → 必读子文件）

| 品类 / 任务 | 必读文件 |
|---|---|
| 3C 数码 / 充电宝 / 磁吸充电（1+1+3 参数解释型） | `tiktok-shop/3c.md` |
| 女装长裙 / 度假裙 / 专业棚拍（ANRABESS 6+6） | `tiktok-shop/case-dress-maxi-puff-sleeve.md` |
| 女装 Phone UGC / 跨境尺码表（7+2） | `tiktok-shop/ugc-fashion.md` |

## 维护约定

- 模式、硬规则、默认结构只在本入口维护；案例复盘写入 `tiktok-shop/` 子目录。
- 新增/重命名案例文件时，同步更新路由表。
