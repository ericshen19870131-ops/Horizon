---
layout: default
title: "Horizon Summary: 2026-11-12 (ZH)"
date: 2026-11-12
lang: zh
---

> 从 56 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [AWS 开源官方本地模拟器 aws-emulator,由大量 AI 智能体用 Rust 编写](#item-tech-news-1) ⭐️ 8.0/10
2. [WSJ 报道称英伟达董事会拟罢免黄仁勋,细节未获证实](#item-tech-news-2) ⭐️ 7.0/10
3. [用电压毛刺绕过熔丝限制，解锁基于 A100 的矿卡](#item-tech-news-3) ⭐️ 7.0/10
4. [Anthropic IPO 路演视频:Claude 跨四大芯片家族训练与部署](#item-tech-news-4) ⭐️ 7.0/10
5. [Hugo van Kemenade 建议用工作流锁文件锁定 GitHub Actions 依赖](#item-tech-news-5) ⭐️ 6.5/10
6. [博文探讨：线性规划能否用于语言模型权重空间编辑](#item-tech-news-6) ⭐️ 6.5/10
7. [The Information 称 Alice Huang 助约 24 万颗受限英伟达芯片入华](#item-tech-news-7) ⭐️ 6.5/10
8. [谷歌推出 Gemini Decisions API，支持多模态封闭式决策](#item-tech-news-8) ⭐️ 6.5/10

**财经新闻**
1. [10 月 CPI 高于预期,美联储官员讨论 12 月加息幅度](#item-finance-news-1) ⭐️ 7.5/10
2. [离岸信托收益征税过渡期结束，累计申报个税超 1600 亿元](#item-finance-news-2) ⭐️ 7.5/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [AWS 开源官方本地模拟器 aws-emulator,由大量 AI 智能体用 Rust 编写](https://github.com/aws/aws-emulator) ⭐️ 8.0/10

AWS 在 GitHub 上发布了开源项目 aws-emulator,用于在本地模拟多种 AWS 服务,以便开发者运行测试而无需调用付费的真实云资源。据 Simon Willison 的转述,该项目用 Rust 编写,由大量智能体完成,前三周提交了 29,684 次;Swami Sivasubramian 在 Werner Vogels 的博客上撰文介绍了其来历。目前在 macOS 和 Windows 上需要借助 Docker 运行。提供的材料只有链接和被截断的评论,因此模拟器覆盖哪些服务、行为与真实 AWS 的一致程度以及后续维护承诺,均无法核实。

hackernews · super\_linear · 11月11日 18:21 · [社区讨论](https://news.ycombinator.com/item?id=50456631)

**「背景：本地云模拟器」** 本地云模拟器是在开发者机器或 CI 中运行的、与 AWS 接口兼容的假服务，让测试代码无需调用真实、收费的云账号即可运行。此前这一领域主要由第三方项目提供，例如 LocalStack，以及据其官网介绍定位为“LocalStack 的直接替代品”的开源项目 Floci（其官网称其免认证令牌、免费）；此次 AWS 自己发布官方版本，因此社区才会讨论它与这些项目的竞争关系和长期维护承诺。

**「影响」** 对在本地或 CI 中测试 AWS 代码的开发者来说,现在多了一个官方出品的替代选择,但不宜用它验证安全相关行为。评论引用的官方安全页面称,不应用它测试 IAM 策略与权限边界、资源策略、KMS 密钥策略、跨账号或跨区域访问等安全控制,并提到它不会拒绝用自身密钥签名的请求。因此,权限逻辑仍需在真实 AWS 环境中验证;另外,macOS 和 Windows 上依赖 Docker,也可能影响把它直接接入现有测试流程。

**「社区讨论」** 评论者 CharlieDigital 表示,由于不清楚 AWS 是否会把它作为正式产品长期维护,他仍倾向于继续使用已经好用的 Floci,并指出 Floci 还支持 GCP 和 Azure。另一位评论者 wg0 认为,没有 AI 和智能体,AWS 很难为如此多的服务做这件事,LocalStack 等同类项目的护城河会因此消失;这只是个人看法,并非已被证实的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/floci-io/floci">GitHub - floci-io/floci: Light, fluffy, and always free - The ...</a></li>
<li><a href="https://floci.io/aws/">floci: Fast, Free AWS Emulator</a></li>

</ul>
</details>

**标签**: `#aws-emulator`, `#local-cloud-development`, `#ai-agents`, `#localstack-alternatives`, `#open-source`

---

<a id="item-tech-news-2"></a>
### [WSJ 报道称英伟达董事会拟罢免黄仁勋,细节未获证实](https://www.wsj.com/business/nvidia-is-preparing-to-oust-nvidia-ceo-jensen-huang-30f421ad) ⭐️ 7.0/10

《华尔街日报》一篇文章的标题称,英伟达正准备罢免首席执行官黄仁勋。该文章在 Hacker News 上获得很高关注。可获取的材料只有标题和付费墙链接,没有正文,因此罢免的原因、时间表、董事会是否已作决定等细节均无法核实。目前只能确认有这样一则报道标题,不能把它当作已经发生的人事变动。

hackernews · jbredeche · 11月11日 22:31 · [社区讨论](https://news.ycombinator.com/item?id=50459703)

**「背景」** 这条消息的原始来源是被付费墙挡住的《华尔街日报》报道，本次提供的原文没有正文。据 CNBC、雅虎财经和 Techmeme 对该报道的转述，英伟达董事会已启动独立调查，并聘请 Wachtell, Lipton, Rosen &amp; Katz 律所核查涉及间谍的指控，报道还称黄仁勋涉及两起婚外情，其中一起对象被怀疑是中国间谍。这些细节目前只是媒体转述和评论区的说法，英伟达是否真的会罢免黄仁勋，现有材料无法确认。

**「社区讨论」** 评论区的主要分歧在于,若传闻属实,哪些指控才构成罢免理由。有评论者认为,涉及个人私生活的指控本身不算关键,而所谓向中国出口合规的问题才是重点,另一位评论者也回顾了英伟达此前对 GPU 走私调查的强烈反应。这些说法都只是评论者的个人看法或转述,文中没有证据支持。另有评论者强调黄仁勋对英伟达推进 CUDA 和深度学习的作用,认为他对公司和行业都很关键。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/11/nvidia-jensen-huang-affair-employee.html">Nvidia prepares to oust Jensen Huang , WSJ reports — stock sinks</a></li>
<li><a href="https://finance.yahoo.com/technology/live/nvidia-live-updates-nvidia-stock-tanks-in-after-hours-after-allegations-of-a-second-affair-surface-222438011.html">Nvidia live updates: Stock tanks after new affair allegations , board ...</a></li>
<li><a href="https://www.techmeme.com/261111/p44">Sources: Nvidia &#x27;s board is preparing to oust Jensen Huang and is...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#AI hardware`, `#export controls`

---

<a id="item-tech-news-3"></a>
### [用电压毛刺绕过熔丝限制，解锁基于 A100 的矿卡](https://blog.kate.land/posts/using-voltage-glitching-to-unlock-the-a100/) ⭐️ 7.0/10

一篇博客介绍了作者用电压毛刺（voltage glitching）攻击，绕过一张基于 NVIDIA A100 的矿卡上由熔丝设定的限制，以解锁芯片的完整能力和显存。由于未提供原文正文，具体步骤、成功率和可复现性无法确认。从评论推断，涉及的是 CMP 系列矿卡，作者称针对 8GB 型号；这些细节来自评论，并非原文核实。

hackernews · lae · 11月11日 10:48 · [社区讨论](https://news.ycombinator.com/item?id=50451903)

**「背景：同一颗 GA100 芯片，靠熔丝区分产品」** 据转述该文章的二手资料,NVIDIA 的 GA100 芯片既用于数据中心的 A100,也用于低端挖矿卡 CMP 170HX,两者的功能差异由芯片内的熔丝设定。电压毛刺\(电压故障注入\)是在芯片运行时短暂扰动供电电压,使内部逻辑出错,作者据称借此操控熔丝控制器、写入原本被锁定的熔丝。原文正文未能获取,以上细节来自对原文的转述和摘要,尚未经过独立验证。

**「影响」** 对持有这类矿卡的玩家来说，这可能提供一条解锁被屏蔽显存与算力的硬件途径，但评论者指出该方法涉及熔丝，比纯软件方式风险更高。尝试前需要自行评估损坏硬件的风险，并等待更完整的复现细节。

**「社区讨论」** 评论者 amelius 质疑，这些芯片被熔丝限制，可能是因为 A100 存在较多制造缺陷、才被降级为矿卡，也就是硅片分级（binning）问题，解锁后未必稳定；这只是推测，并非已证实的事实。另一位评论者 myself248 建议用带独立供电的外置 PCIe 转接板代替让主机进入 ACPI S3 休眠，使主机持续运行、只对目标卡反复断电，从而加快流程；notenchange 则表示自己仍在尝试用软件方式解锁 CMP 170HX，对烧熔丝路线的风险有顾虑。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.kate.land/posts/using-voltage-glitching-to-unlock-the-a100/">Using voltage glitching to unleash the A100 in my mining card</a></li>
<li><a href="https://sitem.co/public/summary/7050/voltage-glitching-unlocks-nvidia-ga100-die-transforming-cmp-170hx-mining-cards-into-high-performance-a100-equivalents">Voltage Glitching Unlocks NVIDIA GA100 Die: Transforming CMP ...</a></li>

</ul>
</details>

**标签**: `#voltage-glitching`, `#NVIDIA A100`, `#hardware-hacking`, `#GPU`, `#mining-card`

---

<a id="item-tech-news-4"></a>
### [Anthropic IPO 路演视频:Claude 跨四大芯片家族训练与部署](https://simonwillison.net/2026/Nov/11/anthropic-ipo-roadshow/) ⭐️ 7.0/10

Simon Willison 指出,Anthropic 于前一天开始 IPO 路演,其路演视频披露了一些此前未公开的业务信息。联合创始人 Tom Brown 在“算力思路”部分称,Anthropic 目前在 AWS Trainium、Google TPU、NVIDIA GPU 和 AMD GPU 四大芯片家族上训练并提供 Claude 服务,这源于早期押注多芯片策略。他还称,今年首次接入 AMD GPU 时,Mythos 在约三天内、几乎无需人工干预就让 Claude 在 AMD 上跑通,并移植或编写了几乎全部内核;过去这类工作需要数十名工程师花数月。这些均为公司在路演中的自述,未见独立验证;Anthropic 也未提供官方文字稿,Willison 用 MacWhisper 自行提取了转录稿。

rss · Simon Willison · 11月11日 15:11

**「背景」** 路演是公司在股票上市前向潜在投资者介绍业务的环节。Anthropic 官网称已启动其 A 类普通股拟议首次公开发行的路演（tool-2-1）；第三方博客称，修订后的 S-1 文件于 11 月 10 日提交，定价区间为每股 70 至 78 美元，发行 8.25 亿股，这些数字未经本文来源核实（tool-2-3）。Tom Brown 所说的“多芯片策略”，难点在于每种芯片都需要各自定制的软件栈和推理栈，开发成本高、难度大；Simon Willison 指出，Anthropic 去年 9 月发布的三起问题事后分析中，已有只影响 TPU 部署的故障，透露过这一做法的迹象。

**「影响」** 如果这些说法属实,多芯片适配的人力成本可能显著下降,AI 模型对单一芯片供应商的依赖也会减弱。不过目前只有公司自述,尚无独立数据,投资者和基础设施从业者在评估其算力优势时应以后续披露的正式文件为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/roadshow-launch">Anthropic launches roadshow for proposed initial public ...</a></li>
<li><a href="https://cellcog.ai/blog/anthropic-ipo-price-range-roadshow/">Anthropic IPO: $70 to $78 a Share, Roadshow Launched</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#IPO`, `#AI infrastructure`, `#multi-chip strategy`, `#Claude`

---

<a id="item-tech-news-5"></a>
### [Hugo van Kemenade 建议用工作流锁文件锁定 GitHub Actions 依赖](https://hugovk.dev/blog/2026/lock-github-actions/) ⭐️ 6.5/10

博客文章《Lock Your GitHub Actions》建议使用 GitHub Actions 的工作流锁文件来固定依赖,以降低供应链风险。本次仅获得标题、链接和评论,没有文章正文,因此无法确认文章的具体操作步骤和细节。评论中 zizmor 维护者 woodruffw 指出,当前版本的锁文件只锁定普通 action 调用;可复用工作流仍需手动用哈希固定,组合 action 则只能通过调用它的工作流间接锁定。

hackernews · gslin · 11月11日 22:16 · [社区讨论](https://news.ycombinator.com/item?id=50459485)

**「背景：工作流依赖锁文件」** GitHub Actions 工作流通常通过标签或分支引用第三方 action，而这些引用可能被移动，因此一旦上游被入侵，就可能带来供应链风险。据 GitHub 2026 年 10 月 14 日的更新日志，工作流锁文件已进入公开预览：接入后的工作流必须在锁文件中为其依赖提供条目，并运行其中记录的提交，即使标签或分支已被移动。GitHub 文档说明，锁文件会为工作流依赖的每个 action（含传递依赖）固定提交 SHA，但不会固定对可复用工作流（jobs.&lt;id&gt;.uses）的调用，这也是评论中提到的主要限制。

**「影响」** 使用 GitHub Actions 的维护者启用锁文件时,不应认为依赖已全部锁定。按评论所述,工作流中调用的可复用工作流仍需手动固定到提交哈希,同时还要检查组合 action 是否通过各调用方得到了锁定。

**「社区讨论」** woodruffw 补充了锁文件的覆盖范围限制;Already\_\_Taken 则认为固定哈希只是把信任从“仓库所有者不移动标签”转移到“合并者确认该提交确为目标仓库的正式发布”,因为 GitHub 上所有 fork 共享同一提交空间,哈希无法区分上游版本和 fork 提交,他主张市场发布应强制使用不可变标签。另有评论者主张尽量避免使用第三方 action,或把简单的 action 直接复制进配置自行掌控,这些只是个人看法,并非定论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.github.com/en/actions/concepts/security/workflow-dependency-lockfiles">Workflow dependency lockfiles - GitHub Docs</a></li>
<li><a href="https://github.blog/changelog/2026-10-14-github-actions-workflow-lockfiles-in-public-preview/">GitHub Actions workflow lockfiles in public preview</a></li>

</ul>
</details>

**标签**: `#github-actions`, `#supply-chain-security`, `#ci-cd`, `#dependency-pinning`, `#devsecops`

---

<a id="item-tech-news-6"></a>
### [博文探讨：线性规划能否用于语言模型权重空间编辑](https://nathan.rs/posts/weight-space-lp/) ⭐️ 6.5/10

一篇博客文章探讨线性规划（LP）能否对语言模型做定向的权重空间编辑，例如在把线性约束作为“保留”条件的同时，消除某一种行为。本次未能获取文章正文，只有标题和评论，因此具体方法、实验规模、模型和实测结果都无法核实。从评论看，文章还与“Astra”的权重编辑结果有关，但该结果的细节同样没有提供。目前只能把它当作一项探索性分析，而不是已验证的成果。

hackernews · emschwartz · 11月11日 12:30 · [社区讨论](https://news.ycombinator.com/item?id=50452655)

**「背景:Astra 的权重编辑实验」** 这篇博文呼应的是 MIT CSAIL 四位研究者在 2026 年 11 月 2 日发表的“权重空间编程”\(Weight-Space Programming\)文章。据二手报道,该文称 GPT-6 Astra 未经训练、直接编辑 Qwen 3.5-0.8B 的权重,使 MATH-500 得分从 7.9% 提高到 48.1%。这些数字来自第三方转述,本文未能核实原文;这篇线性规划博文则探讨,若把“消除某行为、保留另一些行为”写成线性约束,求解器能否完成类似的定向权重编辑。

**「社区讨论」** 评论者 jsw97 认为，文章的意义未必是 LP 能取代 Astra 的工作，而是在给出“消除某行为、保留另一行为”这类线性约束的引导后，求解器可能更有效；这属于对文章意图的推测。其他评论者提出了延伸设想：dansitu 认为这种方法应该在训练中通过正则化实现，mirekrusin 建议用它做权重空间蒸馏，bcmyguest 则关心它在更大模型和多变量奖励下能走多远，这些都只是意见，没有已证实的结果支持。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/weight-space-programming-gpt-6-astra-edits-qwen3-5-0-8b-weights-math-7-9-to-48-1-mit-csail-2026">GPT-6 Astra Edits Qwen Weights : MATH -500 7.9% to... | explainx. ai</a></li>
<li><a href="https://cryptobriefing.com/gpt-6-astra-edits-qwen-weights-math/">GPT-6 Astra reportedly boosts Qwen 3.5-0.8B math up to sixfold by...</a></li>

</ul>
</details>

**标签**: `#linear-programming`, `#model-editing`, `#weight-space`, `#LLM-interpretability`, `#optimization`

---

<a id="item-tech-news-7"></a>
### [The Information 称 Alice Huang 助约 24 万颗受限英伟达芯片入华](https://www.tomshardware.com/tech-industry/policy/alice-huang-reportedly-instrumental-in-securing-over-usd7-5-billion-of-nvidia-ai-gpu-imports-during-three-year-relationship-with-jensen-huang-helped-move-240-000-banned-chips-into-china-mostly-h100-and-h200) ⭐️ 6.5/10

据 Telegram 频道转述 Tom&\#x27;s Hardware 对 The Information 调查的报道，Alice Huang（中文名黄乐）借助与英伟达 CEO 黄仁勋的关系，协助约 24 万颗被禁运的英伟达芯片进入中国，其中多为 H100 和 H200，涉及的 AI GPU 进口金额约 75 亿美元。报道点名的公司包括上海世纪利通和新加坡的 Megaspeed。这些内容均为媒体调查中的指称，转述文本没有提供具体证据、交易时间线或当事方回应，无法据此核实。

telegram · zaihuapd · 11月11日 14:41

**「背景」** H100、H200 等高端 AI 芯片属于美国出口管制限制对华销售的产品。据路透社转述 The Information 的报道，当这些受限芯片订单受阻时，Alice Huang 利用与英伟达的关系拿到货源，协助约 24 万颗 H100、H200 及部分 A100 芯片进入中国。The Information 还称，英伟达因此面临关于 CEO 私人关系和芯片走私指控的调查，不过这些仍是媒体报道中的指控，本文所引材料并未提供独立核实。

**「影响」** 如果上述指称属实，将直接考验美国对 H100、H200 等高端 AI 芯片的出口管制执行，尤其是经第三地公司转运这一环节。目前证据有限，应等待监管机构、英伟达或相关公司的正式回应，再判断是否会带来调查或合规要求的变化。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theinformation.com/articles/jensen-huangs-yearslong-ties-alice-huang-enabled-nvidia-chip-sales-china">How Jensen Huang’s Yearslong Ties to Alice Huang Enabled $7 ...</a></li>
<li><a href="https://www.reuters.com/world/china/nvidia-ceos-affair-aided-75-billion-chip-shipments-china-information-reports-2026-11-10/">Nvidia faces deepening scrutiny over China chip ties, CEO ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#AI export controls`, `#GPU smuggling`, `#China AI hardware`, `#H100/H200`

---

<a id="item-tech-news-8"></a>
### [谷歌推出 Gemini Decisions API，支持多模态封闭式决策](https://blog.google/innovation-and-ai/technology/developers-tools/gemini-decisions-api/) ⭐️ 6.5/10

谷歌发布基于新模型 Gemini Decision 1 的 Gemini Decisions API，面向工具选择、策略检查、模型路由等封闭式决策，现已在 Google AI Studio 提供。它支持文本、图像、音频、视频和 PDF 输入，单次最多可对 1000 个问题打分，返回概率与置信度，谷歌称端到端延迟约 150-250 毫秒。定价为每百万输入 token 0.10 美元、输出免费；“比 Gemini 3.5 Flash-Lite 方案便宜近 5 倍”是厂商说法，来源中没有独立基准验证。Simon Willison 的测试显示，它支持是非、选择和评分量表三类问题；对一段视频的是非题，返回的是约 0.05、0.92 这样的非极端概率，而不是 1.0 或 0.0。

telegram · zaihuapd · 11月12日 00:28

**「背景：决策模型这一类别」** “决策模型”不生成长文本，只针对是/否、选择、按量表打分等封闭式问题，快速返回概率或分数，适合路由、工具选择和策略检查。据 Simon Willison 的转述，这一类别此前已有 Jev 和 OpenAI 的决策模型，Jev 只支持文本和 JSON，OpenAI 支持文本和图像。Gemini Decision 1 的区别在于输入范围，据称覆盖文本、图像、音频、视频和 PDF，其问题类型与 Jev 几乎相同。

**「影响」** 对需要在流水线中批量做分类、路由或合规判断的开发者，它提供了可直接处理音频、视频和 PDF 的选择。按 Simon Willison 的比较，Jev 仅支持文本和 JSON，OpenAI 的决策模型支持文本和图像，而 Gemini 的 0.10 美元定价高于 Jev 的 4.2 美分，因此是否值得用，取决于业务是否真的需要多模态输入。

**「社区讨论」** Hacker News 评论者 waximabbax 认为它比同类决策模型贵，但音频和视频输入在特定场景下很有价值；theanonymousone 则称自己用过的最好模型之一是 respan/span-02，因此对这次发布仍持乐观态度，尽管成本偏高。另有评论者 eminence32 提出疑问：这类模型究竟如何计算概率，讨论中没有给出答案。

**标签**: `#Gemini API`, `#Google AI Studio`, `#model routing`, `#multimodal AI`, `#LLM pricing`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [10 月 CPI 高于预期,美联储官员讨论 12 月加息幅度](https://www.cnbc.com/2026/11/11/goolsbee-october-inflation-fed-rates-disturbing-distressing.html) ⭐️ 7.5/10

美国 10 月消费者价格指数\(CPI\)按季节调整后环比上涨 0.4%,高于经济学家预期,芝加哥联储主席古尔斯比称这份报告“近乎令人不安”。据 CME FedWatch,期货市场目前完全预期美联储 12 月加息,加息半个百分点的概率为 15%。

rss · CNBC Finance · 11月11日 16:49

**「背景」** 美联储 9 月加息四分之一个百分点至 3.75%-4%,10 月维持利率不变;这是 CPI 连续第三个月涨幅偏大,而美联储通常每次只调整四分之一个百分点。

**「影响」** 若通胀持续偏高、美联储加快加息,借款人和企业的融资成本可能面临更大上行压力,不过官员内部对加息节奏尚有分歧。

**标签**: `#Federal Reserve`, `#CPI inflation`, `#interest rate hikes`, `#FOMC`, `#fed funds futures`

---

<a id="item-finance-news-2"></a>
### [离岸信托收益征税过渡期结束，累计申报个税超 1600 亿元](https://www.news.cn/20261111/9bcce99c779b4a6197ff45bbbc3e4c50/c.html) ⭐️ 7.5/10

税务总局 11 月 11 日表示，离岸信托收益征税的 90 天过渡期已结束，累计申报个人所得税超 1600 亿元，其中 10 月当月入库超 1200 亿元。税务部门称，10 月全国个人所得税收入因此增长近 90%（原文未说明对比基数）。

telegram · zaihuapd · 11月11日 10:35

**「背景」** 2026 年 7 月 24 日，财政部、税务总局发布 2026 年第 21 号公告，明确离岸信托（把资产放入境外信托、由受托人管理的安排）收益的个人所得税征管规则，并规定 90 天过渡期内主动申报缴税的不加收滞纳金，期限至 10 月 22 日。

**「影响」** 按税务部门说法，过渡期内申报缴税不加收滞纳金，此后未主动申报或申报不实的纳税人将被督促补缴、加收滞纳金，仍不改正的依法立案稽查。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.iplc.best/posts/9290">iplc.best/posts/9290</a></li>
<li><a href="https://news.creaders.net/china/2026/10/20/3060337.html">截止前三 天 ，北京突然又打了6 个 补丁！ -中国瞭望-万维读者网（电脑版）</a></li>

</ul>
</details>

**标签**: `#离岸信托`, `#个人所得税`, `#税务总局`, `#税收征管`, `#财政收入`

---