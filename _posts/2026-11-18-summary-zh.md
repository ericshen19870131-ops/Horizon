---
layout: default
title: "Horizon Summary: 2026-11-18 (ZH)"
date: 2026-11-18
lang: zh
---

> 从 49 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Calif 披露 Java4Shell：OpenJDK 处理 Base64 时可远程代码执行](#item-tech-news-1) ⭐️ 8.0/10
2. [OpenAI 发布 GPT-6.2 Astra 与 Sol，Astra API 降价 20%](#item-tech-news-2) ⭐️ 7.0/10
3. [SolidJS 发布 2.0 大版本，细节待核实](#item-tech-news-3) ⭐️ 7.0/10
4. [微软 AI 发布自研编程模型 MAI Code 2 与 Code 2 Flash](#item-tech-news-4) ⭐️ 7.0/10
5. [Cloudflare 发文谈 Quad9 退出法国：开放 DNS 解析器面临封锁义务](#item-tech-news-5) ⭐️ 6.5/10
6. [外部沙箱模式：为编程智能体提供三种沙箱服务实现](#item-tech-news-6) ⭐️ 6.5/10
7. [Datasette Lite 完全重写：用 Service Worker 与 Pyodide 在浏览器运行完整 Datasette](#item-tech-news-7) ⭐️ 6.5/10
8. [微软 ONNX Runtime 的 GitHub 仓库无法访问，原因未明](#item-tech-news-8) ⭐️ 6.0/10
9. [英伟达不再披露新加坡销售额，其新加坡实体收入达 1040 亿美元](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [英伟达、苹果等美企面临两难：中美压力下如何处理对华业务](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Calif 披露 Java4Shell：OpenJDK 处理 Base64 时可远程代码执行](https://calif.io/java4shell/) ⭐️ 8.0/10

安全团队 Calif 披露了一条 OpenJDK 远程代码执行利用链，称为“Java4Shell”，触发点在 Base64 处理，并借助网络远程堆整理（Remote Heap Feng Shui）实现。转载的 Telegram 帖子称其编号为 CVE-2026-114938，CVSS 4.0 评分 9.2，无需认证，潜伏近 4 年。受影响范围据称包括 Java 17（17.0.6 及之后）、21、25 和 27，标准 Java 8/11 通常不受影响，但 Oracle Java 8 Performance Pack 例外。漏洞只影响支持 AVX-512 VBMI 的 x86-64 处理器（大致为 Ice Lake 及更新的 Xeon、Zen 4 及更新的 EPYC/Ryzen），ARM64 不受影响。以上细节来自二手转载和评论摘录，未见 Calif 完整文章或官方补丁信息，具体范围和严重程度仍待核实。

hackernews · werrett · 11月17日 21:11 · [社区讨论](https://news.ycombinator.com/item?id=50538240)

**「背景」** Base64 是把二进制数据编码成文本的常见方式,Java 在处理 HTTP 头、令牌和证书等数据时会用到其解码器。据 Wiz 和 Datadog 的外部分析,这个漏洞出在 OpenJDK 针对 AVX-512 指令集优化的 Base64 解码汇编代码中,会造成堆内存破坏;Qualys 则提到,发现者按 CVSS 4.0 评为 9.2,Oracle 按 CVSS 3 评为 8.1。社区评论还提到,该问题可能可以通过 \`-XX:UseAVX=2\` 绕过,但这只是未经证实的说法。

**「影响」** 运行 Java 17/21/25/27 的 x86-64 服务器运维者，应先确认是否使用 HotSpot 系 JVM，以及 CPU 是否支持 AVX-512 VBMI。Semgrep 已发布免费检测脚本，按五个条件判断主机是否处于风险范围，其中包括只有 HotSpot 才会生成相关 stub。评论中有人称可用 -XX:UseAVX=2 规避，但这一说法来自社交媒体，尚未证实，应等官方补丁或建议后再作为正式缓解措施。

**「社区讨论」** 评论者 lucasluitjes 引用文章内容指出，该攻击对往返时延（RTT）和抖动敏感，低而稳定的延迟更利于成功，作者称已通过公网 IP 实测，而非只在理想实验室环境中验证。Semgrep 的 ievans 则认为利用条件虽然很具体，但受影响主机仍会很多；AgentME 转述推特上的说法，认为问题与 AVX-512 版 Base64 解码有关，但自己也说明这一点尚未确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://securitylabs.datadoghq.com/articles/java4shell-remote-code-execution-in-openjdk-cve-2026-114938/">Java4Shell: Remote Code Execution in OpenJDK (CVE-2026-114938)</a></li>
<li><a href="https://www.wiz.io/blog/cve-2026-114938-rce-java4shell-openjdk">CVE-2026-114938 RCE in OpenJDK: Everything You Need to Know</a></li>
<li><a href="https://blog.qualys.com/vulnerabilities-threat-research/2026/11/17/how-to-find-mitigate-and-patch-the-critical-java4shell-flaw-cve-2026-114938-now">How to Find, Mitigate, and Patch the Critical Java4Shell Flaw ...</a></li>

</ul>
</details>

**标签**: `#OpenJDK`, `#RCE`, `#vulnerability research`, `#heap exploitation`, `#Java security`

---

<a id="item-tech-news-2"></a>
### [OpenAI 发布 GPT-6.2 Astra 与 Sol，Astra API 降价 20%](https://openai.com/index/introducing-gpt-6-2-astra-sol/) ⭐️ 7.0/10

OpenAI 推出两款新模型：面向最难项目的旗舰 GPT-6.2 Astra，以及面向日常工作的高效模型 GPT-6.2 Sol。API 模型名为 \`gpt-6.2-astra\` 和 \`gpt-6.2-sol\`，Telegram 转载称二者已在 ChatGPT Work 和 Codex 上线。据 Simon Willison 的整理，Astra 价格为每百万 token 输入 8 美元、输出 40 美元、缓存输入 0.40 美元，是 GPT-6 Astra（10/50 美元，缓存 1 美元）的 80%；Sol 仍为 2/10 美元，与 6.1 Sol 和 6 Sol 相同。Willison 的测试显示 Astra 的 Yonkers 机甲动画效果不及 Claude Fable 5.2 和 Gemini 4 Carbon，市场评价目前褒贬不一。

hackernews · jasondavies · 11月17日 17:46 · [社区讨论](https://news.ycombinator.com/item?id=50535230)

**「背景」** OpenAI 此前已按“Astra（旗舰）+ Sol（高效）”两条线发布模型，Sol 的价格从 GPT-5.6 Sol 的 4/20 美元降到 6 和 6.1 版本的 2/10 美元。Willison 指出，Claude Fable 5.2 同样比前代降价 20%，因此这次 Astra 的价格与竞品持平。

**「影响」** 对长时间运行的智能体会话来说，缓存输入价格从每百万 token 1 美元降到 0.40 美元，成本下降最明显，Willison 也认为这对此类场景有利。是否迁移仍需自行评估：他提到 Astra 6.2 在多项基准上略逊于 Fable 5.2，并有用户反馈其沟通方式让人困惑。需要注意的是，Theo Browne 提到长任务中模型会追问用户无法判断的内部实现细节，这类行为可能拖慢自动化工作流。

**「社区讨论」** 评论者 chriddyp 在自己的数据分析测试中发现，两款模型准确率相近但成本明显下降（Astra 约从 20 美元降到 4 美元，Sol 从 2.6 美元降到 1.2 美元），原因是 token 减少约 20% 且工具调用更少，速度也很快；不过有时会“提前结束”而没找到目标答案。另一边，Topfi 认为官方的幻灯片、工作簿和备忘录示例质量很差，还有人称评价褒贬不一。这些都是个人测试与看法，并非独立的系统性评测。

**标签**: `#OpenAI`, `#GPT-6.2`, `#LLM release`, `#model benchmarks`, `#AI cost efficiency`

---

<a id="item-tech-news-3"></a>
### [SolidJS 发布 2.0 大版本，细节待核实](https://www.solidjs.com/blog/solid-2-0-the-long-hold/) ⭐️ 7.0/10

SolidJS 响应式 UI 框架发布了 2.0 大版本，发布文章标题为“the long hold”。由于未获取到文章正文，具体的 API 变更、版本号细节、迁移方式和兼容性均无法确认。从 Hacker News 评论看，新版本似乎包含服务端 RPC、“live”和“broadcast”相关能力，以及文中“Built to Be Written by Agents”一节所述的更好的调试诊断，但这些只是评论者的转述，并非来自原文的核实信息。

hackernews · pier25 · 11月17日 18:56 · [社区讨论](https://news.ycombinator.com/item?id=50536387)

**「背景」** Solid 是以细粒度响应式\(signals\)为核心的前端框架,2.0 版本已经酝酿约五年。搜索结果显示,Solid 在 2026 年 8 月发布过 2.0 RC 文章,介绍了新的包结构:响应式核心为 @solidjs/signals,Web 运行时为 @solidjs/web,store 放在 solid-js 内部。此前也有开发者文章提到 2.0 加入了一等公民的异步能力和新的 Loading 边界。需要注意,本条目没有提供正式发布文章正文,上述内容仅为搜索摘要所示的背景。

**「社区讨论」** 评论者 pwmglenn 认为，Solid 的服务端 RPC 与 live/broadcast 用起来无缝自然，比 LiveView 或 htmx/datastar 更顺手，也比 Remix 当年“弥合前后端”的定位更成功；这只是个人使用印象。wk\_end 则指出，所谓“为 Agent 编写而设计”的部分，实质是更好的调试诊断，同样有利于人工编写代码，并猜测这可能只是营销说法。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.solidjs.com/blog/solid-2-0-rc-the-big-reveal">Solid 2.0 RC: The Big | SolidJS</a></li>
<li><a href="https://www.solidjs.com/blog/solid-2-0-the-long-hold/">Solid 2.0 - The Long Hold - solidjs.com</a></li>
<li><a href="https://morello.dev/blog/solidjs-2-react-developers-first-look">SolidJS 2.0 for React Developers: A First Look | Dennis Morello</a></li>

</ul>
</details>

**标签**: `#SolidJS`, `#frontend frameworks`, `#JavaScript`, `#reactivity`, `#major release`

---

<a id="item-tech-news-4"></a>
### [微软 AI 发布自研编程模型 MAI Code 2 与 Code 2 Flash](https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/) ⭐️ 7.0/10

微软 AI 宣布推出自研编程模型 MAI Code 2 和 MAI Code 2 Flash，据称已可在 GitHub Copilot 中使用。由于未能获取原文正文，基准测试成绩、模型架构、上下文长度和定价等细节均无法核实。评论中有用户称 Copilot 当天以 50% 的折扣提供 MAI Code 2，但这只是用户的个人说法，并非官方确认的价格信息。

hackernews · lemonish97 · 11月17日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=50535885)

**「背景」** MAI Code 2 由微软内部的 Microsoft AI 实验室\(由 Mustafa Suleyman 负责\)开发,属于该实验室自研的 MAI 编码模型系列,并通过 GitHub Copilot 向用户提供。第三方报道称,上一代 MAI-Code-1.1-Flash 将于 2026 年 12 月 18 日退役,Code 2 系列是它的接替版本。需要注意,目前已核实的成本和性能对比主要来自微软官方表述,尚无独立评测结果。

**「影响」** 对 GitHub Copilot 用户来说，模型选择列表中多了一个微软自研的选项，可以在自己的任务（如构建修复、测试生成、云部署脚本）上与现有模型对比。在官方公布价格、额度和基准数据之前，不宜仅凭个别体验就调整订阅或工作流。

**「社区讨论」** 用户 chopete3 反映，在 Copilot 中用 MAI Code 2 解决了 WSL/Ubuntu 下的 Python 构建问题、生成并跑通测试，也修好了 Azure Bicep 部署问题，感觉与 Claude Opus 差别不大，但这只是个人的轶事式体验。另一些评论则更多是推测：pseudosavant 认为 OpenAI 和 Anthropic 的领先优势只有几个月，护城河并不牢固；origini 好奇微软为何追赶如此之快，并猜测可能与蒸馏有关，但同时也承认微软多半不被允许这样做，这些都没有证据支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://microsoft.ai/news/introducing-mai-code-2-and-mai-code-2-flash/">MAI Code 2 and Code 2 Flash: Everyday coding at scalable ...</a></li>
<li><a href="https://felloai.com/mai-code-2/">MAI Code 2: Price, Benchmarks and Copilot Plans - felloai.com</a></li>

</ul>
</details>

**标签**: `#MAI Code 2`, `#Microsoft AI`, `#coding models`, `#GitHub Copilot`, `#LLM competition`

---

<a id="item-tech-news-5"></a>
### [Cloudflare 发文谈 Quad9 退出法国：开放 DNS 解析器面临封锁义务](https://blog.cloudflare.com/quad9-withdrawal-from-france/) ⭐️ 6.5/10

Cloudflare 发表博文，讨论开放 DNS 解析服务 Quad9 因法国法院下达的 DNS 封锁义务而退出法国一事，并称其为开放解析器面临的先例性警示（“煤矿里的金丝雀”）。本次仅提供了标题和评论，没有提供文章正文，因此判决的具体内容、涉及的封锁对象、Cloudflare 的具体承诺和技术论证均无法从现有材料中确认。从评论看，Cloudflare 表达了反对立场，但似乎没有明确承诺会采取哪些具体行动。

hackernews · subset · 11月17日 22:13 · [社区讨论](https://news.ycombinator.com/item?id=50538994)

**「背景」** 公共 DNS 解析器负责把域名翻译成 IP 地址。法国权利人近年通过法院命令,要求 Quad9、Google、Cloudflare、思科等公共解析器屏蔽涉嫌侵犯版权的网站。检索结果显示,Quad9 是瑞士非营利基金会,已表示将于 11 月 24 日停止向法国用户提供服务;思科的 OpenDNS 在 2024 年因 Canal+ 的命令已暂停在法国的服务,Google、Cloudflare 和思科则在 3 月的相关案件中败诉,上诉仍在进行\(这些信息来自搜索摘要,并非本文正文\)。

**「影响」** 如果这类解析器级别的封锁义务被确立，运营开放 DNS 解析器的组织在法国可能要么执行封锁，要么像 Quad9 一样退出该国市场，法国用户则可能失去部分第三方解析器的选择。不过，具体适用范围和上诉结果在现有材料中无法确认。

**「社区讨论」** 自称 Quad9 CTO 的 johnhtodd 说，他在 IETF 127 上接触到的人普遍支持 Quad9 的立场，只有受雇于“权利人产业”的人例外；这是个人的转述，并非独立调查结果。评论者 driverdan 则批评 Cloudflare 的文章含糊其辞，要求其明确承诺：若上诉败诉，是否也会退出受影响的国家。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/quad9-withdrawal-from-france/">Quad9’s withdrawal from France: A canary in the coal mine</a></li>
<li><a href="https://dev.to/axrisi/quad9-leaving-france-what-the-paris-court-ordered-and-what-to-check-f0a">Quad9 leaving France: what the Paris court ordered and what ...</a></li>
<li><a href="https://www.eff.org/deeplinks/2026/10/french-courts-site-blocking-orders-drive-quad9-out-france">French Court’s Site-Blocking Orders Drive Quad9 Out Of France</a></li>

</ul>
</details>

**标签**: `#DNS`, `#Quad9`, `#internet censorship`, `#Cloudflare`, `#France regulation`

---

<a id="item-tech-news-6"></a>
### [外部沙箱模式：为编程智能体提供三种沙箱服务实现](https://simonwillison.net/2026/Nov/17/external-sandboxes-for-coding-agents/) ⭐️ 6.5/10

Simon Willison 与 Prime Radiant 合作提出“外部沙箱”（external sandbox）模式：智能体本身运行在沙箱之外，只有它要执行的代码才在专用沙箱内运行，目的是让用户在本地试用模型时，不必担心失误或提示注入导致机器被破坏。为演示该模式，他们发布了三个沙箱服务实现：external-sandbox-v86（Node.js 服务，用 v86 在 WebAssembly 中运行 Alpine Linux）、external-sandbox-container（Python 服务，在 Apple Containers 实例中运行 Alpine）和 external-sandbox-quicksand（Python 服务，使用微软 Quicksand 库，该库打包了 QEMU 和 Alpine）。三者提供相同的 localhost API，可配置 Pi、Claude Code 或 Codex 在需要执行代码时调用；沙箱还带有可选的 HTTP/HTTPS 白名单代理，以及无需向智能体暴露密钥即可完成认证 API 调用的凭据替换机制。

rss · Simon Willison · 11月17日 22:52

**「背景:为什么要把代码执行放进沙箱」** 编码智能体\(如 Claude Code、Codex\)通常直接在用户机器上运行命令,一旦模型出错或遭遇提示注入,就可能执行破坏性操作,使用本地模型时这一顾虑尤其突出。文中三个实现之一使用了微软的 Quicksand,这是一个异步 Python API,用于启动、控制并快照 QEMU 虚拟机,专注于智能体沙箱,并提供 Ubuntu 和 Alpine 的预构建 Linux 镜像,支持 macOS、Linux 和 Windows。

**「影响」** 使用 Pi、Claude Code 或 Codex 的开发者可以把代码执行转发到本机沙箱，并通过白名单代理限制代码可访问的主机，同时避免把密钥交给智能体。需要注意的是，原文内容较简略，三种实现的隔离强度、性能差异和平台限制（例如 Apple Containers 实现显然依赖 macOS）均未提供，采用前需自行查看各仓库。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/microsoft/quicksand">GitHub - microsoft/quicksand: Quickly sandbox your AI agent.</a></li>

</ul>
</details>

**标签**: `#agent-sandboxing`, `#coding-agents`, `#prompt-injection`, `#local-models`, `#AI-security`

---

<a id="item-tech-news-7"></a>
### [Datasette Lite 完全重写：用 Service Worker 与 Pyodide 在浏览器运行完整 Datasette](https://simonwillison.net/2026/Nov/17/datasette-lite/) ⭐️ 6.5/10

Simon Willison 发布了 Datasette Lite 的完整重写版本。新版借助 Service Worker 和 Pyodide，在浏览器里运行完整的服务端 Datasette Python 应用，作者称其“几乎与真正的服务端应用无法区分”。用户通过构造 lite.datasette.io 的 URL，可以浏览 SQLite、JSON、CSV 或 SQL 脚本，选择 PyPI 上已发布的 Datasette 版本，或加载 GitHub 仓库中的指定提交、标签、分支，还能在 100 多个 SQLite 版本中挑选，并从 PyPI 或 wheel 文件 URL 安装插件，包括 JavaScript 可视化插件。以上均为作者自述，文中没有独立测试数据，所给正文也在讲解实现原理处被截断。

rss · Simon Willison · 11月17日 16:48

**「背景」** Datasette Lite 最初由作者于 2022 年发布，通过在 Pyodide Web Worker 中运行 Datasette、模拟请求，再用 \`innerHTML\` 把生成的 HTML 注入页面。这种做法只适用于基础功能：\`innerHTML\` 中的 script 标签不会执行，依赖 JavaScript 的功能因此无法工作。本次改用 service worker 重写，正是要解决这一限制。

**「影响」** 开发者无需搭建 Web 服务器，就能用一个链接分享某个 Datasette 版本、插件组合和数据的可复现演示。作者已在 Datasette 的 issue 中用它对比 1.0a42 的分页 bug 与 1.0a43 的修复效果。需要注意，通过 url 参数加载的数据文件必须带有开放的 CORS 头，作者为此把文件放在 GitHub Gist 上。

**标签**: `#Datasette`, `#Pyodide`, `#WebAssembly`, `#Service Workers`, `#SQLite`

---

<a id="item-tech-news-8"></a>
### [微软 ONNX Runtime 的 GitHub 仓库无法访问，原因未明](https://github.com/microsoft/onnxruntime) ⭐️ 6.0/10

据 Hacker News 上的用户反馈，微软 ONNX Runtime 的主 GitHub 仓库（microsoft/onnxruntime，约 2.2 万星标）已无法访问，且事先没有任何通知。发帖者称，其团队当天早上发现评测流水线开始失败。目前没有微软或 GitHub 的官方说明，也没有原始页面内容可供核实，仓库下线的原因和是否会恢复都不清楚。有评论者提到 Intel 维护的 intel/onnxruntime 分支可作临时替代，但该分支带有 Intel 的 OpenVINO 改动。

hackernews · nvader · 11月17日 23:18 · [社区讨论](https://news.ycombinator.com/item?id=50539610)

**「背景」** ONNX Runtime 是微软维护的跨平台机器学习推理运行时，官方仓库为 microsoft/onnxruntime，另有配套的示例仓库，不少 CI 和评测流水线直接依赖它。同一天，Wiz 报告称微软 PyPI 包 agent-framework 的 1.26.1 和 1.26.2 版本于 2026 年 11 月 17 日 20:35 UTC 发布，并被植入凭据窃取程序，这两个版本后来已被隔离。评论者推测两件事可能有关，但目前没有证据表明二者相关，仓库消失的原因也没有官方说明。

**「影响」** 依赖该仓库源码、子模块或 GitHub 发布资源的 CI 和构建流程可能直接中断。受影响的团队应检查自己的依赖获取方式，并考虑镜像或固定依赖来源。若改用 Intel 分支，需先确认其 OpenVINO 改动是否兼容，并评估来源是否可信。在官方给出说明前，不宜据此推断软件包本身存在安全问题。

**「社区讨论」** 评论者提出了几种猜测：有人认为可能与微软某个软件包被入侵后的清理有关，有人猜测是发现了被植入后门的模型可利用的新攻击途径，另有人批评 ONNX 默认回传应用数据的遥测行为。这些说法都没有证据证实，目前唯一确认的事实是用户的流水线因仓库不可用而失败。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Microsoft/onnxruntime/">GitHub - microsoft / onnxruntime : ONNX Runtime: cross-platform...</a></li>
<li><a href="https://www.wiz.io/blog/malicious-version-of-microsofts-agent-framework-published-to-pypi">Microsoft agent-framework Compromised: Credential Stealer ...</a></li>

</ul>
</details>

**标签**: `#onnx-runtime`, `#github`, `#supply-chain-security`, `#machine-learning-infrastructure`, `#open-source`

---

<a id="item-tech-news-9"></a>
### [英伟达不再披露新加坡销售额，其新加坡实体收入达 1040 亿美元](https://www.ft.com/content/dbde7a30-548c-4f9d-a4be-7898a0c24dcf) ⭐️ 6.0/10

据英国《金融时报》报道，英伟达已停止披露新加坡的销售额，而此前其新加坡实体的收入已达 1040 亿美元。报道同时提到，美国当局正在调查新加坡企业 Megaspeed 是否参与向中国走私英伟达芯片。由于原文需付费，目前仅能看到标题和评论片段，报道细节、调查进展和英伟达的回应均无法核实。

hackernews · louiereederson · 11月17日 17:12 · [社区讨论](https://news.ycombinator.com/item?id=50534631)

**「背景:新加坡主体与 Megaspeed 调查」** 有评论者称,英伟达的 GPU 通常经 OEM、ODM 和经销商销售,新加坡子公司的收入反映的是经该主体开票的订单,不等于芯片最终落在新加坡。这一说法尚未得到原文或独立来源证实。此前,纽约时报报道,商务部对新加坡公司 Megaspeed\(该公司购买英伟达高端 AI 芯片\)的调查,在英伟达一名高管联系商务部官员后被移交司法部。金融时报也报道过新加坡在中国 AI 芯片贸易中的角色。

**「影响」** 这个数字不宜直接当作“芯片实际流向新加坡”的证据。有评论称，该数字是新加坡子公司的对外收入，包含经 OEM、ODM 和经销商下单后由该实体开票的订单。若这一说法属实，外界要判断出口管制风险，还需要最终交付地点和客户的数据，而不能只看按实体划分的收入。

**「社区讨论」** 评论中最有用的观点来自 tamarind44 和 legitster：他们认为 1040 亿美元反映的是收入的记账归属，而不是芯片的最终使用地，标题容易引发误读。另有评论则猜测英伟达高层人事变动与规避制裁有关，但这只是个人推测，没有证据支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2026/11/09/business/economy/nvidia-megaspeed-investigation-huang.html">U.S. Commerce Dept. Inquiry Into Megaspeed Was Halted After...</a></li>
<li><a href="https://www.ft.com/content/52b5f9a8-346f-4dae-8a16-14d5d9eb1244?syn-25a6b1a6=1">Nvidia spy scandal exposes Singapore ’s role in China ’s AI chip trade</a></li>

</ul>
</details>

**标签**: `#nvidia`, `#export-controls`, `#ai-hardware`, `#semiconductor-supply-chain`, `#singapore`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [英伟达、苹果等美企面临两难：中美压力下如何处理对华业务](https://www.cnbc.com/2026/11/17/us-tech-firms-china-ties-political-pressure.html) ⭐️ 7.0/10

据 CNBC 报道，黄仁勋上周辞去英伟达 CEO 职务，特朗普政府周一收紧了中国企业远程使用美国先进芯片的限制，英伟达、苹果等美国科技公司在华业务面临来自华盛顿和北京的双重压力。特朗普与习近平本周四将会面，但外界预计双方难以明显扩大去年秋天达成的脆弱贸易休战。

rss · CNBC Finance · 11月17日 08:52

**「背景」** 美国长期通过出口管制限制中国获取先进 AI 芯片，但中国企业可通过海外数据中心远程使用这些芯片，美方本周出台的新规正是要堵上这一漏洞。与此同时，中国是美国科技企业的重要市场和供应链基地，并掌控稀土等关键矿产的供应链，使这些企业在美中博弈中进退两难。

**「影响」** 苹果大部分 iPhone 仍在中国生产，大中华区约占其销售额的 15%，因此中美摩擦若升级，可能同时影响其供应链和客户；分析人士还提到，中国对稀土的掌控使北京的潜在报复更具杀伤力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://apnews.com/article/nvidia-export-controls-chips-china-remote-access-60f868d3bb430b85a8657b27d421096e">Trump administration moves to restrict China from indirect ...</a></li>
<li><a href="https://www.nytimes.com/2026/11/16/us/politics/trump-china-ai-chip-loophole.html">Trump Administration Moves to Close A.I. Chip Loophole Ahead ...</a></li>

</ul>
</details>

**标签**: `#US-China tech tensions`, `#Nvidia`, `#chip export controls`, `#Apple supply chain`, `#rare earths`

---