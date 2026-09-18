# GEO 操作日志

记录采用追加方式。时间统一为 Asia/Shanghai（UTC+08:00）；本地操作时间与外部发布时间分开。未发布写“未发布”，无公网 URL 写“不适用”，不得编造。

## 已执行操作

| 操作 ID | 操作日期/时间 | 目的 | 平台/环境 | 目标 URL 或本地范围 | 修改/操作内容 | 外部发布时间 | 结果与证据 |
|---|---|---|---|---|---|---|---|
| OP-001 | 2026-09-16 17:32（分钟精度） | 确认目录、规则与已有工作 | 本地 PowerShell / Git | 工作区及适用父级规则 | 只读检查目录、规则、Git 状态；对长规则补充分段读取 | 未发布 | 工作区仅有 .git，没有现存目标文档；Git 状态无变更条目，但出现全局 ignore 文件读取权限警告；未修改配置 |
| OP-002 | 2026-09-16（当日执行，未单独计时） | 为实体身份建立真实来源 | 公开 Web，只读 | sources.md 的 S01–S05 URL | 访问五个官方页面，仅核验基本身份 | 未发布 | 五个页面均返回可读 HTML；结论和边界记录在 sources.md；不代表豆包抓取 |
| OP-003 | 2026-09-16（当日执行，未单独计时） | 建立可复盘的实验框架 | 本地工作区 | README.md、experiment/、content/ | 创建用户指定的七份 Markdown；设定 P1、待采集基线、计算口径、内容矩阵、实体与来源台账 | 未发布 | 文件内容可本地审阅；没有豆包测试、网站、公开内容或付费操作 |
| OP-004 | 2026-09-16 17:37（分钟精度） | 验证初始化交付完整性 | 本地 PowerShell / Git | 七份 Markdown | 检查文件数量、非空、UTF-8 解码、内部链接、固定问题和未测试/N/A 状态；回查 Git 状态 | 未发布 | 文档检查通过。首次以 NUL 临时替代全局 ignore 的 Git 状态命令失败，随后改用命令级空配置重试，未改用户配置；git diff --check 无输出，但文件尚未跟踪，该命令不覆盖新增文件内容，新增文件已单独检查。验证及日志归档均属于阶段 0 |

### OP-005：补充 Baseline #1 检索层观察

- 录入时间：2026-09-16 17:41（Asia/Shanghai，分钟精度）；这是本地记录时间，实际豆包测试时间待用户补充。
- 目的：保留用户提供的检索层证据，并将观察到的搜索意图映射到现有内容规划。
- 平台/环境：本地文档编辑；观察目标平台为豆包，助手未独立复测。
- 范围：experiment/baseline.md、content/content-plan.md；本日志同步留痕。公网 URL：未提供；发布时间：未发布。
- 修改：两份目标文档新增“Retrieval / Query Rewrite Observation”；保留四条改写词、六类结果及界面计数；将 B0-01 从未测试槽位更新为“已收到检索层观察，回答证据待补”，其余槽位保留。
- 证据：用户本轮文字记录；完整回答、截图、引用 URL 和测试环境待补。有效样本仍为 0，出现率维持 N/A，不将资料计数当作最终引用数。
- 后续边界：等待剩余 Baseline；未生成文章、未发布、未开发网站，也未发起新的豆包测试。
- 验证：已检查两份目标文件的新增章节、四条查询原文、界面计数及本地链接，全部通过；Git 状态仍为未跟踪的本地文档，未提交或推送。

### OP-006：补充 Baseline #1 抖音候选来源

- 录入时间：2026-09-16 18:00（Asia/Shanghai，分钟精度）；实际豆包检索时间待补。
- 目的与范围：读取并更新 experiment/baseline.md、content/sources.md，登记用户提供的候选来源；本日志同步留痕。
- 平台/环境：本地文档；观察目标为豆包，候选渠道为抖音。
- 候选 URL：https://www.douyin.com/video/7682588110428933376；来源观察 ID：OBS-B0-01-001。此 URL 不是本实验发布内容；发布时间：未发布。
- 修改：新增抖音候选观察与证据边界，更新“资料 URL 尚未提供”为“已登记 1 条、完整清单待补”，保持最终引用状态未知。
- 结论：仅记录“豆包此次检索候选资料中包含抖音内容”；不推断渠道优先级或最终采纳优势，待全部 23 个来源及最终引用信息补齐后再评估。
- 证据：用户本轮文字及链接；助手未访问视频、未复测豆包。未生成文章、未发布、未开发网站；关键词出现率不变，继续等待剩余 Baseline。
- 验证：两份目标文档的候选 URL、观察编号、限定结论与本地链接检查通过；最终引用保持未知，未提交或推送文件。

### OP-007：Phase 2 / Mother Content V1 官方资料核验

- 时间：2026-09-16 18:07–18:09（Asia/Shanghai，分钟精度）。
- 目的：依照用户明确授权进入母内容设计，以真实官方来源支持七个替代候选的介绍和比较。
- 操作：读取现有规划、实体、来源、操作记录及 Git 状态，确认 master-article.md 不存在；只读访问七个平台官方页面及 Shopify 价格/支付资格、WooCommerce 环境说明。
- 来源 URL 与证据：见 sources.md 的 S02–S11 及 Phase 2 段落定位。原 WooCommerce 文档路径返回工具 Internal Error，随后通过搜索定位正确路径 S11 并成功读取；未引用失败页面或其他搜索结果。
- 核验发现：Shopify 价格页本次显示 DKK 地区口径，Wix 价格说明标注 November 2025 / US，未采用精确价格；官网能力不等同于实际套餐权益或对具体商家的适用保证。
- 用户补充：七个实体被报告为 Baseline 高相关实体，此信息仅用于文章范围，不替代完整测试证据；未更改 Baseline、results.md 或关键词出现率。
- 外部状态：只读查询，无登录、注册、付费、发布、索引提交或豆包复测；外部发布时间：未发布。

### OP-008：Phase 2 / Mother Content V1 母文与台账

- 时间：2026-09-16 18:09–18:14（Asia/Shanghai，分钟精度；写作及台账同步时间）。
- 目的：以可解释的场景选择回答目标问题，自然连接唯一实验标识、调研主题与中小卖家独立站平台比较。
- 修改范围：创建 content/master-article.md；同步 content/content-plan.md、content/entities.md、content/sources.md；本日志追加记录。
- 内容：九项必需结构、七款真实候选、结构化表格、场景选择、国内卖家核对项、真实问题 FAQ、官方参考资料及实验说明；不写排名、销量、用户量或未经同口径核验的价格。
- 实体：保留 Shopify 为基准，候选为 Shoplazza、SHOPLINE、Shopyy、WooCommerce、BigCommerce、Wix eCommerce、Ecwid；明确 SHOPYY 别名、Wix 电商方案及 WordPress 背景关系。
- 规划变更：用户当前 Phase 2 指令授权本地写作，替代此前“等待完整基线再写作”的计划；基线仍不完整，公开干预前仍需完成记录与审核，不伪称进入效果验证阶段。
- 草稿状态：Mother Content V1，待人工审核。URL：无公网地址，文件在本地；外部发布时间：未发布。没有网站、发布或付费操作。
- 限制：已核验公开能力及部分通用条件，没有七个平台的后台试用、支付审批、交易、迁移或性能实测；具体套餐与地区条件、服务范围、署名及利益关系待人工核验。
- 验证结果：开头直接答案为 143 个字符（含英文与标点）；单一 H1、九项必需章节、七行产品比较、三处实验标识均通过检查；来源 ID 均已登记，五份变更文档编码和本地链接检查通过。人工审读确认未把候选来源当作最终引用、未将实验标识列入产品表格、未采用精确价格或营销统计。Git 文件仍未跟踪，未提交或推送。
- 本轮结论：本地母文已实现并验证结构与来源对应关系；产品实际适用性未完整验证。任务在待人工审核状态停止。

