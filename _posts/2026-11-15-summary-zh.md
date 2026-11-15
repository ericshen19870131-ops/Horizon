---
layout: default
title: "Horizon Summary: 2026-11-15 (ZH)"
date: 2026-11-15
lang: zh
---

> 从 48 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [星舰第 15 次试飞：飞船在轨返回后被塔架机械臂捕获，助推器溅落](#item-tech-news-1) ⭐️ 8.0/10
2. [Lovable 应用因 Row-Level Security 不足泄露护照信息和 20 万条私信](#item-tech-news-2) ⭐️ 7.5/10
3. [Project Zero 将漏洞披露窗口定为 90 天,并计划逐步缩短](#item-tech-news-3) ⭐️ 7.0/10
4. [意大利监管机构因 Facebook 安卓应用读取相册罚 Meta 8.05 亿欧元](#item-tech-news-4) ⭐️ 7.0/10
5. [Cloudflare 以 Apache 2.0 开源面向 AI 代理的无状态浏览器 Kitesurf](#item-tech-news-5) ⭐️ 6.5/10
6. [特斯拉 Cybercab 订阅条款：车价 29,990 美元，另需月付 299 美元](#item-tech-news-6) ⭐️ 6.5/10
7. [NVIDIA 称用 vLLM 在两台 DGX Station 上以 607.8 tok/s 运行 GLM-5.3](#item-tech-news-7) ⭐️ 6.0/10
8. [PyPI 完成项目页面改版，更清晰展示来源与安全信号](#item-tech-news-8) ⭐️ 6.0/10
9. [美国国税局 Direct File 免费报税系统源码在 GitHub 公开](#item-tech-news-9) ⭐️ 6.0/10
10. [Show HN:约 200 行纯 JAX 复现 DeepSeek V3 架构](#item-tech-news-10) ⭐️ 6.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [星舰第 15 次试飞：飞船在轨返回后被塔架机械臂捕获，助推器溅落](https://www.spacex.com/launches/starship-flight-15) ⭐️ 8.0/10

据 SpaceX 官方宣布及转载的 Telegram 消息，星舰第 15 次试飞中，飞船在轨飞行约 22.5 小时、绕地球约 14 圈后返回得州 Starbase，并首次在轨道返回后被发射塔机械臂直接捕获。飞船还部署了 26 颗 Starlink V3 卫星，其中 3 颗带摄像头，用于检查隔热瓦。超重型助推器因技术问题中止返场，改在墨西哥湾受控溅落并爆炸，具体原因未公布，因此未能实现两级同时回收。需要说明的是，原始来源只有推文和视频链接，上述细节来自转载消息，我们未能独立核实。

hackernews · ls612 · 11月14日 21:22 · [社区讨论](https://news.ycombinator.com/item?id=50500963)

**「背景：星舰回收路线」** “塔捕”是指火箭或飞船垂直返回发射塔，由机械臂夹住承接点，而不是着陆或落海。据维基百科，Flight 14 中 Booster 21 在墨西哥湾受控溅落，Ship 41 入轨并部署了 26 颗 Starlink V3；本次 Flight 15 的目标是首次同时回收助推器和飞船。多家报道称，助推器中止返场并在墨西哥湾爆炸，飞船则在约 22.5 小时后完成塔捕，因此两级同时回收尚未实现。

**「社区讨论」** Hacker News 评论者多持肯定态度，有人称星舰是“做对了的航天飞机”：全可复用、没有固体助推器，轨道器位于顶部。也有人指出，隔热罩能否经受重复使用是关键，最终入轨质量分数仍不明确，下一步是双回收和同一飞船的再次飞行。这些均为评论者的看法或推测，并非已证实的结果。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Starship_flight_15">Starship flight 15 - Wikipedia</a></li>
<li><a href="https://xenospectrum.com/en/starship-flight-15-orbit-starlink-v3-booster-splashdown/">Starship Flight 15: Booster Explodes Over the Gulf, but Ship ...</a></li>
<li><a href="https://tech.yahoo.com/science/articles/spacex-says-starship-flight-15-145300206.html">SpaceX says Starship Flight 15 booster aborted &#x27;chopsticks ...</a></li>

</ul>
</details>

**标签**: `#SpaceX`, `#Starship`, `#reusable rockets`, `#aerospace engineering`, `#hardware`

---

<a id="item-tech-news-2"></a>
### [Lovable 应用因 Row-Level Security 不足泄露护照信息和 20 万条私信](https://www.crissyfield.de/research/lovable-en/) ⭐️ 7.5/10

安全研究团队 Crissy Field 报告称,用 AI 应用生成工具 Lovable 构建的应用暴露了护照信息和超过 20 万条私人消息。作者和 Lovable 安全负责人 Igor 都在评论中指出,根本原因是 Supabase 的 Row-Level Security\(行级安全\)配置不足。Lovable 称,平台会在发布前自动扫描每个应用,并向所有用户免费提供更深入的 SAST 扫描、一键“Fix”和自动修复功能。由于原文正文未提供,受影响应用的数量、研究方法和泄露规模均无法独立核实,以上数字仅来自标题和摘要。

hackernews · armcat · 11月14日 17:43 · [社区讨论](https://news.ycombinator.com/item?id=50499017)

**「背景:Supabase 行级安全与此次排查」** Lovable 是通过对话生成应用的 AI 开发平台,其应用常把 Supabase\(托管的 Postgres 后端\)作为数据库,浏览器前端可直接调用数据接口,因此谁能读写哪些数据,基本取决于行级安全\(RLS\)策略。如果策略缺失或过于宽松,任何人只要在浏览器里查看网络请求,就能取回数据库记录,不需要复杂的攻击手段。据 Cybernews 等媒体转述,Crissy Field 检查了 159,041 个 Lovable 项目,其中 24,664 个应用在无需认证的情况下返回了数据库记录;这些数字来自二手报道,本文未能核对原始研究。

**「影响」** 用 Lovable 等工具生成并发布后端应用的开发者,不能只依赖平台的默认设置和发布前扫描,应自行检查 Supabase 表的 RLS 策略,尤其是存放个人身份信息和私信的表。评论中有人提到,攻击者只需查看浏览器的网络请求就能发现这类问题,所以配置不当的应用风险较高。

**「社区讨论」** 评论者 SOLAR\_FIELDS 认为,Supabase 多年来为方便用户上手而采用宽松默认值,也应承担责任;他还提到该问题据称在 10 月 30 日修复,但有报告称已有项目仍沿用旧默认值,这一点未经验证。liquid\_thyme 主张平台应改用默认拒绝的数据库、最小权限 API 和自动化鉴权测试;Oras 则指出,这类 AI 生成的应用数量庞大、容易被攻击,而普通用户往往不了解其中的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://cybernews.com/security/lovable-ai-apps-expose-personal-information/">Lovable AI apps exposed sensitive data in open databases ...</a></li>
<li><a href="https://dailysecurityreview.com/cyber-security/24664-lovable-built-apps-leak-passports-and-chat-messages/">24,664 Lovable-Built Apps Leak Passports and Chat Messages</a></li>

</ul>
</details>

**标签**: `#ai-code-security`, `#lovable`, `#supabase`, `#row-level-security`, `#data-exposure`

---

<a id="item-tech-news-3"></a>
### [Project Zero 将漏洞披露窗口定为 90 天,并计划逐步缩短](https://projectzero.google/2026/11/disclosure-policy.html) ⭐️ 7.0/10

Google Project Zero 宣布调整漏洞披露政策:从发布当天起采用“Full 90”,即漏洞在报告给厂商 90 天后披露。据评论者引用原文,窗口将在 2027 年 2 月 2 日缩短为“Full 60”\(60 天\),并在 2028 年 1 月 3 日进一步缩短为“Full 30”\(30 天\)。本条目未提供原文正文,调整的理由、宽限期或例外条款等细节均无法核实,上述时间表仅来自评论引用。

hackernews · hacb · 11月14日 11:13 · [社区讨论](https://news.ycombinator.com/item?id=50496051)

**「背景」** Project Zero 是 Google 的安全研究团队,长期通过“报告给厂商后设定固定期限、到期公开”的方式,推动厂商及时修复漏洞。本条目没有提供原文,披露期限逐步缩短到 60 天、30 天的具体日期,仅来自评论者对文章的引述,例外情况和宽限期等细节尚未核实。

**「影响」** 如果时间表属实,厂商和开源维护者需要逐步压缩修复与发布补丁的周期,响应较慢的项目和发行版将面临更大压力。不过,具体是否设有宽限期或例外尚不清楚,受影响团队应以 Project Zero 原文为准来确认时限。

**「社区讨论」** 评论者 wewewedxfgdf 认为 Ubuntu 这类发行版需要比这长得多的时间来修复。glitchc 则主张发现后立即披露,认为只有这样才能迫使厂商修复。Frost1x 提出,发现漏洞的 AI 公司也应向厂商和开源项目提供同样的工具来修补漏洞,以免厂商借此推动用户采用其大模型。这些都是个人观点,并非已证实的事实。

**标签**: `#vulnerability-disclosure`, `#project-zero`, `#security-policy`, `#open-source-security`, `#google`

---

<a id="item-tech-news-4"></a>
### [意大利监管机构因 Facebook 安卓应用读取相册罚 Meta 8.05 亿欧元](https://www.garanteprivacy.it/home/docweb/-/docweb-display/docweb/10321080) ⭐️ 7.0/10

意大利隐私监管机构 Garante 对 Meta 处以 8.05 亿欧元罚款，理由是其 Facebook Android 应用在没有取得具体同意的情况下，读取了约 2000 万意大利用户的相册照片、视频及元数据。涉事功能是 2023 年上线的相册推荐，默认开启，授权提示也比较笼统。Garante 要求 Meta 在 60 天内改为默认关闭，并单独征得用户同意；否则，对未有效授权的用户不得启用该功能。所提供的材料只是简短摘要，没有说明具体法律依据，也没有 Meta 的回应。

telegram · zaihuapd · 11月14日 14:37

**「背景」** 涉事功能是 Facebook 在 2023 年上线的相册推荐功能：在用户授权后，应用会读取手机相册里的照片和视频，据此生成推荐内容。意大利数据保护机构 Garante 认为，该功能默认开启，授权提示又过于笼统，用户并不清楚自己同意的究竟是什么。BBC 的报道也称，监管机构指 Meta 没有充分告知约 2000 万用户它可以访问其照片和视频。

**「影响」** Meta 需要在 60 天内把意大利用户的相册推荐改为 opt-in，并重新设计授权流程。其他需要访问相册等设备数据的应用也应注意：笼统的系统权限提示，加上默认开启的功能，可能不被监管机构视为有效的具体同意。

**「社区讨论」** Hacker News 上有评论者认为报道缺少技术细节，不清楚 Meta 是如何在未同意的情况下读取照片的。另一位评论者引用报道中的说法，指出该功能需要用户在设备上授予权限，并质疑意大利究竟在保护什么；这代表的是个人看法，并非定论，也说明争议焦点在于系统权限是否等同于具体同意。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bbc.com/news/articles/cwn83gxemk35o">Italy fines Meta € 805 m over accessing users&#x27; photos</a></li>

</ul>
</details>

**标签**: `#Meta`, `#privacy regulation`, `#data protection fine`, `#consent`, `#Italy`

---

<a id="item-tech-news-5"></a>
### [Cloudflare 以 Apache 2.0 开源面向 AI 代理的无状态浏览器 Kitesurf](https://www.phoronix.com/news/Cloudflare-Kitesurf-Open-Source) ⭐️ 6.5/10

Cloudflare 以 Apache 2.0 协议开源了 Kitesurf，这是一款面向 AI 代理的无状态浏览器，代码已发布在 GitHub。它基于 Cloudflare Workers 构建，据称无需浏览器容器，即可解析 HTML、处理 CSS 并执行 JavaScript。Cloudflare 称，其目标是为 AI 代理提供轻量、高效的浏览器，相比 Chromium 占用更少的 CPU 和内存，并能在全球 Workers 网络上按需扩展。来源没有给出基准测试数据，也没有说明 CSS 与 JavaScript 的兼容范围或已知限制，上述效率优势目前只是厂商自己的说法，尚未经过独立验证。

telegram · zaihuapd · 11月14日 09:33

**「背景」** AI 代理访问网页通常依赖无头 Chromium，需要在容器或独立浏览器实例中运行，资源开销较大。Cloudflare 官方博客称 Kitesurf 是面向 AI 代理的实验性浏览器引擎，运行在 Workers 的 V8 隔离环境中，而不是自带 Chromium，更看重 token 效率、可扩展性和成本，而非渲染像素；第三方页面还称它起初是把开源 Rust 无头引擎 Obscura 移植到 Workers 上，但这一说法未经官方来源证实。

**「影响」** 如果 Kitesurf 的表现与宣称相符，已在 Workers 上运行 AI 代理的开发者就可以免去维护 Chromium 容器的负担，用更低的资源开销抓取和操作网页。不过来源没有说明它对复杂页面和现有网站的兼容程度，开发者在迁移前应先用自己的目标站点测试渲染与脚本执行效果，并自行对比资源占用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.cloudflare.com/kitesurf-open-source/">Kitesurf is now open source | Cloudflare Blog</a></li>
<li><a href="https://www.aiagentslist.io/agents/kitesurf">Kitesurf Review 2026: Cloudflare &#x27;s Browser Built for AI Agents</a></li>
<li><a href="https://www.aixploria.com/en/kitesurf-cloudflare/">Kitesurf Cloudflare : Reviews, Price, Info &amp; 44 Alternatives AI Tools</a></li>

</ul>
</details>

**标签**: `#Cloudflare Workers`, `#AI agents`, `#headless browser`, `#open source`, `#Kitesurf`

---

<a id="item-tech-news-6"></a>
### [特斯拉 Cybercab 订阅条款：车价 29,990 美元，另需月付 299 美元](https://www.tesla.com/configurator/api/v4/terms?category=autonomy_subs&amp;amp;locale=en_US&amp;amp;model=cc&amp;amp;saleType=Sale) ⭐️ 6.5/10

据特斯拉公布的 Cybercab 自主驾驶订阅条款，车辆售价为 29,990 美元，车主还须每月支付 299 美元订阅费，否则车辆无法运行。特斯拉可提前一个月通知调价；欠费或违规使用可能导致订阅被暂停或取消，累计三次警告则自动驾驶停用一周。车辆只能在指定区域内运行，未经授权不得接入网约车、配送或租赁平台。以上内容来自转述特斯拉、Electrek 和路透社的简短报道，所附链接是条款 API 接口，帖子没有核实完整协议文本，也未说明条款是否为最终版本。

telegram · zaihuapd · 11月15日 01:10

**「背景」** Electrek 在 11 月 13 日报道称，特斯拉已开放个人用途 Cybercab 的订购，价格为 29,990 美元，另需每月 299 美元的强制订阅，且只能在 Robotaxi 的地理围栏内使用；InsideEVs 称该订购面向“部分客户”。此次公布的订阅协议进一步写明了调价、暂停和使用范围等条款。需要注意的是，这些信息来自媒体转述和协议接口页面，协议是否为最终版本尚未得到核实。

**「影响」** 按这些条款，Cybercab 买家购车后仍须持续付费，特斯拉也保留调价、限定使用范围和停用功能的权力。考虑购买者应先核对完整协议，重点看调价通知、警告与停用规则、运行区域和平台接入限制。Electrek 指出，Cybercab 与 Robotaxi 用的 Model Y 同样采用 AI4 硬件和相同的自动驾驶软件，而面向普通车主的 FSD 仍需人类监督。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://electrek.co/2026/11/14/tesla-cybercab-autonomy-subscription-agreement-terms/">Tesla Cybercab&#x27;s autonomy agreement is insane: $299/mo or it ...</a></li>
<li><a href="https://electrek.co/2026/11/13/tesla-cybercab-personal-use-orders-299-subscription-geofence/">Tesla Cybercab orders open at $29,990 + $299/mo, only in ...</a></li>
<li><a href="https://insideevs.com/news/815473/tesla-cybercab-pricing-sales-announced/">Tesla Opens $29,990 Cybercab Orders For &#x27;Select Customers&#x27;</a></li>

</ul>
</details>

**标签**: `#Tesla Cybercab`, `#autonomous driving`, `#subscription model`, `#robotaxi`, `#FSD`

---

<a id="item-tech-news-7"></a>
### [NVIDIA 称用 vLLM 在两台 DGX Station 上以 607.8 tok/s 运行 GLM-5.3](https://developer.nvidia.com/blog/when-one-gpu-isnt-enough-serving-glm-5-3-across-two-nvidia-dgx-stations-with-vllm/) ⭐️ 6.0/10

NVIDIA 开发者博客介绍了如何用 vLLM 把 GLM-5.3 模型部署在两台 NVIDIA DGX Station 上,标题给出的吞吐量为 607.8 tokens/s。由于未提供正文,具体的量化方式、并发条件、批大小、互联方式和测试方法均无法确认,这一数字只能视为厂商博客标题中的说法,尚无独立验证。

hackernews · wondersky · 11月14日 14:09 · [社区讨论](https://news.ycombinator.com/item?id=50497155)

**「背景」** DGX Station 是英伟达的桌边 AI 工作站,搭载 GB300 Grace Blackwell Ultra 桌面超级芯片,官方称其拥有 748 GB 一致性内存和最高 20 petaFLOPS 的 AI 算力。单台机器放不下的大模型,需要用 vLLM 这类推理引擎做张量并行,把模型拆到多台机器上服务。社区已有类似做法,例如用 TP2 把 GLM-5.3-Flash 部署在两台通过 200 GbE RoCE 直连的 DGX Spark 上。本文原文未提供,具体的测试方法和配置无法核实。

**「影响」** 对考虑自托管大模型的团队来说,评论中的成本估算提醒应先核算硬件投入和实际利用率,再决定是否采用这类方案。若主要目的是节省费用而不是隐私或数据控制,按 API 价格对比,回本周期可能很长。

**「社区讨论」** 评论者 hkalbasi 假设整套设备约 10 万美元、GLM-5.3 输出价格为每百万 token 1.4 美元,估算即使满负荷也需约 7 年回本,且未计电费;jbellis 则称约一半价格的 8 张 RTX PRO 6000 配置在 4 bit 下可获得约 60% 更高吞吐,并给出了一个 GitHub 项目。这些均为评论者的观点或引用,未经核实。另有人询问超过两台时的网络方案,以及每台是否有约 500GB 内存未被使用。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/alexellis/glm-5.3-flash-2x-dgx-spark-switchless">GitHub - alexellis/ glm - 5 . 3 -flash- 2 x- dgx -spark-switchless...</a></li>
<li><a href="https://www.nvidia.com/en-us/products/workstations/dgx-station/">Personal AI Supercomputer | NVIDIA DGX Station</a></li>

</ul>
</details>

**标签**: `#vLLM`, `#LLM inference`, `#NVIDIA DGX`, `#multi-node serving`, `#GLM`

---

<a id="item-tech-news-8"></a>
### [PyPI 完成项目页面改版，更清晰展示来源与安全信号](https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/) ⭐️ 6.0/10

PyPI 官方博客称，重新设计的项目页面已全部上线，页面会更清楚地呈现来源证明（provenance）等安全信号。原文内容未能获取，具体改版细节无法确认；从社区评论看，文件列表区域会标明项目是否带有 provenance，例如 datasette 有、dlt 没有。这属于界面层面的更新，而非新的安全机制。

hackernews · rbanffy · 11月14日 15:40 · [社区讨论](https://news.ycombinator.com/item?id=50497892)

**「背景」** PyPI 在 2026 年 7 月 22 日的博客中公布了分阶段的界面改版计划:第一阶段重做项目详情页主体,第二阶段精简文件与发布历史标签页,并在适当位置加入证明\(attestation\)元数据。11 月 6 日的文章宣布这一系列改动完成,其中包括把来源\(provenance\)警告放到页面顶部,与已撤回版本、已归档项目、预发布版本的状态横幅并列。需要注意,这次更新主要是把已有的来源与证明信息展示得更清楚,原文未提供更多细节,不能据此认定 PyPI 新增了安全机制。

**「影响」** 用户在 PyPI 项目页的文件区域就能看出某个包是否发布了 provenance，更便于在选用依赖时做初步判断。不过评论指出，provenance 只能帮助发现原本正常的项目被劫持了发布入口，无法识别本身就是恶意的项目；另外 Trusted Publishing 目前还不支持可复用工作流（reusable workflows），相关项目的维护者暂时无法顺畅使用。

**「社区讨论」** 有评论者担心，这套信任机制实际上依赖大型云和 CI 服务，会加剧中心化与供应商锁定；也有人支持无密钥（keyless）签名，希望它能推动更多第三方 CI 服务补齐 OIDC 等安全能力。另有评论强调，provenance 的作用只限于发现被劫持的项目，不能发现恶意项目。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.pypi.org/posts/2026-11-06-ui-updates-complete/">PyPI&#x27;s redesigned project pages with clearer security signals ...</a></li>
<li><a href="https://blog.pypi.org/posts/2026-07-22-ui-updates/">Planned Updates to the PyPI User Interface - The Python ...</a></li>

</ul>
</details>

**标签**: `#PyPI`, `#supply-chain-security`, `#provenance`, `#Sigstore`, `#trusted-publishing`

---

<a id="item-tech-news-9"></a>
### [美国国税局 Direct File 免费报税系统源码在 GitHub 公开](https://github.com/IRS-Public/direct-file) ⭐️ 6.0/10

美国国税局\(IRS\)的免费在线报税系统 Direct File 已在 GitHub 上以开源仓库形式公开\(IRS-Public/direct-file\),标题标注为 2025 年。所提供的材料只有仓库链接和社区评论,没有说明仓库的架构、覆盖的税表范围、许可证,也没有说明与此前版本相比有何新增内容,因此这些细节无法确认。

hackernews · accountinhn · 11月14日 17:48 · [社区讨论](https://news.ycombinator.com/item?id=50499083)

**「背景」** Direct File 是美国国税局\(IRS\)推出的免费在线报税系统,这次的 GitHub 仓库把它的代码公开。报税软件的核心是“税务规则引擎”,即按税法把收入、扣除等财务资料换算成申报结果。评论中有人提到,IRS FreeFile 等免费服务不支持较复杂的表格,所以这类引擎公开后能否复用受到关注。不过,所提供的材料只有仓库链接和评论,没有说明该仓库的架构、覆盖的税表范围,也没有说明 2025 年版本相比以往有何变化。

**「社区讨论」** 评论者 gouggoung 称,现有免费报税服务\(包括 IRS Free File\)不支持他需要的较复杂表格,这是用户对覆盖范围的反馈。另有评论者提出,可以做一个能在本地处理财务文件的开源税务规则引擎,避免把个人数据交给第三方。atcole 称自己正在开发基于 AI 代理的报税工具 OpenReturn\(仍在测试阶段\),并拿 Direct File 的引擎来验证自己的实现,同时表示求解联邦税法需要消耗大量 token。这些都是评论者个人的说法,未经独立验证。

**标签**: `#open-source`, `#government-tech`, `#tax-software`, `#irs-direct-file`, `#civic-tech`

---

<a id="item-tech-news-10"></a>
### [Show HN:约 200 行纯 JAX 复现 DeepSeek V3 架构](https://github.com/Vaibhaav-Tiwari/deepseek-v3-jax) ⭐️ 6.0/10

Show HN 上出现一个开源项目 deepseek-v3-jax,作者用约 200 行纯 JAX 代码重新实现了 DeepSeek V3 的架构,定位为教学与小规模实验资源。作者说明自己用多本书籍构建了自定义数据集来训练。所提供材料没有给出 README 内容,因此无法确认其中包含哪些组件\(如 MLA、MoE、MTP\),也没有基准测试结果;它是精简的再实现,而非全规模的忠实复现。

hackernews · VaibhaavTiwari · 11月14日 15:04 · [社区讨论](https://news.ycombinator.com/item?id=50497589)

**「背景」** DeepSeek V3 是一个大型语言模型架构,JAX 则是支持 jit、grad、vmap 等可组合变换的 Python/NumPy 数值计算库,因此常被用来写简洁的模型实现。检索到的 Hacker News 页面显示,这个项目的模型约 190 行,是一个 3620 万参数的缩小版,在 MacBook Air M5\(24 GB\)上通过 jax-metal 训练,数据为 207 部旧侦探小说,12,000 步约耗时 2.6 小时。这些数字来自外部页面,未经独立复现,也无法据此判断它包含 DeepSeek V3 的哪些组件。

**「影响」** 对想在非 CUDA 硬件上学习或试验的开发者来说,这是一个可参考的起点:有评论者称它在 Fedora 上通过 ROCm 在 RX 7600 XT 16GB 上端到端跑通。该评论者还提到需要设置环境变量 HSA\_OVERRIDE\_GFX\_VERSION=11.0.0,因为 JAX 插件会拒绝 gfx1102。这只是单个用户的报告,尚无独立验证。

**「社区讨论」** 多位评论者认为从头复现模型是很好的学习方式,其中 joebarbere 报告在 AMD 显卡上顺利运行。nico 则建议使用其他人常用的数据集,这样结果才便于比较,这也呼应了作者自建书籍数据集所带来的可比性局限。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://news.ycombinator.com/item?id=50497589">Show HN: DeepSeek V 3 in ~ 200 lines of pure Jax | Hacker News</a></li>
<li><a href="https://github.com/jax-ml/jax">GitHub - jax -ml/ jax : Composable transformations of Python+NumPy...</a></li>

</ul>
</details>

**标签**: `#JAX`, `#DeepSeek V3`, `#LLM architecture`, `#ROCm`, `#educational implementation`

---