# 每轮测试结果与计算口径

状态：已记录用户提供的 Discovery Test #1 外部搜索观测；豆包自然回答的有效样本仍为 0，出现率为 N/A。协议 P1 见 [baseline.md](baseline.md)，发现诊断与自然回答测试分别统计。

## Phase 4 / Discovery Funnel

记录日期：2026-09-17（Asia/Shanghai）；搜索测试实际时间未提供，不以录入日期替代。Repository：[公开资料库](https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research)。

| 层级 | 阶段 | 判定对象 | 当前状态 | 依据与限制 |
|---|---|---|---|---|
| L0 | PUBLICATION | 资料是否已公开发布 | PASS | 用户确认及 log.md OP-014：GitHub PUBLIC、main 已推送 |
| L1 | PUBLIC ACCESS | 匿名是否可读取公开页面 | PASS | 用户确认及 OP-014：三个公开页面 HTTP 200，正文标识与目标问题可见 |
| L2 | EXACT KEYWORD DISCOVERY | 精确标识查询是否返回本实验资料 | NOT_YET_DETECTED | 用户报告精确查询 NO RESULT；引擎、时间和截图待补 |
| L3 | KEYWORD + TOPIC DISCOVERY | 标识加主题查询是否返回本实验资料 | NOT_YET_DETECTED | 用户报告两条组合查询均 NO RESULT；仅限本轮观察 |
| L4 | TARGET PLATFORM RETRIEVAL | 豆包是否检索到本实验公开资料 | NOT_TESTED | 尚无针对已发布实验资料的检索证据；此前 Baseline 检索其他网页不算通过 |
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

结果结论：公开发布与公开访问通过，Discovery Test #1 暂未检出；目标平台对本实验资料的检索及自然回答复测未执行，无法判断豆包优化效果。本文件采用手工记录，当前没有自动采集或计算程序。
