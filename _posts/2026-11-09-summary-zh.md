---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 45 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [研究者称可远程解锁某品牌汽车,细节与品牌未获证实](#item-tech-news-1) ⭐️ 7.0/10
2. [C++ 委员会论文 P4454R0:C++26 契约投票失败后的出路](#item-tech-news-2) ⭐️ 6.5/10
3. [Llama-modchip 声称在 64GB 内存、无 GPU 机器上运行 284B DeepSeek](#item-tech-news-3) ⭐️ 6.5/10
4. [KetchUp：用 Rust 和 WebGPU 构建的开源 SketchUp 替代品](#item-tech-news-4) ⭐️ 6.0/10
5. [Outlook.com 据报开始拒收未配置 DMARC 域名的邮件](#item-tech-news-5) ⭐️ 6.0/10
6. [Linebender 提出面向微控制器的 JIT 位图文字渲染](#item-tech-news-6) ⭐️ 6.0/10
7. [据报高盛将停用银行家和交易员的 Claude Code](#item-tech-news-7) ⭐️ 6.0/10
8. [iOS 27.2 沙盒逃逸 PoC worse\_query 被公开，尚未修复](#item-tech-news-8) ⭐️ 6.0/10
9. [剑桥团队 AI 辅助设计禽流感候选疫苗，小鼠和雪貂试验显示广谱保护](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [中国延长暂停对美 24%加征关税两个月，保留 10%税率](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [研究者称可远程解锁某品牌汽车,细节与品牌未获证实](https://shubs.io/unlocking-any-car-from-x-brand-in-most-of-the-world/) ⭐️ 7.0/10

一篇安全研究博文声称,可以在世界大部分地区远程解锁某个未点名品牌\(X 品牌\)的汽车。但本次提供的材料没有正文,漏洞的技术原理、影响范围、严重程度和厂商回应都无法从中核实。评论区推测涉事品牌是丰田/雷克萨斯,并提到一篇与 ForgeRock 相关的后续文章,但这些都是读者推测,并非已确认的事实。

hackernews · infosecau · 11月9日 00:10 · [社区讨论](https://news.ycombinator.com/item?id=50419215)

**「背景」** 这类漏洞通常出在联网汽车的账号认证和远程服务后端:车辆与手机应用依靠云端身份系统来授权解锁等指令,后端一旦存在缺陷,影响面就可能覆盖多个地区。原文正文未提供,文中品牌也没有点名;评论区推测是丰田/雷克萨斯,并指向 Sam Curry 关于 ForgeRock 的文章,认为那是“全球范围”问题的来源,但这些都只是评论者的说法,尚未得到证实。本次检索到的工具结果只是雷克萨斯车型和经销商的页面,与该漏洞无关,不能用来佐证。

**「影响」** 在缺少正文的情况下,现有证据不足以判断具体影响。若评论推测属实,丰田/雷克萨斯的联网车主需要关注厂商的修复公告和账户安全建议。但目前还不能确认哪些车型或地区受影响,也不能确认问题是否已修复。

**「社区讨论」** 有评论者根据视频背景中的车型细节\(如 RAV4 的后视镜和前灯\)推测涉事品牌是丰田/雷克萨斯;另一位评论者认为“任何车”的说法过强,称自己 2009 年的凯美瑞和哥哥的第四代 Hilux 似乎都不受影响。还有人提醒,文末链接的 Sam Curry 关于 ForgeRock 的文章对应“全球范围”这一部分,同时有人担忧常联网汽车会变得像智能手机一样难以真正拥有和掌控。

**标签**: `#automotive-security`, `#vulnerability-research`, `#connected-cars`, `#authentication`, `#responsible-disclosure`

---

<a id="item-tech-news-2"></a>
### [C++ 委员会论文 P4454R0:C++26 契约投票失败后的出路](https://isocpp.org/files/papers/P4454R0.pdf) ⭐️ 6.5/10

ISO C++ 委员会文件 P4454R0 讨论了 C++26 中契约\(contracts\)特性的一次未通过的投票,以及 Bjarne Stroustrup 的反对立场对结果的影响。该 PDF 的正文未能获取,以下内容仅来自 Hacker News 评论:有评论者称作者是 Herb Sutter,论文列出了六条前进路径,大致包括跳过正式的 C++26 并把相关特性并入 C++29、从 C++26 中移除契约后通过标准、重新投票,以及调整契约设计。投票的具体细节和最终结果尚无法确认。

hackernews · acossta · 11月8日 23:28 · [社区讨论](https://news.ycombinator.com/item?id=50418818)

**「背景」** C++26 是继 C++23 之后的 ISO/IEC 14882 标准修订版,由 ISO C++ 委员会\(WG21\)表决推进。契约\(contracts\)特性让函数声明可由运行时检查的前置/后置条件,评论者将其与手写断言作比较。Stroustrup 另有一份公开文件《Contracts\_fundamental\_flaws》列出他的反对理由。需要注意,维基百科摘要称 C++26 已于 2026 年 3 月 28 日由 WG21 正式发布,这与本文所述表决失败的时间关系不明,具体表决细节应以论文原文为准。

**「社区讨论」** 评论者 pornel 认为 Stroustrup 公开的反对意见\(其文章《Contracts\_fundamental\_flaws》\)相当合理。digitalPhonix 则认为论文过分强调 Stroustrup 一人的作用,更深层的背景是社区对模块\(modules\)这类庞大、半成品且把难题留给实现者的特性日益厌倦与警惕。另一位评论者 StellarScience 称这份论文写得周到、措辞外交,但也表示自己无法确定 Stroustrup 的反对是否是投票失败的主因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/C++26">C+ + 26 - Wikipedia</a></li>

</ul>
</details>

**标签**: `#C++26`, `#C++ contracts`, `#language standardization`, `#Bjarne Stroustrup`, `#ISO C++ committee`

---

<a id="item-tech-news-3"></a>
### [Llama-modchip 声称在 64GB 内存、无 GPU 机器上运行 284B DeepSeek](https://github.com/synchopate/llama-modchip) ⭐️ 6.5/10

GitHub 项目 llama-modchip 声称,可以在只有 64GB 内存、没有 GPU 的纯 CPU 机器上运行 284B 参数的 DeepSeek 模型。我们没有拿到仓库正文,现有材料里也看不到基准测试、输出质量评估或具体的量化方案,因此该说法目前只是项目方的主张,真实可用性无法验证。Hacker News 上的评论指出,README 难以读懂,量化细节也不清楚。

hackernews · joshcsimmons · 11月8日 10:22 · [社区讨论](https://news.ycombinator.com/item?id=50411961)

**「背景:MoE 模型与极端量化」** llama-modchip 是一组面向 ggml / llama.cpp 的内核补丁、量化转码器和运行时工具,目标是让稀疏混合专家\(MoE\)模型完全在 x86\_64 与 ARM64 的系统内存中运行;仓库页面称其可让 284B 的 DeepSeek-V4-Flash 在不足 59 GiB 内存内运行。MoE 模型每个 token 只激活部分专家,因此总参数量很大而单步计算量相对较小,但全部权重仍须放进内存,这就需要很激进的量化。按 59 GiB 容纳 284B 参数粗略估算,平均每个权重不足 2 比特,这也是评论区质疑输出质量的原因;以上数字均为仓库自述,目前没有看到独立的质量或性能评测。

**「影响」** 想在低配机器上本地部署大模型的开发者,暂时不宜把这一说法当作可行方案。在项目公布量化位宽、速度和质量数据之前,应当自行对照普通 llama.cpp 做测试。有评论者在 Nemotron 上试过,速度与普通 llama.cpp 的 CPU 运行相近,只是预填充看起来更快;他还没有测试 DeepSeek,因为 setup 里找不到对应选项。

**「社区讨论」** 评论的焦点是量化和文档质量。armcat 援引实证研究称,量化的性能变化是非线性的,4-bit 附近的体积与性能比最佳,再往下质量会明显下降;boredatoms 则说量化方式恰恰是最关键的信息,README 却写得像“密集的废话”。aappleby 怀疑仓库由 AI 生成,并报告了上述 Nemotron 对比测试;antirez 则提到,在 128GB 统一内存上可以跑得足够快,能用于编程代理场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/synchopate/llama-modchip">GitHub - synchopate/llama-modchip: Run 284B DeepSeek-V4 ...</a></li>
<li><a href="https://github.com/synchopate/llama-modchip/tree/main">GitHub - synchopate/llama-modchip: Run 284B DeepSeek-V4 ...</a></li>

</ul>
</details>

**标签**: `#local-inference`, `#quantization`, `#DeepSeek`, `#CPU-inference`, `#llama.cpp`

---

<a id="item-tech-news-4"></a>
### [KetchUp：用 Rust 和 WebGPU 构建的开源 SketchUp 替代品](https://ketchup3d.github.io/app/) ⭐️ 6.0/10

KetchUp 是一个在 Hacker News 上发布的开源项目，定位为 SketchUp 的替代品，基于 Rust 和 WebGPU 构建，可在浏览器中运行。由于未能获取到项目页面正文，目前只能确认项目名称、技术栈和定位，其功能完整度、文件格式兼容性、性能和成熟度均无法验证。有评论者称其为“vibecoded”（凭 AI 辅助快速生成），这暗示它可能仍处于早期阶段，但这只是评论者的看法，并非已证实的事实。

hackernews · dcoulmbe · 11月8日 22:35 · [社区讨论](https://news.ycombinator.com/item?id=50418176)

**「背景」** SketchUp 是一款以直观的推拉建模见长的 3D 建模软件,常用于建筑、室内和木工设计。评论中有用户称,其开发商 Trimble 先后取消了免费桌面版和永久授权,并把重心转向网页版,这是人们寻找替代品的原因之一\(这是评论者的说法,未经独立核实\)。KetchUp 的 GitHub 页面称其基于 Rust、WebAssembly 和 WebGPU 构建,可在浏览器或桌面运行,同时自称“100% vibe-coded”\(完全由 AI 辅助生成\),因此成熟度仍需自行评估。

**「影响」** 对不满 SketchUp 授权模式的用户来说，这是一个值得试用的开源选项。有评论称 SketchUp 已取消免费版和永久授权，桌面版只能按年付费，用户在迁移前应先用自己的实际模型测试 KetchUp 的功能和文件兼容性。

**「社区讨论」** 评论的焦点之一是对 SketchUp 授权的不满：ayaros 认为 Trimble 忽视桌面版、转向网页端，并取消了免费版和永久授权；sergio 则表示，自己依赖只能在完整桌面版中打开的房屋模型，因此免费网页版对他不适用。另一条评论中，nico 提出，借助 AI 编程工具，人们也许越来越倾向于只构建自己所需的软件，这属于个人观点；此外，egeozcan 提醒说已有同名的开源绘图工具 ketchup。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Ketchup3D/app">GitHub - Ketchup3D/app: Free, open-source 3D modeling ...</a></li>

</ul>
</details>

**标签**: `#open-source`, `#webgpu`, `#rust`, `#3d-modeling`, `#sketchup-alternative`

---

<a id="item-tech-news-5"></a>
### [Outlook.com 据报开始拒收未配置 DMARC 域名的邮件](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc) ⭐️ 6.0/10

MailRoute 的一篇博客文章称,Outlook.com 正在拒收来自未配置 DMARC 的域名的邮件。目前可用的材料只有文章标题和部分 Hacker News 评论,正文内容无法获取,因此生效时间、适用范围、具体的拒收提示或错误码,以及是否对所有发件人一视同仁,都无法核实。这一说法应视为待证实的报道,而非已确认的微软政策细节。

hackernews · xmddmx · 11月8日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50416158)

**「背景」** DMARC 是发件域名在 DNS 中发布的一条记录,用来声明邮件在 SPF/DKIM 校验不通过时收件方应如何处理。微软 2025 年 4 月 2 日曾宣布,日发送量超过 5000 封的域名必须配置 SPF、DKIM 和 DMARC。据 MailRoute 等媒体报道,自 11 月 5 日起,Outlook.com 与 Hotmail 开始退回没有 DMARC 记录域名的邮件,小型发件人也在其列。这些报道均为第三方说法,微软的具体执行范围尚未得到官方确认。

**「影响」** 自建邮件服务器和小型发件人如果所在域名尚未发布 DMARC 记录,发往 Outlook.com 收件人的邮件可能被拒收,建议立即检查并补上 DMARC 记录\(同时确认 SPF 和 DKIM 配置正确\)。但评论指出,即便认证齐全,Outlook.com 仍可能因不公开的黑名单或静默丢弃而影响投递,所以配置 DMARC 未必能保证送达。

**「社区讨论」** 多数评论者认为要求 DMARC 本身合理\(如 stephbook、klodolph\),主要不满在于 Outlook.com 的做法不透明:Neikius 称其 VPS 服务商被不公开的黑名单整体屏蔽、无从申诉,codethief 则称多年来即使 SPF/DKIM/DMARC 齐全,邮件也会在日志显示已接收后却不进入收件箱。另有评论者 stevefan1999 认为,借助 Stalwart 等工具,自建邮件服务器并不困难,这些均为个人经验,并非已证实的普遍情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://mailroute.net/blog/outlook-rejecting-email-without-dmarc">Outlook.com Is Quietly Rejecting Email From Domains Without DMARC</a></li>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftdefenderforoffice365blog/strengthening-email-ecosystem-outlook%E2%80%99s-new-requirements-for-high%E2%80%90volume-senders/4399730">Strengthening Email Ecosystem: Outlook’s New Requirements for ...</a></li>

</ul>
</details>

**标签**: `#DMARC`, `#email deliverability`, `#Outlook.com`, `#email authentication`, `#self-hosting`

---

<a id="item-tech-news-6"></a>
### [Linebender 提出面向微控制器的 JIT 位图文字渲染](https://linebender.org/blog/jit-bitmap-text/) ⭐️ 6.0/10

Linebender 发布博客文章，介绍一种面向微控制器的文字渲染思路：把位图字体的字形即时编译（JIT）成可执行的机器代码，再运行这些代码把文字绘制到屏幕上。根据抓取到的摘要，这种方式不需要帧缓冲。由于未能获取文章正文，具体实现、目标芯片、性能和内存数据都无法核实，本文不对这些作出判断。

hackernews · dmit · 11月8日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=50412072)

**「背景：逐行“追光束”渲染与位图字体」** 传统做法是在帧缓冲中保存整屏像素，再逐个字形从存储的位图中取数并写入。“追光束”（race the beam）式渲染则不使用完整帧缓冲，而是在显示器扫描输出的同时逐行生成像素，这样屏幕内容就只能写入、无法读回。据 Linebender 原文的搜索摘要，作者在 RP2350 微控制器上的追光束渲染器中实现了这一技术，其核心是用 JIT 即时生成针对某个字符串的优化代码；评论中提到的 1996 年专利 US-6377261-B1 则是把字形编译为“立即数加载／移位／写入内存”指令序列的早期相关思路。

**「影响」** 对内存紧张、无法承担完整帧缓冲的嵌入式显示项目，这种思路提供了一种用代码取代字体数据查表的选择。但评论指出，没有帧缓冲就无法读回屏幕内容，像读取像素颜色、填充和涂色这类操作会受限，开发者需要据此权衡。

**「社区讨论」** 评论者 drfuchs 指出相关的在先技术：1996 年申请的专利 US-6377261-B1 同样把字符编译成“立即数加载/移位/按位或写内存”的指令序列。另一位评论者 codazoda 说，他做复古 BASIC 解释器时选择了帧缓冲，因为无帧缓冲方案会让屏幕变成只写，难以支持读取像素和填充操作，尽管帧缓冲在技术上不那么“酷”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linebender.org/blog/jit-bitmap-text/">JIT bitmap text rendering for microcontrollers - Linebender</a></li>

</ul>
</details>

**标签**: `#microcontrollers`, `#JIT compilation`, `#text rendering`, `#embedded systems`, `#graphics`

---

<a id="item-tech-news-7"></a>
### [据报高盛将停用银行家和交易员的 Claude Code](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 6.0/10

据 Hacker News 上转载的一篇报道,高盛正在撤回银行家和交易员使用的 Anthropic 编码智能体 Claude Code。所提供的材料没有正文,因此高盛给出的官方理由、撤回范围、具体时间以及是否已经全面执行,都无法确认。目前能看到的原因仅来自评论区的推测。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**「背景:从鼓励“氛围编程”到收紧权限」** 据转述 Bloomberg 报道的 AI Weekly 和 The Decoder 称,高盛 CIO Marco Argenti 7 月还公开称赞非技术员工的“vibe coding”,10 月更新内部指引后,Claude Code 和 GitHub Copilot 改为只对工程师开放。高盛给出的理由是“生产力与风险管理”,保留权限的包括约 12,000 名工程师和兼做量化工作的 strats 团队,银行家和交易员此前已使用这些工具数月。该说法目前只来自二手转述,原文没有提供正文,具体风险原因和执行范围尚未得到证实。

**「影响」** 如果报道属实,在受监管金融机构里,把编码智能体交给非工程岗位员工前,可能需要先解决数据权限、审计留痕和成本管控问题。其他企业若在业务岗位部署类似工具,可参考评论中提到的风险点,检查智能体是否同时能接触敏感数据、外部内容和对外通信渠道。不过这只是基于未证实的评论所作的推断,并非高盛已披露的结论。

**「社区讨论」** 评论者提出的解释互相不一致:lukebuehler 认为问题在于在能访问客户和交易数据、邮件、互联网与内网的工作站上运行半自主智能体,构成“致命三要素”;legitster 则称自己所在公司收回 Claude 权限是因为按量计费常常超支。steveBK123 强调银行在数据授权、审计和合规上的约束,fancyfredbot 则推测可能与某次运营损失有关。这些都是评论者的猜测,没有源文佐证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://aiweekly.co/alerts/goldman-sachs-pulls-claude-code-and-github-copilot-from-traders-and-bankers">Goldman Sachs Pulls Claude Code and GitHub Copilot From ...</a></li>
<li><a href="https://the-decoder.com/goldman-sachs-pulls-ai-coding-tools-from-traders-and-bankers/">Goldman Sachs pulls AI coding tools from traders and bankers</a></li>
<li><a href="https://daily.dev/posts/goldman-sachs-is-pulling-claude-code-from-its-bankers-and-traders-dmltlbhnz">Goldman Sachs Is Pulling Claude Code from Its Bankers...</a></li>

</ul>
</details>

**标签**: `#enterprise AI adoption`, `#Claude Code`, `#AI agent security`, `#financial services compliance`, `#Goldman Sachs`

---

<a id="item-tech-news-8"></a>
### [iOS 27.2 沙盒逃逸 PoC worse\_query 被公开，尚未修复](https://x.com/forcequitOS/status/2119475139528020218?) ⭐️ 6.0/10

据 Telegram 转述，开发者 forcequitOS 于 11 月 8 日公开了名为 worse\_query 的零日沙盒逃逸概念验证（PoC）。帖子称其支持 iOS 26.0–26.7.2 及 27.2（含 27.3 beta），可访问系统路径并修改应用数据，使用时需配置 App Group。作者强调该项目仅供开发研究、与越狱无关；帖子还称漏洞已提交苹果但尚未修复，社区已出现基于它的 GestaltX 等工具。以上均为二手转述，版本范围和实际影响尚未经独立验证，也没有披露漏洞机理细节。

telegram · zaihuapd · 11月9日 02:36

**「背景：沙盒逃逸与 bad\_query」** iOS 沙盒会限制每个应用只能访问自身的数据和系统资源，沙盒逃逸漏洞能让应用越出这一边界，读取或修改本不该触及的路径。据 GitHub 仓库及 OneJailbreak 的报道，worse\_query 是此前 bad\_query 的直接继任者并基本取代它，使用时需要为应用配置 App Group 容器，作者称它只是面向开发者的概念验证，本身用途有限。这些说明只来自作者和转载页面，尚未见到苹果的确认或独立的技术分析。

**「影响」** 如果上述说法属实，运行受影响版本（包括 27.3 beta）的设备在苹果发布补丁前，可能面临沙盒隔离被绕过的风险。普通用户应留意苹果后续的安全更新，并谨慎安装来源不明的侧载应用或基于该 PoC 的第三方工具；安全研究人员需先核对作者的 GitHub 原始说明，再评估实际影响。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/forcequitOS/worse_query">GitHub - forcequitOS/worse_query: A sandbox escape for iOS 26 ...</a></li>
<li><a href="https://onejailbreak.com/blog/worse_query-sandbox-escape-for-ios-26-and-27/">worse_query Sandbox Escape for iOS 26 and 27 Released</a></li>
<li><a href="https://hotrepo.ai/forcequitOS/worse_query">forcequitOS/worse_query: iOS sandbox escape proof of concept ...</a></li>

</ul>
</details>

**标签**: `#iOS security`, `#sandbox escape`, `#zero-day`, `#proof-of-concept`, `#Apple vulnerabilities`

---

<a id="item-tech-news-9"></a>
### [剑桥团队 AI 辅助设计禽流感候选疫苗，小鼠和雪貂试验显示广谱保护](https://www.cam.ac.uk/stories/ai-developed-vaccines-against-viruses) ⭐️ 6.0/10

剑桥大学等机构的团队于 2026 年 11 月在线发表于《Cell Reports Medicine》的论文称，他们用 AI 辅助设计了一种新型禽流感候选疫苗。在小鼠和雪貂试验中，该疫苗显示出广谱免疫和保护效果，表现优于研究中使用的、基于 WHO 候选疫苗病毒的对照制剂。团队称，这种人工设计的广谱抗原在自然界并不存在，AI 辅助设计可加快疫苗抗原设计。目前证据仅限动物实验，对人的保护效果尚未证实，团队计划推进人体临床试验。

telegram · zaihuapd · 11月9日 03:00

**「背景：H5Nx 禽流感与计算设计抗原」** H5Nx 禽流感病毒毒株多样且不断演变，各国现有的储备疫苗多基于 WHO 候选疫苗病毒制备，对新出现的变异株覆盖有限。Cell Reports Medicine 论文介绍的思路，是用“数字免疫优化合成疫苗”技术，通过计算方法设计多价抗原，并制成多抗原 mRNA 疫苗，以期同时应对全球不同分支的 H5Nx 病毒。

**「影响」** 如果后续人体试验证实有效，这类广谱抗原有望减少每次出现新毒株都要重新匹配候选疫苗病毒的需要，为应急准备提供另一条路径。但目前来源没有给出 AI 方法、数据或具体定量结果，现阶段只能视为早期动物数据，不能据此判断对人的保护力或上市时间。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.cell.com/cell-reports-medicine/fulltext/S2666-3791%2826%2900548-3">Broad vaccine protection against globally diverse influenza A ...</a></li>
<li><a href="https://www.cam.ac.uk/stories/ai-developed-vaccines-against-viruses">Scientists are using AI to develop superior vaccines against ...</a></li>

</ul>
</details>

**标签**: `#AI-for-science`, `#vaccine design`, `#avian influenza`, `#biotech`, `#Cambridge`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国延长暂停对美 24%加征关税两个月，保留 10%税率](https://mp.weixin.qq.com/s/nNxJB3y0YA_2zJvOK6onUQ) ⭐️ 7.0/10

国务院关税税则委员会公告称，经国务院批准，自 2026 年 11 月 10 日 13 时 01 分起的 2 个月内，中国继续暂停实施对美 24%的加征关税，并保留 10%的加征关税税率。公告称，此举是为落实中美两国元首华盛顿会晤达成的成果共识。

telegram · zaihuapd · 11月9日 04:03

**「背景」** 2025 年 11 月 10 日起，中国已将对美 24%的加征关税暂停一年，同时保留 10%的加征税率；此次公告称，延长暂停是为落实中美元首华盛顿会晤达成的共识。

**「影响」** 在暂停期内，中国对美国商品仍按 10%的加征税率征收，24%的税率暂不实施，涉及对美贸易的进口企业仍适用该较低税率。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xinwen.bjd.com.cn/content/s690ad8dbe4b0221b9bef2bc2.html">国 务 院 关 税 税 则 委 员 会 ：中 国 对 美 关 税 调整，中 美 24 % 关 税 继续 暂 停 1 年</a></li>
<li><a href="https://m.163.com/dy/article/KDJN1560051482MP.html?spss=news-hotlist-wap-index">经 国 务 院 批准：一 年 内继续 暂 停 实施 24 %的 对 美 加 征 关 税 税 率， 保 留 10 ...</a></li>

</ul>
</details>

**标签**: `#中美关税`, `#贸易政策`, `#国务院关税税则委员会`, `#中美关系`, `#关税暂停`

---