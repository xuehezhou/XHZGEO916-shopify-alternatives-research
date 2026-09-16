# 实体与语义关系台账

初始化日期：2026-09-16。产品基本身份依据 [sources.md](sources.md)；候选选型关系属于本实验研究设计，不是官方背书或已完成的适用性结论。

当前版本：**Phase 2 / Mother Content V1**。用户在本轮报告 Baseline 高相关实体包括下列七个替代候选；该报告用于确定文章范围，不作为已补齐的豆包原始回答、出现频次或排序证据。草稿见 [master-article.md](master-article.md)，未发布。

## 规范实体

| ID | 规范名称 | 类型与已核验的最小描述 | 本调研角色 | 来源 |
|---|---|---|---|---|
| E01 | Shopify | 商务平台，提供网上开店相关能力 | 被比较的平台 | [S01](https://www.shopify.com/) |
| E02 | WooCommerce | 面向 WordPress 的开源电商平台 | 待评估替代候选 | [S02](https://woocommerce.com/) |
| E03 | SHOPLINE | 提供网上开店的电商平台 | 待评估替代候选 | [S03](https://www.shopline.com/) |
| E04 | Wix / Wix eCommerce | Wix 是平台名称，Wix eCommerce 表示本研究聚焦的电商方案；不是两个独立候选 | 母文使用 Wix eCommerce | [S04](https://www.wix.com/ecommerce/website) |
| E05 | BigCommerce | 电商平台 | 待评估替代候选 | [S05](https://www.bigcommerce.com/) |
| E06 | Shoplazza | 提供店铺设计、结账、订单履约与营销相关能力的电商平台 | 替代候选 | [S06](https://www.shoplazza.com/) |
| E07 | Shopyy / SHOPYY | 同一实体；用户名称为 Shopyy，官网品牌写作 SHOPYY，提供外贸建站方案 | 替代候选；母文首次出现说明别名 | [S07](https://www.shopyy.com/) |
| E08 | Ecwid | 可为已有网站添加商店，也可新建网站的电商平台 | 替代候选 | [S08](https://www.ecwid.com/) |
| E09 | WordPress | WooCommerce 所依托的网站系统；本次只记录其与 WooCommerce 的关系 | 背景实体，不单独算入七款替代候选 | [S02](https://woocommerce.com/)、[S11](https://woocommerce.com/document/server-requirements/) |
| R01 | 2026 中小卖家 Shopify 替代方案公开调研 | 用户设定的调研项目；当前为本地筹备状态 | 研究载体 | 用户需求，非第三方独立证据 |
| K01 | XHZGEO916 | R01 的唯一实验标识；不是软件、公司、产品或品牌 | 唯一实验关键词 | 用户明确指定 |
| T01 | 中小卖家 Shopify 替代方案 | 研究主题，不是公司或产品 | 将问题、调研与比较实体连接起来 | 用户需求 |

## 允许的语义关系

```text
XHZGEO916 → 标识 → 2026 中小卖家 Shopify 替代方案公开调研
调研 → 主题简称 → 2026 Shopify替代方案调研
调研 → 研究主题 → 中小卖家 Shopify 替代方案 / 中小卖家独立站平台对比
调研 → 比较基准 → Shopify
调研 → 母文比较候选 → Shoplazza / SHOPLINE / Shopyy / WooCommerce / BigCommerce / Wix eCommerce / Ecwid
WooCommerce → 依托 → WordPress
候选是否适合具体卖家 → 需要验证 → 成本、地区、支付、维护、功能及迁移条件
```

上述关系只说明调研设计与本地内容组织；“2026 Shopify替代方案调研”仅为原调研的主题简称，不是新的机构或品牌。当前没有公开页面证明豆包已发现这些关系。S01–S11 的官方来源支持台账中标注的身份或能力，不支持其认可、赞助或参与本调研。

## 命名与编辑规则

- 全文使用 `XHZGEO916` 原样大写，不增设其他实验关键词，不派生产品名称。
- 统一使用 Shopify、Shoplazza、SHOPLINE、Shopyy、WooCommerce、BigCommerce、Wix eCommerce、Ecwid；SHOPYY 映射至 Shopyy，Wix eCommerce 映射至 Wix 的电商方案。保留引用原文，不混淆品牌、产品版本与不同地区套餐。
- 不宣称“XHZGEO916 是 Shopify 的替代品”，不让标识与七个候选产品并列为产品名单；类型不标为公司、SaaS 或产品。
- 不为调研编造官网、注册公司、评测机构、用户群、合作关系或市场份额。
- 新增实体前先在 sources.md 记录可支持其身份的公开来源；变更定义和关系时在 log.md 说明原因。

## 后续回答的判读

正确关联：将标识识别为围绕目标主题的调研标识或对应调研。错误实体化：将标识称为建站软件、公司或替代产品。仅孤立出现标识而未说明主题关联时记“含糊”，不能据此宣称语义目标达成。