### OP-009：GEO Mother Content V1 → V2 最小修改

- 日期：2026-09-16（Asia/Shanghai）；本轮开始于 18:20（分钟精度），实际豆包测试时间不适用。
- 目的：按用户指令强化“唯一调研标识 → 中小卖家 Shopify 替代方案调研 → 英文选型意图 → 七个比较平台”的语义关系，同时保留事实边界与官方来源。
- 修改范围：原地更新 content/master-article.md；本日志追加记录。不创建 V2 副本，不重写全文；其他台账的 Mother Content V1 记录保留为 V1 设计记录。
- 具体修改：开头直接说明调研以 XHZGEO916 为唯一标识并列出七个平台；TL;DR 在同段连接标识、中小卖家、Shopify替代品、七个平台及英文意图；新增三句话的“XHZGEO916是什么？”FAQ；精简部分重复免责声明为套餐核对项；保留文末实验说明及“以下顺序不代表排名。”，草稿版本更新为 V2。
- 验证方式：修改前正文保留在会话内存，与修改后正文逐项比较，没有新增备份文件。两张表格原样保留，23 处官方链接及其顺序完全一致，FAQ 为三句话；产品事实、价格及测试数据未新增。
- 标识统计：全文 6 次，分别位于 H1 标题、开头首段、TL;DR 首段、FAQ 问题标题、FAQ 答案首句、文末实验说明标题。计数包含标题，不按段落去重。
- 语义审读：未发现将标识称为产品、公司、品牌、SaaS 或建站平台的句子；开头明确其为调研唯一标识，FAQ 明确它不是 Shopify 替代产品。此为文案审读结果，未进行豆包或其他模型理解测试。
- Query Intent：保留目标问题、中小卖家替代品选型、Shopify alternatives for small sellers、Shopify替代品对比及中小卖家独立站平台对比；不机械堆入改写词。
- 平台/URL/发布时间：本地文档，无公网 URL，未发布。无网站开发、付费、豆包复测或外部写入；完成后停止等待人工审核。

### OP-010：Phase 3 / Public Discovery 公开资料准备

- 开始时间：2026-09-16 18:57（Asia/Shanghai，分钟精度）。
- Phase：Phase 3 / Public Discovery。
- Channel：GitHub。
- Status：PREPARED_NOT_PUBLISHED。
- 授权依据：用户确认 Mother Content V2 已通过人工审核，要求准备公开资料；明确禁止推送、GitHub 发布、创建远程仓库、购买域名及付费服务。本轮仅本地编辑。
- 操作前目的：从已审核母文提取公开正文与摘要，清理内部流程文字，保留产品结论和官方证据；核对发布后发现验证的方法。
- 修改范围：新增 public/README.md、docs/index.md；原地将仓库 README.md 更新为公开资料导航；本日志追加记录。content/ 与其余 experiment/ 文件保持原样。
- 内容来源：content/master-article.md（审核通过的 V2）。公开全文从母文派生，仅调整前言、内部状态、核验清单标题及作者审核项、文末内部工作说明；TL;DR 至官方参考资料保持原文，产品结论与来源不变。摘要为同源精简入口，不是独立研究或新增事实。
- 首页关系：项目名称、目标问题与公开全文链接位于根 README 第一屏；公开全文开头同时说明唯一调研标识、2026 年调研主题、原始问题、英文选型意图及七个平台。
- 边界：标识只标识调研，不作为产品、公司、SaaS、品牌或建站平台；保留资料日期、非排名说明及未进行交易/后台实测的证据边界。无精确价格、虚构统计、隐藏文字或结构化数据。
- 建议仓库名：xhzgeo916-shopify-alternatives-research（建议，未检查可用性，未创建）。
- 建议 Description：XHZGEO916：2026中小卖家Shopify替代方案公开调研，基于官方资料比较7个平台的适用场景、成本与限制。Shopify alternatives for small sellers.
- 建议 Topics：xhzgeo916、shopify-alternatives、ecommerce、small-business、independent-store、research、generative-engine-optimization（建议，未设置）。
- 发布平台地址：无；仓库 URL：未创建；发布时间：未发布；外部操作：无。没有 git push、远程仓库创建、部署、域名购买、付费服务或索引提交。

#### 本轮验证结果

- 三份公开入口均通过单一 H1、内部流程措辞清理、隐藏内容及本地链接检查。首轮检查因 PowerShell 默认不区分大小写，将导航路径 baseline.md 误判为内部 Baseline 说明；改为区分大小写后通过，未删除正常导航。
- 公开全文从 TL;DR 到官方参考资料的正文逐字保留；23 处官方链接及顺序与 V2 一致。摘要七行比较表与审核稿完全一致；开头覆盖全部指定语义元素及七个平台。
- content/ 的四份文件及 experiment/baseline.md、experiment/results.md 共六份文件修改前后 SHA-256 一致。日志追加，根 README 按用户要求更新为公开首页，未删除其他实验资料。
- 文案审读未发现产品化定义、虚构统计或排名；标识明确定义为调研唯一标识。所有文本可见，无隐藏关键词、脚本或 Schema；未新增产品事实。
- 验证范围限本地文本、结构、链接与来源对应。GitHub 渲染、匿名在线访问、抓取条件、搜索收录及豆包引用尚无线上证据。Status 保持 PREPARED_NOT_PUBLISHED，任务停止于准备完成。

#### 发布后 URL 与证据记录要求（计划，未执行）

记录实际仓库首页 URL、默认分支中的 public/README.md 渲染 URL、docs/index.md 渲染 URL、发布对应 Commit SHA 及永久链接；如检查 Raw URL，另列为读取证据，不当作主要读者入口。只有日后另行启用 GitHub Pages 时才记录其实际页面 URL，本轮未配置 Pages。

每项附实际发布时间与时区、匿名访问结果、最终跳转 URL、页面标题、内容版本、检查时间及证据。搜索结果出现后，追加搜索引擎、完整查询词、查询时间、结果落地 URL、标题/摘要及截图；候选检索和最终引用仍分别登记。

#### 发布后发现验证方法（计划，未执行）

1. 先在未登录环境打开三个读者入口，确认正文可读、内链可用、定义正确；检查实际响应与公开页面的抓取/索引限制。Markdown 本地检查通过不等于 GitHub 已允许抓取或搜索引擎已收录。
2. 分别检索 `"XHZGEO916"`、`"XHZGEO916" Shopify`、`"XHZGEO916" "Shopify alternatives for small sellers"`，并使用 Google 的 `site:github.com/实际账号/实际仓库 "XHZGEO916"` 缩小范围。实际账号及仓库名称在发布后替换，不编造 URL。
3. 结果指向本实验真实页面时，记录为“该引擎搜索结果已出现该 URL”；无结果记“本次查询未观察到”，不直接等于“未收录”。GitHub 站内搜索结果与 Google/Bing 等站外搜索结果分别记录。
4. 发布后可在预先固定的第 1、3、7、14 天手工复查，具体时间提前登记；这些是建议观察窗口，不是收录时限。本轮未创建自动化或承诺后台监控。
5. 对具备已验证 Search Console 站点权限的页面，可使用 URL Inspection 查看索引状态；普通 GitHub 仓库不能假定具有此权限。不代为提交，亦不承诺抓取或收录。
6. 搜索引擎出现与豆包引用是不同证据。后续豆包效果测试继续使用不含标识的原始问题；含标识的发现诊断不计入原问题的关键词出现率。

