---
layout: default
title: "Horizon Summary: 2026-11-11 (ZH)"
date: 2026-11-11
lang: zh
---

> 从 31 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [DeepMind 推出 AlphaProof Code：用 Lean/Rocq 证明验证真实软件库](#item-tech-news-1) ⭐️ 7.5/10
2. [VulnCheck 称 Glasswing 七个月成果平平，评论区质疑其数据口径](#item-tech-news-2) ⭐️ 7.0/10
3. [.NET 11 运行时更新：运行时级 async 与十进制转换变化](#item-tech-news-3) ⭐️ 7.0/10
4. [Chips and Cheese 解析 AMD Zen 6：分支预测、向量加载与执行单元调整](#item-tech-news-4) ⭐️ 7.0/10
5. [Blender 5.3 发布,新增原生高斯泼溅支持](#item-tech-news-5) ⭐️ 7.0/10
6. [Chrome 发布 modern-web-guidance 1.0，引导编程智能体使用原生 Web 特性](#item-tech-news-6) ⭐️ 6.5/10
7. [Synaptics 专利主张致 DisplayLink 开源驱动工作停摆](#item-tech-news-7) ⭐️ 6.5/10

**财经新闻**
1. [美联储理事沃勒:12 月加息可能性大,不排除加息 50 个基点](#item-finance-news-1) ⭐️ 8.0/10
2. [美国汽油均价 7 月以来首次跌破每加仑 4 美元](#item-finance-news-2) ⭐️ 6.0/10
3. [Polymarket 称年化收入已超 18 亿美元](#item-finance-news-3) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [DeepMind 推出 AlphaProof Code：用 Lean/Rocq 证明验证真实软件库](https://deepmind.google/blog/introducing-alphaproof-code/) ⭐️ 7.5/10

DeepMind 发布了 AlphaProof Code，这是一个通过编写 Lean 或 Rocq 等系统中的形式化证明，来验证真实软件库的智能体。目前只有标题、链接和部分评论可供参考，没有原文正文，因此具体的技术细节、验证对象、规模和评测结果都无法核实。评论中提到的“验证整个库后未发现 bug”只是读者转述，并非已确认的结果。

hackernews · ilreb · 11月10日 12:11 · [社区讨论](https://news.ycombinator.com/item?id=50439193)

**「背景」** 形式化验证是在 Lean、Rocq 等证明助手中，为代码满足某条明确写出的规格提供可由机器检查的证明。因此证明只能保证已被形式化的性质，规格是否完整、是否过窄，仍需要人来判断，这也是评论区质疑“零漏洞”结果的核心。DeepMind 原文未能获取，据多家二手报道，此次验证对象是 Signal 协议的实际实现代码，AI 代理在约四周内写出六百多万行 Lean 证明；这些细节尚未经原文或独立评测核实。

**「影响」** 如果要依赖这类工具，关键是先看它证明的规约有多强。评论者指出，智能体可能只证明了范围很窄的性质，或者只验证实现而没有质疑规约本身，在这种情况下，“证明通过”并不等于代码没有缺陷。在 DeepMind 公布完整论文或评测之前，应把它视为尚未经独立验证的厂商声明。

**「社区讨论」** hedora 认为，对一个历史上出过 bug 的非平凡库，验证后却发现零 bug 令人怀疑，可能是定理写错了或只证明了狭窄的性质。thibsrn 则观察到该智能体似乎只挑战实现、不挑战规约，并质疑它与普通编码智能体的区别；r0ze-at-hn 等人也提醒，AI 在自己写 Lean 时很容易“作弊”。这些都是评论者的看法，不是已确认的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://codingislove.com/alphaproof-code-signal/">DeepMind&#x27;s AlphaProof Code formally verifies Signal&#x27;s ...</a></li>
<li><a href="https://cellcog.ai/blog/alphaproof-code-signal/">AlphaProof Code: DeepMind&#x27;s AI Proves Signal&#x27;s Code</a></li>

</ul>
</details>

**标签**: `#formal-verification`, `#AlphaProof`, `#DeepMind`, `#AI-coding-agents`, `#Lean`

---

<a id="item-tech-news-2"></a>
### [VulnCheck 称 Glasswing 七个月成果平平，评论区质疑其数据口径](https://www.vulncheck.com/blog/anthropic-glasswing-november-update) ⭐️ 7.0/10

VulnCheck 发表博文，评估 Anthropic 的 Glasswing AI 漏洞挖掘项目运行七个月后的表现。标题称其发现“平平”，同时给开源维护者增加了负担。本次未能获取博文正文，因此文中的具体数据和论证过程无法核实，以上判断只能依据标题和评论区的转述。

hackernews · panic · 11月10日 22:17 · [社区讨论](https://news.ycombinator.com/item?id=50447074)

**「背景:Glasswing 与公开漏洞台账」** Anthropic 于 2026 年 4 月 7 日启动 Project Glasswing,这是围绕未公开发布的前沿模型 Claude Mythos Preview 构建的协同漏洞研究计划,目标是让关键开源项目的维护者借助 AI 更早发现并修复漏洞。5 月 22 日,Anthropic 在更新中公布了一个仪表盘\(台账\),跟踪其所扫描开源漏洞在各披露环节的进展。VulnCheck 此前的文章已经基于这些公开台账做过核对,指出 GHSA 台账、CVE 台账和主台账之间的数字对不上\(例如 CVE 台账列出 70 个 CVE,主台账为 82 个\)。这次的评估同样依赖公开披露数据。

**「社区讨论」** 多位评论者反驳了博文的结论。Fil-C 维护者 pizlonator 称，自己收到 Anthropic 提交的 9 份报告，全部是真实漏洞、没有误报，报告质量“极佳”，但修复补丁质量一般。另有评论者指出，博文依据的是 Anthropic 面向开源软件的协调披露公开记录，而 Glasswing 的多数发现来自合作伙伴对自家闭源代码的扫描，这些漏洞不会获得 CVE 编号，因此公开 CVE 数据不能反映项目的实际效果。这些说法都是评论者的个人陈述，未经独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/project/glasswing">Project Glasswing \ Anthropic</a></li>
<li><a href="https://www.anthropic.com/news/glasswing-initial-update">Project Glasswing: An initial update \ Anthropic</a></li>
<li><a href="https://cloudsecurityalliance.org/artifacts/project-glasswing-ai-discovery-outpaces-open-source-patching-capacity">Project Glasswing: AI Discovery Outpaces Open Source Patching ...</a></li>
<li><a href="https://www.vulncheck.com/blog/anthropic-glasswing-receipts">The Anthropic Glasswing Receipts Are Starting to Trickle... | VulnCheck</a></li>

</ul>
</details>

**标签**: `#AI security research`, `#vulnerability discovery`, `#open source maintainers`, `#Anthropic Glasswing`, `#CVE analysis`

---

<a id="item-tech-news-3"></a>
### [.NET 11 运行时更新：运行时级 async 与十进制转换变化](https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-11/runtime) ⭐️ 7.0/10

微软发布了 .NET 11 运行时的新特性文档页面。所提供的原文只有指向 .NET 11 发布公告的链接,没有具体特性清单,因此完整的运行时变更无法据此核实。从社区评论看,较受关注的是运行时级 async 支持:评论者称它不再依赖编译器生成的状态机,堆栈跟踪更易读,且性能据称与原方案相当。评论还提到了新的版本管理工具 dotnetup,以及一项十进制转换的兼容性变更。

hackernews · stevefan1999 · 11月10日 12:20 · [社区讨论](https://news.ycombinator.com/item?id=50439284)

**「背景」** 此前 C\# 的 async/await 由编译器把异步方法改写成状态机,挂起与恢复的逻辑也生成在用户代码里,所以堆栈跟踪里会出现这些生成出来的结构。按微软文档的说法,.NET 11 引入了运行时原生异步\(Runtime Async V2\),开始由运行时自己管理异步方法的挂起与恢复,以取代编译器生成的状态机。这一页是 .NET 11 运行时的新特性概览,迁移到新版本的开发者还需要对照微软单独列出的 .NET 11 重大变更清单。

**「影响」** 升级到 .NET 11 的开发者应先查阅微软的兼容性变更文档。有评论者贴出的示例显示,\(decimal\)0.1 在 .NET 10 中得到 0.1,在 .NET 11 中得到 0.1000000000000000055511151231。涉及金融计算、序列化或数值比较的代码可能因此行为改变,升级前应加以测试。

**「社区讨论」** 评论者 wofo 对运行时 async 感到意外:去掉代码中的状态机能让堆栈跟踪更友好,但他没想到切换到运行时实现后性能还能持平。另一位评论者 1a527dd5 提醒注意十进制转换的行为变化;还有人认为 C\# 和 .NET 因旧印象\(如仅限 Windows\)而被低估。这些均为评论者个人看法,未经原文证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-us/dotnet/core/whats-new/dotnet-11/runtime">What&#x27;s new in .NET 11 runtime | Microsoft Learn</a></li>
<li><a href="https://learn.microsoft.com/en-us/dotnet/core/compatibility/11">Breaking changes in .NET 11 | Microsoft Learn</a></li>

</ul>
</details>

**标签**: `#dotnet-11`, `#runtime-async`, `#csharp`, `#microsoft`, `#breaking-changes`

---

<a id="item-tech-news-4"></a>
### [Chips and Cheese 解析 AMD Zen 6：分支预测、向量加载与执行单元调整](https://chipsandcheese.com/p/amds-zen-6-family-feeding-the-beast) ⭐️ 7.0/10

Chips and Cheese 发表了对 AMD Zen 6 CPU 家族的微架构分析，标题为“Feeding the Beast”，主题是核心如何更好地获得数据与指令。本次只提供了标题、简短分析摘要和评论节选，没有文章正文，因此无法核实文章的完整结论与测量数据。评论引用的细节包括：2-ahead 分支预测、每周期四次向量加载（256 位或更窄）、整数乘法单元由三个减为两个，以及 PDEP/PEXT 吞吐从每周期三条降到两条。这些说法均来自评论转述，不是已核实的原文内容。

hackernews · pixelpoet · 11月10日 17:02 · [社区讨论](https://news.ycombinator.com/item?id=50443090)

**「背景:Zen 6 与“喂饱核心”问题」** Zen 6 是 AMD 下一代 Zen 架构,与前两代一样分为标准版和高核心密度的 Zen 6c 版,据 Wikipedia 称每个 CCD 最多可容纳 32 个核心。这类分析文章关注的核心问题是:当内存速度相对核心越来越慢时,分支预测、向量加载带宽等前端和访存设计如何让执行单元持续有活干。由于未获取到文章全文,具体测量结论需以原文为准;评论中提到的 2-ahead 分支预测、每周期四次向量加载、整数乘法单元由三个减为两个等细节,只是读者转述。

**「社区讨论」** 评论者 bmenrigh 称，AM5 平台上 Zen 4/5 的 I/O die 与内存控制器是主要短板，双通道下很难超过 3600 MT/s，并希望 Zen 6 改善这一点，同时转述了新 I/O 芯粒将采用更小制程的传闻。其他评论者则关注执行单元的取舍：Remnant44 推测乘法器减少可能是为 VNNI 流水线腾出面积，并好奇 gather 性能是否终于可用；Aardwolf 则询问 PDEP/PEXT 是否与乘法器共用电路，目前没有看到确切答案。另有评论者 bee\_rider 对每个 CCD 多达 32 个 C 核心提出疑问，想知道在 NUMA 最低层级之下是否还有更小的逻辑单元，该问题同样没有得到确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Zen_6">Zen 6 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#AMD Zen 6`, `#CPU microarchitecture`, `#memory subsystem`, `#hardware analysis`, `#Chips and Cheese`

---

<a id="item-tech-news-5"></a>
### [Blender 5.3 发布,新增原生高斯泼溅支持](https://www.blender.org/download/releases/5-3/) ⭐️ 7.0/10

Blender 5.3 已发布,标题称其加入了对高斯泼溅\(Gaussian Splat\)的原生支持。社区评论还提到几何节点的 bundle、list 和 closure 等功能,以及视频编辑器的改进。由于未能获取发布页正文,完整功能清单、高斯泼溅的具体能力\(导入格式、渲染方式等\)和技术细节均无法核实。

hackernews · amlib · 11月10日 16:15 · [社区讨论](https://news.ycombinator.com/item?id=50442426)

**「背景：什么是高斯泼溅」** 3D 高斯泼溅（Gaussian Splatting）是一种用大量带位置、颜色、透明度和形状的半透明椭球来表示并渲染真实场景的技术，常用于由照片或视频重建的场景。此前这类数据多需借助专用工具或插件处理；据 Blender 开发者文档的渲染发行说明，5.3 版加入了 3D 高斯泼溅的导入、点云支持、几何节点集成，以及在 Workbench、EEVEE 和 Cycles 中的渲染。

**「影响」** 一位用户称,在 M4 设备上用 5.3 测试版打开约 400 万个泼溅点的场景\(由 Spirula Studio 导出\),运行流畅且与界面整合良好,说明原生支持可能让处理高斯泼溅的 3D 工作流不必依赖外部工具。这只是单个用户的体验,尚无独立基准测试;从事相关工作的用户可先用自己的数据验证兼容性和性能。

**「社区讨论」** 用户 mturk 认为,几何节点中的 bundle 配合 list 和 closure,让可视化节点更接近传统编程方式,对复杂流程帮助很大,他此前已在 alpha 版中使用。另有用户 throw\_m239339 询问 Alembic 导出问题是否已修复,同时肯定视频编辑器的进步;Retro\_Dev 则联想到三角形泼溅,认为 GPU 本就擅长渲染三角形。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://developer.blender.org/docs/release_notes/5.3/rendering/">Rendering - Blender Developer Documentation</a></li>

</ul>
</details>

**标签**: `#Blender`, `#Gaussian Splatting`, `#3D Rendering`, `#Open Source`, `#Geometry Nodes`

---

<a id="item-tech-news-6"></a>
### [Chrome 发布 modern-web-guidance 1.0，引导编程智能体使用原生 Web 特性](https://github.com/GoogleChrome/modern-web-guidance) ⭐️ 6.5/10

Chrome 团队联合 Firefox、MDN 和 Edge 发布了开源项目 modern-web-guidance 1.0。它包含 200 多篇、约 1.7MB 的人工编写 Web 最佳实践指南，以 agent skill 加检索式 CLI 的形式提供，通过 npx 安装。目的是让编程智能体优先使用 \`&lt;dialog&gt;\`、\`CSS.highlights\`、\`field-sizing\` 等浏览器原生能力，而不是惯用的 div+JS 写法。作者称，该项目在 200 个任务、约 1,700 条 Playwright/AST 断言上测试 codex、claude 和 agy，通过率从无指导时的 55% 升至 92%；另有一个基于 3 万个 GitHub 仓库训练的 \`legacy-scan\`，在留出仓库上平均精度为 92%。这些数据均为项目方自述，摘要中没有独立复现。

hackernews · paulirish · 11月10日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50443812)

**「背景」** 大模型虽然知道不少新的 Web 平台特性，但生成代码时仍倾向于沿用训练数据中常见的旧模式，例如自己用 JS 实现对话框、自动增高的文本框等。Agent skill 是向智能体按需注入领域知识的机制，该项目试图在不占满上下文窗口的前提下实现这一点。作者称，检索部分已从约 500MB 的原生方案缩减为约 7MB 的纯 JS 包，在本机 CPU 上搜索约需 10ms。

**「影响」** 使用 Claude、Codex 等智能体做前端开发的团队，可以试用该 skill，或对现有 \`./src\` 运行 \`legacy-scan\` 找出可现代化的旧写法。不过评论者指出，指南可能推荐仅 Chrome 稳定支持的特性，采用前需要对照目标浏览器的兼容性，并检查智能体的改动是否引入了跨浏览器问题。

**「社区讨论」** 评论者 surround 列出了指南可能推荐的一批仅 Chrome 稳定、Firefox 和 Safari 尚不支持的特性，例如 CSS @function 和 calc-size\(\)；advisedwang 则担心这会进一步放大 Chrome 对标准的影响力，导致“请使用某浏览器访问”的局面重现。simonw 另建议在 GitHub Pages 上发布便于 grep 的 Markdown 索引，让智能体无需安装即可通过 HTTP 读取。

**标签**: `#coding-agents`, `#web-platform`, `#chrome`, `#agent-skills`, `#open-source`

---

<a id="item-tech-news-7"></a>
### [Synaptics 专利主张致 DisplayLink 开源驱动工作停摆](https://lwn.net/SubscriberLink/1102549/acbc92e00cee3a3f/) ⭐️ 6.5/10

据 LWN 报道\(经订阅者链接分享\),Synaptics 向 DisplayLink 开源驱动的开发者提出专利主张并发出要求函,导致相关驱动的开发工作停止。评论中引用的信件称,若对方不在期限内照办,Synaptics 将索要 2.5 万美元,以补偿其整理“侵权行为”文档所花的成本。本次可用材料只有标题和部分评论,没有文章正文,因此具体涉及哪些专利、哪些开发者、法律依据是否成立,均无法核实。

hackernews · speckx · 11月10日 18:02 · [社区讨论](https://news.ycombinator.com/item?id=50443824)

**「背景」** DisplayLink 是 Synaptics 旗下的 USB 扩展显示技术,依赖软件驱动在主机端压缩并传输画面,Linux 上长期缺少官方的完全开源驱动。据 Tom&\#x27;s Hardware 和 Phoronix 报道,名为 Vino 的开源驱动开发者收到了 Synaptics 的停止侵权函,相关代码随后下线,往来信件附在 LKML 邮件列表的讨论串中。Synaptics 官网只提到社区拥有的开源库 LibDLO。上述报道中关于专利主张的法律依据尚未经独立验证。

**「影响」** 对依赖 DisplayLink 扩展坞的 Linux 用户来说,开源驱动的维护可能停滞,短期内只能继续使用厂商的专有驱动,或改用 Thunderbolt/USB4 或 DisplayPort alt mode 方案。对其他硬件驱动的逆向工程者来说,这也提示了专利风险;但这一案件的法律依据尚未得到验证,不宜据此推断一般性结论。

**「社区讨论」** 多位评论者认为,要求对方承担取证文档成本的做法明显不合理,更像是吓阻手段;xxpor 则指出,专利的前提是公开披露技术,逆向工程本身并不构成专利侵权,Synaptics 的主张在法律上站不住脚。另有评论者\(kieranl、cbdumas\)认为 DisplayLink 正在被 Thunderbolt/USB4 扩展坞取代,且使用体验不佳,但这些只是个人看法,并非已证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/peripherals/docking-stations-hubs/synaptics-sends-cease-and-desist-order-to-creator-of-open-source-displaylink-driver-dares-him-to-publicize-its-threats-dev-reverse-engineers-displaylink-using-claude-ai-and-rust-synaptics-threatens-to-bill-creator-for-legal-documentation">Synaptics sends cease-and-desist order to creator of open - source ...</a></li>
<li><a href="https://www.synaptics.com/products/displaylink-graphics/embedded/sdk">Software Tools | Synaptics</a></li>
<li><a href="https://www.phoronix.com/news/Synaptics-Blocks-Vino-Driver">Synaptics Appears To Use Legal Threats To Block Open - Source ...</a></li>

</ul>
</details>

**标签**: `#patents`, `#open-source`, `#DisplayLink`, `#Linux-drivers`, `#Synaptics`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储理事沃勒:12 月加息可能性大,不排除加息 50 个基点](https://www.cnbc.com/2026/11/10/fed-governor-waller-sees-december-hike-likely.html) ⭐️ 8.0/10

美联储理事沃勒周二表示,他倾向于 12 月加息;若通胀数据高于预期,应考虑加息 50 个基点\(0.5 个百分点\),而不是常规的 25 个基点。达拉斯联储主席洛根则预计,在暂停观察效果之前,还会再加息两次、每次 25 个基点。

rss · CNBC Finance · 11月10日 17:13

**「背景」** 美联储在 2026 年 9 月 16 日把联邦基金利率（银行间隔夜拆借的基准利率）目标区间上调 0.25 个百分点至 3.75%–4%，这是三年多来的首次加息；10 月会议没有加息，但库克和哈马克对此表示反对。

**「影响」** 10 月 CPI\(消费者价格指数\)环比上涨 0.4%,核心 CPI 上涨 0.3%,均比道琼斯预期高 0.1 个百分点;交易员据此完全计入 12 月加息 25 个基点,并给出 12.5%的加息 50 个基点的概率,这意味着借贷成本可能继续上升。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.federalreserve.gov/newsevents/pressreleases/monetary20260916a.htm">Federal Reserve issues FOMC statement</a></li>
<li><a href="https://www.cnbc.com/2026/09/16/fed-rate-decision-september-2026.html">Fed rate decision September 2026: Rates rise to 3.75%-4% - CNBC</a></li>

</ul>
</details>

**标签**: `#Federal Reserve`, `#interest rate hikes`, `#October CPI inflation`, `#Christopher Waller`, `#monetary policy`

---

<a id="item-finance-news-2"></a>
### [美国汽油均价 7 月以来首次跌破每加仑 4 美元](https://www.cnbc.com/2026/11/10/us-gas-prices-below-four-dollars.html) ⭐️ 6.0/10

据美国汽车协会\(AAA\)数据,美国普通汽油全国均价周二降至每加仑 3.9788 美元,为 7 月以来首次低于 4 美元,较一周前下降约 17 美分,较一个月前下降近 39 美分。

rss · CNBC Finance · 11月10日 16:29

**「背景」** 美国与伊朗的冲突已持续近九个月，而全球约五分之一的石油供应要经过霍尔木兹海峡，冲突升级后油价和汽油价格因此大幅上涨。市场对局势缓和的预期会压低“地缘风险溢价”，也就是油价中为供应中断风险额外加上的那部分价格。

**「影响」** 汽油价格回落减轻了驾车家庭的加油支出,但美联储理事沃勒提醒,能源价格较年初仍然偏高,对通胀的最终影响取决于价格能否持续在较低水平;Bespoke 投资集团也指出,此次下降有一部分是季节性因素。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/world/2026/mar/02/oil-prices-iran-war-strait-of-hormuz-shipping">Gas prices soar and oil jumps as Iran war pushes... | The Guardian</a></li>

</ul>
</details>

**标签**: `#gasoline prices`, `#oil markets`, `#energy inflation`, `#Federal Reserve`, `#Middle East supply`

---

<a id="item-finance-news-3"></a>
### [Polymarket 称年化收入已超 18 亿美元](https://www.cnbc.com/2026/11/10/polymarket-annualized-revenue-us-growth.html) ⭐️ 6.0/10

预测市场平台 Polymarket 周二告诉 CNBC,其年化收入已超过 18 亿美元,6 月时该公司披露的这一数字为 10 亿美元以上。公司称增长主要来自其美国交易所;该数据为公司提供,未经独立核实。

rss · CNBC Finance · 11月10日 13:00

**「背景」** Polymarket 是一个让用户对赛事、政治等事件结果买卖“事件合约”的预测市场平台，今年 5 月推出美国本土交易所，与面向海外的去中心化平台分开运营。美国商品期货交易委员会（CFTC）10 月下旬被报道正在调查它是否违反 2022 年和解协议，即禁止美国用户使用其海外平台。

**「影响」** Polymarket 正面临美国商品期货交易委员会\(CFTC\)的调查,涉及广告做法,以及是否违反此前禁止美国居民使用其国际平台的和解协议;公司还可能面临来自国会的更多审查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/10/27/cftc-probes-polymarket-over-2022-settlement.html">CFTC probes Polymarket over 2022 settlement - CNBC</a></li>
<li><a href="https://www.reuters.com/business/finance/us-agency-is-again-probing-if-polymarket-broke-2022-settlement-sources-says-2026-10-27/">US agency is again probing if Polymarket broke 2022 ...</a></li>

</ul>
</details>

**标签**: `#Polymarket`, `#prediction markets`, `#CFTC investigation`, `#startup funding`, `#event contracts`

---