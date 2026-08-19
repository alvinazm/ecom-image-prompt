# ecom-image-prompt — 电商套图提示词工作台

一个 Codex skill：把用户输入（产品 / 平台 / 风格 / 数量）转换成**可直接复制**的 AI 生图提示词。只产出提示词，不执行任何生图动作、不调用生图工具，生成由用户自行在任意生图工具中完成。

## 功能特性

- **多平台覆盖**：Amazon、Shopify、TikTok Shop、淘宝 / 天猫 / 京东 / 拼多多、1688、Shopee、Ozon、Lazada、Coupang
- **自动路由**：识别用户提到的平台 / 品类 / 关键词，加载对应平台的规则模块
- **平台级硬规则**：每个平台遵循自己的审美与合规（Ozon 大字俄文、Coupang 韩文海报、Shopify premium DTC、1688 工厂信任等）
- **品类级知识库**：服装、3C、家具、美妆、口腔护理、茶器、户外等类目的完整套图逻辑与案例复盘
- **合规与本地化**：内置合规底线（不编造数据、禁止绝对化用语、禁平台 UI）与目标市场本地化（语言 / 模特 / 单位制）
- **案例库**：跨平台套图案例展示，直接复用已验证的视觉签名

## 使用方法

按标准字段提问，字段能省则省，缺失的由模型自动补全并先确认：

```text
平台：TikTok Shop
产品：女装 V 领灯笼袖抽绳腰连衣裙
地区：美国
套图要求：主图 5 张 + 详情页 5 张
规格：碎花/几何印花、收腰、长款、Boho Maxi
风格：Phone UGC 镜自拍 + 街拍
```

流程：识别平台与品类 → 加载对应平台模块 → 确认风格 → 输出确认稿 → 用户确认 → 交付完整提示词（并提示用户自行生图）。

> 社媒平台（Instagram / Pinterest / 小红书 / 抖音小红书 UGC 种草）请走 `ss-art-prompt-social-image`（社媒图需配贴文文案）。

## 项目结构

```
SKILL.md                                # 总入口：路由 + 总工作流 + 通用输出格式
references/platforms/
├── amazon.md / shopify.md / ...        # 9 个平台入口：定位 + 硬规则 + 路由表
├── amazon/ / shopify/ / ...            # 平台子目录：品类/图类型规则（唯一事实源）
├── shopee.md / lazada.md / coupang.md  # 规则内联型平台（无子目录）
└── _sop-common.md 等 3 个公共文件       # 跨平台共享 SOP、简报模板、案例库
```

分层原则：**入口只做路由，子目录是唯一事实源**。品类细节只写入子目录文件，入口文件不承载执行细节，避免内容重复与漂移。

## 与其他 skill 的关系

本 skill 是电商套图提示词的统一入口，汇总了原 Amazon / Shopify / TikTok Shop / 淘宝系 / 1688 / Ozon 等 skill 的平台逻辑，并补齐了 Shopee、Lazada、Coupang。原 skill 均保留，可继续单独使用；社媒类需求统一分流到 `ss-art-prompt-social-image`。

## 维护约定

- 品类 / 图类型规则只在 `references/platforms/{platform}/` 子目录维护
- 入口文件只维护平台定位、平台硬规则和路由表，不复述子目录细节
- 新增 / 重命名子文件时，同步更新入口路由表
- 原始 skill 更新时，同步对应子目录文件；社媒模块同步到 `ss-art-prompt-social-image`
