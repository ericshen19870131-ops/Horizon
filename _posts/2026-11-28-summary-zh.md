---
layout: default
title: "Horizon Summary: 2026-11-28 (ZH)"
date: 2026-11-28
lang: zh
---

> 从 39 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Linux 内核 nfsd 曝 CVE-2026-99362，预认证堆溢出可致 root](#item-tech-news-1) ⭐️ 8.0/10
2. [弗吉尼亚等州总检察长起诉 SpaceX，指控 Grok 涉儿童剥削与非自愿图像](#item-tech-news-2) ⭐️ 7.0/10
3. [SemiAnalysis：Trainium3 在 InferenceX 上的推理成本与微架构测试](#item-tech-news-3) ⭐️ 7.0/10
4. [美国空军 Cloud One 云平台据报遭黑客入侵](#item-tech-news-4) ⭐️ 6.5/10
5. [报道称黑客用 AI 工具 Artex 攻击美国多家情报机构](#item-tech-news-5) ⭐️ 6.5/10
6. [微软推进以 Windows 内置驱动取代部分第三方驱动](#item-tech-news-6) ⭐️ 6.5/10

**财经新闻**
1. [国常会：完善资本市场稳市机制，优化汇金类“平准基金”功能](#item-finance-news-1) ⭐️ 7.0/10
2. [DeepSeek 完成第二轮融资，蜜雪冰城认缴 5 亿元](#item-finance-news-2) ⭐️ 7.0/10
3. [央行发布大额存单新规，个人起购门槛降至 10 万元](#item-finance-news-3) ⭐️ 7.0/10
4. [标普 500 指数进入回调区间,熊市与衰退并非必然接踵而至](#item-finance-news-4) ⭐️ 6.5/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Linux 内核 nfsd 曝 CVE-2026-99362，预认证堆溢出可致 root](https://opensec.in/blog/nfs2root-cve-2026-99362) ⭐️ 8.0/10

OpenSec 披露 Linux 内核 NFS 服务器 nfsd 存在预认证堆溢出漏洞 CVE-2026-99362，CVSS 评分 9.8。据该文介绍，攻击者无需登录，向 tcp/2049 发送一条连接即可越界写入内核堆并获得 root shell。该漏洞自 2014 年的 Linux 3.16 起存在，影响启用 NFSv4.1 或 4.2 的主机，包括文件服务器、NAS 和集群存储节点。修复已随 6.12.117、6.18.61、7.3.2 和 7.4-rc1 发布，CVE 于 2026 年 11 月 20 日公开；以上均出自 OpenSec 的说法，此转载未提供利用细节，也未见独立验证。

telegram · zaihuapd · 11月27日 12:57

**「背景：nfsd 与受影响的组件」** nfsd 是 Linux 内核内置的 NFS 服务器，通过 tcp/2049 对外提供文件共享。据 computingforgeeks 的分析，该漏洞是 NFSv4.1/4.2 会话回复缓存中的堆越界写入，客户端在认证之前就能触发；OpenSec 将其命名为 NFS2ROOT。Red Hat 的公告指出，RHEL 默认配置不运行也不启用内核 nfsd，因此受影响的主要是主动开启 NFS 服务并暴露 2049 端口的主机。

**「影响」** 运行 nfsd 并启用 NFSv4.1/4.2 的管理员应检查内核版本，升级到上述修复版本并重启。暂时无法升级时，可用防火墙限制 tcp/2049 的访问来源。实际风险取决于 NFS 服务是否暴露在不可信网络中。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://access.redhat.com/security/cve/cve-2026-99362">CVE-2026-99362 - Red Hat Customer Portal</a></li>
<li><a href="https://computingforgeeks.com/nfs2root-cve-2026-99362/">NFS2ROOT (CVE-2026-99362): Check, Patch, Mitigate ...</a></li>

</ul>
</details>

**标签**: `#Linux kernel`, `#CVE-2026-99362`, `#NFS`, `#remote code execution`, `#vulnerability disclosure`

---

<a id="item-tech-news-2"></a>
### [弗吉尼亚等州总检察长起诉 SpaceX，指控 Grok 涉儿童剥削与非自愿图像](https://www.oag.state.va.us/media-center/news-releases/jay-jones/3162-attorneys-general-jones-and-rayfield-file-suit-against-spacex-parent-company-of-x-xai-and-grok-over-creation-and-promotion-of-child-exploitation-and-non-consensual-images-on-platform) ⭐️ 7.0/10

弗吉尼亚州总检察长 Jay Jones 与另一位总检察长 Rayfield（据新闻稿链接）对 SpaceX 提起诉讼。起诉文件称 SpaceX 是 X、xAI 和 Grok 的母公司，诉讼针对这些平台上儿童剥削图像和非自愿图像的生成与传播。目前仅有标题和链接可用，起诉书的法律依据、具体指控、涉案时间范围和诉讼请求均未提供，无法确认。

hackernews · DeepLogin · 11月27日 19:42 · [社区讨论](https://news.ycombinator.com/item?id=50670855)

**「背景:诉讼主体与指控依据」** 据《纽约时报》报道,提起诉讼的是俄勒冈州和弗吉尼亚州,两州指控马斯克旗下公司通过 Grok Imagine 图像生成工具生成性化图像,违反了消费者保护法。CNBC 称,两州总检察长 Rayfield 与 Jones 在起诉书中都强调,未经同意的性化图像造成的伤害不限于画面中的受害者,也会让被迫接触这些内容的人感到恐惧和焦虑。弗吉尼亚州官方公告称,SpaceX 是 X、xAI 和 Grok 的母公司,因此被列为被告。

**「社区讨论」** 评论多为推测：有人不确定 Grok 是管控过松，还是用户通过诱导绕过了限制；也有人质疑为何不追究使用者。有评论者称最高法院已裁定“出于个人消费用 AI 制作儿童性虐待材料”属受保护言论，但所提供材料中没有任何依据，不应视为既定事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cnbc.com/2026/11/23/oregon-virginia-spacex-grok-deepfake-lawsuits.html">SpaceX sued by 2 states over AI deepfake porn, Grok safety claims</a></li>
<li><a href="https://www.nytimes.com/2026/11/23/technology/spacex-lawsuit-ai-sexualized-images.html">SpaceX Sued By Oregon and Virginia Over A.I.-Generated Sexualized...</a></li>

</ul>
</details>

**标签**: `#AI safety`, `#Grok`, `#xAI`, `#AI regulation`, `#content moderation`

---

<a id="item-tech-news-3"></a>
### [SemiAnalysis：Trainium3 在 InferenceX 上的推理成本与微架构测试](https://newsletter.semianalysis.com/p/trainium3-inferencex) ⭐️ 7.0/10

SemiAnalysis 发布了对 AWS Trainium3 推理性能和微架构的深度分析。文章称，Trainium3 与 TPU 已上线其开源基准 InferenceX，在 GB300 的单 token 总拥有成本（TCO）上“不相上下，甚至更优”。在 AgentX（回放真实编程智能体会话）测试中，文章称 Trainium3 采用 PDS + vLLM，在整条 TCO 与 p90 交互性曲线上，性能/成本优于除 Vera Rubin 外的所有加速器。文章还用自家 UBenchX 微基准套件测试，称 Trainium 的描述符生成引擎（DGE，对应 Nvidia TMA 和 AMD MI455X TDM）在小消息尺寸下即可达到峰值 HBM 带宽利用率，而 Nvidia GPU 做不到。以上结论均为作者自测与自述，所提供节选仅为开头部分，具体数据和测试条件无法核实。

rss · Semianalysis · 11月27日 15:54

**「背景：DGE 与 Trainium3」** 文中提到的 Trainium 描述符生成引擎\(DGE\)负责 DMA 数据搬运,SemiAnalysis 将其类比为 Nvidia 的 TMA 和 AMD 的 TDM。AWS Neuron 文档对 DGE 的 DMA 模式有专门说明,并提到 Trainium3 NeuronCore 已在 Neuron 2.33.1 中获得支持。SemiAnalysis 此前\(2025 年 12 月 4 日\)就发表过 Trainium3 的分析文章,当时的判断是它“可能成为挑战者”;本文则基于 InferenceX 的实测数据,把讨论推进到推理性价比和微架构微基准。

**「影响」** 对评估推理加速器的团队来说，这篇文章提供了一个可参考的数据点：比较 Trainium3 与 GB300 时，应看 TCO 下的性能/成本曲线，而不只看峰值算力。不过结论依赖 SemiAnalysis 自己的测试配置和 TCO 模型，并受到 AWS 工程师协助验证实验的影响，采购或迁移前仍应用自己的工作负载复测，并核对 InferenceX 与 UBenchX 的开源代码和数据。

<details><summary>参考链接</summary>
<ul>
<li>Descriptor Generation Engine (DGE) Reference - AWS Neuron Documentation</li>
<li>AWS Trainium3 Deep Dive | A Potential Challenger Approaching</li>

</ul>
</details>

**标签**: `#Trainium3`, `#AWS`, `#AI accelerators`, `#microarchitecture`, `#ML inference`

---

<a id="item-tech-news-4"></a>
### [美国空军 Cloud One 云平台据报遭黑客入侵](https://news.sky.com/story/us-air-forces-cloud-computing-platform-hacked-13617163) ⭐️ 6.5/10

天空新闻\(Sky News\)报道称,美国空军的 Cloud One 云计算平台遭到黑客入侵。社区评论引用的报道称,该平台于 2017 年推出,整合了微软、亚马逊、甲骨文和 Alphabet 四家运营商的资源,支撑数十个应用,包括人事数据、薪酬、后勤与维修管理。本次提供的材料只有标题和评论,没有文章正文,因此攻击方式、影响范围、攻击者身份和数据是否泄露均未知。

hackernews · freakynit · 11月27日 12:54 · [社区讨论](https://news.ycombinator.com/item?id=50666375)

**「背景：Cloud One 是什么」** 据社区评论引述的报道，Cloud One 于 2017 年上线，是美国空军的统一 IT 平台，整合了微软、亚马逊、甲骨文和 Alphabet 四家运营商的资源，承载人事、薪酬、后勤和维修等数十个应用。外部搜索结果显示，Reuters 援引三名知情人士称黑客已入侵该平台，可能危及大量战术、人事和后勤数据；这些结果均为转述，入侵方式、影响范围和归因目前仍未公开。

**「影响」** 一位自称工作部分依托 Cloud One 的评论者称,过去一个月该平台出现明显中断,基础设施正在重建,访问受到严格限制,他因此提前休假。这是未经证实的个人说法,但说明依赖该平台的用户可能面临访问受限和服务不稳定,需要等待官方说明和恢复安排。

**「社区讨论」** 评论者主要质疑把多家云厂商及其分包商拼合在一起会扩大访问面,其中一人主张改由政府内部的全职运维团队负责。另有评论回忆旧时的物理隔离做法,也有人认为本地部署可能回潮。这些均为个人观点,尚无技术细节证明入侵与多厂商架构有关。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybernews.com/security/hackers-breach-us-air-force-flagship-cloud-one/">US Air Force Cloud One Breach: Hackers Hit Military Cloud ...</a></li>
<li><a href="https://www.cbsnews.com/news/u-s-air-force-cloud-platform-breached-by-hackers/">U.S. Air Force cloud platform breached by hackers, report says</a></li>
<li><a href="https://cybersecuritynews.com/hackers-break-u-s-air-force-cloud/">Hackers Break Into U.S. Air Force Cloud Platform Used to ...</a></li>

</ul>
</details>

**标签**: `#cybersecurity`, `#government cloud`, `#Air Force Cloud One`, `#data breach`, `#multi-cloud`

---

<a id="item-tech-news-5"></a>
### [报道称黑客用 AI 工具 Artex 攻击美国多家情报机构](https://www.forbes.com/sites/the-wiretap/2026/11/25/us-government-under-ai-cyberattack) ⭐️ 6.5/10

据福布斯转述《纽约时报》的报道，黑客在 AI 工具辅助下攻击了美国中央情报局、国家地理空间情报局和国家情报总监办公室。报道称此次攻击看起来不算严重，受影响的是非机密的侦察数据。攻击者使用的 Artex 可整合多个开源 AI 模型来测试网络和计算机防御；据称一名中国开发者今年早些时候发布了该工具，后来它被用于多起攻击（包括针对欧盟的一起），开发者已将其从自己的 GitHub 账号删除。这些内容均来自二手转述，原文没有给出攻击手法、Artex 的技术细节或归因证据。

telegram · zaihuapd · 11月27日 10:42

**「背景：Artex 是什么」** 据 AI Threat Watch 的介绍，Artex 是一个开源的自主攻击型 AI 智能体框架，由 DeepSeek、Claude 等大语言模型驱动，可自动化、低成本地执行入侵操作，原本用于测试网络和计算机防御。TechCrunch 报道称，FBI 已就其被用于入侵网络发出警告；开发者在其被滥用后改为闭源，但 FBI 称此前的开源版本仍在流传，依然“广泛可得”。这说明下架代码并不能阻止已扩散版本继续被攻击者使用。

**「影响」** 按报道所述，Artex 可整合开源模型来测试网络和计算机防御，已被用于针对政府机构的攻击。这意味着防御方需要把此类 AI 辅助的自动化探测纳入威胁模型。不过原文没有说明该工具具体如何工作，也没有给出可用于检测的指标，因此目前还不足以据此制定具体的防护措施。关于 FBI 此前曾警告该工具被广泛使用的说法，也尚未得到进一步印证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcrunch.com/2026/11/16/fbi-says-artex-ai-open-source-hacking-tool-used-to-breach-networks-in-under-three-hours/">FBI says Artex AI open source hacking tool used to... | TechCrunch</a></li>
<li><a href="https://ai-threat.watch/aof/artex/">ARTEX : agentic offensive framework | AI Threat Watch</a></li>

</ul>
</details>

**标签**: `#AI cybersecurity`, `#intelligence agencies`, `#Artex`, `#open-source AI misuse`, `#cyberattack`

---

<a id="item-tech-news-6"></a>
### [微软推进以 Windows 内置驱动取代部分第三方驱动](https://www.techspot.com/news/114721-microsoft-wants-replace-most-third-party-device-drivers.html) ⭐️ 6.5/10

据 TechSpot 报道，微软在 Ignite 2026 上表示，正为整类硬件开发新的内置驱动，让 Windows 更多依赖自带驱动，以减少第三方代码进入内核。打印机是首批重点，近期推出的 Windows Ready Print 模式旨在取代旧式第三方打印驱动。Windows 产品经理 Mehmet Kucukgoz 称，SoundWire、SDCA 等音频类驱动将很快成为内置组件，I3C 总线、USB 以太网和 MIPI 摄像头类驱动仍在开发中。微软还在 Windows 硬件工程大会上推出驱动质量倡议（DQI），要求提升驱动的可靠性、质量和安全标准，并鼓励第三方开发者和 OEM 定制驱动尽量采用内置驱动。上述内容均为微软的计划与表态，来源是 Telegram 对 TechSpot 文章的简短转述，未给出具体发布时间表，也没有独立验证。

telegram · zaihuapd · 11月28日 02:09

**「背景」** 内置驱动（inbox driver）是随 Windows 一同发布的通用类驱动，可让常见设备即插即用，不必另行下载厂商驱动。外部报道指出，同一类硬件在 Windows 上往往存在数百种第三方驱动变体，碎片化问题突出；第三方驱动运行在内核层，一旦出现缺陷或漏洞，就会影响系统稳定与安全，微软此举正是为了减少这类风险。

**「影响」** 对硬件厂商、OEM 和驱动开发者而言，相关设备类别的驱动开发方向将转向依托 Windows 内置类驱动，而非自行维护内核态驱动。涉及打印、音频、摄像头等产品的团队，宜评估现有定制驱动能否迁移到内置驱动，但目前缺少具体时间表和兼容性细节，实际迁移成本尚无法判断。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://windowsforum.com/windows-news.4/microsoft-driver-resiliency-inbox-drivers-isolation-and-kernel-safeguards.389927/">MS Driver Resiliency: Inbox Driver Isolation &amp; Kernel Safeguards</a></li>
<li><a href="https://3dnews.ru/1151918/microsoft-reshila-izbavit-windows-11-ot-zooparka-drayverov-radi-stabilnosti-i-bezopasnosti">Microsoft решила избавить Windows 11 от зоопарка драйверов...</a></li>

</ul>
</details>

**标签**: `#Windows`, `#device drivers`, `#kernel security`, `#Microsoft`, `#hardware ecosystem`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [国常会：完善资本市场稳市机制，优化汇金类“平准基金”功能](https://www.tmtpost.com/nictation/8220182.html) ⭐️ 7.0/10

11 月 27 日，国务院总理李强主持召开国务院常务会议，提出要持续完善资本市场稳市机制，加力发挥“国家队”稳市作用，进一步优化中央汇金公司的类“平准基金”功能，并提供充足流动性保障。会议还要求推动上市公司加大分红回购力度，并表示将实施好存量政策、谋划出台增量政策。

telegram · zaihuapd · 11月27日 05:35

**「背景」** 中央汇金是被称为资本市场“国家队”的国有投资机构，此前已表示将发挥类似“平准基金”（市场剧烈波动时由官方资金入场买入、稳定市场）的作用并增持 ETF，央行也承诺必要时通过再贷款提供资金。

**「影响」** 会议要求完善保险、企业年金、社保基金等中长期资金入市的支持引导政策，并坚决查处财务造假、违规减持等行为，与 A 股投资者和上市公司直接相关；但报道未给出具体规模、时间表或实施细则，增量政策尚在“谋划”阶段。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://tt.jxnews.com.cn/news/2685145/">中 国 版 平 准 基 金 来了，释放 稳 市 强信号</a></li>
<li><a href="https://www.21jingji.com/article/20260307/herald/ce60c4c8e0398fe4b7f596959ac4bf6a.html">重磅！ 央 行定调， 中 央 汇 金 扛“ 稳 市 大旗” - 21经济网</a></li>

</ul>
</details>

**标签**: `#China capital markets`, `#State Council`, `#Central Huijin`, `#market stabilization`, `#long-term capital inflows`

---

<a id="item-finance-news-2"></a>
### [DeepSeek 完成第二轮融资，蜜雪冰城认缴 5 亿元](https://m.sohu.com/a/1107027659_115479) ⭐️ 7.0/10

据搜狐网报道，DeepSeek 完成第二轮融资，规模在 1000 亿至 1055 亿元人民币之间，投后估值约 6155 亿元。新增 31 家出资人包括腾讯、宁德时代、中国移动、vivo，蜜雪冰城认缴 5 亿元。

telegram · zaihuapd · 11月27日 06:33

**「背景」** 据报道，DeepSeek 今年 6 月完成首轮外部融资，总额超 500 亿元、投后估值接近 4000 亿元；此次是第二轮。蜜雪冰城并非直接入股，而是通过砺思资本管理的基金间接出资，该基金是一只投向非上市企业的私募股权基金。

**「影响」** 蜜雪的 5 亿元通过砺思资本管理的基金投入，该基金扩募后规模为 75.2 亿元；相比蜜雪集团 2025 年 335.6 亿元的营收，这笔出资占比较小。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.php.cn/faq/2770291.html">DeepSeek “变胖了”： 融 资 500亿，买国产算力、招人、冲刺AGI...</a></li>
<li><a href="https://post.smzdm.com/p/am96nlkk/">DeepSeek 首 轮 融 资 超500亿元，创国产AI纪录_IT互联网_什么值得买</a></li>
<li><a href="https://www.chinaventure.com.cn/news/78-20261108-393950.html">梁文锋攒了一个老乡局 | 投中网</a></li>

</ul>
</details>

**标签**: `#DeepSeek`, `#AI financing`, `#venture capital`, `#Mixue Group`, `#China tech valuation`

---

<a id="item-finance-news-3"></a>
### [央行发布大额存单新规，个人起购门槛降至 10 万元](https://www.news.cn/fortune/20261127/70789d77822242cc82216f51a416f872/c.html) ⭐️ 7.0/10

中国人民银行 11 月 27 日公布《大额存单管理办法》，将个人认购起点由 20 万元降至不低于 10 万元，机构由 1000 万元降至不低于 500 万元，自 2027 年 3 月 21 日起施行。同日发布的《人民币存贷款利率管理规定》也自该日起施行，要求金融机构自主确定存贷款利率，不得以高息揽储等不正当手段吸收存款。

telegram · zaihuapd · 11月27日 11:36

**「背景」** 大额存单是银行发行的大额定期存款凭证，认购有最低金额要求；此前的认购起点由 2015 年《大额存单管理暂行办法》规定，个人 20 万元、机构 1000 万元。

**「影响」** 资金量较小的个人和机构投资者将可以更低的金额购买大额存单，而银行在揽储时将受到利率管理规定的约束。

**标签**: `#大额存单`, `#中国人民银行`, `#存款利率`, `#金融监管`, `#银行业`

---

<a id="item-finance-news-4"></a>
### [标普 500 指数进入回调区间,熊市与衰退并非必然接踵而至](https://www.cnbc.com/2026/11/27/the-sp-500-is-in-a-correction-bear-markets-and-recessions-dont-always-follow.html) ⭐️ 6.5/10

标普 500 指数 11 月 20 日单日下跌 3.7%,收于 6,910.39 点,较 10 月 6 日创下的收盘纪录高点 7,818.93 点低 11.6%,自 2025 年 4 月以来首次进入回调区间。德意志银行策略师亨利·艾伦认为,历史上熊市常伴随的几类触发因素目前尚未出现。

rss · CNBC Finance · 11月27日 13:21

**「背景」** 回调指股指较近期高点下跌 10%,熊市则指跌幅达 20%或以上;CNBC 分析显示,标普 500 的 13 次熊市中有 8 次与美国国家经济研究局认定的衰退重叠,另有 5 次没有。

**「影响」** 艾伦称,自 1962 年以来的熊市都至少伴随衰退、经济数据恶化引发衰退担忧或美联储连续加息之一,而目前 11 月美国综合 PMI 初值为 54.6\(高于 50 代表活动扩张\),这是他的个人判断,并非定论。

**标签**: `#S&amp;P 500 correction`, `#bear markets`, `#recession risk`, `#Federal Reserve`, `#AI valuations`

---