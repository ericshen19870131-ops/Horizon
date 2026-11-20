---
layout: default
title: "Horizon Summary: 2026-11-20 (ZH)"
date: 2026-11-20
lang: zh
---

> 从 41 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Anthropic 登陆纳斯达克,首日交易波动明显](#item-tech-news-1) ⭐️ 8.0/10
2. [PostgreSQL 19 发布：新增 WAIT FOR LSN，发布时间推迟约两个月](#item-tech-news-2) ⭐️ 8.0/10
3. [Anthropic 称 Claude 解决两个黑洞物理开放问题，过程与验证未公开](#item-tech-news-3) ⭐️ 7.5/10
4. [OpenAI 称其模型参与 Jalapeño 与 AMD GPU 设计优化](#item-tech-news-4) ⭐️ 7.5/10
5. [OpenJDK 公开 PR 疑似早已修复“java4shell”漏洞,披露经过引发争议](#item-tech-news-5) ⭐️ 7.0/10
6. [英国政府被迫承认向苹果发出加密技术能力通知](#item-tech-news-6) ⭐️ 7.0/10
7. [Google Play 将自 2027 年 4 月起强制大屏自适应质量标准](#item-tech-news-7) ⭐️ 7.0/10
8. [PHP 流包装器漏洞：httpS:// 大写 s 会静默退化为明文传输](#item-tech-news-8) ⭐️ 7.0/10
9. [Zerodha 分享基于 SQLite 的分布式高性能 Blob 存储实践](#item-tech-news-9) ⭐️ 6.5/10

**财经新闻**
1. [Anthropic 登陆纳斯达克，首日开盘较发行价涨 34%](#item-finance-news-1) ⭐️ 8.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Anthropic 登陆纳斯达克,首日交易波动明显](https://www.reuters.com/business/finance/anthropics-historic-debut-put-ais-promise-peril-wall-st-test-2026-11-19/) ⭐️ 8.0/10

路透社报道称,Anthropic 已在纳斯达克上市,并将其视为华尔街对 AI 前景与风险的一次检验。本次未提供路透社正文,以下数字仅来自 Hacker News 评论,尚未核实:股票代码为 ANT,发行价 83 美元,开盘价 111.5 美元,收盘价 97.17 美元,市值约 1.26 万亿美元。按这些数字计算,收盘价比发行价高约 17%,比开盘价低约 12.9%,因此以发行价认购者账面盈利,开盘后买入者则亏损。

hackernews · wslh · 11月19日 17:02 · [社区讨论](https://news.ycombinator.com/item?id=50562754)

**「背景」** Anthropic 是 Claude 大模型的开发商,公司形式为公益公司\(PBC\),股票以代码 ANT 在纳斯达克上市,首个交易日为 2026 年 11 月 19 日,发行价定为每股 83 美元。据 Yahoo Finance 报道,ANT 首日收盘较发行价上涨约 17%,散户交易十分活跃,但按 Vanda Research 的数据,净流入的起步速度慢于 2026 年 6 月 SpaceX\(SPCX\)上市时。评论区提到的开盘价 111.5 美元、收盘价 97.17 美元和约 1.26 万亿美元市值,未在这些检索结果中得到独立证实,仅应视为评论者的说法。

**「社区讨论」** 评论者 cmiles8 认为,市值跌至约 1.26 万亿美元,远低于数周前市场期待的 2 万亿美元以上,也低于 OpenAI 在私募市场寻求的估值,对 OpenAI 不是好兆头。另有评论者\(如 capital\_guy、beachy\)认为软件工程师的好日子可能接近尾声,但这只是个人看法,并非已证实的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://finance.yahoo.com/technology/live/anthropic-ipo-live-anthropic-stock-begins-trading-in-record-81b-raise-with-15t-valuation-192410598.html">Anthropic IPO live: Anthropic stock closes up 17% from initial price ...</a></li>
<li><a href="https://admiralmarkets.com/analytics/traders-blog/anthropic-stock-ant-first-day-trading">Anthropic Stock ( ANT ): First Day of Trading After $ 83 IPO</a></li>
<li><a href="https://www.fastcompany.com/91645598/anthropic-ipo-what-time-trading-start-stock-price-live-update">ANT stock update: Anthropic rises double digits on first trading day</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI industry`, `#valuation`, `#software careers`

---

<a id="item-tech-news-2"></a>
### [PostgreSQL 19 发布：新增 WAIT FOR LSN，发布时间推迟约两个月](https://simonwillison.net/2026/Nov/19/postgresql-19/) ⭐️ 8.0/10

PostgreSQL 19 已正式发布。按惯例新版本通常在 9 月发布，今年晚了约两个月，Simon Willison 引用 Robert Haas 的文章称，主要原因是团队要集中处理一批由 AI 报告的漏洞。Willison 最看重的新特性是 \`WAIT FOR LSN\` 命令：把读请求发往备库（standby）的应用，可以让备库先重放 WAL 到指定 LSN，再执行查询，从而读到刚在主库写入的数据。用法是写入后在主库用 \`pg\_current\_wal\_insert\_lsn\(\)\` 取得 LSN（如 \`0/0306EE20\`），存入签名 cookie 等位置，下次请求时在备库执行 \`WAIT FOR LSN &\#x27;...&\#x27; WITH \(TIMEOUT &\#x27;0.1s&\#x27;\)\`；超时参数可选，备库在限定时间内未追上则报错。

rss · Simon Willison · 11月19日 20:43

**「背景」** PostgreSQL 通常在每年 9 月前后发布新的大版本。据 PostgreSQL 开发者 Robert Haas 在 10 月下旬发表的文章,PostgreSQL 19 的延期与 AI 工具报告的大量问题有关,他预计发布时间会推迟到 11 月,但认为这次延期不算严重,是项目重视质量的结果。就 \`WAIT FOR LSN\` 而言,备库复制存在延迟,应用刚在主库写入数据后,如果把读请求发往备库,可能读不到这些数据;Wikipedia 的 MediaWiki 此前在 MySQL 复制上手工实现了类似的等待机制。

**「影响」** 使用只读备库分担查询的 PostgreSQL 应用，此前需要自行实现“写后读”一致性，现在可以用原生命令替代，不过应用仍须自己保存并传递 LSN，并处理超时报错（例如回退到主库读取）。该命令是 19 版新增功能，需要升级后才能使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://neon.com/blog/postgres-19-is-late-and-its-ais-fault">Postgres 19 is late, and it&#x27;s AI&#x27;s fault - Neon</a></li>
<li><a href="https://lwn.net/Articles/1104210/">Haas: Postgres 19 is late, and it&#x27;s AI&#x27;s fault - lwn.net</a></li>
<li><a href="https://daily.dev/posts/robert-haas-postgres-19-is-late-and-it-s-ai-s-fault-kwpwxnhxe">Robert Haas: Postgres 19 is late, and it&#x27;s AI&#x27;s fault - daily.dev</a></li>

</ul>
</details>

**标签**: `#PostgreSQL`, `#database releases`, `#read-your-writes consistency`, `#AI-reported vulnerabilities`, `#open source`

---

<a id="item-tech-news-3"></a>
### [Anthropic 称 Claude 解决两个黑洞物理开放问题，过程与验证未公开](https://www.anthropic.com/research/claude-black-hole-physics) ⭐️ 7.5/10

Anthropic 发布研究文章，称其 Claude 模型给出了黑洞物理中两个理论开放问题的解答。据社区评论转述，其中第二个结果是：在给定中心荷（central charge）下，证明了与之相容的黑洞质量上限。Anthropic 自己也表明，这两项结果都不直接描述我们的宇宙，也没有实际应用，只是有助于理解量子力学与相对论如何统一的长期理论研究。这属于厂商的一方说法；所提供的材料没有显示独立验证，也没有披露提示词和具体工作流程。

hackernews · cybermango · 11月19日 17:30 · [社区讨论](https://news.ycombinator.com/item?id=50563148)

**「背景」** 这两个问题都属于理论物理中长期存在的量子引力研究，即设法让量子力学与广义相对论相容。按公告所述，两项结果既不直接描述我们的宇宙，也没有实际应用。社区评论者对第二项结果的解读是：在给定中心荷（central charge）的前提下，给黑洞质量设定上限，超出上限的理论就不能算作该宇宙的自洽量子引力理论。这一解读来自评论者的概括，并非经过独立核实的论文结论。

**「影响」** 在论文经过同行评审或独立复核之前，这些结果更适合作为“AI 辅助理论研究”的待验证案例，而不是已确认的物理结论。研究者若想评估其可复现性，需要先看到 Claude 的提示词、人工参与程度和验证步骤，而目前这些信息尚未提供。

**「社区讨论」** 评论者 dap 质疑“Claude 解决了问题”的拟人化表述，并指出博客、摘要和两篇论文中都没有出现“prompt”一词，因此看不出具体的提示和人类参与情况。chunky1994 粗读后认为，第一个结果更像复杂且易出错的计算，第二个结果更有意义；也有评论者抱怨讨论大多偏离论文本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/research/claude-black-hole-physics">Claude solves two open problems in the physics of black holes</a></li>

</ul>
</details>

**标签**: `#AI for science`, `#Anthropic Claude`, `#black hole physics`, `#theoretical physics`, `#LLM reasoning`

---

<a id="item-tech-news-4"></a>
### [OpenAI 称其模型参与 Jalapeño 与 AMD GPU 设计优化](https://openai.com/index/advancing-chip-design-with-our-models/) ⭐️ 7.5/10

OpenAI 称其模型参与了自研推理芯片 Jalapeño 的设计：向量单元的标准单元面积减少约 13%，矩阵单元减少约 10%，相关优化已在芯片点亮（bring-up）阶段得到验证。在与 AMD 的合作中，OpenAI 称其旗舰 GPU IP 的功耗、性能、面积（PPA）指标相对高度优化的基线最高提升 14%，部分改动已进入送厂制造的设计。OpenAI 还宣布与 Synopsys 合作训练 GPT-Synopsys 模型。以上数字均为 OpenAI 自述，消息来自对其官方公告的简要转述。

telegram · zaihuapd · 11月19日 09:30

**「背景：从优化型 EDA 到大模型参与设计」** EDA 即电子设计自动化软件，芯片团队借助它在功耗、性能、面积（PPA）之间权衡。据 Tom&\#x27;s Hardware 报道，第一代 AI 增强的 EDA 软件（如 Synopsys DSO.ai）主要用机器学习和强化学习解决目标明确的优化问题。OpenAI 此次的说法是让通用模型直接改进 Jalapeño 的电路和 RISC‑V 核，再用 Synopsys 工具验证每次修改没有改变模块行为，并评估 PPA 的取舍。

**「影响」** 如果这些数据属实，AI 辅助的 EDA 优化已经进入实际流片的设计，芯片设计团队可以考虑在面积和 PPA 调优环节试用这类模型。不过转述内容没有说明基线的具体定义、测试方法，也没有第三方验证，“最高 14%”只是上限，并不代表所有模块都能达到这一水平，评估时应等待更详细的技术资料。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/silicon-is-starting-to-design-silicon-how-ai-is-being-used-in-chipmaking-from-eda-tools-to-openais-jalapeno-and-beyond">How close is AI to designing the very same chips it runs on?</a></li>
<li><a href="https://openai.com/de-DE/index/advancing-chip-design-with-our-models/">Chipdesign mit OpenAI -Modellen voranbringen | OpenAI</a></li>

</ul>
</details>

**标签**: `#AI chip design`, `#EDA`, `#OpenAI`, `#AMD GPU`, `#Synopsys`

---

<a id="item-tech-news-5"></a>
### [OpenJDK 公开 PR 疑似早已修复“java4shell”漏洞,披露经过引发争议](https://github.com/openjdk/jdk/pull/32781) ⭐️ 7.0/10

Hacker News 上的讨论指出,OpenJDK 的 PR \#32781 疑似修复了一个被称为“java4shell”的严重漏洞,而该 PR 据称早在 2026 年 9 月就已公开。评论者称,PR 作者 10 月 1 日收到 Oracle 邮件,要求在获得批准前不要推进 PR;10 月 28 日又表示该修复已由 Oracle 接手。由于未提供 PR 正文,漏洞的技术细节、影响范围和严重程度均无法核实,以上经过也只是评论者的转述。

hackernews · notmine1337 · 11月19日 11:47 · [社区讨论](https://news.ycombinator.com/item?id=50558906)

**「背景:Java4Shell 是什么」** Java4Shell 是安全公司 Calif 对一个 OpenJDK 内存破坏漏洞起的名字。其文章称,无需凭据的远程攻击者可以覆写堆内存,以类似 Heartbleed 的方式读取内存,并进一步实现远程代码执行。该漏洞已被分配 CVE-2026-114938,Palo Alto Networks 称其于 2026 年 11 月 17 日公开披露;不过各来源对受影响组件的描述不一\(Calif 称是 Base64 解码器,Palo Alto 称是 HotSpot 运行时\),本条目也未提供 PR 正文,具体技术细节仍需以官方公告为准。

**「影响」** 在 Oracle 或 OpenJDK 给出正式公告前,Java 用户和运维人员无法从现有材料判断受影响的版本或具体修复版本。建议关注官方安全公告和 Adoptium 的更新,而不是依赖社区转述。

**「社区讨论」** 评论者主要争论两点:一是披露流程,即公开 PR 被要求暂缓,之后由 Oracle 接手;二是 Calif 研究者所用的 LLM 是否看过这个早先的 PR,而不是独立发现漏洞。dlor 称自己独立发现了同一问题并已报给 Oracle,其工具运行时无法联网,但不能排除训练数据中含有该 PR。darkamaul 则认为无法确定模型是否查看过仓库的 issue 和 PR,并强调判断漏洞严重性与构造利用链仍需要人工监督。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://calif.io/java4shell">Java4Shell: Write once, RCE everywhere - calif.io</a></li>
<li><a href="https://cybersecuritynews.com/java4shell/">Critical Java4Shell Flaw Lets Hackers Execute Code Without ...</a></li>
<li><a href="https://www.paloaltonetworks.com/blog/cloud-security/java4shell-cve-2026-114938-risks-mitigations/">Java4Shell (CVE-2026-114938): Risks and Mitigations</a></li>

</ul>
</details>

**标签**: `#java-security`, `#vulnerability-disclosure`, `#openjdk`, `#llm-security-research`, `#rce`

---

<a id="item-tech-news-6"></a>
### [英国政府被迫承认向苹果发出加密技术能力通知](https://macanorak.com/uk-government-forced-to-admit-it-issued-apple-a-secret-encryption-order/) ⭐️ 7.0/10

据调查权力法庭\(Investigatory Powers Tribunal\)的一份裁决,英国政府被迫承认曾向苹果发出一份与加密相关的秘密“技术能力通知”\(technical capability notice\)。通知的具体内容目前仍然保密。评论区引用的裁决显示,媒体是通过保密的安全简报得知该通知的,而非泄密。由于原文页面没有可用内容,以上信息主要来自摘要和评论,而非对裁决全文的核实。

hackernews · Terretta · 11月19日 16:21 · [社区讨论](https://news.ycombinator.com/item?id=50562113)

**「背景」** 技术能力通知\(TCN\)是英国《调查权力法》授予内政大臣的权力,可要求通信运营商保留或提供执法机关访问数据的技术能力,且通常禁止当事方公开该通知的存在。调查权力法庭\(IPT\)是审理公民对政府监控措施提出质疑的独立法庭,检索到的庭审文件显示,该庭此前已认定,披露这些程序的存在、各方身份,以及案件涉及内政大臣向运营商发出技术能力通知的权力,不会损害国家安全。本次裁决的具体内容和通知本身的技术要求仍未公开,因此不能据此推断通知对苹果加密功能提出了哪些具体要求。

**「社区讨论」** 评论者 natch 认为,苹果的表述已从“包括苹果在内无人能访问你的数据”弱化为“苹果无法访问你的数据”,并推测用户的密钥可能只是用来解开另一把密钥的 KEK;这只是个人推断,尚无证据证实。另一位评论者 fweimer 提供了裁决原文链接,并指出关键结论是媒体通过保密简报获知此事,通知内容仍未公开。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://investigatorypowerstribunal.org.uk/judgement/1-mr-vincent-kearney-2-british-broadcasting-corporation-v-1-chief-constable-of-the-police-service-of-northern-ireland-2-chief-constable-of-durham-constabulary-3-security-service-4-governme/">Apple Inc and Secretary of State for the Home Department and ...</a></li>
<li><a href="https://www.judiciary.uk/judgments/apple-inc-v-home-secretary-and-others/">Apple Inc -v- Home Secretary and others - Courts and ...</a></li>
<li><a href="https://techcrunch.com/2026/11/19/u-k-government-forced-to-disclose-secret-apple-backdoor-order/">UK government forced to disclose secret Apple backdoor order</a></li>

</ul>
</details>

**标签**: `#encryption`, `#UK surveillance`, `#Apple`, `#privacy policy`, `#Investigatory Powers Tribunal`

---

<a id="item-tech-news-7"></a>
### [Google Play 将自 2027 年 4 月起强制大屏自适应质量标准](https://developer.android.google.cn/blog/posts/google-play-adaptive-quality-standards?hl=zh-cn) ⭐️ 7.0/10

据 Telegram 频道转述 Google 官方 Android 开发者博客，Google Play 将提高应用质量标准，要求 Android 应用适配折叠屏等大屏设备。自 2027 年 4 月起，应用需达到规定的自适应兼容等级，避免界面拉伸、黑边、比例锁定等问题，并在设备形态切换时保持应用状态；未达标的应用可能面临更新发布限制或商店曝光下降。开发者还需提交折叠屏设备截图，并且自 2027 年 8 月起，新应用及更新须以 Android 17（API 37）为目标版本。以上均为已宣布的未来要求，尚未生效；该转述较简略，具体的兼容等级划分和处罚细则未在所给文本中说明，转述中“日期和苹果一样”的说法也未经文中证实。

telegram · zaihuapd · 11月19日 08:42

**「背景」** Android 官方的自适应应用质量指南把应用在大屏和折叠屏上的适配程度分成多个等级，此次新规要求应用至少达到其中的 Tier 3。搜索结果显示，这一要求同样适用于折叠屏设备，并要求应用提供专门的折叠屏截图。这些结果主要是对官方博客的摘录或转述，未提供更多细节。

**「对开发者的影响」** 面向 Google Play 发布的 Android 应用，尤其是仍锁定竖屏、固定比例或在折叠与展开时丢失状态的应用，需要在 2027 年 4 月前完成大屏自适应改造，否则更新发布可能受限，商店曝光也可能下降。开发者还应准备折叠屏设备截图，并在 2027 年 8 月前把新应用和更新的目标版本升级到 Android 17（API 37），同时测试升级后的行为变更。需要注意的是，现有材料没有给出具体的兼容等级细则和处罚触发条件，应以 Google 官方文档为准。

<details><summary>参考链接</summary>
<ul>
<li>Elevating apps: New adaptive quality standards on Google Play | Android Developers&#x27; Blog</li>
<li>&quot; Heads up devs: Google Play is introducing new foldable quality requirements! For apps ... - X</li>
<li>Google is finally getting serious about Android apps on foldables! Starting April 2027, new ...</li>

</ul>
</details>

**标签**: `#Google Play`, `#Android`, `#foldable devices`, `#adaptive UI`, `#platform policy`

---

<a id="item-tech-news-8"></a>
### [PHP 流包装器漏洞：httpS:// 大写 s 会静默退化为明文传输](https://x.com/ljachowicz/status/2123477025268924514) ⭐️ 7.0/10

据 X 帖子及 Telegram 转载，PHP 的 HTTP/FTP 流包装器在识别 scheme 时不区分大小写，但只有第五个字符是小写 s 才启用 TLS。因此 HTTPS://、httpS://、FTPS:// 这类写法会以明文 HTTP/FTP 发送，令牌、Basic 认证、Cookie、POST 请求体和 FTP 登录信息都可能暴露；被第三方重定向到此类地址同样受影响。该漏洞编号为 CVE-2026-128064（GHSA-f6gg-rchx-xw8j），CVSS 4.0 评分 8.2，据称已在 PHP 8.2.36、8.3.37、8.4.28、8.5.13 和 8.6.0 修复。8.1 及更早的 EOL 版本不会获得修复，只能手动把 URL scheme 统一转成小写。以上信息均来自转载帖，未附官方公告或技术细节；标题中“20 年无人发现”的说法也未经验证。

telegram · zaihuapd · 11月20日 03:04

**「背景」** PHP 的 HTTP/FTP 流包装器让 file\_get\_contents\(\)、fopen\(\) 等函数可以直接读取 http://、https://、ftps:// 这类 URL，包装器按 scheme 决定是否启用 TLS。外部登记信息（CVE 记录与 PHP 8 ChangeLog）显示，该缺陷的机制是 scheme 识别不区分大小写，但启用 TLS 时只认固定位置的小写“s”，该编号 GHSA-f6gg-rchx-xw8j / CVE-2026-128064 已列入 PHP 8 更新日志的修复项；“20 年无人发现”的说法在这些资料中未得到印证。

**「影响」** 使用 PHP 的 file\_get\_contents、fopen 等流包装器访问 HTTP/FTP 资源的应用，应尽快升级到上述修复版本，并对 URL 做规范化。仍在运行 PHP 8.1 及更早版本的系统得不到官方补丁，只能在代码中把 scheme 转成小写，同时检查是否有用户输入或重定向会产生大写 s 的 URL。升级前建议先对照 PHP 官方安全公告核实 CVE 编号和版本号。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://everycve.com/CVE-2026-128064">CVE - 2026 - 128064 : Mixed-case HTTPS and FTPS URLs can expose...</a></li>
<li><a href="https://www.php.net/ChangeLog-8.php">PHP : PHP 8 ChangeLog</a></li>

</ul>
</details>

**标签**: `#PHP`, `#security-vulnerability`, `#TLS`, `#CVE`, `#stream-wrappers`

---

<a id="item-tech-news-9"></a>
### [Zerodha 分享基于 SQLite 的分布式高性能 Blob 存储实践](https://zerodha.tech/blog/high-performance-distributed-blob-storage/) ⭐️ 6.5/10

Zerodha 工程团队发布博文,介绍其基于 SQLite 构建的分布式高性能 Blob 存储系统。文章正文未能获取,以下信息来自标题、摘要和评论区的转述:写入前先压缩 Blob;原始文件在大于约 100 KiB 时开始优于 SQLite,而据称 99% 的压缩后数据低于 100 KiB;文中还提到删除行不会缩小 SQLite 文件。这些均为作者自述的经验,未见独立的基准测试验证。

hackernews · ghostfoxgod · 11月19日 08:39 · [社区讨论](https://news.ycombinator.com/item?id=50557537)

**「背景」** SQLite 是嵌入式关系数据库,通常用于存放元数据或小型记录,把它当作 Blob 存储并不常见。此类用法的性能取决于 Blob 大小、事务提交方式\(是否批量提交\)以及文件空间管理,所以这类案例常围绕大小阈值和写入方式展开。

**「社区讨论」** 评论者 anacrolix 称自己多年尝试用 SQLite 做此类场景,认为没有批量提交时事务提交开销过高,并为此自行写了 possum;sgarland 则认为“删除行不会缩小文件”在各类关系数据库中都是常识,属于文档已有的内容。sneilan1 也追问:文章称其他数据库难以存储多 MB 的 Blob,但是否试过在应用层压缩后再测试这些数据库?

**标签**: `#sqlite`, `#blob-storage`, `#distributed-systems`, `#storage-engineering`, `#performance`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [Anthropic 登陆纳斯达克，首日开盘较发行价涨 34%](https://www.cls.cn/detail/2539480) ⭐️ 8.0/10

据财联社报道，Anthropic 今日在纳斯达克上市，发行价 83 美元/股，开盘报 111.5 美元，较发行价上涨 34%，按开盘价计算市值约 1.5 万亿美元。IPO 发行 9.8 亿股，总额约 813.4 亿美元，另有 260 亿美元同步私募配售，投资方包括谷歌、英伟达、微软等战略投资者。

telegram · zaihuapd · 11月19日 16:56

**「背景」** Anthropic 此前最近一次私募融资是 2026 年 5 月的 H 轮，融资 650 亿美元，估值为 9650 亿美元；据报道，其 IPO 前的目标估值最高约 1.4 万亿美元。同步私募配售是指在公开发行股票的同时，向特定机构投资者直接定向出售股份。

<details><summary>参考链接</summary>
<ul>
<li>Anthropic raises $65B Series H at $965B valuation</li>
<li>Anthropic is targeting a valuation of up to $1.4tn in its initial public offering. The target valuation marks a jump from $965bn in its last private financing in May but falls short of the record set</li>

</ul>
</details>

**标签**: `#Anthropic IPO`, `#AI sector valuation`, `#Nasdaq listing`, `#private placement`, `#strategic investors`

---