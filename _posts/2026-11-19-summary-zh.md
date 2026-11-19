---
layout: default
title: "Horizon Summary: 2026-11-19 (ZH)"
date: 2026-11-19
lang: zh
---

> 从 51 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Nginx HTTP/2 曝未认证远程代码执行漏洞，已发布修复版本](#item-tech-news-1) ⭐️ 8.0/10
2. [谷歌发布 Gemini 4 Neon：100 万 token 上下文，主打编程智能体](#item-tech-news-2) ⭐️ 7.5/10
3. [Ruby 公布 Regexp 与 String 大小写转换的多个内存漏洞](#item-tech-news-3) ⭐️ 7.0/10
4. [Genie 4 通过 Project Genie 上线,面向符合条件的 AI Ultra 订阅用户](#item-tech-news-4) ⭐️ 7.0/10
5. [Quad9 因法国法院要求 DNS 封锁而退出法国](#item-tech-news-5) ⭐️ 6.5/10
6. [微软 AI 在 Ignite 2026 发布七款新模型,主打性价比](#item-tech-news-6) ⭐️ 6.0/10
7. [OpenAI 发文介绍用其模型推进芯片设计,细节有限](#item-tech-news-7) ⭐️ 6.0/10

**财经新闻**
1. [美联储 10 月会议纪要:多数官员预计还需加息](#item-finance-news-1) ⭐️ 8.0/10
2. [美联储理事沃勒称 12 月可能需加息 50 个基点](#item-finance-news-2) ⭐️ 8.0/10
3. [腾讯三季度营收低于预期，资本开支大幅超预期](#item-finance-news-3) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Nginx HTTP/2 曝未认证远程代码执行漏洞，已发布修复版本](https://www.wiz.io/blog/nginx-http2-rce-vulnerabilities) ⭐️ 8.0/10

Wiz 报告了 Nginx HTTP/2 实现中的未认证远程代码执行漏洞，所附 CVE 链接包括 CVE-2026-123007 和 CVE-2026-123633。据 Telegram 转述的 Xint 披露（NGINX2Root），5 个 nginx 漏洞加一个 Linux 内核缺陷可串联起来，让攻击者从 nginx 访客提权到主机 root；其中 CVE-2026-123007 是 HTTP/2 流控内存破坏，未认证即可在 worker 进程中执行命令。转述称 nginx 1.30.7 与 1.31.9 已于 11 月 18 日修复 10 个 CVE，Rapid7 已发布 PoC，暂无在野利用报告，无法升级时应关闭对外 HTTP/2。需要注意，提供的内容只有 CVE 链接和转述，Wiz 文章的技术细节未能核实，严重程度和可利用条件尚未得到独立确认。

hackernews · speedping · 11月18日 15:19 · [社区讨论](https://news.ycombinator.com/item?id=50547374)

**「背景」** 这批漏洞被 Xint 命名为 “NGINX2Root”，其中未认证远程代码执行对应的 CVE-2026-123007 位于 nginx 的 HTTP/2 实现。据 Xint 和 The Hacker News 报道，nginx 自 2015 年 9 月发布的 1.9.5 版本引入 HTTP/2，此后到 1.31.8 的所有官方发行版都含有这段有缺陷的代码，修复版本为 1.30.7 和 1.31.9。本文给出的来源内容只有 CVE 链接和评论，具体利用条件需以 Xint 等厂商的技术分析为准。

**「影响」** 运行对外 HTTP/2 的 nginx 管理员应尽快升级到 1.30.7 或 1.31.9；若无法立即升级，按转述可临时关闭对外 HTTP/2。由于 PoC 已公开，且有评论称修复提交在披露前约一周已出现在开源仓库，未打补丁的服务器面临的风险窗口可能比公告日期显示的更长。

**「社区讨论」** 评论者 black3r 指出，修复提交在披露前约一周已公开，且提交信息注明“Reported by Xint.io”，熟练的攻击者可借此做补丁比对；既然临时方案只是关闭 HTTP/2，他认为厂商本应提前发出提醒。对实际危害则有分歧：fduran 称 HTTP/2 在 nginx 中默认不启用，约 12% 的服务器在使用；testtestmetest 则声称利用需要约 128GB 的 HTTP/2 流量和特定 CPU 指令，认为问题被夸大，但这一说法尚未被来源证实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thehackernews.com/2026/11/10-year-old-nginx-http2-flaw-lets.html">10-Year-Old NGINX HTTP / 2 Flaw Lets Unauthenticated Attackers...</a></li>
<li><a href="https://xint.io/blog/nginx2root-remote-code-execution">NGINX 2 Root : New Remote Code Execution Vulnerabilities in nginx ...</a></li>

</ul>
</details>

**标签**: `#nginx`, `#remote-code-execution`, `#http2`, `#vulnerability-disclosure`, `#web-security`

---

<a id="item-tech-news-2"></a>
### [谷歌发布 Gemini 4 Neon：100 万 token 上下文，主打编程智能体](https://blog.google/innovation-and-ai/models-and-research/gemini-models/introducing-gemini-4-neon/) ⭐️ 7.5/10

据谷歌官方博客及 Telegram 渠道的转述，谷歌推出 Gemini 4 Neon，主打复杂软件工程、知识工作和科研工作流的快速端到端执行，已向开发者、企业以及 Google AI Pro/Ultra 订阅用户开放。定价为每百万输入 token 3 美元（缓存输入 0.15 美元）、输出 15 美元，支持 100 万 token 上下文。谷歌称其在 Artificial Analysis 编程智能体指数上以 58.6 分排名第一，在智能指数 xhigh 档以 61 分位列总榜第三，Terminal-Bench 4.1 得分 65.2%，默认 high 档单任务成本比 Carbon 低 32%。这些数据目前均为厂商报告的成绩，转述中没有给出测试方法，也未见独立复现。

telegram · zaihuapd · 11月19日 02:00

**「背景：Gemini 4 模型分层」** 原文对比的“Carbon”是 Gemini 4 系列中的另一款模型。据 Google DeepMind 的模型卡，Carbon 定位于复杂知识工作、工程、网络安全和科学推理中的长周期智能体任务，模型卡标注日期为 2026 年 11 月 10 日。同一页面称 Neon 介于深度与效率之间，面向高频复杂工作流，系列中还有负责日常快速执行的 Hydrogen。因此，Neon 的“成本降低 32%”是与同系列的旗舰 Carbon 比较，而不是跨厂商比较；该数字仍是厂商口径，尚无独立验证。

**「影响」** 对正在为编程智能体选型的开发者来说，Neon 提供了一个有明确价格和长上下文的新选项。不过“成本降低 32%”所依据的任务集和对比设置并未说明，Carbon 的具体定位在转述中也没有解释，因此采用前最好用自己的真实任务测一下实际成本和成功率。

**「社区讨论」** Hacker News 评论者 declanjackson 认为，Neon 的综合智能高于 Carbon，但 Carbon 仍被定位为“长程任务”模型，在 CritPt 这类研究级推理评测中得分更高。也有用户抱怨模型命名越来越难与具体用途对应，还有用户称自己的实际体验中 Gemini 不如 Opus 5.5，尽管基准成绩相近，这些属于个人主观感受。另一位用户观察到 OpenRouter 上 Neon 的速度约为每秒 127 token，明显快于 Carbon 的 46 token，但这是某一时刻的观测，不代表稳定表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-neon/">Gemini 4 Neon - Model Card — Google DeepMind</a></li>
<li><a href="https://deepmind.google/models/model-cards/gemini-4-carbon/">Gemini 4 Carbon - Model Card — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#Gemini 4 Neon`, `#Google`, `#LLM release`, `#coding agents`, `#model pricing`

---

<a id="item-tech-news-3"></a>
### [Ruby 公布 Regexp 与 String 大小写转换的多个内存漏洞](https://www.ruby-lang.org/en/news/2026/11/18/multiple-vulnerabilities-in-regexp-and-string/) ⭐️ 7.0/10

Ruby 官方发布安全公告,披露 Regexp 和 String 大小写转换代码中的多个漏洞。社区讨论提到的细节包括:Windows-1252 编码下 ß 转大写会变成 “SS”,可能造成缓冲区溢出;Shift\_JIS 字符串在超过 4GB 时调用 downcase 也存在溢出问题。需要注意,本条目未提供公告正文,具体严重程度、受影响版本和修复版本均无法确认,上述技术细节只来自评论者的分析和复现,请以官方公告为准。

hackernews · runesoerensen · 11月18日 23:52 · [社区讨论](https://news.ycombinator.com/item?id=50554038)

**「背景：大小写转换为何会出现内存问题」** Ruby 的 String 提供 upcase、downcase 等大小写转换方法，按字符串编码的规则逐字符映射（见 Ruby 官方文档对 String 大小写方法的说明）。有些映射会改变长度，例如评论者 tptacek 指出，Windows-1252 下的 ß 转大写会变成 “SS”，输出需要比输入更多的空间。这类转换在 C 语言层实现，如果缓冲区扩容或长度计算有误，就可能造成内存越界写入。由于未能获取公告原文，具体受影响版本和严重程度仍无法确认。

**「对 Ruby 用户的影响」** 仍在运行 Ruby 3.2 及更早版本的用户不会获得这批修复，因为这些分支已经终止维护，只能升级到仍受支持的版本。oss-security 的通告称这次共披露七个漏洞。同日发布的 Ruby 3.3.14 注明包含安全修复，3.3 分支用户应尽快升级。对网站和服务来说，凡是会对不可信输入调用 \`upcase\`、\`downcase\` 或使用 Regexp 的场景，尤其是涉及 Windows-1252、Shift\_JIS 等非 UTF-8 编码的场景，都应优先排查并升级。这里没有核实各漏洞的具体严重程度和全部受影响版本，请以官方通告为准。

**「社区讨论」** tptacek 认为 Windows-1252 的 ß→SS 漏洞很有意思:转换代码似乎逐字符检查缓冲区余量,当字符串末尾是 ß 时就可能写越界。pentestercrab 给出了针对 Shift\_JIS 超大字符串 downcase 的复现脚本。另有评论者指出,公告致谢了 Ada Logics 的 Stephan Lipp 和 Anthropic,并据此认为 AI 正在发现成熟 C 代码中的内存破坏漏洞;这是评论者的推断,并非公告已证实的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.ruby-lang.org/en/master/String.html">class String - Documentation for Ruby 4.1</a></li>
<li><a href="https://www.openwall.com/lists/oss-security/2026/11/19/1">oss-security - Ruby: multiple vulnerabilities in Regexp and ...</a></li>
<li><a href="https://www.ruby-lang.org/en/news/2026/11/18/ruby-3-3-14-released/">Ruby 3.3.14 Released | Ruby - Ruby Programming Language</a></li>
<li><a href="https://seclists.org/oss-sec/2026/q4/782">oss-sec: Ruby: multiple vulnerabilities in Regexp and String ...</a></li>

</ul>
</details>

**标签**: `#ruby`, `#security-vulnerability`, `#memory-safety`, `#string-encoding`, `#ai-vulnerability-discovery`

---

<a id="item-tech-news-4"></a>
### [Genie 4 通过 Project Genie 上线,面向符合条件的 AI Ultra 订阅用户](https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/) ⭐️ 7.0/10

Google DeepMind 宣布 Genie 4 已通过 Project Genie 提供使用。根据评论和分析摘要,访问对象似乎是符合条件的 Google AI Ultra 订阅用户。目前提供的材料只有标题和少量评论,没有正文,因此 Genie 4 的具体能力、基准测试、技术改动和地区范围都无法核实。

hackernews · leumon · 11月18日 18:49 · [社区讨论](https://news.ycombinator.com/item?id=50550415)

**「背景」** Genie 是 Google DeepMind 的“世界模型”系列,能根据输入生成可实时交互的模拟环境,而非只输出固定的视频。Project Genie 是 Google 面向消费者的体验入口。据 Google 页面,Genie 4 此前仅作为研究预览提供给受信任的测试者,如今 Project Genie 开始向符合条件的 Google AI Ultra 订阅用户推送新体验。评论中有用户称其 Ultra 账户仍显示 Genie 3,这可能与地区或推送进度有关,但目前没有官方说明。

**「影响」** 对想试用的用户来说,是否能用上 Genie 4 取决于订阅资格和所在地区。有评论者称,他的英国非 Workspace 账号显示 Ultra 对应的是 Genie 3,而 Workspace 账号似乎无法订阅 Ultra。这说明购买前最好先在自己的账号和地区确认实际可用的版本;不过这只是单个用户的反馈,不能代表官方的完整发布范围。

**「社区讨论」** 讨论主要围绕访问方式和更广泛的担忧展开:kingrolo 抱怨 Google 对订阅资格和地区可用性说明不清;alecst 则认为社区更多在谈价格和能力,较少讨论这类技术可能带来的负面后果。也有评论者认为,这类世界模型将来或许能成为游戏引擎的一种形态,但这属于个人推测,材料中没有相关证据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/google-deepmind/genie-4-now-available-project-genie/">Project Genie update featuring Genie 4 - The Keyword</a></li>
<li><a href="https://deepmind.google/models/genie/">Genie 4 — Google DeepMind</a></li>

</ul>
</details>

**标签**: `#Genie 4`, `#world models`, `#Google DeepMind`, `#generative AI`, `#product availability`

---

<a id="item-tech-news-5"></a>
### [Quad9 因法国法院要求 DNS 封锁而退出法国](https://techstackups.com/articles/quad9-leaves-france-dns-blocking/) ⭐️ 6.5/10

一篇文章认为,DNS 解析器不是执行反盗版封锁的合适位置,起因是公共 DNS 服务 Quad9 在法国法院下令封锁后退出法国。文章正文未能获取,因此具体的法院命令内容、涉及的域名、退出时间和技术细节均无法从现有材料核实。评论中有用户贴出 Quad9 和 Cloudflare 的相关博客链接,但这些链接的内容同样未在材料中提供。

hackernews · ritzaco · 11月18日 13:18 · [社区讨论](https://news.ycombinator.com/item?id=50545958)

**「背景：公共 DNS 解析器与法国的封锁令」** Quad9 是一家非营利的公共 DNS 解析器，负责把域名解析为 IP 地址，因此法院可以要求它拒绝解析被指控侵权的域名，以此阻断用户访问。据 TorrentFreak 和 CyberInsider 10 月下旬的报道，巴黎法院因涉嫌传播未经授权的体育赛事转播，向 Quad9 发出了封锁令，Quad9 将于 11 月 24 日停止为法国用户提供服务，成为第二家因此退出法国的 DNS 解析器。

**「社区讨论」** 有评论者\(trentnix\)认为,除起诉盗版者之外的“反盗版”手段,都可能成为压制政府不喜欢的言论的后门。另一位评论者\(skrebbel\)则追问,问题究竟出在法官理解有误,还是法官只是在依法办案、真正的问题在法律本身,并指出这决定了批评应指向法院还是立法者;这是提问,不是已查证的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cyberinsider.com/quad9-to-leave-france/">Quad9 to leave France after court orders piracy-related DNS ...</a></li>
<li><a href="https://torrentfreak.com/dns-resolver-quad9-will-leave-france-after-court-orders-piracy-blocking-penalty/">DNS Resolver Quad9 Will Leave France After Court Orders ...</a></li>

</ul>
</details>

**标签**: `#DNS`, `#Quad9`, `#internet censorship`, `#piracy`, `#France`

---

<a id="item-tech-news-6"></a>
### [微软 AI 在 Ignite 2026 发布七款新模型,主打性价比](https://microsoft.ai/news/microsoft-ignite-2026/) ⭐️ 6.0/10

微软 AI 在 Ignite 2026 相关页面中宣布了七款新模型,定位为“可扩展的性价比”。由于未提供原文内容,基准测试、定价、架构、上线时间和可用范围均无法核实,目前只能确认发布公告的标题与方向。社区讨论主要围绕其中的编程模型 MAI Code 2,以及微软与其他前沿模型厂商的竞争力。

hackernews · gmays · 11月18日 16:08 · [社区讨论](https://news.ycombinator.com/item?id=50548021)

**「背景」** 这组模型是微软在 Ignite 2026 上由 Microsoft AI\(MAI\)发布的,核心是被微软称为新旗舰智能体编码模型系列的 MAI Code 2,宣传重点是“性价比”,即以更低价格逼近竞品模型的表现。微软在官方文章和主题演讲稿中称,MAI Code 2 在面向 GitHub Copilot 日常企业编码任务的四项基准上平均达到 GPT 6.1 Sol 的 98% 表现,成本仅为其 40%;MAI Code 2 Flash 则称在 65% 的价格下与 GPT-6 Luna 相当。这些数字目前都来自微软自己的说明,尚未见独立评测验证。

**「社区讨论」** 有用户\(johnshahbazian\)称自己试用了 MAI Code 2,日常工作中表现不错,微软将其与 Opus 或 Sol 相提并论,他认为说得过去;另一位用户\(athrowaway3z\)则认为微软等厂商已接近 Opus 5 水平,削弱了对 Anthropic 高价的认可。这些都是个人的、未经验证的使用感受。另有评论认为微软应开放部分模型权重以争取市场份额,也有评论批评 Ignite 主题演讲缺乏创新,这些同样属于个人观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026/">Seven new world-class models at scalable price-performance ...</a></li>
<li><a href="https://microsoft.ai/news/microsoft-ignite-2026-mai-keynote/">Microsoft Ignite 2026: MAI keynote transcript | Microsoft AI</a></li>
<li><a href="https://windowsforum.com/news/microsoft-ignite-2026-mai-code-2-models-agent-365-governance-and-enterprise-ai-stack.453003/">Microsoft Ignite 2026: MAI Code 2 Models, Agent 365 ...</a></li>

</ul>
</details>

**标签**: `#Microsoft AI`, `#LLM models`, `#price-performance`, `#MAI Code`, `#AI industry competition`

---

<a id="item-tech-news-7"></a>
### [OpenAI 发文介绍用其模型推进芯片设计,细节有限](https://openai.com/index/advancing-chip-design-with-our-models/) ⭐️ 6.0/10

OpenAI 发布了题为“Advancing chip design with our models”的文章,介绍将其模型应用于芯片设计。但本次提供的材料没有正文,只有标题、链接和部分评论,因此具体的技术方法、使用的模型、性能结果和可用性都无法核实。评论中提到一款名为“Jalapeño”的芯片以及 RISC-V 设计,但这些信息来自评论者,未经原文证实。

hackernews · vighneshiyer · 11月18日 17:45 · [社区讨论](https://news.ycombinator.com/item?id=50549493)

**「背景」** 芯片设计通常先用 RTL（寄存器传输级代码）描述电路，再通过 EDA 工具完成综合、布局布线和仿真验证，结果常以 PPA（功耗、性能、面积）衡量；AI 辅助设计就是让模型参与改写电路或自动化这些流程。检索到的摘要称，OpenAI 的模型优化了其 Jalapeño 芯片中的电路并改进了 RISC‑V 核设计，第三方博客还提到相对基线最高有 14% 的 PPA 提升，并涉及 AMD GPU 的 RTL。这些数字来自二次转述，原文正文未能获取，具体评测方法和基线都无法核实。

**「影响」** 由于缺少原文内容,目前无法判断该工作对 EDA 从业者或芯片设计团队的具体影响。有评论者质疑相关 RISC-V 设计是否对外共享,若未开放,外部团队就难以复现或直接利用这些成果;在确认原文内容和开放程度之前,不宜据此调整工具链或工作流程。

**「社区讨论」** jacquesm 认为,AI 公司正向各行业扩张,并使用不对外开放的模型,这意味着它们在与自己的客户竞争,同时还掌握客户的动向。skyberrys 则分享了个人经验:把芯片设计当作软件问题,让智能体编写生成电路的代码并自动化 EDA 流程,还能照看多小时的仿真运行,但他的设计大部分是模拟电路,只有一小部分是 RTL。这属于个人经验,不是普遍结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/advancing-chip-design-with-our-models/">Advancing chip design with OpenAI models</a></li>
<li><a href="https://explainx.ai/blog/openai-amd-jalapeno-chip-design-astra-ppa-november-2026">OpenAI AMD Chip Design: 14% PPA in 5 Months (Nov 2026 ...</a></li>

</ul>
</details>

**标签**: `#chip design`, `#OpenAI`, `#EDA`, `#AI agents`, `#RISC-V`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美联储 10 月会议纪要:多数官员预计还需加息](https://www.cnbc.com/2026/11/18/fed-minutes-october-2026.html) ⭐️ 8.0/10

美联储 10 月会议纪要显示,几乎所有官员认为进一步加息“可能是适当的”,但委员会仍以 10 比 2 的投票将联邦基金利率维持在 3.75%–4%;库克和哈马克两人投票支持加息四分之一个百分点。

rss · CNBC Finance · 11月18日 19:41

**「背景」** 美联储担心与伊朗战争和特朗普关税相关的涨价\(多为暂时因素\)会变得根深蒂固;10 月 CPI 环比上涨 0.4%,核心 CPI 上涨 0.3%,均比预期高 0.1 个百分点。

**「影响」** 据 CME FedWatch,市场已完全计入 12 月 8–9 日会议加息四分之一个百分点,并认为 2027 年再加息两次的可能性较大,因此借贷成本可能继续上升;沃勒则表示 12 月可能需要加息半个百分点来“震动”市场。

**标签**: `#Federal Reserve`, `#FOMC minutes`, `#interest rates`, `#inflation`, `#AI financial risk`

---

<a id="item-finance-news-2"></a>
### [美联储理事沃勒称 12 月可能需加息 50 个基点](https://www.cnbc.com/2026/11/18/federal-reserve-governor-christopher-waller.html) ⭐️ 8.0/10

美联储理事沃勒周三表示，为遏制通胀，12 月 8 日至 9 日的议息会议上可能需要加息半个百分点（50 个基点），以“震慑市场”；期货市场目前完全定价的是加息 25 个基点（据 CME FedWatch）。

rss · CNBC Finance · 11月18日 15:13

**「背景」** 美联储 9 月进行了三年多来的首次加息，10 月维持利率不变；今年 2 月底美国和以色列对伊朗发动打击后，能源价格上涨，加上关税影响，多数通胀指标仍高于 3%，而美联储的目标是 2%。

**「影响」** 这只是沃勒个人的观点，并非美联储的决定：纽约联储主席威廉姆斯认为目前不需要采取剧烈行动，沃勒也表示，若 12 月加息 25 个基点并明确暗示 1 月再加息，也可以不加 50 个基点，但美联储主席沃什反对这类前瞻指引，因此 12 月的加息幅度仍存在不确定性。

**标签**: `#Federal Reserve`, `#interest rates`, `#inflation`, `#monetary policy`, `#FOMC`

---

<a id="item-finance-news-3"></a>
### [腾讯三季度营收低于预期，资本开支大幅超预期](https://api3.cls.cn/share/article/2537922?os=android&amp;amp;sv=8.8.5&amp;amp;app=cailianpress&amp;amp;selected=) ⭐️ 7.0/10

腾讯公布 2026 年第三季度财报:营收 2073 亿元,同比增长 8%,低于市场预期;归母净利润 636 亿元,同比增长 0.8%。当季资本开支为 814.33 亿元,远高于市场预估的 554 亿元,单季自由现金流为负 691 亿元。

telegram · zaihuapd · 11月18日 09:20

**「背景」** WorkBuddy 是腾讯推出的办公 AI 智能体工具，用户用自然语言描述需求，它可自主规划并执行任务，交付文档、表格、PPT 等成果。资本开支指企业用于购买设备、建设数据中心等长期资产的支出，自由现金流则大致是经营现金流扣除资本开支后剩下的现金。

**「影响」** 资本开支大幅增加,同时自由现金流\(经营现金流扣除资本开支后剩余的现金\)转为负值,说明本季公司投入明显多于现金回笼;但来源未说明其中多少属于 AI 投入,也未说明现金流为负的具体原因。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.workbuddy.cn/docs/workbuddy/Overview">WorkBuddy 简介 | WorkBuddy - AI Agent 办公新范式</a></li>

</ul>
</details>

**标签**: `#Tencent`, `#Q3 earnings`, `#AI capex`, `#free cash flow`, `#China tech`

---