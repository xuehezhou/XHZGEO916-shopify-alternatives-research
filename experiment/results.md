# 每轮测试结果与计算口径

状态：Round #1 已完成（用户确认）；已记录 Discovery Test #1 及 Doubao Retrieval Test #1：A/B=NOT_FOUND、C=FOUND_INCORRECTLY（错误关联，不是正确检索）。Phase 5 / Distribution Round #2 调整为 GitHub Pages 独立静态网页，已实际验证公开访问并登记 PUBLISHED；Juejin、Douyin 均为 SKIPPED。豆包自然回答有效样本仍为 0，出现率 N/A。协议 P1 见 [baseline.md](baseline.md)。

## Phase 4 / Discovery Funnel

### 当前状态（Query C 登记后 / Phase 5）

按用户本次指定口径维护以下层级；旧口径保留在后方历史表中，避免把层级调整误记成新的测试结果。

| 层级 | 阶段 | 当前状态 | 依据与限制 |
|---|---|---|---|
| L0 | Publication | PASS | GitHub 与 GitHub Pages 已公开；知乎/CSDN 发布为用户反馈，见 OP-017/OP-025 |
| L1 | Public Access | PASS | 已核验 GitHub 与 GitHub Pages 匿名 HTTP 200；不扩展为知乎/CSDN 匿名访问验证通过 |
| L2 | General Search Discovery | NOT_YET_DETECTED | Discovery Test #1 三条诊断查询的用户观测，无新增公开搜索测试 |
| L3 | Doubao Exact Retrieval | NOT_FOUND | Query A 精确实体查询与 Query B 显式搜索均未找到，依据用户观测 |
| L4 | Doubao Topic Association | INCORRECT | Query C 的用户观测为 FOUND_INCORRECTLY，模型猜测未建立正确调研关系 |
| L5 | Natural Answer Mention | NOT_TESTED | 尚无原始目标问题的自然回答复测 |

口径映射：旧 L2 精确关键词与旧 L3 关键词加主题发现合并到当前 L2；旧 L4 目标平台检索在当前口径下区分为 L3 精确实体检索与 L4 主题关联。Query A/B/C 不计入 L5 自然提及。CONTENT SEMANTICS=PASS（用户认可已审核内容，不等于豆包已理解）；当前工作诊断的主要瓶颈是 Discovery / Retrieval，具体原因未确定。NEXT ACTION：READY_FOR_DISCOVERY_TEST。

### 历史漏斗快照（Query A 登记后，旧口径）

记录日期：2026-09-17（Asia/Shanghai）；搜索测试实际时间未提供，不以录入日期替代。Repository：[公开资料库](https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research)。

| 层级 | 阶段 | 判定对象 | 当前状态 | 依据与限制 |
|---|---|---|---|---|
| L0 | PUBLICATION | 资料是否已公开发布 | PASS | 用户确认及 log.md OP-014：GitHub PUBLIC、main 已推送 |
| L1 | PUBLIC ACCESS | 匿名是否可读取公开页面 | PASS | 用户确认及 OP-014：三个公开页面 HTTP 200，正文标识与目标问题可见 |
| L2 | EXACT KEYWORD DISCOVERY | 精确标识查询是否返回本实验资料 | NOT_YET_DETECTED | 用户报告精确查询 NO RESULT；引擎、时间和截图待补 |
| L3 | KEYWORD + TOPIC DISCOVERY | 标识加主题查询是否返回本实验资料 | NOT_YET_DETECTED | 用户报告两条组合查询均 NO RESULT；仅限本轮观察 |
| L4 | TARGET PLATFORM RETRIEVAL | 豆包是否检索到本实验公开资料 | Query A：NOT_FOUND；原始目标问题：NOT_TESTED | 用户报告精确实体诊断未找到匹配；模型字符拆解不算检索成功；详见下方 Query A |
| L5 | NATURAL ANSWER MENTION | 豆包在无标识提示的原始问题回答中是否自然提及标识 | NOT_TESTED | 尚无对应复测证据；诊断查询不计入 P1 出现率 |

漏斗各层独立按证据记录；上层通过不自动表示后续层通过。PUBLICATION = PASS，PUBLIC_ACCESS = PASS，SEARCH_DISCOVERY = NOT_YET_DETECTED。搜索结果未检出不等于实验失败，也不能据此断言所有搜索引擎均未收录。

## Discovery Test #1

