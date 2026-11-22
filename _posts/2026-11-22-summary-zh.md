---
layout: default
title: "Horizon Summary: 2026-11-22 (ZH)"
date: 2026-11-22
lang: zh
---

> 从 28 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [黎曼猜想的 Lean 形式化证明发布，约 1700 万行代码获社区认证](#item-tech-news-1) ⭐️ 8.0/10
2. [微软发布 Windows RDMA over USB4 开发者预览，多台 PC 可合跑本地大模型](#item-tech-news-2) ⭐️ 7.5/10
3. [Linebender 的 Raph Levien 发文，为新的 Rust GUI 项目提建议](#item-tech-news-3) ⭐️ 7.0/10
4. [GPGME 2.3.0 之前版本存在 double free 漏洞,被报道可致远程代码执行](#item-tech-news-4) ⭐️ 7.0/10
5. [特朗普称仍支持卢特尼克，望已辞职的黄仁勋道歉后回归](#item-tech-news-5) ⭐️ 7.0/10
6. [OpenRouter 邮件警告：发往 MiniMax 模型的提示词疑被第三方读取](#item-tech-news-6) ⭐️ 6.5/10
7. [浙江大学在超导芯片「天目 2 号」上首次真机实现 QRAM](#item-tech-news-7) ⭐️ 6.5/10
8. [特斯拉开始在海外推送 FSD v15，称安全关键场景处理提升 25 倍](#item-tech-news-8) ⭐️ 6.5/10
9. [显示器内置以太网/USB 集线器使 2.5G 下载速度降低约 75%](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [习近平借主办峰会扩大外交影响力](#item-finance-news-1) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [黎曼猜想的 Lean 形式化证明发布，约 1700 万行代码获社区认证](https://leanprover-community.github.io/blog/posts/riemann-hypothesis/) ⭐️ 8.0/10

据转载的 Lean 社区博客内容，Levent Alpöge 于 2026 年 11 月 20 日发布了黎曼猜想的 Lean 形式化证明，代码库约 1700 万行。11 月 21 日，Lean FRO 与 Mathlib Initiative 联合声明认证该命题与证明均正确：命题与 Mathlib 中的 RiemannHypothesis 一致，代码库可无错编译，多个独立证明检查器验证证明有效。需要注意，未提供博客原文，上述内容来自转载摘要；评论称证明由 Claude 与人类专家协作完成，并涉及广义黎曼猜想（GRH），但具体范围未能在原文中核实。

hackernews · g-b-r · 11月21日 14:36 · [社区讨论](https://news.ycombinator.com/item?id=50589618)

**「背景：形式化验证与信任基础」** Lean 是交互式定理证明器，由内核逐步检查形式化证明；Mathlib 是其主要数学库，其中已有 \`RiemannHypothesis\` 这一形式化命题。因此“黎曼猜想已被验证”是否成立，取决于该命题是否忠实、代码库能否无误编译，以及检查器本身是否可靠。Lean 社区博客称，该命题已由 Lean 与数论专家审核，Alpöge 的代码库可正确编译。Alpöge 是数论学者，后加入 Anthropic；第三方报道称这一证明由 Claude 辅助完成，但该说法不是来自 Lean 社区博客的原文。

**「影响」** 对数学界和形式化社区而言，这一结果的可信度取决于命题是否忠实表达、各检查器是否真正独立。有评论者提到此前曾有伪造的反驳通过某个检查器，因此读者在引用该结论前，应查阅社区声明中的命题定义和检查器清单。

**「社区讨论」** 有评论者认为，多种语言实现的内核并带有自身一致性证明，使利用漏洞通过验证的可能性极小；另一些评论者则质疑检查器并不像宣传的那样独立，并提到 Claude 同时参与了内核提交和证明编写，形成某种“单一生态”。还有评论者指出，人类专家参与降低了模型钻空子的风险，但对命题表述是否忠实仍存疑虑，这些均为评论者观点，而非已证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Levent_Alp%C3%B6ge">Levent Alpöge - Wikipedia</a></li>
<li><a href="https://leanprover-community.github.io/blog/posts/riemann-hypothesis/">Lean verification of the Riemann Hypothesis | Lean community blog</a></li>
<li><a href="https://kingy.ai/blog/levent-alpoge-claude-riemann-hypothesis-proof/">Riemann hypothesis proof verified in Lean</a></li>

</ul>
</details>

**标签**: `#Lean`, `#Riemann Hypothesis`, `#formal verification`, `#AI theorem proving`, `#Claude`

---

<a id="item-tech-news-2"></a>
### [微软发布 Windows RDMA over USB4 开发者预览，多台 PC 可合跑本地大模型](https://videocardz.com/newz/microsoft-brings-rdma-over-usb4-to-windows-allowing-multiple-pcs-to-run-one-local-ai-model) ⭐️ 7.5/10

微软发布了 Windows 的 RDMA over USB4 开发者预览。多台 PC 通过普通 USB4 线缆连接后，可共享内存与 GPU 算力，运行同一个本地大模型，无需专用网卡或交换机。演示中，三台 AMD Ryzen AI Max+ 395 机器以 4-bit 量化运行 Qwen3-235B-A22B，速度约为 18.5 token/s。该功能将通过 Windows Insider 推送，目前仍处于预览阶段。

telegram · zaihuapd · 11月21日 06:13

**「背景：RDMA 与 NetworkDirect」** RDMA（远程直接内存访问）允许一台机器在较少占用操作系统和 CPU 的情况下，直接读写另一台机器上经授权的内存，通常用于数据中心的高速互联。据微软技术社区博客和 Guru3D 的介绍，此次预览是把 Windows 在数据中心 RDMA 网卡上使用的 NetworkDirect API 适配到 USB4 链路上，让兼容的推理框架能够把一个模型分布到多台 PC 的内存和 GPU 算力上运行。

**「影响」** 如果该功能按演示工作，拥有多台支持 USB4 的 PC 的开发者和爱好者，可以不购买专用网络设备，就尝试跨机器运行单机内存放不下的大模型。不过，来源没有给出延迟、带宽、框架支持和测试方法，18.5 token/s 也只来自一次演示，实际效果仍需独立测试验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://techcommunity.microsoft.com/blog/microsoftusbblog/introducing-rdma-over-usb4%C2%AE-on-windows-run-larger-local-ai-models-across-pcs/4574602">Introducing RDMA over USB 4 ® on Windows : run larger local AI ...</a></li>
<li><a href="https://www.guru3d.com/story/microsoft-previews-usb4-links-that-let-windows-pcs-pool-memory-and-gpu-resources/">Microsoft previews USB 4 links that let Windows PCs pool memory ...</a></li>

</ul>
</details>

**标签**: `#RDMA`, `#USB4`, `#local-LLM-inference`, `#Windows`, `#distributed-inference`

---

<a id="item-tech-news-3"></a>
### [Linebender 的 Raph Levien 发文，为新的 Rust GUI 项目提建议](https://linebender.org/blog/next-100-guis/) ⭐️ 7.0/10

Linebender 的 Raph Levien\(raphlinus\)发表博文《Advice for the next 100 Rust GUIs》，面向正在开发新 Rust GUI 工具包的人给出建议。由于未能获取文章正文，具体建议、结论和技术细节无法在此核实，以下只能依据标题、作者和评论区反映的讨论方向。

hackernews · raphlinus · 11月21日 21:17 · [社区讨论](https://news.ycombinator.com/item?id=50593737)

**「背景」** Linebender 是围绕 Rust 图形与界面开发的开源社区，据分析材料，其项目包括 Xilem、Vello、Druid 和 Parley，涉及 UI 框架、GPU 渲染和文本布局。Rust 的 GUI 生态目前较为分散，没有公认的标准方案，因此这类面向开发者的经验总结值得关注。

**「社区讨论」** 评论多围绕实际开发中的难点。weinzierl 说，他在 Bevy 里播放视频时，因为应用只拥有一个 swapchain，视频无法占用独立的硬件图层，只能把帧复制成纹理再由引擎合成；skhameneh 则说自研 Rust GUI 进展缓慢，文本换行、光标定位和文本选择等细节耗时最多。另有评论者推荐其他方案：tauchunfall 提到 Native Shell 未被收入 2026 年的 Rust GUI 库调查，dv\_dt 认为 GUI 应对异步有明确设计，并以 Qt 的信号/槽为例，jacoplane 则选择 Flutter 加 flutter\_rust\_bridge。这些都是评论者的个人经验和看法，并非文章的结论。

**标签**: `#rust`, `#gui`, `#linebender`, `#ui-frameworks`, `#rendering`

---

<a id="item-tech-news-4"></a>
### [GPGME 2.3.0 之前版本存在 double free 漏洞,被报道可致远程代码执行](https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html) ⭐️ 7.0/10

GnuPG 项目发布公告,披露 GPGME 库中的一个 double free 漏洞,标题称其可导致 RCE。据评论中转引的公告内容,2.3.0 之前的 GPGME 均受影响,无论是共享库、DLL 还是静态链接。漏洞由 Johan Carlsson 发现,GitLab 于 2026 年 11 月 12 日通知 GnuPG,原定 11 月 25 日协调披露,因 GitLab 因另一个漏洞需提前更新,最终于 11 月 20 日提前披露。由于未能获取公告原文,具体利用条件和影响范围尚未核实。

hackernews · gdgghhhhh · 11月21日 08:32 · [社区讨论](https://news.ycombinator.com/item?id=50587208)

**「背景」** GPGME 是供应用程序嵌入、用来调用 GnuPG 功能的 C 库,所以这次的漏洞出在 GPGME,不在 GnuPG 主程序里。GnuPG 公告称,漏洞由 Johan Carlsson 发现,GitLab 于 2026-11-12 通知项目方。原定 11 月 25 日协调披露,因 GitLab 要为新的 Ruby2Shell 漏洞提前更新,GPGME 的漏洞也在 11 月 20 日提前公开。The Hacker News 报道称,修复版本是 GPGME 2.3.1,2.3.0 从未公开发布。这与评论中“2.3.0 之前的版本受影响”的说法略有出入,具体影响范围应以官方公告为准。

**「影响」** 按评论转引的公告,Gpg4win、GnuPG Desktop、多数邮件客户端、许多 XMPP 客户端、Samba 和 Flatpak 等软件使用 GPGME,静态链接的程序也受影响,因此维护者需要检查自己链接的 GPGME 版本并升级到 2.3.0 或更高版本。GitLab 因支持签名提交,其验证路径存在代码执行风险,已发布 Omnibus 相关补丁,自托管用户应尽快更新。

**「社区讨论」** 有评论者 mik1998 指出,这只是 double free,并非完整的 RCE 利用链,质疑漏洞报告有意夸大。另有评论称 Red Hat 早在约五年前就修复了该问题而上游遗漏,但这一说法依据不足,仍待验证。另一位用户询问 apt 等是否受影响,在已有评论中尚无确认。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://lists.gnupg.org/pipermail/gnupg-announce/2026q4/000517.html">[Announce] GnuPG Security Advisory for GPGME (T8557,CVE-2026 ...</a></li>
<li><a href="https://thehackernews.com/2026/11/gnupg-warns-critical-gpgme-flaw-could.html">GnuPG Warns Critical GPGME Flaw Could Expose App Data via ...</a></li>

</ul>
</details>

**标签**: `#GnuPG`, `#GPGME`, `#vulnerability`, `#memory-safety`, `#security-disclosure`

---

<a id="item-tech-news-5"></a>
### [特朗普称仍支持卢特尼克，望已辞职的黄仁勋道歉后回归](https://www.reuters.com/world/us/trump-says-he-still-backs-lutnick-urges-nvidias-huang-apologize-2026-11-20/) ⭐️ 7.0/10

据 Telegram 频道转述的路透社报道，特朗普 11 月 20 日表示仍支持商务部长卢特尼克，称其“做得很好”，尽管英伟达风波令外界质疑他对中国芯片销售的处理。报道称英伟达 CEO 黄仁勋已辞职，特朗普说希望他“郑重道歉后回归”，并称已与习近平谈及此事。财长贝森特则称相关通话并未涉及黄仁勋，与特朗普的说法相矛盾。

telegram · zaihuapd · 11月21日 05:03

**「背景」** 美国商务部负责管理先进芯片对华出口的许可与管制，因此商务部长卢特尼克处理对华芯片销售的方式，与英伟达这类供应商的业务直接相关。原文只说黄仁勋已辞职，没有交代原因，也没有说明争议的具体内容。搜索摘要显示，其他媒体也在报道特朗普呼吁黄仁勋道歉并回归，并提到众议院民主党人正在调查英伟达与商务部官员的往来；有摘要还提到辞职与个人传闻有关，但这一说法尚未获原文证实，不宜当作定论。

**「影响」** 这条消息的核心事实尚未得到充分验证：转述文本没有说明黄仁勋辞职的原因、争议的具体内容，也没有提供路透社原文细节。对关注英伟达对华销售和出口管制的读者，应以路透社原文及英伟达、白宫的正式表态为准，不宜仅凭这条简短转述判断公司人事或政策走向。

<details><summary>参考链接</summary>
<ul>
<li>President Donald Trump said he would like to see former Nvidia ...</li>
<li>Trump Urges Nvidia to Reinstate Jensen Huang Amid Congressional ...</li>

</ul>
</details>

**标签**: `#Nvidia`, `#chip export controls`, `#US-China tech policy`, `#Jensen Huang`, `#AI hardware`

---

<a id="item-tech-news-6"></a>
### [OpenRouter 邮件警告：发往 MiniMax 模型的提示词疑被第三方读取](https://news.ycombinator.com/item?id=50585962) ⭐️ 6.5/10

据转述的 OpenRouter 用户邮件，发往 MiniMax 模型的请求内容可能被第三方读取。安全研究者在 2026 年 7 至 10 月向这些模型发送了含测试 URL 的提示词，第三方在 40 到 130 小时后访问了这些 URL。OpenRouter 称问题出在 MiniMax 及其转发方 AtlasCloud、Novita、StreamLake，已下架相关端点的“零数据保留”标签，并建议涉及敏感凭证的用户更换 API Key 和密码。目前 OpenRouter 官网尚未公布该通知，来源是 Telegram 对邮件内容的二手转述，泄露原因和影响范围均不明确。

telegram · zaihuapd · 11月21日 06:53

**「背景」** OpenRouter 是一个 LLM API 聚合平台，会根据实时数据把请求路由到不同的模型和推理服务商，因此提示词实际由第三方服务商处理。「零数据保留」标签用于标明端点不会留存用户提示词内容，这次被下架的正是这一标签。研究者的做法是在提示词中埋入测试 URL（canary），若之后有第三方访问这些 URL，就说明内容被读取。

**「影响」** 凡是通过 OpenRouter 调用过上述 MiniMax 端点、且提示词中包含 API Key、密码等凭证或敏感数据的用户，应按邮件建议轮换凭证，并检查这些内容是否需要视为已暴露。在原因查明之前，不应把相关端点的“零数据保留”承诺当作有效保障。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openrouter.ai/">OpenRouter</a></li>

</ul>
</details>

**标签**: `#OpenRouter`, `#LLM privacy`, `#MiniMax`, `#data retention`, `#API security`

---

<a id="item-tech-news-7"></a>
### [浙江大学在超导芯片「天目 2 号」上首次真机实现 QRAM](https://finance.sina.com.cn/stock/2026-11-21/doc-iniznhsk3530826.shtml) ⭐️ 6.5/10

据新浪财经转述，浙江大学团队在自研超导量子芯片「天目 2 号」上，首次在真实硬件上实现了量子随机存储器（QRAM），成果称已发表于《自然·物理》。芯片上运行了可调取 4 位和 8 位数据的原型，准确率分别为 80.9%和 60.4%。团队称其线路深度比未优化方案降低 30%以上，并首次验证该架构具备局部抗噪特性。团队下一步将推进 QRAM 的规模化研究。

telegram · zaihuapd · 11月21日 08:31

**「背景：QRAM 是什么」** QRAM（量子随机存储器）的作用是让量子计算机以叠加态方式一次访问多个经典数据地址，是许多需要加载大量经典数据的量子算法所依赖的基础组件，但此前多停留在理论架构层面。外部报道称，浙江大学此次采用的是 bucket-brigade（水桶接力）架构，并在超导处理器上实现了 4 位和 8 位 QRAM，查询保真度分别约为 81% 和 60%。这些报道发表于 2026 年 6 月，与本条新闻的数据一致，但主要是对同一成果的转述，并非独立复现。

**「影响」** QRAM 是许多量子算法读取经典数据时所需的基础部件，此次演示给出了硬件层面的初步数据点。不过原型只有 4 位和 8 位，8 位时准确率降至 60.4%，距离实用规模仍有明显差距。另外，30%的线路深度降低和局部抗噪特性只是报道中的说法，原文没有给出架构、噪声模型和对比基准，需要查阅论文原文核实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://thequantuminsider.com/2026/06/05/chinese-scientists-demonstrate-quantum-random-access-memory-architecture-aimed-at-solving-data-bottleneck/">Chinese Scientists Demonstrate Quantum Random Access Memory ...</a></li>
<li><a href="https://thequbitreport.com/hardware/2026/06/06/zhejiang-university-achieves-breakthrough-with-worlds-first-superconducting-qram-prototype/">Zhejiang University Achieves Breakthrough with World’s First ...</a></li>

</ul>
</details>

**标签**: `#quantum computing`, `#QRAM`, `#superconducting qubits`, `#Zhejiang University`, `#Nature Physics`

---

<a id="item-tech-news-8"></a>
### [特斯拉开始在海外推送 FSD v15，称安全关键场景处理提升 25 倍](https://x.com/Tesla/status/2124222447855743019) ⭐️ 6.5/10

特斯拉据称已于当日开始在海外推送 FSD v15。官方称新版本对安全关键场景的处理能力提升至 25 倍，并新增“Tesla Reality View”可视化界面，可在车机屏幕上叠加摄像头画面与 FSD 行驶规划，支持全屏、地图或分屏视图以及安静模式。其他改动包括：导航将转弯等信息叠加显示，转向灯提示音更轻柔并逐渐减弱，同时优化了坑洼、碎片等路况的行驶体验，以及学校区域和恶劣天气下的速度控制。来源是特斯拉官方帖子的转述，未说明适用的硬件、具体地区、推送节奏或版本号细节。

telegram · zaihuapd · 11月22日 00:03

**「背景」** FSD（Full Self-Driving，全自动驾驶）是特斯拉面向车主的驾驶辅助软件，采用端到端神经网络，由摄像头画面直接生成驾驶决策。此前有报道称 v15 将随节日更新推出，马斯克称其新界面会“以令人震撼的方式渲染现实”（Not a Tesla App）。需要注意，“25 倍”是特斯拉自己的说法，目前未见指标定义、对比基线或独立测评。

**「影响」** “25 倍”是特斯拉自己的说法，来源中没有给出指标定义、对比基线或测试方法，因此无法据此判断实际安全水平的变化。海外车主可先留意自己的车辆是否收到推送，并把 Reality View 和各项路况、速度控制的改进当作需要实际验证的功能；FSD 仍需驾驶员保持监督。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.notateslaapp.com/news/5057/tesla-fsd-v15-coming-next-month-with-holiday-update-musk">Tesla FSD V 15 Arriving Next Month: Home Garage... - Not a Tesla App</a></li>
<li><a href="https://www.youtube.com/watch?v=eNBqkc7V1nU">Introducing Tesla Self-Driving V 15 - YouTube</a></li>

</ul>
</details>

**标签**: `#Tesla FSD`, `#autonomous driving`, `#FSD v15`, `#driver assistance`, `#product release`

---

<a id="item-tech-news-9"></a>
### [显示器内置以太网/USB 集线器使 2.5G 下载速度降低约 75%](https://blog.tymscar.com/posts/studiodisplayethernet/) ⭐️ 6.0/10

一篇博客文章记录了一次网络排障:作者在 2.5G 对称宽带下,通过显示器内置的 USB/以太网路径联网,下载速度下降约 75%,换用另一种网卡适配器后恢复。文章原文未能获取,以下技术解释来自评论区的转述:经显示器转接增加了延迟,笔记本无法及时确认\(ACK\)数据包,导致适配器缓冲区被填满并丢包。该结论未经独立验证,也没有具体型号或测试数据可供核对。

hackernews · soheilpro · 11月21日 10:36 · [社区讨论](https://news.ycombinator.com/item?id=50587875)

**「背景」** TCP 下载依赖接收端及时回送确认包。若链路中的 USB 集线器或适配器增加延迟,又有缓冲区限制,就可能出现排队、溢出和丢包,从而拉低吞吐。这类行为在 USB 网卡与集线器中通常很不透明,用户很难直接看到。

**「影响」** 如果你通过显示器、扩展坞或 USB 集线器使用高速以太网,而速度明显低于线路速率,可以直接对比使用其他适配器或直连时的速度。评论中有用户提到,在 MacBook 加雷电扩展坞的环境下遇到类似问题,最终启用流量控制后情况改善到可接受程度,但这只是个人经验,并非普遍结论。

**「社区讨论」** 评论者 fancyfredbot 指出,不少人误解了文章,真正的原因是经显示器转接带来的额外延迟使笔记本来不及确认数据包,进而造成适配器缓冲区被填满并丢包;manarth 则认为问题本质在于 USB 网络交换设备,是不是显示器并不关键。另有读者 gh123man 称自己多年来在 MacBook 与雷电扩展坞上遇到类似问题,最终靠启用流量控制缓解。

**标签**: `#networking`, `#USB hub`, `#troubleshooting`, `#hardware`, `#Ethernet`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [习近平借主办峰会扩大外交影响力](https://www.cnbc.com/2026/11/21/china-xi-trump-putin-global-diplomacy-shenzhen.html) ⭐️ 6.0/10

特朗普、习近平和普京周四在深圳举行首次三方面对面会晤，这是亚太经合组织（APEC）领导人会议的一部分；习近平还宣布，中国将向亚太地区提供 2000 万美元支持。据中方通报，三方讨论了乌克兰、中东和朝鲜半岛问题，目前报道未提及具体协议。

rss · CNBC Finance · 11月21日 06:00

**「背景」** 去年 9 月,习近平在天津上合组织峰会期间曾与普京、印度总理莫迪合影;中国还曾在 2023 年促成沙特与伊朗恢复外交关系,近年来越来越多地扮演东道主和斡旋者的角色。

**「影响」** 分析人士认为，中国正通过主办多边峰会扩大影响力，并把外交重点放在贸易、投资等经济合作上；但各国优先事项不同，要达成共识并不容易。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/2025_Tianjin_SCO_summit">2025 Tianjin SCO summit - Wikipedia</a></li>

</ul>
</details>

**标签**: `#China diplomacy`, `#APEC Shenzhen`, `#US-China relations`, `#Xi Jinping`, `#geopolitics`

---