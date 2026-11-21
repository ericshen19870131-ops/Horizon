---
layout: default
title: "Horizon Summary: 2026-11-21 (ZH)"
date: 2026-11-21
lang: zh
---

> 从 48 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [GitHub 仓库声称证明无外力 Navier–Stokes 方程有限时间爆破](#item-tech-news-1) ⭐️ 8.0/10
2. [Alpöge 称借助 Claude 证明广义黎曼猜想，尚待独立验证](#item-tech-news-2) ⭐️ 8.0/10
3. [Thinking Machines 发布开放权重循环 Transformer 模型 Inkling 2 Mini](#item-tech-news-3) ⭐️ 8.0/10
4. [陶哲轩博文称无外力欧拉/纳维-斯托克斯奇点与广义黎曼猜想相关，细节未获证实](#item-tech-news-4) ⭐️ 8.0/10
5. [KVM 漏洞 CVE-2026-99312：AMD 主机内存可被虚拟机读取](#item-tech-news-5) ⭐️ 7.5/10
6. [Signal 就如何防止移动系统 AI 代理抓取私密应用数据发声](#item-tech-news-6) ⭐️ 7.0/10
7. [台积电据称暂停接收中国企业 16nm 及以下制程订单](#item-tech-news-7) ⭐️ 7.0/10
8. [Cursor 拟逐步停用中国开源权重模型，Composer 2 基于 Kimi K2.5](#item-tech-news-8) ⭐️ 6.5/10

**财经新闻**
1. [沃什不愿给出利率指引,美联储官员反而发声更多](#item-finance-news-1) ⭐️ 7.0/10
2. [美国企业转向净发行股票，市场股票供应增加](#item-finance-news-2) ⭐️ 6.5/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [GitHub 仓库声称证明无外力 Navier–Stokes 方程有限时间爆破](https://github.com/tristanbuckmaster/navier-stokes/) ⭐️ 8.0/10

一个 GitHub 仓库\(tristanbuckmaster/navier-stokes\)声称证明了无外力 Navier–Stokes 方程存在有限时间爆破,并在 Hacker News 上引发讨论。所提供材料只有仓库链接,没有可读取的正文,证明细节、同行评审和独立验证情况均无从核实,因此这仍是未经确认的说法。评论者提到的相关进展\(带外力版本的爆破、OpenAI 的相关发布、千禧年难题传闻\)也只是匿名评论中的说法,同样未获证实。

hackernews · trotro · 11月20日 15:34 · [社区讨论](https://news.ycombinator.com/item?id=50576232)

**「背景」** 纳维–斯托克斯方程描述粘性流体的运动。“光滑初始数据是否会在有限时间内形成奇点（爆破）”是克雷数学研究所千禧年大奖难题的核心问题。据 OfficeChai 报道，Alpöge 和 Buckmaster 的论文声称，在没有外力作用的情况下，光滑初始数据也会在有限时间内产生奇点；Magica 称这篇 79 页、有 AI 辅助的论文缺少数值证书，独立验证尚未完成，因此仍属未经证实的主张。

**「影响」** 若证明经审查成立,无外力版本比依赖精心设计外力的例子更接近原始的千禧年难题表述,数学界和流体力学研究者需要等待严格审查再做判断。在此之前,不宜把它当作已确认的结论引用。

**「社区讨论」** 有评论者区分了两类结果:tancop 指出,OpenAI 的例子依赖精心设计的外力,而本次是无外力版本,因此在某种意义上更“现实”。另一些评论者则带着兴奋和传闻色彩讨论其意义,并希望看到数值模拟或物理演示;这些观点都不是已验证的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://officechai.com/ai/tristan-buckmaster-levent-alpoge-claim-proof-of-navier-stokes-millennium-prize-problem-without-forcing/">Tristan Buckmaster, Levent Alpöge Claim Proof Of Navier ...</a></li>
<li><a href="https://magica.com/news/alpoge-buckmaster-navier-stokes-unforced-blowup-claim">Alpöge and Buckmaster’s unverified Navier–Stokes claim | Magica</a></li>

</ul>
</details>

**标签**: `#Navier-Stokes`, `#mathematics`, `#fluid dynamics`, `#Millennium Problems`, `#AI-assisted research`

---

<a id="item-tech-news-2"></a>
### [Alpöge 称借助 Claude 证明广义黎曼猜想，尚待独立验证](https://alpo.ge/remark.pdf) ⭐️ 8.0/10

Levent Alpöge 在 alpo.ge/remark.pdf 发布文稿，称自己与 Claude 合作发现了黎曼猜想的证明，方法还可推广到广义黎曼猜想（GRH），他预计给予更多时间也能处理扩展黎曼猜想。他称二人已在不带额外假设的前提下完成了形式化。Telegram 转述 Scientific American 的报道称，证明已用 Lean 编码发布，文稿超过 25 万页；Hacker News 评论者则称 Lean 压缩包约 1.3GB、约 1500 万行代码。目前这些都是作者的声明和社区转述，所提供材料中没有经过同行评审的确认，也无法据此评估证明的具体内容。

hackernews · iamronaldo · 11月20日 14:16 · [社区讨论](https://news.ycombinator.com/item?id=50574968)

**「背景：黎曼猜想与 Lean 形式化验证」** 黎曼猜想由伯恩哈德·黎曼于 1859 年提出，涉及素数的分布规律，是数学界最著名的未解难题之一；广义黎曼猜想是其推广形式。Lean 是一种可由计算机逐步检查每个推理步骤的证明语言，因此如果 Lean 形式化文件确实没有额外假设，其正确性理论上可以由机器验证，而不必只依赖人工审阅。根据 Scientific American 等报道，Alpöge 于 11 月 20 日发布了借助 Claude 完成的证明及 Lean 代码，但这些说法目前仍属作者声明，独立验证尚未完成。

**「影响」** 该证明以 Lean 形式化发布，原则上可以由机器检查，而不必只靠人工通读，因此验证的重点会转向 Lean 代码能否通过检查，以及定理陈述和定义是否忠实对应黎曼猜想与 GRH。有评论者引用 MIT 的 Andrew Sutherland 页面，称已有多项检查在进行，但该页面仍在更新，部分检查尚未完成，在专业数学界和形式化社区给出独立结论之前，不宜将其视为已证实。

**「社区讨论」** 评论者 dawdler-purge 引用 Sutherland 的 MIT 页面，认为多种形式化检查已使正确性几乎无疑，但该页面自己注明部分检查仍在进行。另有评论者提到一个据称完全由人类完成的 GRH 证明（Alessandro Masullo 的“匆忙公告”），还有人引用陶哲轩一个月前对 AI 攻克该问题的怀疑态度，说明讨论中同时存在震惊、对时间线的担忧与对验证的期待。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Levent_Alp%C3%B6ge">Levent Alpöge - Wikipedia</a></li>
<li><a href="https://www.scientificamerican.com/article/anthropic-mathematician-claims-to-prove-riemann-hypothesis-most-famous-problem-in-all-of-math/">Anthropic mathematician claims to prove Riemann hypothesis , most...</a></li>

</ul>
</details>

**标签**: `#Riemann hypothesis`, `#Lean formalization`, `#AI mathematics`, `#theorem proving`, `#unverified claim`

---

<a id="item-tech-news-3"></a>
### [Thinking Machines 发布开放权重循环 Transformer 模型 Inkling 2 Mini](https://thinkingmachines.ai/news/inkling-2-mini/) ⭐️ 8.0/10

Thinking Machines 发布了开放权重模型 Inkling 2 Mini。根据 Hacker News 评论,它采用循环\(looped\)Transformer 架构,并且端到端使用 nvfp4 训练。评论者称其基准成绩可与 Qwen3.8-27B 相当,但这只是转述的说法,尚未独立验证。由于未获取到原文内容,以上细节均来自评论,而非官方页面。

hackernews · jasondavies · 11月20日 20:12 · [社区讨论](https://news.ycombinator.com/item?id=50581260)

**「背景:循环 Transformer」** 循环\(looped\)Transformer 让模型重复运行部分层,用同一组参数换取更多计算。据 Thinking Machines 官方介绍,Inkling 2 Mini 会循环其中间层,以便每个 token 推理得更充分,并用更少的 token 得出答案。官方称它是 Inkling 系列中最小的模型,可在笔记本上运行。第三方机构 Artificial Analysis 称其为 26B 总参数、5.4B 激活参数的混合专家\(MoE\)模型,在该机构的智能指数上得分 20。

**「影响」** 对想在本地运行模型的用户来说,早期报告显示它已经可用:在 Ryzen 395 上用 llama.cpp Vulkan 约 27 token/s,但需要合并四个尚未上游的 PR\(32694、32657、32429、32704\);在 32GB 的 M1 Pro 上用 q4 量化约 10 token/s。评论中还提到了 Unsloth 发布的 GGUF 版本,可用于 Ollama 或 llama.cpp。不过,llama.cpp 对该模型的支持仍依赖未合并的 PR,使用前需要留意版本兼容性。

**「社区讨论」** 评论者 montroser 认为,如果基准成绩在真实场景中成立,表现将非常出色;dgacmu 的测试则显示结果不一:Python 写作任务完成得很好,但在识别硬币的任务上输出了大量无关内容,最终失败。另有评论者 lilytweed 预测,开放权重的循环架构会促使更多开放模型跟进,并关注其对安全性与可解释性的影响,不过这只是个人推测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thinkingmachines.ai/news/inkling-2-mini/">Introducing Inkling 2 Mini - Thinking Machines Lab</a></li>
<li><a href="https://thinkingmachines.ai/inkling/">Inkling - Thinking Machines Lab</a></li>
<li><a href="https://artificialanalysis.ai/articles/inkling-2-mini">Thinking Machines has released Inkling 2 Mini, an open ...</a></li>

</ul>
</details>

**标签**: `#open-weights-llm`, `#looped-transformer`, `#local-inference`, `#nvfp4-training`, `#llama.cpp`

---

<a id="item-tech-news-4"></a>
### [陶哲轩博文称无外力欧拉/纳维-斯托克斯奇点与广义黎曼猜想相关，细节未获证实](https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/) ⭐️ 8.0/10

陶哲轩在博客发表了题为《无外力欧拉奇点、无外力纳维-斯托克斯奇点与广义黎曼猜想》的文章，标题把流体方程的奇点问题与广义黎曼猜想联系在一起。但本次未提供正文，具体结论、论证方式和适用范围均无法核实。仅从 Hacker News 评论可知，有人称这是一项借助 AI、用 Lean 形式化验证的成果：证明规模约 1500 万行，两个独立内核据称都接受了它，陶哲轩也被转述称其“似乎用到了朗兰兹纲领和算术几何的全部现代进展”。这些说法均来自评论转述，尚未得到原文或独立来源证实。

hackernews · archon1410 · 11月20日 17:21 · [社区讨论](https://news.ycombinator.com/item?id=50578358)

**「背景」** Euler 与 Navier–Stokes 方程描述流体运动,三维情形下光滑初值是否会在有限时间内形成奇点\(爆破\),是数学中长期未解的难题。广义黎曼猜想\(GRH\)则是数论中的核心猜想。Lean 是一种形式化证明助手,由其内核逐步检查证明。本文所能确认的只有 Tao 博客确有这篇文章\(tool-1-1\),正文未提供;“AI 参与”“Lean 验证”“约 1500 万行”等说法仅来自评论区,尚未证实。

**「影响」** 如果评论所述属实，关键问题将变成：如何确认如此庞大的 Lean 代码所证明的命题确实是预期的数学命题。读者在采信前，应先核对陶哲轩原文、Lean 中的定理陈述及其定义，以及形式化项目的公开仓库和独立复核结果。

**「社区讨论」** 评论者 chunky1994 指出，两个独立内核都接受证明，说明利用内核漏洞通过检查的可能性较低；swingboy 则追问，面对 1500 万行代码，如何确认通过编译的是“正确的命题”而不是被悄悄改弱的陈述。另有评论者表达对职业和科研空间的担忧，softwaredoug 则质疑新的数学抽象从何而来，这些多为个人看法，不是已确认的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://terrytao.wordpress.com/2026/11/20/unforced-euler-singularity-unforced-navier-stokes-singularity-and-the-generalized-riemann-hypothesis/">Unforced Euler singularity , unforced Navier - Stokes singularity...</a></li>

</ul>
</details>

**标签**: `#AI mathematics`, `#formal verification`, `#Lean theorem prover`, `#Riemann Hypothesis`, `#Navier-Stokes`

---

<a id="item-tech-news-5"></a>
### [KVM 漏洞 CVE-2026-99312：AMD 主机内存可被虚拟机读取](https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html) ⭐️ 7.5/10

Linux 内核 KVM 被披露存在漏洞 CVE-2026-99312，仅影响启用嵌套虚拟化的 AMD 主机。据报道，研究人员在 DigitalOcean 上从虚拟机内读取到约 127 GB 的宿主机内存。上游修复已于 11 月 18 日随稳定内核 7.3.5 等版本发布，但 Debian、Ubuntu 等发行版内核尚未修复。来源是对 The Hacker News 报道的简短转述，未提供根因细节和 CVSS 评分。

telegram · zaihuapd · 11月20日 14:23

**「背景：嵌套虚拟化与该漏洞的来源」** 嵌套虚拟化允许虚拟机内部再运行一个虚拟化层，由宿主机上的 KVM 为其模拟虚拟化能力，因此这部分代码在宿主机和客户机之间形成了额外的攻击面。据 The Hacker News 和 DigitalOcean 的说明，这个漏洞源于 KVM 中的一个过期（stale）指针，且相关代码只存在于 KVM 对 AMD 嵌套虚拟化的支持中，所以 Intel 主机不受影响。Terra Security 的分析则称，该问题的根源可追溯到此前的一次安全修复，但搜索摘要没有给出具体细节。

**「影响」** 运行 AMD 平台并启用嵌套虚拟化的 KVM 宿主机，尤其是云服务和多租户环境，应检查自身是否受影响。在发行版内核补丁发布前，可先关闭嵌套虚拟化作为临时缓解措施，之后尽快升级到已修复的内核。依赖 Debian、Ubuntu 内核的用户需关注发行版的安全公告。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/new-linux-kvm-flaw-cve-2026-99312-lets.html">Linux KVM Flaw CVE - 2026 - 99312 Lets Guest VMs Access Host ...</a></li>
<li><a href="https://www.digitalocean.com/blog/cve-2026-99312-kvm-patch">Virtualization , Responsible Disclosure, and CVE - 2026 - 99312</a></li>
<li><a href="https://www.terra.security/blog/kvm-guest-to-host-escape">KVM Guest-to- Host Escape | Terra Security Research</a></li>

</ul>
</details>

**标签**: `#KVM`, `#CVE-2026-99312`, `#virtualization security`, `#AMD`, `#Linux kernel`

---

<a id="item-tech-news-6"></a>
### [Signal 就如何防止移动系统 AI 代理抓取私密应用数据发声](https://signal.org/blog/protecting-your-privacy/) ⭐️ 7.0/10

Signal 发布博文,讨论如何限制移动操作系统中的 AI 代理读取和捕获私密应用中的内容。但本次提供的材料没有博文正文,只有标题、链接和评论,因此具体技术机制、发布的功能、适用系统版本和上线时间都无法核实。评论中提到 Signal 对取得进展“谨慎乐观”,并提到一项“取证调查”,这些说法同样只来自评论转述,未经原文确认。

hackernews · dotcoma · 11月20日 09:42 · [社区讨论](https://news.ycombinator.com/item?id=50572348)

**「背景」** 手机操作系统内置的智能体式 AI\(如 Gemini、Siri\)可以读取屏幕上的内容来了解用户,这意味着即便聊天经过端到端加密,明文在显示时仍可能被系统级 AI 捕获并存储。据 The Verge 报道,Signal 总裁 Meredith Whittaker 称这类功能“削弱了 Signal 独立保证隐私的能力”;Signal 在博客中表示正在限制这些 AI 智能体获取其数据,并呼吁操作系统厂商提供更好的控制手段。具体技术机制在本文提供的原始内容中无法核实。

**「社区讨论」** 有评论者转述 Meredith Whittaker 的访谈称,即使自己没安装 AI 应用,联系人设备上的 AI 应用也可能让聊天内容泄露。另一些评论者主张用户应夺回对操作系统的控制,例如改用 GrapheneOS 或 Linux,而不是只靠应用层防截屏;也有人希望 Signal 公开取证调查结果,供资源较少的开发者参考。还有评论者抱怨防截屏限制影响了正常使用,例如 Windows 上无法截取 Signal 聊天。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://signal.org/blog/protecting-your-privacy/">Signal &gt;&gt; Blog &gt;&gt; Signal is Serious About Protecting Your Privacy</a></li>
<li><a href="https://www.theverge.com/ai-artificial-intelligence/1038390/signal-blocking-ai-agent-screenshots-mobile-app">Signal is blocking Gemini and Siri AI from reading your... | The Verge</a></li>

</ul>
</details>

**标签**: `#AI agents`, `#mobile privacy`, `#Signal`, `#operating systems`, `#data security`

---

<a id="item-tech-news-7"></a>
### [台积电据称暂停接收中国企业 16nm 及以下制程订单](https://appleinsider.com/articles/26/11/20/apple-supplier-tsmc-cuts-off-china-chip-orders-amid-tighter-export-controls) ⭐️ 7.0/10

据 AppleInsider 报道\(经 Telegram 转载\),台积电已通知客户,暂停接收中国公司 16nm 及以下先进制程的订单。按收紧后的美国半导体出口新规,除非事先取得美国出口许可或豁免,否则不得供货。此前台积电可自行评估客户设计是否符合豁免条件,现在必须由客户提前申请。报道称美国获批名单中有苹果、AMD、英伟达,尚无中国公司,台积电表示将遵守新规。以上内容均来自转载的媒体报道,文中没有台积电或美国政府的原始声明。

telegram · zaihuapd · 11月21日 02:01

**「背景」** 美国此前已多次限制先进制程芯片流向中国。据搜索结果引用的路透社 2024 年 11 月报道，美国曾要求台积电停止向中国出口用于 AI 应用的芯片。本次的变化是，原先由台积电自行评估客户设计是否符合豁免条件，现在需客户提前申请美国许可；不过相关细节目前仅见于 AppleInsider 转述，尚无台积电或美国政府的原始文件佐证。

**「影响」** 按报道,中国芯片设计企业短期内只能转向 28nm、40nm 等较旧制程。报道还称,这会使它们无法获得 AI 数据中心所需的高带宽内存,但原文没有解释这一限制的具体机制。需要先申请许可的中国客户,应关注美国批准进展以及台积电后续的正式说明。

<details><summary>参考链接</summary>
<ul>
<li>TSMC has suspended some chip orders amid tighter export controls</li>
<li>U.S. Export Controls and China: Advanced Semiconductors</li>

</ul>
</details>

**标签**: `#TSMC`, `#export controls`, `#semiconductors`, `#China`, `#AI hardware`

---

<a id="item-tech-news-8"></a>
### [Cursor 拟逐步停用中国开源权重模型，Composer 2 基于 Kimi K2.5](https://www.cnbc.com/2026/11/20/cursor-chinese-ai-models-geopolitical-risk.html) ⭐️ 6.5/10

据一条引用 CNBC 的 Telegram 帖子称，被描述为 SpaceX 旗下的 AI 编程平台 Cursor 表示，出于“地缘政治风险”，正在考虑逐步停用中国开发的开源权重模型。帖子称，Cursor 的 Composer 2 编程模型基于月之暗面的 Kimi K2.5 构建。帖子还说，这一表态出自美国众议院国土安全委员会与美中特别委员会的报告；该报告建议推出“美国国家开源权重计划”，并主张在禁止 DeepSeek 进入联邦系统的行政令基础上，禁止联邦系统使用中国开发的 AI 模型。目前信息来自简短转述，没有给出停用时间表、技术细节或直接引语，Cursor 的说法也只是“正在考虑”，尚未确认实际执行。

telegram · zaihuapd · 11月20日 16:13

**「背景」** 开源权重模型公开了训练好的参数,企业可以在其上继续训练或微调,再打包成自己的产品;按报道,Cursor 的 Composer 2 编程模型就是基于月之暗面的 Kimi K2.5 构建的。搜索结果显示,Cursor 向美国众议院国土安全委员会和美中特别委员会表示,将研究逐步停用中国开发的开源权重模型,CNBC 是根据一份众议院报告报道此事的。报告还建议,在已有的禁止 DeepSeek 进入联邦系统的行政令基础上,进一步禁止联邦系统使用中国开发的 AI 模型。目前这只是“考虑”,尚无停用时间表。

**「影响」** 如果 Cursor 付诸实施，Composer 2 所依赖的 Kimi K2.5 基座可能需要替换或重新训练，使用该模型的开发者要留意后续的模型更换与行为变化。不过现有材料没有说明时间安排，也没有说明这一设想是否涉及联邦以外的商业用户，用户暂时只能等待官方进一步说明。

<details><summary>参考链接</summary>
<ul>
<li>Cursor weighs phasing out Chinese AI models: House report - CNBC</li>
<li>Cursor Tells House It May Drop Chinese Open-Weight Models</li>
<li>Cursor considers phasing out Chinese AI models, CNBC reports</li>

</ul>
</details>

**标签**: `#Cursor`, `#open-weight models`, `#AI policy`, `#US-China tech`, `#Kimi K2.5`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [沃什不愿给出利率指引,美联储官员反而发声更多](https://www.cnbc.com/2026/11/20/warsh-fed-forward-guidance-rate-hikes.html) ⭐️ 7.0/10

美联储主席沃什上任约六个月来一直避免暗示利率走向,但其他官员公开发言明显增多,多数人认为应尽快加息。其中理事沃勒提出 12 月可能加息 50 个基点\(0.5 个百分点\);据 CME FedWatch,交易员目前预期 12 月至少加息 25 个基点的概率为 100%。

rss · CNBC Finance · 11月20日 21:10

**「背景」** “前瞻指引”是央行提前向市场透露未来利率可能走向,沃什认为这会束缚决策者;美联储 10 月会议维持利率不变,克利夫兰联储主席哈马克投票反对,主张加息 25 个基点。

**「影响」** 据美国银行经济学家巴韦分析,官员观点分歧又缺少主席的明确指引,可能加大利率市场的波动。

**标签**: `#Federal Reserve`, `#Kevin Warsh`, `#forward guidance`, `#interest rate hikes`, `#FOMC`

---

<a id="item-finance-news-2"></a>
### [美国企业转向净发行股票，市场股票供应增加](https://www.cnbc.com/2026/11/20/equity-issuance-bull-market-problem.html) ⭐️ 6.5/10

据 Acadian Asset Management 的分析，截至上周后期，美国企业净新发行股票已相当于总市值的 3.1%，企业已从回购转向发行股票。本周 Anthropic 以每股 83 美元的价格 IPO，募资 810 亿美元，进一步增加了股票供应。

rss · CNBC Finance · 11月20日 14:15

**「背景」** 过去企业大量回购股票，减少了市场上可交易的股票数量，也会抬高每股收益，一些投资者因此认为这支撑了股价；Acadian 的 Owen Lamont 称，2024 年企业还是净回购方，如今已变为净发行方。

**「潜在影响」** Lamont 和文章认为，股票供应增加可能成为这轮已持续四年的牛市的阻力；但净发行量仍低于科技泡沫和新冠时期的高点，且他也无法排除当前是 AI 泡沫，因此这一影响仍属推测。

**标签**: `#equity issuance`, `#share buybacks`, `#bull market`, `#AI IPOs`, `#market supply`

---