- Round：Discovery Test #1。
- Channel：GitHub（内容发布渠道，不是已知的搜索引擎名称）。
- Keyword：XHZGEO916。
- Target Query：Shopify有哪些适合中小卖家的替代品？
- Repository：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research
- 证据来源：用户本轮提供的外部搜索结果文字；助手本轮未独立执行搜索。
- 实际测试时间、搜索引擎、地区/语言、登录状态、结果页 URL、截图及检索范围：均未提供，待补。录入时间不作测试时间。

| 测试 ID | 完整查询（按用户原文） | Result | 对应层级 | 判定 |
|---|---|---|---|---|
| D1-01 | `"XHZGEO916"` | NO RESULT | L2 | NOT_YET_DETECTED |
| D1-02 | `"XHZGEO916" Shopify` | NO RESULT | L3 | NOT_YET_DETECTED |
| D1-03 | `"XHZGEO916" "Shopify" "中小卖家"` | NO RESULT | L3 | NOT_YET_DETECTED |

结论：GitHub 公开页面已经存在，但在用户报告的本轮公开搜索中，暂未检测到目标关键词对应的实验资料。当前仅说明搜索索引尚未检测到，不判定实验失败，不填入虚构的收录日期、排名、索引延迟原因或预计收录时间。

本轮三条查询是发现诊断，不属于豆包 P1 自然回答样本，不把 3 次 NO RESULT 换算成自然回答出现率 0%。保留原始记录，后续测试使用新轮次追加，不能覆盖本轮未检出的结果。

## Doubao Retrieval Test #1 / Query A

- 测试 ID：DBR1-A。
- Platform：豆包。
- Query：`XHZGEO916是什么？`
- Result：NOT_FOUND。
- Recorded At：2026-09-17 10:34:56 +08:00（登记时间，不是实际测试时间）。
- 证据来源：用户提供的测试结果及观察摘要；助手未独立执行此查询。实际测试时间、完整回答、截图、会话条件和检索来源列表未提供，保留未知。

### Observed

用户观察到豆包明确表示，全网公开检索没有匹配到 XHZGEO916。随后模型按字符结构推测 XHZ 是自定义前缀、GEO 指 geography/GIS、916 是序列编号，并猜测它可能是个人项目编号、内部业务编码或输入错误。

以上是用户转述的模型推断，不是已核验的实体含义，不属于正确 Retrieval；“全网公开检索没有匹配”仅作为模型在本次回答中的表述记录，不视为已证明所有公开搜索或网页均无该标识。

### Expected / Diagnosis

- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识，不是产品、公司、SaaS、品牌或 Shopify 替代品。
- Diagnosis：Exact Entity Retrieval 尚未成功（仅限本次 Query A 用户观测）。
- **L3 Doubao Exact Retrieval = NOT_FOUND**。
- 层级口径：上项沿用本次用户指定的豆包精确实体诊断标签。原 Discovery Funnel 的 L3 是 KEYWORD + TOPIC DISCOVERY，两者不互相覆盖；本次诊断对应原漏斗 L4 下的精确实体查询，原始目标问题检索仍为 NOT_TESTED。
- 不据此判定整体实验失败，不推断索引延迟原因，不归因到 GitHub、知乎或 CSDN 中某一渠道。渠道级来源证据未提供，既有渠道表不补造结果。
- Query A 在 Prompt 中直接给出标识，属于辅助诊断，不计入 P1 自然回答出现率，也不把模型复述或拆解标识算作自然提及；有效自然回答样本 N 仍为 0，出现率 N/A。
- Query A 登记时：Query B / Query C 均为 NOT_TESTED，等待用户提供测试记录；Query B 的后续记录见下节。
- 当时 NEXT ACTION：WAITING_FOR_QUERY_B_AND_QUERY_C。仅登记结果，不修改研究内容，不发布新渠道，不自动继续测试。

## Doubao Retrieval Test #1 / Query B

- 测试 ID：DBR1-B；Platform：豆包。
- Query：`搜索一下XHZGEO916`
- Result：NOT_FOUND。
- Recorded At：2026-09-17 10:39:42 +08:00（登记时间，不是实际测试时间）。
- 证据来源：用户提供的测试结果与观察摘要；助手未独立执行此查询。实际测试时间、完整回答、截图、会话条件和检索来源列表未提供，保留未知。

### Observed

用户明确要求搜索 XHZGEO916 后，豆包仍表示：“全网公开检索没有匹配到该编号”。随后模型猜测其可能是输入错误、内部私有编码、GNSS/测绘编号等。

以上引文与观察来自用户提供的记录。后续猜测均属于模型推断，不是对公开 GEO 内容的 Retrieval，也不是 XHZGEO916 的真实定义。模型表述不作为全网未收录的独立证明；仅凭回答摘要不推断实际搜索覆盖范围或工具执行细节。

