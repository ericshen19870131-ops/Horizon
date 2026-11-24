---
layout: default
title: "Horizon Summary: 2026-11-24 (ZH)"
date: 2026-11-24
lang: zh
---

> 从 41 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Anthropic 发布 AI 撰写的 VP≠VNP 证明及 Lean 4 形式化](#item-tech-news-1) ⭐️ 8.5/10
2. [英伟达董事会恢复黄仁勋 CEO 职务](#item-tech-news-2) ⭐️ 8.0/10
3. [Ladybird 浏览器发布首个 Alpha 版，支持 macOS 与 Linux](#item-tech-news-3) ⭐️ 8.0/10
4. [智谱 GLM-5.4 发布：首个循环 Transformer 编程模型](#item-tech-news-4) ⭐️ 7.5/10
5. [NariQ:Qwen3.8-27B 低比特 GGUF 量化,自称约 10 GB 达 BF16 水平](#item-tech-news-5) ⭐️ 7.0/10
6. [Stalwart 宣称已可作为 Microsoft Exchange 的直接替代品](#item-tech-news-6) ⭐️ 6.5/10

**财经新闻**
1. [英伟达董事会恢复黄仁勋 CEO 职务](#item-finance-news-1) ⭐️ 8.0/10
2. [纽约联储威廉姆斯：为抑制通胀，未来可能逐步加息](#item-finance-news-2) ⭐️ 7.0/10
3. [英伟达恢复黄仁勋 CEO 职务，美股反弹但分歧仍在](#item-finance-news-3) ⭐️ 7.0/10
4. [AI 股抛售拖累 DeepSeek 等中国 AI 公司上市计划](#item-finance-news-4) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Anthropic 发布 AI 撰写的 VP≠VNP 证明及 Lean 4 形式化](https://github.com/anthropics/formal-math/tree/main/vp-vnp) ⭐️ 8.5/10

Anthropic 在 GitHub 仓库 anthropics/formal-math 中公开了论文《VP ≠ VNP over every field》及配套 Lean 4 形式化证明。据转载信息，仓库称结果由内部研究用 Claude 模型发现，论文和代码均由 AI 撰写。论文给出哈密顿圈多项式的超多项式算术电路下界，并据此推出 VP 是 VNP 的真子类；若成立，将解决 Valiant 1979 年的代数复杂度猜想，但它只涉及算术电路，与 P 对 NP 无直接关系。仓库称，除预留文件外没有 sorry，并通过三条标准公理审计和独立内核 nanoda 复核；不过目前尚无人类数学家通读全文，附录 Q 也列出了形式化陈述与声称命题之间的出入。这些都是作者一方的说法，结论尚未得到独立专家确认。

hackernews · mikeryan52 · 11月23日 22:09 · [社区讨论](https://news.ycombinator.com/item?id=50620102)

**「背景：VP 与 VNP 是什么」** VP 指可由多项式规模算术电路计算的多项式族，VNP 则是可表示为 VP 多项式指数项求和的多项式族，哈密顿圈多项式和积和式（permanent）都属于 VNP。Valiant 在 1979 年提出猜想：VP 是 VNP 的真子类。这被视为 P 与 NP 问题在代数计算模型中的类比，但它只涉及算术电路，证明它并不能直接解决 P 与 NP。

**「影响」** Lean 能检查证明是否严密，却无法确认形式化陈述与论文声称的命题一致，因此关键检查点是附录 Q 所列出入以及 Lean 中各项定义是否忠实。在专家完成这项审阅前，不宜把“VP≠VNP 已被证明”当作既成事实，只能视为待验证的声明。

**「社区讨论」** 评论者 fons 称自己重新运行了检查，证明这些定理蕴含对声称命题的“盲”重述，并给出了独立仓库，这是目前唯一提到的外部核对，但不等于专家审阅。amichail 则引用论文原文指出，作者尚未分析该结果与相对化、代数化障碍的关系；其余评论多为对 AI 数学能力和公司竞争的看法，并非对证明本身的检验。

**标签**: `#algebraic-complexity`, `#VP-vs-VNP`, `#formal-verification`, `#AI-for-mathematics`, `#complexity-theory`

---

<a id="item-tech-news-2"></a>
### [英伟达董事会恢复黄仁勋 CEO 职务](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo.html) ⭐️ 8.0/10

英伟达董事会宣布恢复黄仁勋的首席执行官职务，距他被迫离任不到两周。评论区引用的董事会声明称，董事会在决策过程中“收到了美国政府高层的意见”，并据此确信黄仁勋复职“不构成国家安全风险”。所提供的材料只有链接和评论摘录，没有文章正文，因此当初罢免的具体原因、指控内容和董事会的完整理由均未得到证实。“表决完全一致”“美国司法部表示不会起诉”等说法也只来自评论者。

hackernews · jaz · 11月23日 14:00 · [社区讨论](https://news.ycombinator.com/item?id=50611576)

**「背景:罢免与复职的经过」** 英伟达官网公告称,黄仁勋即日起恢复总裁、首席执行官和董事会成员的职务。福克斯新闻报道称,此事源于他与一名涉嫌为中国从事间谍活动的女子的关系,董事会此次是在听取美国政府高级官员的意见后,确认其复职不构成国家安全风险。美联社报道称,董事会在数日前还拒绝了他提出的回归请求,这次是出人意料的转向。需要注意,原始来源没有说明罢免的具体理由,上述起因出自媒体报道,尚未得到英伟达公告的证实。

**「社区讨论」** 评论者的看法不一。icyfox 称自己与英伟达员工交流过，认为特拉华州的 Caremark 判例对董事责任的门槛很高，加上司法部不起诉的说法，董事个人可能免责。015UUZn8aEvW 则认为这与 2023 年 OpenAI 事件类似：公司名义上的治理结构未必就是实际的治理结构。apexalpha 批评美国一边迫使 ASML 和日本芯片企业配合对华制裁，一边对英伟达网开一面；x313 则认为没有证据表明英伟达有违法行为。这些都是评论者的观点，不是已核实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nvidianews.nvidia.com/news/nvidia-board-reinstates-jensen-huang-as-president-ceo-and-board-director">NVIDIA Board Reinstates Jensen Huang as President, CEO and...</a></li>
<li><a href="https://www.foxnews.com/live-news/ai-news-tech-markets-nvidia-11-23-26">Jensen Huang reinstated as Nvidia CEO after security review</a></li>
<li><a href="https://www.wral.com/news/ap/39d4b-nvidia-board-unanimously-reinstates-jensen-huang-as-ceo/">Stocks soaring after Nvidia board reinstates Jensen Huang as CEO</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#export controls`, `#AI hardware industry`

---

<a id="item-tech-news-3"></a>
### [Ladybird 浏览器发布首个 Alpha 版，支持 macOS 与 Linux](https://ladybird.org/posts/alpha/) ⭐️ 8.0/10

Ladybird 项目发布了首个 alpha 版本，用户现在可以在 macOS 和 Linux 上直接安装，无需自行编译。Ladybird 自行实现了 HTML 解析、CSS、布局、JavaScript 和 WebAssembly 等核心组件，同时仍使用 HarfBuzz、Skia、ffmpeg 和 SQLite 等外部库。据其 10 月月报，Ladybird 在 web-platform-tests（约 225 万个子测试）上通过 2,184,722 项，高于 Safari 的 2,172,990 项，低于 Firefox 和 Chrome；这是项目自己公布的数据，月报称大部分增长来自用 AI 编程代理在 5 天内集中补全功能。Andreas Kling 在公告中明确说明，alpha 版有些网站无法使用，也会崩溃；作者 Simon Willison 的试用中，除 Datasette Lite 因 Service Worker 的 \`startMessages\` 未实现而失败外，其余测试页面（包括 ffmpeg 与 Pyodide 的 WebAssembly 应用）均正常运行。

hackernews · janvdberg · 11月23日 16:13 · [社区讨论](https://news.ycombinator.com/item?id=50614249)

**「背景：从头自研的浏览器引擎」** Ladybird 源自 SerenityOS 项目，目标是不依赖 Chromium、WebKit 或 Gecko，自行实现 HTML 解析、CSS、布局、JavaScript 乃至 WebAssembly。它仍使用 HarfBuzz（文本整形）、Skia（2D 图形）、ffmpeg（视频）和 SQLite 等外部组件。在此之前，用户只能自行编译 Ladybird，这次 alpha 才首次提供 macOS 和 Linux 的安装包。衡量其兼容性的常用指标是 web-platform-tests（WPT）测试套件，据 10 月月报，Ladybird 在该套件约 225 万个子测试上的通过数已超过 Safari。

**「影响」** 对想试用的用户和网站开发者来说，现在可以直接安装 Ladybird 测试兼容性，并通过浏览器内置功能提交页面损坏和崩溃报告。不过它仍是 alpha，Service Worker 等功能尚不完整，依赖这些功能的 Web 应用可能无法运行，不宜当作主力浏览器处理敏感任务。

**「社区讨论」** 多位评论者称试用体验良好：freakynit 测试了许多网站，称渲染全部正确，只是滚动略有卡顿；alentred 说 Proxmox 的 noVNC 界面甚至比 Firefox 更流畅。也有人表达了其他关切：kvuj 认为改用 SQLite、Skia 等成熟库大幅改善了浏览器，但怀念早期 SerenityOS 的自研精神；drnick1 则希望 Ladybird 将来认真应对浏览器指纹问题。

**标签**: `#Ladybird`, `#web browsers`, `#browser engine`, `#open source`, `#alpha release`

---

<a id="item-tech-news-4"></a>
### [智谱 GLM-5.4 发布：首个循环 Transformer 编程模型](https://z.ai/blog/glm-5.4) ⭐️ 7.5/10

Z.ai（智谱）发布 GLM-5.4，称其为公司首个采用循环 Transformer（Loop Transformer）架构的模型，面向通用编程场景。官方的说法是：一组权重共享的层在一次前向传播中重复迭代，不断精炼上一轮的隐藏状态，从而在不增加参数量的前提下获得更深的网络。目前模型尚未开放权重，也不能通过 OpenRouter 或常规 Z.ai API 访问，只能订阅其 Coding Plan 并使用兼容 OpenAI Responses API 的接口（https://api.z.ai/api/v1）调用。来源材料未提供基准测试成绩或模型规模，相对 GLM-5.3 的实际提升尚无法确认；Simon Willison 的“骑自行车的鹈鹕”SVG 测试显示 5.4 与 5.3 在低、高、最大三档推理强度下质量相近，这只是个人的非正式测试。

hackernews · foohis · 11月23日 10:06 · [社区讨论](https://news.ycombinator.com/item?id=50609685)

**「背景:循环 Transformer 是什么」** 标准 Transformer 在一次前向传播中,每一层只运行一次;循环\(Loop\)Transformer 则让一组共享权重的层重复迭代多次,不断精修上一轮的隐藏状态,从而在不增加参数量的前提下获得更深的计算深度。按 Z.ai 的开发者文档,GLM-5.4 把 GLM-5 基座模型的 28 层复用了两轮迭代;这是厂商自述,尚无独立验证。Simon Willison 还提到,Thinking Machines Lab 在 11 月 20 日发布的 Inkling 2 Mini 同样采用循环结构\(中间层对每个 token 运行三次\),说明这一思路最近开始在生产级模型中出现。

**「对开发者的影响」** 想试用 GLM-5.4 的开发者目前必须订阅 Z.ai 的 Coding Plan：该模型不在普通 API 套餐和 OpenRouter 上提供，也没有开放权重。据 Simon Willison 的实测，Coding Plan 的密钥可用于同一个 OpenAI 兼容的 Responses API（api.z.ai/api/v1），他自己的 llm-glm 插件也能调用新模型；而现有的 llm-zai 插件暂不支持。他的“骑自行车的鹈鹕”测试中，5.4 与 5.3 的输出质量相近，评论中也有人反映推理冗长、完成时间偏长。因此在没有基准测试数据之前，现有 GLM 用户不宜只因架构更新就迁移，应先用自己的编码任务测量质量和耗时。

**「社区讨论」** 评论者 HarHarVeryFunny 称赞智谱公开技术细节，认为循环 Transformer 是值得探索的方向，不过仍有问题待解决。另一位评论者 lnenad 则反映，国产模型常有“马拉松式思考”，即便面对简单任务也反复自我怀疑，完成时间明显长于前沿模型，并推测这是它们在基准上接近前沿模型的原因，但这只是个人推测和使用感受。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.z.ai/guides/llm/glm-5.4">GLM-5.4 - Overview - Z.AI DEVELOPER DOCUMENT</a></li>

</ul>
</details>

**标签**: `#GLM-5.4`, `#loop transformer`, `#coding LLM`, `#Zhipu AI`, `#model architecture`

---

<a id="item-tech-news-5"></a>
### [NariQ:Qwen3.8-27B 低比特 GGUF 量化,自称约 10 GB 达 BF16 水平](https://huggingface.co/nari-labs/Qwen3.8-27B-NariQ-GGUF) ⭐️ 7.0/10

Nari Labs 发布了 NariQ,这是 Qwen3.8-27B 的 3 比特及以下 GGUF 量化版本。官方称,3-bit 版本文件约 10 GB,在智能体、数学、多语言和图像理解任务上接近 BF16。其自报成绩\(BF16 / 3-bit / 2.5-bit / 2-bit\)包括:DeepSWE 39.8 / 41.0 / 41.9 / 28.6,Terminal-Bench 2.1 为 62.6 / 63.8 / 60.2 / 52.4,AIME 25+26 为 97.7 / 98.3 / 96.5 / 86.0。2-bit 版本在多数测试中明显下降。运行这些文件目前需要 Nari Labs 自己的 llama.cpp 分支\(nari-llama.cpp\);官方称在 RTX PRO 6000 上解码速度与其他量化版本相当,而评论引用的说明显示,在 18 GB 的 M3 Pro\(Metal\)上 3.0bpw 文件解码仅约 3.8 tok/s。以上数据均为官方自报,尚无独立验证。

hackernews · toebee · 11月23日 13:42 · [社区讨论](https://news.ycombinator.com/item?id=50611402)

**「背景」** 量化是把模型权重从 BF16 压缩到更低比特的做法,用来缩小文件体积、降低显存占用,但比特越低,越容易损失长程推理和智能体任务的表现。据 Hugging Face 模型页的镜像说明,NariQ 是基于“网格编码”\(trellis-coded\)的训练后量化\(PTQ\),校准数据取自真实的编程智能体轨迹,并以可在单张 GPU 上运行的布局存储;运行需要 Nari Labs 自己的 llama.cpp 分支。

**「影响」** 想在本地运行 27B 模型的用户,可以在 3-bit 约 10 GB 的文件上试用 NariQ,但必须编译并使用 Nari Labs 的 llama.cpp 分支,无法直接用于上游 llama.cpp。Apple Silicon 用户还要面对很慢的 Metal 解码速度,因此应先用自己的工作负载验证,再决定是否采用。

**「社区讨论」** rao-v 一直怀疑高算力 QAT 式量化会过拟合基准,但认为该项目覆盖了多种长程任务并使用了留出\(held out\)测试,检查比较扎实;WithinReason 则认为图表里的大部分提升来自测试框架\(harness\)的差异,而非模型本身。Retro\_Dev 追问压缩后究竟丢失了哪些信息,指出基准不可能涵盖训练数据的全部内容。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ai.atomgit.com/hf_mirrors/nari-labs/Qwen3.8-27B-NariQ-GGUF">nari-labs/Qwen3.8-27B-NariQ-GGUF - AtomGit</a></li>

</ul>
</details>

**标签**: `#quantization`, `#local-llm`, `#llama.cpp`, `#Qwen`, `#model-compression`

---

<a id="item-tech-news-6"></a>
### [Stalwart 宣称已可作为 Microsoft Exchange 的直接替代品](https://stalw.art/blog/microsoft-exchange-replacement/) ⭐️ 6.5/10

开源邮件服务器 Stalwart 发布博文,宣称自己现在可以作为 Microsoft Exchange 的“drop-in replacement”\(即插即用式替代品\)。由于未提供原文内容,具体支持哪些协议\(如 MAPI、EWS\)、兼容到什么程度、适用哪些版本和客户端,均无法核实;目前只能确认这是厂商自己的说法,不是已验证的兼容性结果。

hackernews · shaunpud · 11月23日 22:32 · [社区讨论](https://news.ycombinator.com/item?id=50620349)

**「背景」** Stalwart 是用 Rust 编写的开源邮件与协作服务器。Exchange 长期是企业邮件服务器的默认选择,Outlook 则是配套客户端。据 Stalwart 博客和媒体报道,1.2.0 版本新增了 Exchange 客户端使用的协议,包括 MAPI over HTTP、Exchange Web Services\(EWS\)和 Exchange ActiveSync。报道还提到,Exchange Online 的 EWS 将于 2027 年 4 月完全终止,新版 Outlook for Windows 只能通过微软云使用。这些背景有助于理解评论区对“drop-in replacement”说法的质疑。

**「影响」** 对考虑从 Exchange 迁移的组织来说,评论提出了几个需要先验证的问题:Outlook 客户端的实际连接行为、法规要求的邮件归档功能\(如德国 GoBD\),以及是否仍要依赖微软的客户端和协议。在这些问题确认之前,最好先做试点,不要仅凭“替代品”的说法就规划整体迁移。

**「社区讨论」** 多位 Hacker News 评论者认为“drop-in”说法夸大了:rmoriz 指出,德国要求邮件不可篡改地留存最长 10 年\(GoBD\),而 Stalwart 的常规方案和开源版本据称都没有这项功能;traceroute66 则提到新版 Outlook 对 IMAP 的处理,以及 Office 365 的捆绑服务。andreashaerter 则认为,支持 MAPI 等微软协议只是延缓锁定,还可能损害开放邮件生态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://stalw.art/blog/microsoft-exchange-replacement/">Stalwart is now a drop-in replacement for Microsoft Exchange</a></li>
<li><a href="https://www.startuphub.ai/ai-news/technology/2026/stalwart-1-2-0-replaces-exchange-and-keeps-outlook-working">Stalwart 1.2.0 replaces Exchange and keeps Outlook…</a></li>
<li><a href="https://linuxiac.com/stalwart-1-2-offers-open-source-microsoft-exchange-replacement/">Stalwart 1.2 Offers Open-Source Microsoft Exchange Replacement</a></li>

</ul>
</details>

**标签**: `#stalwart`, `#microsoft-exchange`, `#mail-server`, `#open-source`, `#self-hosting`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [英伟达董事会恢复黄仁勋 CEO 职务](https://nvidianews.nvidia.com/news/nvidia-board-reinstates-jensen-huang-as-president-ceo-and-board-director) ⭐️ 8.0/10

英伟达董事会据公告一致通过,让黄仁勋立即恢复总裁、首席执行官和董事职务,此前担任临时 CEO 的 Colette Kress 继续任首席财务官。董事会称,在听取美国政府高层意见后认为其复任不构成国家安全风险,但由独立董事主持的、针对“黄仁勋曾被外国情报活动盯上”报道的调查仍在进行。

telegram · zaihuapd · 11月23日 14:02

**「背景」** 据 CNBC、商业内幕等媒体报道，黄仁勋此前突然辞去英伟达 CEO 职务，约 11 天后复任，其间由首席财务官 Colette Kress 担任临时 CEO；辞职发生在有报道称董事会已就他是否曾成为外国情报活动目标展开调查之后。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-returns-colette-kress-cfo.html">Nvidia reinstates Jensen Huang as CEO; Colette Kress remains CFO</a></li>
<li><a href="https://www.cnet.com/tech/services-and-software/nvidia-ceo-jensen-huang-resigns/">Nvidia CEO Jensen Huang Resigns, Creating a &#x27;Stress Test... - CNET</a></li>
<li><a href="https://www.businessinsider.com/nvidia-reinstates-jensen-huang-ceo-president-board-2026-11">Nvidia Reinstates Jensen Huang As CEO - Business Insider</a></li>

</ul>
</details>

**标签**: `#NVIDIA`, `#CEO succession`, `#corporate governance`, `#national security`, `#export controls`

---

<a id="item-finance-news-2"></a>
### [纽约联储威廉姆斯：为抑制通胀，未来可能逐步加息](https://www.cnbc.com/2026/11/23/john-williams-fed-inflation-rate-hikes.html) ⭐️ 7.0/10

纽约联储主席威廉姆斯周一表示，让通胀回到 2%的目标仍有工作要做，需要“随时间推移”采取行动，但未明确谈及 12 月是否加息。他预计通胀将在 2027 年更接近 2%，并在 2028 年达到目标（均为他的预测）。

rss · CNBC Finance · 11月23日 21:02

**「背景」** 美联储今年 9 月将基准利率上调 25 个基点至 3.75%-4%，这是 2023 年以来的首次加息，10 月会议维持利率不变；当前通胀压力被归因于伊朗冲突、AI 建设带来的商品需求和关税。

**「影响」** 市场目前已完全定价 12 月 8-9 日的联邦公开市场委员会（FOMC）会议将把 3.75%-4%的目标利率区间上调 0.25 个百分点，这些言论是 12 月决议前最后一次重要的美联储官员政策表态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/09/16/fed-rate-decision-september-2026.html">Fed rate decision September 2026 : Rates rise to 3 . 75 %- 4 %</a></li>
<li><a href="https://tradingeconomics.com/united-states/interest-rate">United States Fed Funds Interest Rate</a></li>

</ul>
</details>

**标签**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#FOMC`

---

<a id="item-finance-news-3"></a>
### [英伟达恢复黄仁勋 CEO 职务，美股反弹但分歧仍在](https://www.cnbc.com/2026/11/23/nvidia-jensen-huang-ceo-market-rally.html) ⭐️ 7.0/10

英伟达恢复黄仁勋的 CEO 职务后，周一美股三大指数大幅反弹。此前自 11 月 12 日宣布他离任至上周五，标普 500 指数下跌超过 9%，三大指数上周五均收于“回调区间”（较高点下跌至少 10%）。分析人士对这是否标志着持久的底部看法不一。

rss · CNBC Finance · 11月23日 18:00

**「背景」** 英伟达于 11 月 12 日宣布黄仁勋离任,据《卫报》报道,由首席财务官科莱特·克雷斯临时接任。不过这轮下跌在此之前就已开始,起因是市场担心 AI 基建的融资、中期选举后的数据中心审批,以及大型云计算公司的资本开支\(用于建设数据中心等的投资\)可能已见顶。

**「影响」** 部分策略师认为，抛售的原因（AI 建设融资、中期选举后数据中心审批、大型云厂商资本支出可能见顶）仍未解决，因此依赖 AI 投资的“卖铲子”类公司仍面临不确定性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theguardian.com/technology/2026/nov/12/nvidia-ceo-jensen-huang-resigns">Jensen Huang resigns as Nvidia CEO after alleged... | The Guardian</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#stock market correction`, `#AI trade`, `#market strategy`

---

<a id="item-finance-news-4"></a>
### [AI 股抛售拖累 DeepSeek 等中国 AI 公司上市计划](https://www.bloomberg.com/news/articles/2026-11-23/china-s-next-ai-deals-clouded-by-selloff-after-anthropic-ipo) ⭐️ 7.0/10

据彭博报道,Anthropic 创纪录的 IPO 后全球股市加速下跌,给 DeepSeek、月之暗面、阶跃星辰等正在筹备或考虑发行股份的中国 AI 公司的上市计划蒙上阴影。报道称,中国科技股自 6 月底以来累计蒸发 1.7 万亿美元。

telegram · zaihuapd · 11月23日 09:31

**「背景」** 据 CNBC 报道，Anthropic 的 1195 亿美元由 IPO 募资 935 亿美元和科技巨头按发行价认购的 260 亿美元合计而成。MiniMax 等中国 AI 公司此前已在香港上市，DeepSeek 等公司的上市计划还在筹备或考虑阶段。

**「影响」** 报道提到,智谱较 6 月高点下跌超 85%,MiniMax 本月跌破发行价,这可能让上述公司的上市时机和定价面临更大不确定性,但具体是否推迟,来源并未明确。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/21/anthropic-ipo-tech-selloff.html">Anthropic’s record IPO collides with tech’s worst week on ...</a></li>
<li><a href="https://www.forbes.com/sites/ywang/2026/11/20/minimax-founder-falls-from-billionaire-ranks-after-losing-116-billion-in-ai-rout/">MiniMax Founder Falls From Billionaire Ranks After Losing...</a></li>

</ul>
</details>

**标签**: `#AI IPOs`, `#Chinese tech stocks`, `#Anthropic IPO`, `#market selloff`, `#DeepSeek`

---