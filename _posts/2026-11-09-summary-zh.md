---
layout: default
title: "Horizon Summary: 2026-11-09 (ZH)"
date: 2026-11-09
lang: zh
---

> 从 47 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [研究者披露联网汽车后端漏洞,可远程解锁某品牌车辆](#item-tech-news-1) ⭐️ 7.0/10
2. [C++ 委员会论文探讨 C++26 契约投票失败及后续六条路径](#item-tech-news-2) ⭐️ 6.5/10
3. [报道称高盛将从银行家和交易员处撤下 Claude Code](#item-tech-news-3) ⭐️ 6.0/10
4. [llama-modchip 称可在 64GB 内存、无 GPU 下运行 284B DeepSeek](#item-tech-news-4) ⭐️ 6.0/10
5. [Outlook.com 据报开始拒收未配置 DMARC 域名的邮件](#item-tech-news-5) ⭐️ 6.0/10
6. [Linebender 博文:面向微控制器的 JIT 位图文本渲染](#item-tech-news-6) ⭐️ 6.0/10
7. [Frontier3DBench：测试编码智能体构建 3D 物体、场景与交互世界](#item-tech-news-7) ⭐️ 6.0/10
8. [黄仁勋承认婚外情并致歉，英伟达董事会将独立调查间谍指控](#item-tech-news-8) ⭐️ 6.0/10
9. [Win11 测试设置内统一「应用更新」页，取代第三方弹窗](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [中国延长对美 24%加征关税暂停期，保留 10%税率](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [研究者披露联网汽车后端漏洞,可远程解锁某品牌车辆](https://shubs.io/unlocking-any-car-from-x-brand-in-most-of-the-world/) ⭐️ 7.0/10

安全研究者 shubs 发布了一篇技术文章,称某汽车品牌的联网后端存在漏洞,攻击者可借此在全球大多数地区远程解锁该品牌车辆。本次只提供了标题和评论,没有文章正文,因此具体的漏洞原理、受影响车型和修复情况都无法核实。评论区推测涉及的品牌是丰田/雷克萨斯,并与 ForgeRock 身份平台有关,但这些都是社区推断,并非已确认的事实。

hackernews · infosecau · 11月9日 00:10 · [社区讨论](https://news.ycombinator.com/item?id=50419215)

**「背景：联网汽车的身份认证后端」** 联网汽车的手机应用通过厂商云端后台下发解锁等远程指令，后台的身份认证平台（如 ForgeRock 的 OpenAM/OpenIDM）一旦被攻破，攻击者就可能绕过车主账号直接控制车辆。据搜索到的二手报道，Shubham Shah 与 Sam Curry 的攻击链包括：JavaScript 包中暴露的 OpenIDM 硬编码管理员凭据、用路径穿越绕过保护 OpenIDM 端点的 WAF，以及 MFA 绕过。报道称该攻击链可从车牌号出发，在澳大利亚、美国和加拿大对车辆发送远程命令；本文未提供原文正文，品牌是否为丰田/雷克萨斯目前仍只是评论区的推测。

**「影响」** 在缺少原文细节的情况下,可以确定的是:联网汽车的身份认证和远程控制后端一旦存在缺陷,影响会跨越地区和车型。车主和车企安全团队应关注厂商的正式公告与修复进展,并留意评论中的反驳:并非所有车型都接入此类服务,例如有评论者认为自己的 2009 款 Camry 和第四代 Hilux 不受影响,“任何车辆”的说法可能夸大了范围。

**「社区讨论」** 评论者根据视频背景中的车型推断品牌是丰田/雷克萨斯,另有评论称这两个品牌使用 ForgeRock 的 OpenAM 和 OpenIDM 管理身份与后端认证,并推荐阅读 Sam Curry 的后续文章了解“全球范围”的部分。也有人质疑“任何车辆”的说法过强,并担忧始终联网的汽车会像智能手机一样让用户失去控制权;这些都是个人观点或推测,并非文章已证实的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://samcurry.net/forgerock">Hacking Two Automakers: ForgeRock Path Confusion, RCE, and ...</a></li>
<li><a href="https://daily.dev/posts/unlocking-any-car-from-x-brand-in-most-of-the-world-mhczvgj4u">Unlocking any car from X brand in most of the world</a></li>
<li><a href="https://news.lavx.hu/article/researchers-describe-chain-that-could-unlock-connected-cars-from-a-major-automaker">Researchers describe chain that could unlock connected cars ...</a></li>

</ul>
</details>

**标签**: `#vehicle-security`, `#connected-cars`, `#vulnerability-research`, `#authentication`, `#identity-management`

---

<a id="item-tech-news-2"></a>
### [C++ 委员会论文探讨 C++26 契约投票失败及后续六条路径](https://isocpp.org/files/papers/P4454R0.pdf) ⭐️ 6.5/10

一份编号为 P4454R0 的 ISO C++ 委员会论文讨论了 C++26 中“契约”\(contracts\)特性引发的分歧：C++26 的相关投票据称未能通过，而 Bjarne Stroustrup 的反对可能是原因之一。论文原文未能获取，以下内容仅依据标题和 Hacker News 评论摘录。评论者称作者是 Herb Sutter，并称论文列出了六种后续方案，例如跳过 C++26 并把相关特性并入 C++29、从 C++26 中移除契约后通过标准、重新投票、调整契约设计等。投票的具体细节和论文的完整论点尚无法核实。

hackernews · acossta · 11月8日 23:28 · [社区讨论](https://news.ycombinator.com/item?id=50418818)

**「背景：契约特性与 C++26 投票」** 据 The Register 2026 年 3 月 31 日报道，ISO C++ 委员会（WG21）在伦敦克罗伊登的会议上批准了 C++26 标准草案，其中包含契约（Contracts）特性，尽管 Bjarne Stroustrup 等人反对。另据第三方网站报道，C++26 的 DIS（国际标准草案）投票于 10 月 23 日未能通过：20 张赞成票中有 12 张（60%），低于所需的 66.7%，22 个国家中有 9 个投反对票，超过 ISO 允许的 25% 上限。这些数字来自二手报道，本文未能核对 ISO 的原始记录。

**「社区讨论」** 评论者 pornel 认为 Stroustrup 提出的反对意见（他撰写了题为《Contracts\_fundamental\_flaws》的文档）相当合理。digitalPhonix 则认为不应过度强调 Stroustrup 一人的立场，社区对“大而不完整、留给实现者自行填补”的特性（以模块为例）日益疲惫和警惕，这才是这次投票的背景。这些都是个人看法，并非已证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.theregister.com/software/2026/03/31/contracts-are-in-c26-despite-disagreement-over-their-value/5229065">Contracts are in C++26 despite disagreement over their value</a></li>
<li><a href="https://elsolitario.org/en/2026/10/26/according-to-seacord-cpp26-fails-dis-ballot-12-of-20/">C++26 DIS Ballot: What Happened and Why It Failed</a></li>

</ul>
</details>

**标签**: `#C++26`, `#contracts`, `#language standardization`, `#Bjarne Stroustrup`, `#ISO C++ committee`

---

<a id="item-tech-news-3"></a>
### [报道称高盛将从银行家和交易员处撤下 Claude Code](https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers) ⭐️ 6.0/10

据 The State of AI 网站报道,高盛正在撤回银行家和交易员使用 Claude Code\(Anthropic 的编程智能体\)的权限。目前没有可获取的原文内容,高盛撤回的具体原因、范围、时间表以及是否有官方说明均未得到确认。该消息在 Hacker News 上引发大量讨论,但各种解释都只是评论者的推测。

hackernews · TheWiggles · 11月8日 18:16 · [社区讨论](https://news.ycombinator.com/item?id=50415628)

**「背景」** 据检索到的报道,高盛此前已在今年 4 月禁止其香港银行家使用 Claude,并且目前是 Anthropic IPO 的牵头承销商之一。今年 7 月,高盛 CIO Marco Argenti 还公开称赞非技术员工的“vibe coding”,而现在 Claude Code、GitHub Copilot 等 AI 编程工具据称只对工程师开放。原文正文未提供,高盛的真实原因尚未得到证实,评论中提到的“致命三要素”\(敏感数据、对外通信、不受监督的智能体\)只是读者的推测。

**「影响」** 在原因得到证实之前,金融等强监管机构的 IT 与安全团队可以先自查:能否让编码智能体运行在同时接触客户或交易数据、邮箱、互联网和内网的工作站上,以及是否有按用量计费的预算管控和访问审计。这是基于评论者假设做出的提醒,并非已证实的高盛结论。

**「社区讨论」** 评论者提出了几种互不相同的猜测:lukebuehler 认为问题在于把半自主的智能体放在同时接触敏感数据、邮件和互联网的主力工作站上,即所谓“致命三要素”;legitster 则称自己所在的公司因按量计费反复超支而收回 Claude 权限,并转向计费更平稳的 Gemini。另有人\(steveBK123\)强调银行对数据授权、审计和审批链的合规要求,fancyfredbot 则猜测可能与某次交易员相关的运营损失有关。这些都是未经证实的推测。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.thestateofai.com/news/goldman-sachs-claude-code-traders-bankers">Goldman Sachs Is Pulling Claude Code From Its Bankers and...</a></li>
<li><a href="https://the-decoder.com/goldman-sachs-pulls-ai-coding-tools-from-traders-and-bankers/">Goldman Sachs pulls AI coding tools from traders and bankers</a></li>

</ul>
</details>

**标签**: `#Claude Code`, `#enterprise AI adoption`, `#AI agent security`, `#Goldman Sachs`, `#financial compliance`

---

<a id="item-tech-news-4"></a>
### [llama-modchip 称可在 64GB 内存、无 GPU 下运行 284B DeepSeek](https://github.com/synchopate/llama-modchip) ⭐️ 6.0/10

GitHub 项目 llama-modchip 声称,可在仅有 64GB 内存、没有 GPU 的机器上运行 2840 亿参数的 DeepSeek 模型。现有材料只有标题和 Hacker News 评论摘录,没有仓库正文、量化位宽、基准测试或实现方法,因此该说法的真实性和实用性尚未得到验证。评论者表示,仓库说明中没有清楚给出量化方案。

hackernews · joshcsimmons · 11月8日 10:22 · [社区讨论](https://news.ycombinator.com/item?id=50411961)

**「背景」** 本地大模型推理通常依赖量化\(降低权重位宽\)来压缩内存占用,在 llama.cpp 这类 CPU 推理框架上尤其如此。检索到的仓库页面称,llama-modchip\(v2.4.0\)的目标是在纯 CPU、不足 59 GiB 内存的条件下运行 284B 的 DeepSeek-V4-Flash,并在 256K 上下文下让 30B MoE 模型达到最高 111 tok/s;这些数字都是项目自述,尚无独立验证。评论中有人指出,4 比特以下的低位宽量化通常会明显损失质量,而该项目采用的量化方式在已有材料中并不清楚。

**「影响」** 在量化位宽和质量数据公开之前,想在本地 CPU 上运行大模型的用户不宜直接按该标题采购硬件或迁移部署。更稳妥的做法是先自行用小模型对比该项目与原版 llama.cpp 的速度和输出质量。评论中有用户在 Nemotron 上测试,发现其速度与普通 llama.cpp 的 CPU 推理相近,只有预填充\(prefill\)似乎更快;该用户尚未测试 DeepSeek,因为 &quot;modchip setup&quot; 中没有对应选项。

**「社区讨论」** 讨论的主要分歧在于质量与可信度。armcat 指出,已有实证研究显示量化的性能变化是非线性的,体积与性能之比通常在 4 比特附近最优,更低会明显降质;boredatoms 和 aappleby 则批评 README 难以读懂,并质疑这个疑似 AI 生成的仓库是否真有实质改进。另有评论列举的吞吐数据对应的是其他硬件和模型,不能当作该仓库的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/synchopate/llama-modchip">GitHub - synchopate/llama-modchip: Run 284B DeepSeek-V4 ...</a></li>
<li><a href="https://daily.dev/posts/llama-modchip-284b-deepseek-on-64gb-ram-no-gpu-wd0eeu1zf">Llama-modchip: 284B DeepSeek on 64GB RAM, no GPU - daily.dev</a></li>

</ul>
</details>

**标签**: `#local-llm-inference`, `#quantization`, `#deepseek`, `#cpu-inference`, `#llama.cpp`

---

<a id="item-tech-news-5"></a>
### [Outlook.com 据报开始拒收未配置 DMARC 域名的邮件](https://mailroute.net/blog/outlook-rejecting-email-without-dmarc) ⭐️ 6.0/10

MailRoute 的一篇博客称,Outlook.com 现在会拒收来自未配置 DMARC 的域名的邮件。该博客由 Hacker News 用户转发,本次提供的材料只有标题和评论,没有正文,因此具体的拒收条件、生效时间、适用范围和返回的错误信息都无法确认。MailRoute 是一家销售邮件安全服务的厂商,此说法目前只是单一来源的报道,尚未得到独立验证。

hackernews · xmddmx · 11月8日 19:20 · [社区讨论](https://news.ycombinator.com/item?id=50416158)

**「背景：DMARC 是什么」** DMARC 建立在 SPF 和 DKIM 之上。域名所有者通过 DNS 发布策略，说明邮件认证失败时接收方应如何处理，并可接收报告。此前 Google、Yahoo 等大型邮箱服务商已对批量发件人提出认证要求。微软官方问答页面也提到，发往 Outlook.com/Hotmail 的邮件可能因垃圾邮件信誉或未满足较新的发件人认证要求而被拒收。不过，目前提供的材料没有说明此次执行范围和具体规则。

**「影响」** 向 Outlook.com 用户发信的域名所有者,尤其是小型发件人和自建邮件服务器的运维者,应尽快检查自己的域名是否已发布 DMARC 记录,并确认 SPF 和 DKIM 配置正确。由于评论反映拒收有时并不明确,发件人最好主动监测投递结果,不要只依赖退信提示。

**「社区讨论」** 多数评论者认为要求 DMARC 本身合理,stephbook 等人认为发件人早就该配置;但 Neikius 和 codethief 称,Outlook.com 长期存在静默丢信、使用不公开黑名单的问题,即使 SPF、DKIM、DMARC 都配置正确也可能被丢弃,这是自建邮件服务器运维者的主要痛点。这些都是个人经验,并非已验证的普遍情况。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://learn.microsoft.com/en-in/answers/questions/5790042/outlook-com-rejecting-email-messages-for-security">outlook . com rejecting email messages for security... - Microsoft Q&amp;A</a></li>

</ul>
</details>

**标签**: `#DMARC`, `#email deliverability`, `#Outlook.com`, `#email authentication`, `#self-hosting`

---

<a id="item-tech-news-6"></a>
### [Linebender 博文:面向微控制器的 JIT 位图文本渲染](https://linebender.org/blog/jit-bitmap-text/) ⭐️ 6.0/10

Linebender 发布博文,介绍在微控制器上用即时\(JIT\)生成代码的方式渲染位图文本。目前只能获知标题、来源和评论,未获得正文,因此具体实现方式、性能数据和适用硬件均无法核实。从评论推断,思路大致是用生成的代码取代对字体位图数据的读取,但这只是对评论的转述,不是对原文的确认。

hackernews · dmit · 11月8日 10:42 · [社区讨论](https://news.ycombinator.com/item?id=50412072)

**「背景：无帧缓冲的“追光束”渲染」** 文章作者 Raph Levien 在 RP2350 微控制器上实现了“追光束”（race-the-beam）渲染器，即不保存完整帧缓冲，而是在显示扫描的同时逐行生成像素。传统位图文本渲染需要不断从字体数据中取出字形位图，这个技术的思路是用 JIT 为待显示字符串即时生成优化过的机器码，把对字体数据的读取换成执行代码。评论区有读者指出，1996 年申请的专利 US-6377261-B1 已描述过把字形编译成指令的类似做法，这是读者的说法，本文未核对专利全文。

**「社区讨论」** 评论者 drfuchs 指出,1996 年申请的专利 US-6377261-B1 已描述类似做法:把字形编译为“立即数加载/移位/按位或写入内存”的指令序列,像素隐含在机器码的立即数中,不再读取字库位图,这在一定程度上削弱了该思路的新颖性。codazoda 则提出取舍:这种直接写屏的方式使屏幕变成“只写”,而他的 BASIC32 解释器需要读取像素颜色和做填充操作,因此选择了帧缓冲。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://linebender.org/blog/jit-bitmap-text/">JIT bitmap text rendering for microcontrollers - Linebender</a></li>
<li><a href="https://linebender.org/blog/">| Homepage for the Linebender organization</a></li>
<li><a href="https://techbytes.app/posts/jit-bitmap-text-rendering-for-microcontrollers/">JIT bitmap text rendering for microcontrollers | Tech Bytes</a></li>

</ul>
</details>

**标签**: `#microcontrollers`, `#text-rendering`, `#JIT-compilation`, `#embedded-graphics`, `#bitmap-fonts`

---

<a id="item-tech-news-7"></a>
### [Frontier3DBench：测试编码智能体构建 3D 物体、场景与交互世界](https://www.reddit.com/r/MachineLearning/comments/1xrhg3a/can_coding_agents_build_interactive_3d_worlds/) ⭐️ 6.0/10

Einsia 团队发布了 Frontier3DBench 基准，用来测试编码智能体能否从单个 3D 物体一路做到可交互的世界。基准包含 145 个任务、9 个类别，评测 11 种模型–harness 配置，产出可编辑的 Blender 项目和可运行的 Unreal Engine 世界，并通过渲染视图、场景检查和运行时测试评估外观、结构与行为。作者报告称，GPT-6.1-sol 在总分、物体和场景上领先，GPT-6-astra 在交互世界上领先；所有配置在基于参考的重建任务上得分都低于文本驱动生成；在 165 份世界提交中，局部机制平均 83.08 分，有状态工作流仅 30.26 分（满分 100）。以上均为作者自述结果，来自其自己发布的帖子，尚无独立复现，评分可靠性等方法细节在所给材料中也不明确。

reddit · r/MachineLearning · /u/OliviaYii · 11月9日 03:41

**「背景」** 此前针对编程智能体的评测多集中在代码补全或软件工程任务上,而 3D 内容创作需要智能体通过 Blender、Unreal Engine 等工具生成可编辑的工程文件,并在渲染结果、场景结构和运行时行为上接受检验。Frontier3DBench 试图把这一能力拆成从单个物体、场景到带有协同交互和持久状态的互动世界三个层级。需要注意的是,上述结果和模型名称均来自作者在 Reddit 上的自述,所提供的材料中没有独立验证。

**「影响」** 如果这些结果成立，开发者在用编码智能体做游戏或仿真时，可以较放心地让它实现孤立的局部机制，但涉及多对象协同和持久状态的工作流仍需要更多人工检查与拆解。使用该基准前，应先查阅项目页、论文和 GitHub 仓库，核实评分方式和模型配置，因为帖子中的模型名称无法凭现有材料验证。

**标签**: `#Frontier3DBench`, `#coding agents`, `#3D generation`, `#benchmark`, `#Unreal Engine`

---

<a id="item-tech-news-8"></a>
### [黄仁勋承认婚外情并致歉，英伟达董事会将独立调查间谍指控](https://www.bloomberg.com/news/articles/2026-11-08/nvidia-board-to-probe-spying-case-after-ceo-jensen-huang-admits-infidelity) ⭐️ 6.0/10

据 Telegram 频道转引 Bloomberg 和英伟达新闻室的内容，英伟达董事会将成立独立董事委员会，并与外部律师合作，调查首席执行官黄仁勋是否成为外国情报行动的目标。帖子中附有一封署名黄仁勋、写给员工的邮件：他承认对妻子不忠并道歉，称支持并将全力配合调查，调查结果出炉前继续担任 CEO。邮件提到“新闻报道中提出的国家安全问题”，但没有说明具体指控、涉及哪个国家、调查范围或时间表。以上均来自转载帖，我们未能直接核对 Bloomberg 原文或英伟达的官方公告。

telegram · zaihuapd · 11月8日 21:39

**「背景」** 这次调查的起因是此前有媒体报道称,黄仁勋可能成为外国情报行动的目标。路透援引英伟达声明称,董事会正是因这些报道而启动独立调查;彭博也报道,董事会要查明他是否被卷入外国间谍图谋。目前所引资料没有披露具体指控细节、调查范围和时间表,黄仁勋邮件中也只提到“新闻报道提出的国家安全问题”。

**「影响」** 在调查结论公布前，黄仁勋的去留和英伟达与美国监管机构的关系都存在不确定性，投资者和合作伙伴应以董事会和公司的正式披露为准，而不是依据二手转载判断。帖子中“特朗普：他是个好人”一句没有给出来源，不宜当作已核实的表态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-11-08/nvidia-board-to-probe-spying-case-after-ceo-jensen-huang-admits-infidelity">Nvidia Board to Probe Spying Case After CEO Jensen Huang ...</a></li>
<li><a href="https://www.reuters.com/world/china/nvidia-launches-probe-after-report-ceo-huang-was-target-foreign-intelligence-2026-11-08/">Nvidia probes whether CEO Huang was target of foreign spying ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Jensen Huang`, `#corporate governance`, `#national security`, `#tech industry`

---

<a id="item-tech-news-9"></a>
### [Win11 测试设置内统一「应用更新」页，取代第三方弹窗](https://www.windowslatest.com/2026/11/09/for-20-years-windows-apps-like-java-have-nagged-you-with-their-own-update-pop-ups-and-windows-11-now-wants-to-end-it/) ⭐️ 6.0/10

据 Windows Latest 报道，Windows 11 正在测试「应用更新」功能，计划在“设置 &gt; 应用”中集中显示第三方应用的更新，取代 Java 等应用各自弹出的更新提示。开发者需要注册为更新提供方，并提供更新检查脚本；Windows 沿用系统更新的智能调度，结合使用状态、电量和网络状况安排安装，默认每 22 小时扫描一次。来源称该功能仍处于测试最后阶段，目前尚不可用，具体上线时间和版本未见说明。

telegram · zaihuapd · 11月9日 02:09

**「背景：第三方应用更新为何分散」** 长期以来，Windows 上的第三方应用大多依赖各自的更新机制，例如 Java 等应用会自行弹出更新提示；这些机制通常没有与 Windows Update 或微软商店统一整合，用户需要分别应对各应用的提醒。此前已有讨论提到，Windows 11 设置中出现的“应用更新”页面主要列出由微软商店管理的应用，而此次测试的是把更多第三方应用纳入统一调度。

**「影响」** 对第三方应用开发者而言，若要接入该页面，需要注册为提供方并实现更新检查脚本，而不是继续依赖自带的弹窗或后台更新程序。不过现有材料没有说明接入的具体接口、要求或是否强制，开发者需等待微软的正式文档。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://umatechnology.org/how-to-auto-update-install-apps-in-windows-11/">How to Auto Update Install Apps in Windows 11 - UMA Technology</a></li>
<li><a href="https://windowsforum.com/threads/windows-11-app-updates-in-settings-signal-move-toward-unified-update-orchestration.391426/">Windows 11 App updates in Settings signal move... | Windows Forum</a></li>

</ul>
</details>

**标签**: `#Windows 11`, `#app updates`, `#Windows Settings`, `#software distribution`, `#third-party apps`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国延长对美 24%加征关税暂停期，保留 10%税率](https://mp.weixin.qq.com/s/nNxJB3y0YA_2zJvOK6onUQ) ⭐️ 7.0/10

据国务院关税税则委员会公告，自 2026 年 11 月 10 日 13 时 01 分起，中国将在 2 个月内继续暂停实施对美 24%的加征关税，同时保留 10%的加征税率。公告称，此举是为落实中美两国元首在华盛顿会晤达成的共识。

telegram · zaihuapd · 11月9日 04:03

**「背景」** 中国对美国商品除正常关税外还加征了额外关税（其中 24% 的部分已暂停实施）：2025 年 8 月，中国先将这部分暂停 90 天；此后又宣布在一年内继续暂停，并保留 10% 的加征税率，此次是在该安排基础上再延续 2 个月。

**「影响」** 在 2 个月暂停期内，对美商品的加征关税仍按 10%而非 24%的税率执行，这直接关系到向中国出口美国商品的企业和相关进口商的成本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://xinwen.bjd.com.cn/content/s690ad8dbe4b0221b9bef2bc2.html">国 务 院 关 税 税 则 委 员 会 ：中 国 对 美 关 税 调整，中 美 24 % 关 税 继续 暂 停 1年</a></li>
<li><a href="https://www.163.com/dy/article/K6PK1HVO0514E1NL.html">中 美 发布联合声明： 24 % 对 等 关 税 暂 停 90天， 保 留 10 ...</a></li>

</ul>
</details>

**标签**: `#中美贸易`, `#关税政策`, `#国务院关税税则委员会`, `#贸易休战`, `#对美加征关税`

---