### Expected / Diagnosis

- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识，不是产品、公司、SaaS、品牌或 Shopify 替代品。
- **Diagnosis：Explicit Search Retrieval = NOT_FOUND**。
- **L3 Doubao Exact Retrieval = NOT_FOUND**；本次显式搜索未建立与公开调研的正确关联。
- Query A/B 属于两种不同措辞的诊断观测，不证明持续或全网不可检索，不据此归因于任一发布渠道，也不判定整体实验失败。
- Query B 的 Prompt 直接含实验标识，不计入 P1 自然回答样本或自然提及出现率；N=0、出现率 N/A 不变。
- Query B 登记时：Query C 待提供，L4 Doubao Topic Association = WAITING_TEST；L5 Natural Answer Mention = NOT_TESTED。Query C 后续记录见下节。
- 当时 NEXT ACTION：WAITING_FOR_QUERY_C。仅本地记录，不修改 Mother Content，不发布新渠道，不自动测试。

## Doubao Retrieval Test #1 / Query C

- 测试 ID：DBR1-C；Platform：豆包；Query：`XHZGEO916和Shopify有什么关系？`
- Result：FOUND_INCORRECTLY（保留用户原始结果标签；表示错误关系猜测，不表示找到了公开资料）。
- Recorded At：2026-09-17 10:43:08 +08:00；实际测试时间未提供，不以登记时间替代。
- Observed：用户报告模型错误推测为 ERP 内部编号、私有 Shopify App ID、GEO 地区功能编号、主题/Pixel/脚本标记。均为模型推断，不是正确 Retrieval。
- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识，不是产品、品牌、公司、SaaS 或 Shopify 替代品。
- Diagnosis：DOUBAO TOPIC ASSOCIATION = INCORRECT；L4 更新为 INCORRECT。未建立正确语义关系，也没有已核验的来源命中证据。
- 证据来源：用户文字观测；完整回答、截图、检索来源列表及会话条件未提供，助手未独立执行查询。不把猜测写入真实实体表，不据此证明全网未收录或判定整体实验失败。
- 计量：Prompt 中直接提供标识及 Shopify，为辅助关联诊断，不计入 P1 自然回答样本；N=0、出现率 N/A，L5=NOT_TESTED 不变。

## Distribution Round #2

- Phase：5 / Independent Public Page；Channel：GitHub Pages；Type：Independent Static Web Page。
- Target：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- Reason：不继续增加需要额外账号或视频制作的渠道；利用当前公共仓库发布可直接读取正文的独立 HTML 页面。
- 计划变更：本轮原抖音、掘金方案均取消，Juejin=SKIPPED、Douyin=SKIPPED；已有素材保留，不继续发布。历史准备与阻塞记录见 OP-020 至 OP-024。此变更是执行成本选择，不是渠道检索效果结论。
- 变量控制：保留 GitHub、知乎、CSDN 既有发布，仅新增 GitHub Pages 页面；Mother Content 核心结论不变。新页面被访问不表示已被发现或召回，后续效果不能未经证据归因。
- Repository：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research
- Public URL / HTML canonical：https://xuehezhou.github.io/XHZGEO916-shopify-alternatives-research/
- 完整调研资料来源仍为 GitHub Repository；新页面 HTML canonical 指向自身的实际 Pages URL。
- Branch / Source：main /docs；build_type=legacy；docs/.nojekyll；无框架、后端、构建依赖或执行脚本。
- Content Commit：5efb57ca62f277ab39f3db8d7ecc72bac980d17d（feat: add public GEO research page）。
- Build Completed At：2026-09-17 16:24:56 +08:00（GitHub Pages builds/latest status=built、updated_at=2026-09-17T08:24:56Z）。
- Public Access Verified At：2026-09-17 16:25:43 +08:00；无 Authorization/Cookie 的独立 HTTP 请求返回 200。
- Published At：2026-09-17 16:25:43 +08:00（保守采用完整公开验证时间，不声称为最早可访问时刻）。

| Channel | 当前状态 | URL | Published At | DISCOVERED | RETRIEVED | MENTIONED |
|---|---|---|---|---|---|---|
| GitHub Pages | PUBLISHED | https://xuehezhou.github.io/XHZGEO916-shopify-alternatives-research/ | 2026-09-17 16:25:43 +08:00（公开验证时间） | NOT_TESTED | NOT_TESTED | NOT_TESTED |
| Juejin | SKIPPED | 不适用，本轮取消 | 未发布 | NOT_TESTED | NOT_TESTED | NOT_TESTED |
| Douyin | SKIPPED | 不适用，本轮取消 | 未发布 | NOT_TESTED | NOT_TESTED | NOT_TESTED |