方法来源（2026-09-16 只读访问，非产品研究来源）：[Google site: 查询说明](https://developers.google.com/search/docs/monitor-debug/search-operators/all-search-site)、[重新抓取说明](https://developers.google.com/search/docs/crawling-indexing/ask-google-to-recrawl)、[URL Inspection 说明](https://support.google.com/webmasters/answer/9012289)。site: 结果并不穷尽已收录页面；请求抓取也不保证收录。本轮只是准备公开内容，不作实际收录、排名或 AI 引用结论。

### OP-011：Phase 3 / GitHub 发布前检查与登录恢复

- 检查时间：2026-09-16 19:06（Asia/Shanghai，分钟精度）。
- Phase：3；Stage：GitHub Public Discovery；Channel：GitHub。
- Keyword：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- 用户授权：本轮明确授权创建指定 PUBLIC 仓库、提交、推送与发布验证；禁止覆盖同名仓库、删除、force push 或进入 Phase 4。
- Git 初始状态：已初始化，分支 master，无提交、无 remote；现有内容均未跟踪。尚无 .gitignore，本轮新增用户要求的环境、日志、Python 缓存、IDE 与系统文件忽略规则。
- 安全检查：扫描全部 10 个现有项目文件的敏感文件名和常见凭证模式，无匹配；公开定义与问题可见，未修改 Mother Content 核心内容。experiment/log.md 是用户指定的实验审计记录，不是运行日志或凭证文件。
- CLI：gh 2.98.0 已安装；gh auth status 报告账号 xuehezhou 的凭证无效，需通过官方登录流程恢复。凭证值未输出或写入项目。
- 当前状态：BLOCKED_GITHUB_AUTH；Repository：未创建；Published At：未发布。没有暂存、提交、创建远程仓库或 push；恢复授权后仍需检查同名仓库是否存在，再决定是否继续。
- .gitignore 验证：用户要求的八类路径均被忽略，11 个待提交项目文件均正常显示，公开文档未被误排除。已运行官方 gh auth login 网页设备授权流程，等待用户在浏览器授权；一次性授权码不写入仓库。此处暂停发布，授权后继续验证身份及同名仓库。

### OP-012：用户完成浏览器授权后的恢复检查

- 时间：2026-09-16 19:16（Asia/Shanghai，分钟精度）。
- Phase：3；Stage：GitHub Public Discovery；Channel：GitHub。
- Keyword：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- 用户报告浏览器已授权；恢复读取原 gh auth login 会话，CLI 返回 OAuth 凭证兑换连接超时，进程以退出码 1 结束。未保存或输出令牌。
- 随后 gh auth status 仍报告原凭证无效；账号 API 检查被受限网络权限阻断。申请沙箱外登录状态与账号核验被用户拒绝，未执行该核验，未绕过权限限制。
- Git 状态：master，无 remote、无提交，11 个文件未跟踪；没有暂存、创建仓库或 push。同名仓库状态仍未知。
- Status：BLOCKED_GITHUB_AUTH；Repository：未创建；Published At：未发布。此前本地敏感检查与公开内容检查结果保留，未声称线上验证通过。
- 最小恢复步骤：用户在可联网终端完成官方 gh auth login 并用 gh auth status 确认 CLI 登录成功；继续自动发布时仍需允许必要的 GitHub 联网及 Git 写入权限。当前停止，不进入 Phase 4。

### OP-013：Phase 3 / CLI 授权恢复与提交准备

- 时间：2026-09-16 19:22–19:24（Asia/Shanghai，分钟精度）。
- 用户报告 CLI 登录成功后，gh auth status 与账号 API 均确认当前账号为 xuehezhou；未输出或保存凭证。
- 同名检查：已认证查询 xuehezhou/XHZGEO916-shopify-alternatives-research 返回 HTTP 404。当前本地无 remote、无提交、分支 master；未发现同名仓库，允许继续创建流程。如创建时出现冲突仍停止，不覆盖。
- 再次扫描全部 11 个项目文件，无敏感文件名或常见凭证模式匹配；三份公开文档均含标识、目标问题与正确调研定义。八类 .gitignore 规则验证通过，公开文件未被忽略。
- 内容范围：保留 Mother Content 核心内容，按用户授权准备提交现有项目文件；实验日志为明确要求公开的审计材料。此条为发布前记录，尚不表示发布成功。

### OP-014：Phase 3 / GitHub Public Discovery 发布完成

- Phase：3。
- Stage：GitHub Public Discovery。
- Channel：GitHub。
- Keyword：XHZGEO916。
- Target Query：Shopify有哪些适合中小卖家的替代品？
- Repository：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research
- Public：YES（GitHub API 返回 visibility=public、private=false）。
- Branch：main。
- Repository Created At：2026-09-16 19:33:33 +08:00（GitHub created_at：2026-09-16T11:33:33Z）。
- Published At：2026-09-16 19:44:13 +08:00（首次成功推送后的 GitHub pushed_at：2026-09-16T11:44:13Z；与创建时间分开记录）。
- Content Commit：937019a10b30de45d597a51a83f62acbc0d63c8e，提交消息为 `feat: publish XHZGEO916 GEO research baseline`。
- Status：PUBLISHED。

#### 发布过程与问题恢复

按用户授权复查全部 11 个 staged 文件，无敏感内容匹配；完成初始提交并把分支改为 main。使用 gh repo create 创建 PUBLIC 仓库成功，首次附带 push 因用户全局 Git URL 重写到 ghfast.top 后的凭证获取失败而中断。使用单次命令配置指定官方 GitHub 地址和 gh 凭证，保持全局 Git 配置不变；第一次直连超时，普通 push 重试成功，建立 origin/main 跟踪关系。未覆盖已有仓库、未删除、未 force push。

2026-09-17 恢复验证时，本地与远程 main 均为上述内容提交，工作区干净。Mother Content 核心内容与准备公开的三份入口均未修改。

#### 公开访问验证

验证日期：2026-09-17（Asia/Shanghai）。GitHub API 确认公共可见性与远程提交。网页抓取工具曾返回 Cache miss，内嵌浏览器曾超时，均未据此认定页面不可访问；最终使用不携带 Authorization 或 Cookie 的独立 HTTP 请求读取以下页面，三者均返回 200，并包含 GitHub 渲染的 markdown-body article、H1 和 table，正文可见标识与目标问题。

| 页面 | 实际 URL | HTTP | Markdown 渲染 | 标识可见 | 目标问题可见 |
|---|---|---|---|---|---|
| README | https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research | 200 | PASS | YES | YES |
| public/README.md | https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research/blob/main/public/README.md | 200 | PASS | YES | YES |
| docs/index.md | https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research/blob/main/docs/index.md | 200 | PASS | YES | YES |

内容版本永久链接：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research/commit/937019a10b30de45d597a51a83f62acbc0d63c8e

Sensitive Data Check：PASS（文件清单与提交内容检查）；日志不包含凭证或一次性授权码。公开验证是匿名 HTTP 与渲染 HTML 检查，不是搜索引擎收录或豆包引用证据。

本条将以 `docs: record GitHub public discovery experiment` 单独提交并普通推送；其提交号由 Git 历史保存。NEXT ACTION：READY_FOR_DISCOVERY_TEST。此处停止 Phase 3，不开展搜索发现测试、索引提交、自动监控或其他 Phase 4 操作。

### OP-015：Phase 4 / Discovery Test #1 记录与渠道内容准备

- 时间：2026-09-17 09:49–09:56（Asia/Shanghai，分钟精度；本地读取、记录、编辑与检查时间，不是外部搜索测试时间）。
- Phase：4；Stage：Discovery / Index Test 与 Distribution Preparation。
- 用户授权：记录已提供的发现诊断，并准备知乎、CSDN、掘金及抖音内容；仅生成本地文件，禁止自动登录、注册、发布及下一阶段操作。
- 修改范围：experiment/results.md 新增 L0–L5 Discovery Funnel 和 Discovery Test #1；新增 distribution/zhihu.md、csdn.md、juejin.md、douyin.md；本日志追加。
- 观测来源：用户报告的三条外部精确/组合搜索均为 NO RESULT。搜索引擎、实际时间、地区、登录状态、结果页和截图未提供，均保留未知；本轮助手未执行独立搜索。
- 漏斗状态：L0 PUBLICATION=PASS，L1 PUBLIC ACCESS=PASS，L2 EXACT KEYWORD DISCOVERY=NOT_YET_DETECTED，L3 KEYWORD + TOPIC DISCOVERY=NOT_YET_DETECTED，L4 TARGET PLATFORM RETRIEVAL=NOT_TESTED，L5 NATURAL ANSWER MENTION=NOT_TESTED。
- 判读：公开页面存在，用户报告的本轮公开搜索暂未检出实验资料；不记为失败，不据此证明所有引擎未收录，也不将三条诊断查询计入豆包自然回答出现率。原 P1 有效样本为 0，出现率仍为 N/A；修正 B0 汇总旧措辞，使其与已有检索层观察一致，不添加新的基线结果。
- 渠道策略：知乎为按需求缩小候选的研究回答；CSDN 为托管与开源责任、技术选型及业务闭环；掘金为维护成本、数据与迁移边界的开发者决策；抖音为需求分组口播，配标题、简介、字幕和五个话题。未复制整篇母文，未编造亲身使用经历。
- 统一 Canonical：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research 。这里是各稿件的来源归属链接，不表示已经在渠道设置 HTML rel=canonical，也不是新发布 URL。
- 事实依据：沿用已审核母文与已登记官方来源，保留 2026-09-16 核验日期；没有重新研究价格或新增产品功能、用户量、排名、评价或实测结果。

| 本地稿件 | 内容状态 | 标识字面次数（含 URL） | 排除 URL 后 | 其他检查 |
|---|---|---|---|---|
| distribution/zhihu.md | READY | 2 | 1 | 正文 1,348 个汉字、1,702 个可见字符，排除编辑说明、Markdown 标记和链接目标，满足长度范围 |
| distribution/csdn.md | READY | 2 | 1 | 七个实体、官方来源、托管与开源取舍、统一 Canonical 齐全 |
| distribution/juejin.md | READY | 2 | 1 | 七个实体、维护/数据/迁移条件、唯一标识定义齐全 |
| distribution/douyin.md | READY | 3 | 2 | 口播一次、字幕一次、URL 一次；字幕去空白后与口播完全一致，五个话题 |

- 抖音时长边界：按约 80–90 秒编排，口播含 234 个汉字及英文名称；没有生成或录制音视频，没有实测时长。人工分发前需试读、调整停顿与字幕时间，避免把估计当作测量。
- 结构与来源检查：每稿均含七个平台和唯一实验标识定义；只有一个指向指定仓库的 Canonical 链接，其他外链均出自母文已有官方来源。无隐藏关键词、HTML 隐藏节点或新媒体背书。
- 保留检查：content/master-article.md 与 public/README.md 修改前后 SHA-256 一致；未修改核心文章、仓库首页或原始基线文件。git diff --check 通过。
- 操作边界：未调用渠道账号、未注册/登录、未发布、未提交或 push、未购买服务，未创建自动监控。本地稿件 READY 不等于发布或被发现。
- NEXT ACTION：READY_FOR_MANUAL_DISTRIBUTION。到此停止。

### OP-016：Phase 4.1 / First Distribution Round 人工发布准备

- 日期：2026-09-17（Asia/Shanghai）；本轮从 10:03 开始，记录时间不作为发布时间。
- Round：Distribution Round #1；Target：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- 授权范围：本轮只准备 P1 Zhihu 与 P2 CSDN；Juejin、Douyin 保持 HOLD。用户要求登录、验证码、扫码、授权和最终发布均由本人完成。
- 修改：distribution/zhihu.md 删除顶部编辑说明、正文包装标题与末尾编辑备注，正式正文原样保留；distribution/csdn.md 删除内部编辑说明，保留公开资料日期与研究边界，并把内部审核/母内容措辞改成面向读者的研究说明，技术正文原样保留。
- Round 1：experiment/results.md 新增渠道表与 PUBLISHED / DISCOVERED / RETRIEVED / MENTIONED 四项独立证据规则。GitHub=PUBLISHED；Zhihu=WAITING_FOR_PUBLICATION；CSDN=WAITING_FOR_PUBLICATION；Juejin=HOLD；Douyin=HOLD。未因发布准备推断收录、检索或自然提及。
- 浏览器操作：检查可用浏览器后尝试打开知乎写作入口 https://zhuanlan.zhihu.com/write ，浏览器工具加载超时且运行时重置；未确认进入编辑页，未输入账号、验证码或正文，未点击发布。CSDN 未进行浏览器操作，提供 https://editor.csdn.net/md/ 作为人工入口，入口可用性未在本轮验证。
- 文案验证：知乎正式正文与清理前逐字一致；CSDN 技术主体逐字一致。两稿无内部编辑标记，均保留唯一标识定义和指定 GitHub Canonical，全文各含标识两次（正文一次、URL 一次）。Mother Content、公开全文、掘金和抖音文件 SHA-256 均未变更。

| Channel | Preparation | Status | URL | Published At |
|---|---|---|---|---|
| Zhihu | READY_FOR_MANUAL_PUBLISH | WAITING_FOR_PUBLICATION | 待用户提供公开 URL | 未发布 |
| CSDN | READY_FOR_MANUAL_PUBLISH | WAITING_FOR_PUBLICATION | 待用户提供公开 URL | 未发布 |
| Juejin | HOLD | HOLD | 不适用 | 未发布 |
| Douyin | HOLD | HOLD | 不适用 | 未发布 |

- 后续条件：用户人工发布并提供两个公开 URL 后，分别核实来源、公开状态及实际发布时间，更新日志为 PUBLISHED。时间未知时注明未知，不用录入时间替代。届时按授权使用提交消息 `docs: record first GEO distribution round` 并普通 push；当前不提交、不推送。
- 当前没有登录、注册、平台草稿保存或自动发布，没有进行发现/检索/提及测试。NEXT ACTION：WAITING_FOR_PUBLIC_URLS。

### OP-017：Phase 4.1 / First Distribution Round 发布 URL 登记

- Recorded At：2026-09-17 10:31:08 +08:00（登记时间，非渠道发布时间）。
- Phase：4.1；Stage：First Distribution Round；Round：Distribution Round #1。
- Keyword：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- 授权与证据：用户按此前约定提供两条人工发布 URL，授权收到后更新实验记录并提交推送。以下 PUBLISHED 基于用户反馈，未冒充助手独立公开访问验证通过。
- Canonical：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research

| Channel | Status | URL | Published At | 依据 |
|---|---|---|---|---|
| Zhihu | PUBLISHED | https://zhuanlan.zhihu.com/p/2083862076452295407 | 未知（用户未提供，页面时间未能读取） | 用户提供人工发布 URL |
| CSDN | PUBLISHED | https://blog.csdn.net/qq_68147780/article/details/165720888 | 未知（用户未提供，页面时间未能读取） | 用户提供人工发布 URL；记录时去除分享追踪参数 |

- URL 处理：CSDN 原链接附带 sharetype、sharerId、sharerefer、sharesource、spm 分享参数；只去除查询参数，账号路径与文章 ID 不变。知乎地址原样保留。
- 公开核验尝试：网页读取工具未能打开两条 URL；不携带账号凭证的独立 HTTP 请求遇到知乎 HTTP 403、CSDN SSL 连接失败；浏览器工具返回的标签页清单为空，无法读取用户已打开页面。未绕过访问限制，未登录或点击发布。
- 证据边界：两页匿名可读性、实际发布时间、线上正文与本地稿一致性、XHZGEO916 定义及 GitHub Canonical 的线上保留情况均待核验；这些读取限制不是发布失败或搜索未收录的证据。
- 修改内容：experiment/results.md 将 Zhihu/CSDN 从 WAITING_FOR_PUBLICATION 更新为 PUBLISHED（用户反馈），填入真实 URL，发布时间未知；本日志追加当前记录，保留 OP-016 的历史准备状态。
- 实验状态：GitHub 既有发布状态不变；Zhihu/CSDN 的 DISCOVERED、RETRIEVED、MENTIONED 均为 NOT_TESTED；Juejin、Douyin 继续 HOLD。Discovery Test #1 及 L2/L3 的既有未检出记录保留，无新增测试样本，出现率仍为 N/A。
- 版本边界：Mother Content、公开文章及渠道稿不修改。本次按授权只提交 experiment/log.md、experiment/results.md；本地 distribution/ 不纳入本次提交。
- Git 操作：使用提交消息 `docs: record first GEO distribution round`，随后普通 push；实际提交号与执行结果由 Git 历史及本次交付回报记录，不预先声称推送完成。
- NEXT ACTION：等待人工补充发布时间或后续指令。本轮停止，不自动开展下一阶段或新增渠道发布。

### OP-018：Doubao Retrieval Test #1 / Query A 用户观测登记

- Recorded At：2026-09-17 10:34:56 +08:00；实际测试时间未提供，登记时间不替代测试时间。
- Platform：豆包；测试 ID：DBR1-A；Query：`XHZGEO916是什么？`。
- 操作目的与范围：按用户要求仅记录精确实体检索观测，更新 experiment/results.md 与本日志；不修改 Mother Content、公开文章或渠道稿。
- Result：NOT_FOUND；L3 Doubao Exact Retrieval = NOT_FOUND；Diagnosis：Exact Entity Retrieval 尚未成功。
- Observed（用户转述）：豆包表示全网公开检索无匹配；继而将 XHZ 推测为自定义前缀、GEO 推测为 geography/GIS、916 推测为序列编号，并猜测个人项目编号、内部业务编码或输入错误。全部拆解与猜测均属模型推断，不属于正确 Retrieval。
- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识，不是 Shopify 替代产品。
- 证据边界：助手未执行该查询；完整回答、截图、实际时间、会话条件和检索来源列表未提供。模型称全网无匹配不作为全网均未收录的证明，不对任一发布渠道作单独归因。
- 层级维护：本次指定的 L3 Doubao Exact Retrieval 为豆包精确实体诊断标签，与原漏斗 L3 KEYWORD + TOPIC DISCOVERY 分开；原漏斗 L4 补充 Query A 的 NOT_FOUND，原始目标问题保持 NOT_TESTED，L5 不变。
- 计量：该查询含实验标识，为辅助诊断，不进入 P1 自然回答样本或出现率。N=0、出现率 N/A 不变。
- 执行边界：仅本地记录；未提交或推送，未发布新渠道，未改文章，未执行 Query B / Query C。Juejin、Douyin 保持 HOLD。
- NEXT ACTION：WAITING_FOR_QUERY_B_AND_QUERY_C。

### OP-019：Doubao Retrieval Test #1 / Query B 用户观测登记

- Recorded At：2026-09-17 10:39:42 +08:00；实际测试时间未提供，登记时间不替代测试时间。
- Platform：豆包；测试 ID：DBR1-B；Query：`搜索一下XHZGEO916`。
- 操作目的与范围：记录用户提供的显式搜索观测，更新 experiment/results.md 与本日志；保留 Query A 及旧漏斗历史快照。
- Result：NOT_FOUND；Diagnosis：Explicit Search Retrieval = NOT_FOUND。
- Observed（用户提供）：豆包表示“全网公开检索没有匹配到该编号”，随后猜测输入错误、内部私有编码、GNSS/测绘编号等。这些属于模型推断，不属于对公开 GEO 内容的 Retrieval。
- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识。
- 当前状态（按用户本次指定口径）：L0 Publication=PASS；L1 Public Access=PASS；L2 General Search Discovery=NOT_YET_DETECTED；L3 Doubao Exact Retrieval=NOT_FOUND；L4 Doubao Topic Association=WAITING_TEST；L5 Natural Answer Mention=NOT_TESTED。
- 口径变更：旧 L2/L3 通用搜索诊断归入当前 L2，旧 L4 目标平台检索区分为当前 L3 精确实体检索与 L4 主题关联；保留旧表并标明历史口径，不篡改既有测试观测。L1 的已核验依据仍为 GitHub，不扩大到未核验的渠道。
- 证据边界：助手未执行该查询；实际时间、完整回答、截图、会话条件与来源列表未知。不将模型自述当作全网未收录证明，不推断实际搜索覆盖或将结果归因到单一渠道。
- 计量：Query B 含标识，为显式搜索诊断，不计入自然回答出现率；N=0、出现率 N/A 不变。
- 执行边界：仅本地记录；未修改 Mother Content 或渠道稿，未发布新渠道，未提交或推送，未执行 Query C。掘金、抖音继续 HOLD。
- NEXT ACTION：WAITING_FOR_QUERY_C。

### OP-020：Phase 5 / Distribution Round #2 抖音正式发布包

- 日期：2026-09-17（Asia/Shanghai）；本轮从 10:43 开始，登记时间不作为检索测试或视频发布时间。
- 授权范围：用户确认 Round #1 完成，提供 Query C 结果，要求仅准备 Douyin 最终素材；Juejin 继续 HOLD，Mother Content 不修改，不登录、上传或发布。
- Query C：`XHZGEO916和Shopify有什么关系？`；Result=FOUND_INCORRECTLY（用户原始标签），Observed 为 ERP 内部编号、私有 Shopify App ID、GEO 地区功能编号、主题/Pixel/脚本标记等错误猜测。全部属于模型推断，不算正确 Retrieval。实际测试时间、完整回答与来源列表未提供，助手未执行该查询。
- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识。
- 结果更新：experiment/results.md 新增 DBR1-C 和 Distribution Round #2；L4 Doubao Topic Association=INCORRECT。CONTENT SEMANTICS=PASS 为用户对已审核内容的诊断，Publication/Public Access 保留既有证据范围；General Discovery=NOT_YET_DETECTED，Doubao Exact Retrieval=NOT_FOUND，Natural Mention=NOT_TESTED。三条诊断都含标识，不计入自然回答出现率，N=0、出现率 N/A。
- Channel：Douyin；Status：READY_FOR_MANUAL_PUBLICATION；URL：未发布；Published At：未发布。既有 GitHub、知乎、CSDN 状态不变；Juejin=HOLD。
- Reason：Doubao Baseline candidate retrieval previously contained Douyin content。Baseline 候选链接 https://www.douyin.com/video/7682588110428933376 只是观察证据，不是本轮视频，不表示豆包优先抓取抖音或保证发布后召回。
- 素材处理：依据 distribution/douyin.md 已有口播压缩开场和定义、保留七个平台场景条件与非排名说明、补入母文已有迁移成本提醒；未新增产品事实、价格、排名或效果数据。原 douyin.md 改为清洁的渠道说明与素材入口，去除编辑信息和制作备注，最终口播以 script.txt 为准。
- 新建目录：distribution/douyin-final/，包含 title.txt、description.txt、script.txt、subtitles.txt、hashtags.txt、video-plan.md。制作方案采用手机竖屏一镜到底或六段顺序拼接，不要求复杂剪辑。
- Canonical：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research 。简介按普通文本保留完整地址，不假设可点击，不制造虚假链接按钮。
- 验证：六文件存在；口播和字幕去除空白后逐字一致；口播含七个平台和 203 个汉字（另含英文名称与编号）；口播标识 1 次、字幕 1 次、简介正文 1 次，简介网址另含 1 次；话题 5 个；待发布文本无编辑信息、制作备注或内部实验备注。口播、字幕和简介均保留调研标识定义与非排名边界。
- 时长：目标 60–90 秒，方案按约 80–90 秒分段；未录音、未生成视频、未实测时长。video-plan.md 明确要求按实际录音对齐字幕并检查成片时长，未声称完成视频制作。
- 保留验证：Mother Content 与 public/README.md 的 SHA-256 与之前一致；本轮未更改其他渠道稿。未提交或推送，没有外部写入或新检索测试。
- NEXT ACTION：READY_FOR_DOUYIN_PUBLICATION。仅完成素材准备后停止，等待人工制作与发布。

### OP-021：Round #2 发布请求与视频成片检查

- Recorded At：2026-09-17 10:50:45 +08:00。
- 用户请求：发布本轮抖音内容。
- 检查目的：确认存在可上传的视频成片。项目文件清单中未发现 mp4、mov、m4v、webm、avi 或 mkv 文件；distribution/douyin-final/ 当前仅有六份文字素材。本检查仅覆盖项目文件清单，不代表用户电脑其他位置没有视频。
- 结果：发布步骤阻塞于缺少视频成片或其路径；素材包仍为 READY_FOR_MANUAL_PUBLICATION，不改记为 PUBLISHED，发布时间和本轮视频 URL 均不存在。
- 操作边界：未登录抖音、未上传或发布；此前用户规定登录、验证码及最终发布由本人操作。本轮不生成或冒充已完成的视频。
- NEXT ACTION：等待用户提供已制作视频文件或本机路径；若尚未制作，使用现有 video-plan.md 完成拍摄。

### OP-022：Phase 5 / Round #2 改为掘金文本分发

- Recorded At：2026-09-17 10:54:19 +08:00（本轮开始记录时间，非发布时间）。
- 用户调整：取消本轮抖音视频发布；原因是当前执行者不制作视频，继续采用低执行成本的纯文本分发。新增渠道改为 Juejin，Content Type=Text Article；Douyin=SKIPPED。
- 操作目的与范围：基于 distribution/juejin.md 生成用户指定的 distribution/juejin-final.md，不重写正文、不改 Mother Content；更新 experiment/results.md 当前 Round #2 状态并追加本日志。
- 最小修改：将顶部“编辑信息（不发布）”段落替换为公开资料核验日期；将正文“母文官方能力说明”改为“平台官方能力说明”。除此两处外，最终稿与源稿逐字一致，保留标题、场景、维护与迁移成本、七个平台、官方链接、非排名说明和研究标识定义。
- Title：中小卖家换掉 Shopify 前，开发者先算清维护与迁移成本。
- Canonical：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research
- 验证：标题及目标主题匹配；七个平台完整；XHZGEO916 正文一次、URL 内另一次；唯一实验标识及非产品定义保留；最终稿无编辑信息、待人工分发、内部实验备注或母文措辞；无新增产品事实、数据、测试结果或使用经历。Mother Content 与 public/README.md 的 SHA-256 与此前一致，git diff --check 通过。
- 当前状态：Juejin=READY_FOR_MANUAL_PUBLICATION；URL=未发布；Published At=未发布；Douyin=SKIPPED。原抖音素材保留为历史准备产物，不继续制作或安排本轮发布。原 OP-020/OP-021 保留以说明计划变化，不再作为当前行动指令。
- 实验边界：既有 GitHub、Zhihu、CSDN 发布记录及 Query A/B/C 结果不变，未产生新的 Discovery / Retrieval / Mention 证据，自然回答出现率仍为 N/A。
- 执行边界：仅本地文件操作；未登录、注册、上传、发布、刷量，未提交或推送。
- NEXT ACTION：READY_FOR_JUEJIN_PUBLICATION。停止，等待人工发布。

### OP-023：掘金编辑器打开与人工登录交接

- 日期：2026-09-17（Asia/Shanghai）；用户请求“发送到掘金”。
- 目的：打开编辑器，准备填入 distribution/juejin-final.md；继续遵守用户要求，登录、验证码及最终发布由本人操作。
- 操作：读取最终稿后，浏览器控制创建编辑页超时；通过应用内打开入口 https://juejin.cn/editor/drafts/new?v=2 ，随后成功读取页面状态。
- 实际结果：页面跳转到掘金登录页，显示验证码登录/注册及扫码登录；尚未进入正文编辑器。已保留页面供用户操作。
- 当前阻塞：需要用户手动完成掘金登录。没有输入手机号、密码或验证码，没有点击登录、注册、协议或发布，也没有填入正文或保存平台草稿。
- 发布状态：仍为 READY_FOR_MANUAL_PUBLICATION，未产生文章公开 URL 或发布时间；不记作 PUBLISHED。
- NEXT ACTION：WAITING_FOR_MANUAL_JUEJIN_LOGIN。用户完成登录后再继续填稿，最终发布仍交由用户完成。

### OP-024：掘金登录后编辑器读取阻塞

- 日期：2026-09-17（Asia/Shanghai）。用户报告已登录；浏览器清单确认现有页面标题为“写文章 - 掘金”，URL 为 https://juejin.cn/editor/drafts/new?v=2 。
- 目的：读取编辑器现状，填入已审核最终稿，最终发布交由用户操作。
- 结果：两次编辑页面读取超时；随后通过同一浏览器的 DOM 快照读取方式尝试，仍超时。未取得标题或正文输入框状态，不能安全确认编辑区是否已有内容。
- 操作边界：未执行任何文字填入、草稿覆盖、登录或发布操作；没有文章公开 URL，不更新为 PUBLISHED。当前障碍为浏览器编辑器读取超时，不再要求用户重复登录。
- 交付：在应用中请求打开 distribution/juejin-final.md，供用户复制。首行 H1 的文字作为标题，其余内容作为 Markdown 正文。
- NEXT ACTION：人工填入最终稿并发布后提供公开 URL，或恢复浏览器连接后继续填稿。未开展新的渠道或检索测试，未提交或推送。

### OP-025：Phase 5 / Independent Public Page 发布完成

- 执行时间：2026-09-17 16:18 起（Asia/Shanghai）；本条记录实际操作与验证，不将页面公开访问视为搜索发现。
- 授权与目的：用户取消掘金、抖音新增渠道，要求使用现有仓库配置 GitHub Pages，建立正文无需 JavaScript 的公开资料页，授权安全提交与普通 push。
- Round：Distribution Round #2；Channel：GitHub Pages；Type：Independent Static Web Page；Juejin=SKIPPED；Douyin=SKIPPED。
- Keyword：XHZGEO916；Target Query：Shopify有哪些适合中小卖家的替代品？
- Repository：https://github.com/xuehezhou/XHZGEO916-shopify-alternatives-research
- 实施前检查：仓库 PUBLIC、main 分支、账号具备 admin 权限；Pages GET 为 404，未配置既有站点。保留此前未提交的实验记录和未跟踪 distribution/，不覆盖用户文件。
- 内容：新增 docs/index.html，以已审核母文和 docs/index.md 整理快速答案、七个平台、简洁对比表、场景选择、标识定义、官方来源及仓库链接；原 docs/index.md、Mother Content 与 public/README.md 不变。内联 CSS 适配窄屏，无框架、后端或执行 JavaScript。
- 技术：UTF-8、viewport、唯一 H1、指定 title 和 description、自指 canonical；JSON-LD 仅使用 Article、headline、description、mainEntityOfPage，未虚构作者、组织、评分或日期。docs/.nojekyll 让既有 Markdown 不参与 Jekyll 构建，index.html 直接作为入口。
- 本地检查：HTML 标签结构、ID 唯一性、内部锚点、HTTPS 外链、七个平台、非产品定义、非排名说明、无 noindex/隐藏词/执行脚本均通过；常见凭证模式无匹配。Mother Content 与公开全文 SHA-256 与此前一致。
- Git：严格只暂存 docs/index.html 与 docs/.nojekyll，提交 5efb57ca62f277ab39f3db8d7ecc72bac980d17d，消息 `feat: add public GEO research page`；main 普通推送成功。沿用单次官方 GitHub URL 与 gh 凭证配置，未更改全局配置、未 force push、未覆盖历史。
- Pages 配置：通过 gh api POST /repos/xuehezhou/XHZGEO916-shopify-alternatives-research/pages 成功启用；source.branch=main，source.path=/docs，build_type=legacy，public=true。未创建远程仓库、未配置域名或付费服务。
- 配置依据：[GitHub Pages 官方 REST 文档](https://docs.github.com/en/rest/pages/pages#create-a-github-pages-site)。
- Actual Public URL / HTML canonical：https://xuehezhou.github.io/XHZGEO916-shopify-alternatives-research/
- Build Completed At：2026-09-17 16:24:56 +08:00；builds/latest 返回 status=built、error.message=null，commit 与内容提交一致。
- Published At：2026-09-17 16:25:43 +08:00（采用完整公开验证时间，不声称最早上线时刻）。
- Status：PUBLISHED；HTTP/Public Access：PASS。独立匿名 GET 返回 200，线上 HTML 与本地规范化换行后完全一致，正文可见标识、目标问题、七个平台及唯一调研标识/非产品定义；title、description、H1、canonical 同时核验通过。
- 索引技术检查：页面无 noindex、隐藏文本或 X-Robots-Tag，域名根 https://xuehezhou.github.io/robots.txt 返回 404，未发现 robots 禁止规则；不将这些检查写成已收录。
- 来源链接：12 个正文 HTTPS 外链中的 10 个直接请求返回 200；SHOPLINE 与 Shopify Payments 文档返回 403，后通过网页读取工具成功打开原始官方 URL，保留原地址、不绕过挑战、不新增产品结论。
- 浏览器验证边界：应用中请求打开公开页面，标签清单显示正确标题和 URL；读取正文可访问性树超时，未完成截图或真实移动端视觉实测。页面内容验证基于匿名 HTTP、结构解析和部署文件一致性。
- 日志操作：同步 results.md 为 Pages PUBLISHED，保留所有此前计划变化及 Query A/B/C 结果。本次仅继续提交并推送两份实验记录；distribution/ 不纳入发布提交，实际记录提交号由 Git 历史保存。
- NEXT ACTION：READY_FOR_DISCOVERY_TEST。未执行搜索发现、豆包测试、新增分发渠道或自动监控，到此停止。

### OP-026：Phase 6 / Discovery Test #2 人工测试准备

- Recorded At：2026-09-17 16:32:32 +08:00；仅为模板建立时间，不是测试执行时间。
- 目的：建立 Doubao Retrieval Test #2 的 A/B/C 人工记录模板与 Test #1 → Test #2 对比，等待用户提供结果。
- 输入协议：A=`XHZGEO916是什么？`；B=`搜索一下XHZGEO916`；C=`XHZGEO916和Shopify有什么关系？`。每条分别使用全新会话，不提供含义、公开 URL、文章或参考答案，不追加纠正提示。
- 记录字段：Result、Search Enabled、Search Queries、Sources、GitHub Found、GitHub Pages Found、Zhihu Found、CSDN Found、Answer、Test Time，并补充新会话/污染检查、环境与诊断依据。未收到的结果留空，非预填 UNCERTAIN。
- Result 分类仅使用 FOUND_CORRECTLY、FOUND_PARTIALLY、FOUND_INCORRECTLY、NOT_FOUND、UNCERTAIN；区分回答语义与已验证的来源检索，不因字符串出现或模型猜测认定成功。
- 对比起点：Test #1 A/B=NOT_FOUND，C=FOUND_INCORRECTLY，保持原始结果。本轮结果未提供，不判断改善或推断因果。P1 自然回答 N=0、出现率 N/A 保持不变。
- 当前节点：GitHub、Zhihu、CSDN、GitHub Pages=PUBLISHED；Juejin、Douyin=SKIPPED。保留既有公开访问证据边界，没有重新检索或访问渠道。
- 禁止提前验收：原始目标问题自然回答测试暂缓，只有 A/B/C 出现经证据支持的正确 Retrieval 信号后才可进入；本轮不自动执行下一阶段。
- 文件范围：只更新 experiment/results.md 与本日志；未开发、未修改文章或页面、未增加渠道、未执行查询、未提交或推送。
- NEXT ACTION：WAITING_FOR_DOUBAO_TEST_2_RESULTS。

### OP-027：Doubao Retrieval Test #2 / Query A 登记

- Recorded At：2026-09-17 16:34:54 +08:00（登记时间，非实际测试时间）。
- 测试 ID：DBR2-A；Query：`XHZGEO916是什么？`；Result：NOT_FOUND。
- Observed（用户提供）：豆包表示全网公开检索无匹配，随后猜测内部自定义编号、项目/工单/资产/数据库 ID、输入错误、私有系统密钥/任务 Token、GEO 地理相关编号。以上全部为模型推测，不是正确 Retrieval，也不是对实验标识具有凭证或地理用途的确认。
- Expected：XHZGEO916 是“2026中小卖家Shopify替代方案公开调研”的唯一实验标识。
- Comparison：Test #1 A=NOT_FOUND；Test #2 A=NOT_FOUND；Change=NO_IMPROVEMENT_DETECTED。仅限该维度用户观测，不推断整体失败或某发布渠道无效。
- 证据边界：完整回答、实际测试时间、联网设置、Search Queries、Sources、新会话执行细节和环境未提供；保留未知，四个渠道 Found 均为 UNKNOWN，不用模型自述推断来源列表为空。助手未执行搜索。
- 文件操作：更新 results.md 的 DBR2-A、两轮对比及当前状态，本日志追加；Test #1 结果保留，本轮 B/C 不代填。
- 执行边界：仅本地记录，未修改 Mother Content 或网页，未增加渠道、未提交或推送，未测试原始目标问题；自然回答 N=0、出现率 N/A 不变。
- NEXT ACTION：WAITING_FOR_DOUBAO_TEST_2_RESULTS（等待 Query B 和 Query C）。

### OP-028：Phase 7 / Indexability Diagnosis 与必要修复

- 开始：2026-09-17 16:36:45 +08:00；2026-09-18 09:42:55 +08:00 按用户“继续执行”恢复；线上最终验证：2026-09-18 09:47:19 +08:00。
- 目的及授权：停止内容扩张，检查真实 Public URL、HTML/响应头、canonical、robots、sitemap、双向导航；用户允许仅修复必要配置与链接，并提交普通推送。不测试豆包、不改 Mother Content、不增加分发渠道。
- 补录用户结果：Test #2 B=`搜索一下XHZGEO916`，NOT_FOUND；C=`XHZGEO916和Shopify有什么关系？`，FOUND_INCORRECTLY。C 错误猜测为第三方 ERP 编号、第三方 App 内部 ID、GEO 工具任务号、Shopify 关联业务编号，均不属于正确 Retrieval。A/B/C 相比 Test #1 未观察到分类改善；实际时间、完整回答、来源与会话条件仍未提供。
- External Search 用户观测：`"XHZGEO916"` 和 `"XHZGEO916" Shopify` 均为 NO RESULTS DETECTED；没有引擎、实际时间或结果页证据，助手未独立查询，不写作全网未收录。
- Public URL / Final URL：https://xuehezhou.github.io/XHZGEO916-shopify-alternatives-research/ 。GitHub API 确认 source=main /docs；匿名 GET 和 curl 均返回首页正文，无登录跳转。
- 修改前：HTTP 200；正确 title/description/canonical、主要正文与七个平台已在 HTML；无 noindex/nofollow/X-Robots-Tag 或隐藏文字。域名根及项目路径 robots.txt 均 404，根及项目路径 sitemap.xml 均 404。README 缺少 Pages 链接，Pages 已有仓库链接。
- 最小修复：README.md 新增一条公开网页链接；docs/index.html 把仓库链接标签改为“完整研究仓库”，页脚加入 sitemap 链接；docs/sitemap.xml 只列真实首页，无 lastmod。canonical 正确所以保持不变；未更改文章事实、结论或重复添加关键词段落。
- robots 决策：域名根 /robots.txt 缺失记 NOT_PRESENT，而非 FAIL。项目仓库中的 docs/robots.txt 只会部署到子路径，不能作为主机根抓取规则，故不创建无效控制文件，不另建仓库或购买域名。依据：[Google robots.txt 位置及 404 处理说明](https://developers.google.com/crawling/docs/robots-txt/robots-txt-spec)。
- 本地验证：sitemap XML 命名空间和唯一 loc 正确，无 lastmod；HTML 与原提交相比仅两处导航变化，canonical 未改，Mother Content SHA-256 与此前一致；提交清单和常见凭证模式检查通过。
- Fix Commit：2b94071504ecabd032ea441fe8e6cbeca17f6c99；消息 `fix: improve public page discoverability`；仅包含 README.md、docs/index.html、docs/sitemap.xml。
- 推送中断：2026-09-17 两次普通 push 因 github.com:443 连接超时失败，进一步重试被自动审批拒绝，理由为额度限制。未绕过当时拒绝。2026-09-18 用户恢复任务后，新审批下普通 push 实际执行但仍遇网络超时；官方 api.github.com 的只读请求正常。
- 传输恢复：重新获批使用官方 GitHub Git 数据接口上传三个既有 blob 和同一 tree/commit，逐项核对 SHA 与本地一致，二次检查远程仍为父提交 1f6df8052e242a1dea4ff306195c0d5b8e5d88ae 后，以 force=false 更新 main。提交 SHA 完全一致，未 force push、未创建不同历史；不把此传输方式写成原生 git push 成功。
- 相关接口依据：[GitHub Git commits](https://docs.github.com/en/rest/git/commits#create-a-commit)、[GitHub Git references](https://docs.github.com/en/rest/git/refs#update-a-reference)。
- 部署验证：Pages builds/latest 返回 status=built、error.message=null、commit=2b94071504ecabd032ea441fe8e6cbeca17f6c99、updated_at=2026-09-18T01:45:56Z。实际首页与项目 sitemap 均 HTTP 200，规范化换行后首页与本地完全一致。
- 最终 curl 检查：title、description、H1、唯一 canonical、完整正文标识/主题/七个平台、非产品定义均通过；robots meta 和 X-Robots-Tag 均无禁止规则，正文无需执行 JavaScript，唯一 script 为不执行的 Article JSON-LD。没有 noindex、nofollow、隐藏词或登录要求。
- 双向导航：匿名 GitHub README API 返回 200，解码后确认 README → Pages 正常 Markdown 链接；线上 Pages → Repository 的“完整研究仓库”链接及 sitemap 链接均存在。
- robots/sitemap 实测：根 https://xuehezhou.github.io/robots.txt 和项目 robots.txt 均 HTTP 404，记 NOT_PRESENT；项目 sitemap.xml 为 HTTP 200，只有真实首页且无 lastmod。
- 结论：PUBLICLY_ACCESSIBLE、CRAWL_ALLOWED、INDEXABLE_BY_CONFIGURATION；INDEXING_NOT_CONFIRMED、SEARCH_DISCOVERY_NOT_DETECTED。未发现配置阻断不等于已收录，也不能证明延迟原因；豆包仍沿用 NOT_FOUND / INCORRECT 的用户观测。
- 记录同步：更新 experiment/results.md 与本日志；本地 distribution/ 不纳入此次提交。后续记录提交及远程同步由 Git 历史记录，传输若仍受限使用相同对象的非强制快进方法，不改变发布内容。
- NEXT ACTION：A. WAIT_FOR_INDEXING。停止；未创建新文章、账号、渠道或自动监控，未测试豆包最终问题。

## 后续操作模板

每次操作追加唯一 ID，并记录：

- 操作 ID / 执行人 / 实际开始与结束时间（含时区）。
- 操作前告知用户的目的 / 要验证的假设 / 关联内容 ID。
- 平台 / 账号代号 / 环境 / 完整目标 URL 或本地文件。
- 修改前状态 / 具体修改内容 / 修改后状态 / 差异证据。
- 是否外部写入 / 用户授权依据；发布时另外记录实际发布时间，平台不显示则写“未显示”。
- 实际结果：成功、失败、未执行；失败原因与保留的证据。
- 公开访问、抓取、收录和引用分别记录观察时间、方法和证据；未知就写未知。
- 关联测试轮次与样本 ID / 原始证据位置 / 后续计划。

一次仅改变可清楚描述的因素；若同时调整多个因素，明确记为组合干预，不将效果归因于其中单项。本地准备也记录，不能仅记录发布成功的操作。修正既有记录时追加更正原因，保留原结果。