- 验证：线上 HTML 与本地文件规范化换行后完全一致；title、description、canonical、唯一 H1、UTF-8、viewport、正文标识、目标问题、七个平台及非产品定义齐全。正文无需 JavaScript，只有不执行的 Article JSON-LD，省略未知作者及日期。
- 索引限制：HTML 无 noindex 或隐藏关键词，无 X-Robots-Tag；域名根 robots.txt 返回 404，无该文件的禁止规则。这些是技术可访问性检查，不是已索引证明。
- 外链：12 个 HTTPS 正文链接中 10 个独立请求返回 200；SHOPLINE 和 Shopify Payments 文档请求返回 403，随后通过网页读取工具成功打开原始官方 URL。所有来源地址沿用母文或指定仓库，内部锚点有效。
- 浏览器清单能看到已发布网页的正确标题和 URL，但正文可访问性树读取超时；公开验证依赖成功的匿名 HTTP 与 HTML 检查，不冒充完成浏览器截图或移动设备实测。
- 本轮未执行豆包或通用搜索测试；保留 Test #1 的历史观测，自然回答出现率仍为 N/A。NEXT ACTION：READY_FOR_DISCOVERY_TEST。到此停止。

## Distribution Round #1

- Phase：4.1 / First Distribution Round。
- 建立日期：2026-09-17（Asia/Shanghai），不是渠道发布时间。
- Channels：GitHub、Zhihu、CSDN。
- Target：XHZGEO916。
- Target Query：Shopify有哪些适合中小卖家的替代品？
- 本轮变量：在既有 GitHub 资料基础上，仅安排 P1 知乎、P2 CSDN 人工发布；掘金与抖音保持 HOLD。两条新增渠道构成本轮组合干预，未来效果不得未经证据归因到单一渠道。
- Canonical：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research

| 渠道 | 优先级 | 发布状态 | 准备状态 | URL | Published At | DISCOVERED | RETRIEVED | MENTIONED |
|---|---|---|---|---|---|---|---|---|
| GitHub | 既有来源 | PUBLISHED | 已公开 | https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research | 2026-09-16 19:44:13 +08:00 | NOT_YET_DETECTED（Discovery Test #1） | NOT_TESTED | NOT_TESTED |
| Zhihu | P1 | PUBLISHED（用户反馈） | 已收到人工发布 URL | https://zhuanlan.zhihu.com/p/2083862076452295407 | 未知（待补平台显示时间） | NOT_TESTED | NOT_TESTED | NOT_TESTED |
| CSDN | P2 | PUBLISHED（用户反馈） | 已收到人工发布 URL | https://blog.csdn.net/qq_68147780/article/details/165720888 | 未知（待补平台显示时间） | NOT_TESTED | NOT_TESTED | NOT_TESTED |
| Juejin | 本轮暂停 | HOLD | 不发布 | 不适用 | 未发布 | NOT_TESTED | NOT_TESTED | NOT_TESTED |
| Douyin | 本轮暂停 | HOLD | 不发布 | 不适用 | 未发布 | NOT_TESTED | NOT_TESTED | NOT_TESTED |

### 四项证据分别维护

| 状态 | 达成条件 | 必须保留的证据 |
|---|---|---|
| PUBLISHED | 具体渠道内容已实际发布并能确认公开页面 | 真实 URL、实际发布时间及平台显示/用户报告依据；匿名可读性另行检查 |
| DISCOVERED | 指定公开搜索的结果出现本实验真实内容 URL | 引擎、查询、时间、落地 URL 及结果证据；未检出不记实验失败 |
| RETRIEVED | 豆包针对记录的问题实际检索到本实验资料 | 完整 Prompt、检索候选 URL、时间和原始证据；候选出现与最终引用分开 |
| MENTIONED | 豆包在未提示标识的原始目标问题中自然提及标识 | 完整回答、时间、会话条件；字面提及与语义正确率按 P1 分别统计 |

发布成功只更新 PUBLISHED，不自动改成 INDEXED、DISCOVERED、RETRIEVED 或 MENTIONED。尚未执行的检测保持 NOT_TESTED，已有未检出的结果保持 NOT_YET_DETECTED；人工打开页面不算搜索发现。

2026-09-17 用户按约定提供知乎与 CSDN 人工发布 URL，据此登记为 PUBLISHED（用户反馈），关联日志 OP-017。CSDN URL 去除分享追踪参数后记录文章地址。用户未提供实际发布时间；助手网页工具未能读取两页，独立 HTTP 请求分别遇到知乎 403 与 CSDN SSL 连接错误，浏览器工具未列出可读取的标签页。因此匿名可读性、线上正文与本地稿一致性、标识及 Canonical 在线保留情况均待核验，Published At 保留未知，不以登记时间代替。

NEXT ACTION：等待人工补充可见发布时间或后续测试指令。按此前授权以 `docs: record first GEO distribution round` 提交并普通推送日志及本结果表；提交与推送结果以 Git 历史及本次回报为准。本轮只登记发布反馈，不执行新的搜索发现、豆包检索或自然提及测试。

## 计量规则

- 有效样本数 N：符合 P1、回答已完成且证据完整的样本数。未测试、失败和受污染样本不计入；无命中及无引用的正常回答计入。
- 正文命中数 H：豆包最终回答正文中，完整、大小写一致地出现 `XHZGEO916` 的有效样本数。每个样本最多计 1 次；嵌入更长字母数字串的不计；不计用户 Prompt、界面元素、URL 字符串、独立引用卡或展开的网页原文中的出现。
- **关键词出现率 = H / N × 100%**。N = 0 时显示 N/A，H 暂不计算；不能把 0/0 写成 0%。
- 正确关联数 C：正文命中且明确将标识描述为本调研标识或对应调研，并与中小卖家 Shopify 替代方案关联的有效样本数。若同时虚构成产品/公司/品牌，不计 C。
- **正确关联率 = C / N × 100%**；有 H 时可另报“命中中的正确比例 C/H”。
- 引用卡、标题或 URL 的标识出现单列“引用区命中”，不混入正文出现率。引用目标是否确为本实验发布内容、是否支持该句需打开核验；无法核验记“未知”。
- 错误实体化即使字面命中仍计 H，但单列错误并不算实验语义目标达成。
- 比较轮次使用相同协议和环境。出现率变化 = 本轮出现率 − B0 出现率，单位为百分点；任一轮 N = 0 时为 N/A。

## 轮次汇总

| 轮次 | 阶段 | 实际时间窗口 | 协议/环境 | 关联操作 ID | 计划样本 | 已尝试 | 有效 N | 命中 H | 出现率 | 正确 C | 正确关联率 | 引用本实验内容的有效样本数 | 错误实体化样本数 | 相比 B0（百分点） |
|---|---|---|---|---|---|---:|---:|---|---|---|---|---|---|---|
| B0 | 优化前基线，B0-01 检索层观察已收到，回答证据待补 | 待填 | P1 / 环境待补 | 无公开干预 | 5 | 已报告 1 次观察，完整尝试数待补 | 0 | 未计算 | N/A | 未计算 | N/A | 未计算 | 未计算 | N/A |

R1、R2 等复测轮次仅在实际执行后添加。每轮固定计划 5 个有效样本，失败尝试全部保留；如未完成则报告实际 N 及原因，不补造数据。测试窗口应在执行前写入日志，避免选择性汇报。

## 单次结果登记表

当前无完整自然回答数据；执行后逐行追加，包括失败尝试。B0 原始证据维护在 baseline.md，此处引用同一份证据，避免重复转录产生冲突。Discovery Test #1 仅登记在上方独立表格。

| 样本 ID | 轮次 | 实际时间 | Prompt/环境 | 有效性及原因 | 正文命中（1/0/未知） | 正确关联（1/0/未知） | 引用区命中 | 引用本实验内容及核验状态 | 错误实体化 | 品牌与引用记录位置 | 原始证据位置 |
|---|---|---|---|---|---|---|---|---|---|---|---|

## 汇总与解释

1. 核对样本 ID 唯一性、证据完整性及协议执行情况，记录排除原因。
2. 从有效记录统计 N、H、C，保留整数分子/分母，百分比保留两位小数。
3. 把测试轮次关联到 log.md 中的操作 ID、实际发布时间、平台和 URL；记录距发布时间的间隔。
4. 检索实验标识的诊断查询、追问及变体问题另行标记为诊断，不纳入 P1 出现率。
5. 单次或小样本命中只能表示观察结果；平台随机性、索引延迟、个性化及模型变化均可能影响结果，不能仅凭前后差异宣称因果或稳定排名。

结果结论：GitHub 公开发布与公开访问通过，Discovery Test #1 暂未检出；豆包 Query A/B 为 NOT_FOUND，Query C 为 FOUND_INCORRECTLY，主题关联 INCORRECT，均依据用户观测。原始目标问题自然回答复测未执行，出现率 N/A。本轮 GitHub Pages 已验证公开发布，掘金和抖音均为 SKIPPED；Mother Content 未修改，不预判新页面的索引或召回效果。
