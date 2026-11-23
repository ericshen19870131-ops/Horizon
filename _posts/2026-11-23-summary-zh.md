---
layout: default
title: "Horizon Summary: 2026-11-23 (ZH)"
date: 2026-11-23
lang: zh
---

> 从 35 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [OpenAI 发文称困惑度可衡量模型智能,正文细节未获证实](#item-tech-news-1) ⭐️ 7.0/10
2. [GL.iNet 发布安全公告，具体漏洞细节未能核实](#item-tech-news-2) ⭐️ 6.0/10
3. [Masullo 手稿的 Lean 形式化进度图:证明正确性仍存争议](#item-tech-news-3) ⭐️ 6.0/10
4. [倡导组织预测:2028 年 Anthropic 电力 87%来自天然气、11%来自煤炭](#item-tech-news-4) ⭐️ 6.0/10
5. [FT 称太子集团关联人涉英伟达芯片对华走私，集团否认](#item-tech-news-5) ⭐️ 6.0/10
6. [Windows Server 2028 默认不含 WoW64，32 位应用需手动装回](#item-tech-news-6) ⭐️ 6.0/10
7. [谷歌据称搭建“Mirror Dimension”模拟互联网测试 Chrome AI 代理](#item-tech-news-7) ⭐️ 5.5/10

**财经新闻**
1. [美股科技股大跌，中韩及台湾推出稳市措施](#item-finance-news-1) ⭐️ 8.0/10
2. [超级厄尔尼诺海温破纪录，粮食援助面临压力](#item-finance-news-2) ⭐️ 6.0/10
3. [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资](#item-finance-news-3) ⭐️ 5.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [OpenAI 发文称困惑度可衡量模型智能,正文细节未获证实](https://openai.com/index/perplexity-and-intelligence/) ⭐️ 7.0/10

OpenAI 发布了题为《Perplexity and Intelligence》的文章,据评论判断,其观点是:困惑度\(即交叉熵损失\)与模型能力之间存在清晰的趋势,并覆盖了多代模型。由于未提供文章正文,具体数据、评测集和方法均无法核实,以下只能依据标题和评论。评论中提到,微软的 Mustafa Suleyman 称,经 OpenAI 许可,在其评测集上报告了 MAI-2 Base 的对数困惑度为 0.819,与 GPT-5.6 Sol 基础模型处于同一水平;这是评论者转述的推文内容,本文未独立核实。

hackernews · acossta · 11月22日 17:06 · [社区讨论](https://news.ycombinator.com/item?id=50601525)

**「背景：困惑度是什么」** 困惑度（perplexity）衡量语言模型预测下一个 token 时的“意外程度”，本质上是交叉熵损失的指数形式：完全预测准确时为 1，随机猜测时等于词表大小。据 OpenAI 页面摘录，文中所报告的数值来自 GPT-3.5 以来一直使用的内部代码库留出数据集（固定快照），因此不同实验室之间因评测集与训练数据不同而难以直接比较。

**「社区讨论」** 评论者 hazrmard 指出文章没有定义困惑度,并解释它是模型预测下一个 token 时的“惊讶程度”,最优为 1,最差等于词表大小。jrflo 对趋势如此清晰感到意外,原以为强化学习兴起后交叉熵已不再关键,并称赞这是比层出不穷的复杂基准更简单的指标;d\_burfoot 则认为“预测即压缩”的智能观几乎是必然的,并提到自己 2008 年的论文已论述过类似观点。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://openai.com/index/perplexity-and-intelligence/">Perplexity and Intelligence | OpenAI</a></li>
<li>Perplexity and Intelligence | OpenAI</li>

</ul>
</details>

**标签**: `#perplexity`, `#LLM evaluation`, `#scaling trends`, `#OpenAI`, `#benchmarks`

---

<a id="item-tech-news-2"></a>
### [GL.iNet 发布安全公告，具体漏洞细节未能核实](https://www.gl-inet.com/en-us/blogs/blog/glinet-security-notice-2026-11-20) ⭐️ 6.0/10

GL.iNet 于 2026 年 11 月 20 日在官网发布了一则安全公告，涉及其网络设备和 KVM 产品。但本次提供的材料只有标题和社区评论，没有公告正文，因此具体漏洞、受影响型号、固件版本、严重程度和修复方式均无法确认。评论中提到有用户已经打了补丁，但这属于个人说法，不能代替厂商公告。

hackernews · gregsadetsky · 11月22日 23:06 · [社区讨论](https://news.ycombinator.com/item?id=50604988)

**「背景」** GL.iNet 生产家用和小型办公路由器以及 Comet 系列 KVM\(远程控制设备\),设备可通过厂商的云端服务进行远程管理。官网首页已列出这份 2026-11-20 的安全公告,但本文未提供公告正文,具体漏洞、受影响型号和严重程度无法确认。俄文媒体 Dzen 的转述称,GL.iNet 于 11 月 20 日发现云端远程管理服务存在漏洞,攻击者借此在部分设备上植入恶意软件,公司仍在调查连接到受感染 KVM 的电脑是否受到影响;这一说法尚未在公告原文中得到核实。

**「影响」** GL.iNet 路由器或 KVM 的用户应直接阅读厂商公告，核对自己的型号是否受影响，并安装官方修复。评论者还建议关闭云端和远程访问功能，以缩小攻击面。不过 KVM 缺少 OpenWrt 支持，这类设备的用户无法通过更换固件来规避风险，这一点来自评论者的说法，尚未核实。

**「社区讨论」** Hacker News 评论者主要担心云连接固件带来的风险：有人主张刷入 OpenWrt 或自建路由器，也有人建议关闭云端和远程访问。另有用户贴出 GL.iNet 论坛帖子，称该厂商至少从去年起可能就已遭入侵，但这只是未经证实的说法。还有评论者指出，许多 GL.iNet 路由器可以刷 OpenWrt，而 KVM 不行。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.gl-inet.com/">GL . iNet - Connecting Beyond Limits</a></li>
<li><a href="https://dzen.ru/b/awOoLmLzbVc2iUyf">Через облако GL . iNet заразили роутеры и KVM -устройства... | Дзен</a></li>

</ul>
</details>

**标签**: `#security-advisory`, `#GL.iNet`, `#router-security`, `#OpenWrt`, `#IoT-firmware`

---

<a id="item-tech-news-3"></a>
### [Masullo 手稿的 Lean 形式化进度图:证明正确性仍存争议](https://claude.ai/artifact/CtQyX8qfYAF822bgHJHHE3) ⭐️ 6.0/10

这是一个公开的进度图,用来跟踪社区对 Alessandro Masullo 手稿的 Lean 形式化工作,对应的 GitHub 仓库名为 riemann-masullo。原文页面没有提供可读正文,所以具体的形式化范围、完成比例和技术细节无法从来源确认。评论显示,一位参与的数学家欢迎有余力的人用 AI 代理参与这个项目,但这只是评论者的说法。进度图本身不能证明手稿正确,因为只要有一处漏洞,整个证明都可能失效。

hackernews · Qision · 11月22日 23:12 · [社区讨论](https://news.ycombinator.com/item?id=50605045)

**「背景：Masullo 手稿与 Lean 形式化」** 这份进度图追踪的是社区用 Lean 证明助手，对 Alessandro Masullo 声称证明广义黎曼猜想（GRH）的手稿所做的逐条形式化。Lean 会机械检查每一步推理，因此只有当整条证明链都被形式化后，才能证明手稿正确；进度条只显示已完成的部分，不能说明核心论证没有漏洞。据外部报道，Ravi Vakil 称有人已报告该草稿存在问题，草稿正在大幅修订，志愿者目前只开始了 Lean 版本；这与评论中“教授们已拉开距离、手稿需要大修”的说法相符。

**「影响」** 对关注该声明的读者来说,这个进度条只说明形式化工作推进到了哪里,不能当作证明已被验证的证据。在核心论证的漏洞问题解决之前,应以数学界的审查结论为准,而不是以形式化的完成度为准。

**「社区讨论」** 自称参与该仓库的数学家 kopje\_koffie 表示,勘误清单中的数百个问题轻重不一,许多已经修复,现在判断核心思路是否存在大漏洞还为时过早。其他评论者则提醒不要把进度条当作证明基本正确的信号。其中 ion\_trapper 称,最初发布声明的 Ravi Vakil 说自己没有审阅过手稿,Brian Conrad 则认为手稿需要大幅修改,这些说法均来自评论,未经来源页面核实。hodgehog11 则称,根据其他评论,证明中可能有重大漏洞。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nacionale.com/en/articles/what-happens-next-alessandro-masullo-riemann-proof-revision-credit-clay-prize">Vakil : problems reported in Masullo &#x27;s GRH draft</a></li>
<li><a href="https://news.ycombinator.com/item?id=50605045">Progress map for the Lean formalization of Alessandro ...</a></li>

</ul>
</details>

**标签**: `#lean-formalization`, `#formal-verification`, `#ai-assisted-mathematics`, `#proof-checking`, `#riemann-masullo`

---

<a id="item-tech-news-4"></a>
### [倡导组织预测:2028 年 Anthropic 电力 87%来自天然气、11%来自煤炭](https://betterdatacenterproject.com/2026/11/16/how-ai-is-powered-a-breakdown-of-byop-and-grid-power/) ⭐️ 6.0/10

倡导组织 The Better Data Center Project 发布分析文章,预测到 2028 年,Anthropic 为 AI 数据中心获得的电力中约 87%来自天然气、11%来自煤炭。这一数字来自单一倡导型来源,未提供正文内容,其测算方法、数据来源和假设均无法核实,应视为该组织的预测,而非已经证实的结果。文章标题还提到“BYOP\(自带电源\)”与电网供电的区别,但具体细节同样无法确认。

hackernews · happosai · 11月22日 08:57 · [社区讨论](https://news.ycombinator.com/item?id=50597612)

**「背景:BYOP 与这一预测的来源」** “BYOP”\(自带电源\)指数据中心在现场自建燃气轮机等发电设施,而不完全依赖电网;Better Data Center Project 与 Earthjustice 曾在 10 月发布报告,批评这类电厂规避监管、危害社区和气候。此次 87% 天然气、11% 煤炭的数字出自该组织 11 月 16 日的案例研究,据报道是其依据许可证、申报文件和美国环保署\(EPA\)模型作出的 2028 年估算,涉及 Anthropic 约 15 吉瓦的已签约算力,并非实测数据,也不是 Anthropic 的声明。评论中提到的 Colossus 1 是位于孟菲斯的数据中心,据 LinkedIn 帖子称 Anthropic 已租用其全部约 300 兆瓦容量,另有报道称 xAI 的 Colossus 数据中心因约 50 台未获许可的燃气轮机被起诉。

**「社区讨论」** 评论者多从道德与监管角度发表看法:contemporary343 批评 Anthropic 租用 Colossus 1 造成孟菲斯当地污染,且在美国缺少可再生能源承诺;sollewitt 则主张通过监管,避免环境外部成本转嫁给社区。也有评论者补充背景,例如 gregwebs 指出美国天然气多为页岩油开采的副产品,但这些均为个人观点,并未验证原文数字。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://explainx.ai/blog/anthropic-data-center-power-gas-coal-byop-2028-better-datacenter-november-2026">Anthropic Power Mix: 87% Gas, 11% Coal by 2028 (Study ...</a></li>
<li><a href="https://earthjustice.org/feature/data-center-byop-energy-report">The AI Gas Rush: Risks and Implications of “Bring Your Own ...</a></li>
<li><a href="https://topfive.ai/wire/better-data-center-project-projects-87-of-anthropics-2028-compute-power-from-gas/">Better Data Center Project projects 87% of Anthropic&#x27;s 2028 ...</a></li>
<li><a href="https://www.linkedin.com/posts/jkarnik_anthropic-just-rented-an-entire-data-center-activity-7458001482953621504-eKFB">Anthropic Rents 300MW Data Center from Elon Musk for AI... | LinkedIn</a></li>
<li><a href="https://dailyinference.com/p/anthropic-overtakes-openai-meta-encrypted-chat">Anthropic overtakes OpenAI in business adoption, Meta launches...</a></li>

</ul>
</details>

**标签**: `#AI energy consumption`, `#data centers`, `#Anthropic`, `#fossil fuels`, `#AI policy`

---

<a id="item-tech-news-5"></a>
### [FT 称太子集团关联人涉英伟达芯片对华走私，集团否认](https://www.ft.com/content/f3ad8a81-3890-4a8a-8853-ff0a94b08ba9?syn-25a6b1a6=1) ⭐️ 6.0/10

据转述《金融时报》报道，被美国财政部称为柬埔寨太子集团“二号人物”的胡小伟，被知情人士指涉嫌参与把英伟达芯片运入中国。报道称，该集团被指拥有涉及空壳公司和地下融资渠道的网络，并用私人飞机走私货物。贸易数据显示，2024 年 12 月至 2025 年 12 月，Megaspeed 马来西亚子公司申报进口货物价值约 46 亿美元，其中部分芯片据称流入中国黑市。太子集团否认胡小伟曾为其工作，并称相关指控缺乏事实依据。

telegram · zaihuapd · 11月22日 04:34

**「背景」** Megaspeed 此前已被《纽约时报》2025 年 10 月的报道关注：该公司被指把大量英伟达芯片送往马来西亚、印尼的数据中心，这些中心可能远程为中国客户提供服务；这种做法未必违法，但若代表中国公司进行则可能被认定为违规。马来西亚贸工部（MITI）称从未批准 Megaspeed 或其马来西亚关联公司 Speedmatrix，并正与海关核查相关芯片是否违反《2010 年战略贸易法》而被再出口。另据检索结果，美国财政部 OFAC 于 2026 年 6 月制裁了包括胡小伟在内的九人，称其为太子集团的“二号人物”；本文所述其涉及对华芯片走私的指控，目前仅见于《金融时报》援引的匿名知情人士和贸易数据，太子集团予以否认。

**「影响」** 这些说法主要依据匿名知情人士和贸易数据，目前尚未得到独立证实，也未见官方定性。如果情况属实，涉及马来西亚等转口环节的大额进口可能促使监管部门和芯片供应商加强对东南亚分销商及最终用户的审查，相关企业应留意合规核查要求。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.nytimes.com/2025/10/09/technology/nvidia-chips-china-megaspeed.html">A Mystery C.E.O. and Billions in Sales: Is China Buying Banned Nvidia ...</a></li>
<li><a href="https://www.cryptopolitan.com/malaysia-megaspeed-re-exported-nvidia-chips/">Malaysia checks whether Megaspeed re-exported Nvidia AI chips</a></li>
<li>Treasury Further Dismantles Overseas Scam Operations Targeting ...</li>
<li>OFAC Expands Sanctions on Prince Group Tied to Global Scam ...</li>

</ul>
</details>

**标签**: `#Nvidia`, `#chip smuggling`, `#export controls`, `#AI hardware supply chain`, `#China`

---

<a id="item-tech-news-6"></a>
### [Windows Server 2028 默认不含 WoW64，32 位应用需手动装回](https://www.windowslatest.com/2026/11/23/32-bit-apps-days-are-numbered-as-microsoft-strips-support-bit-by-bit-starting-with-windows-server-2028-but-windows-11-is-safe-for-now/) ⭐️ 6.0/10

据 Windows Latest 报道，微软在 Ignite 2026 上表示，计划于 2027 年秋季与 Windows 11 27H2 一同发布的 Windows Server 2028 将默认不再包含 WoW64 兼容子系统，因此开箱后无法运行 32 位应用。需要时可通过按需功能（FoD）把 WoW64 装回，Server Core 上一般用 PowerShell 或 DISM 添加。微软称此举是为了减少攻击面、阻止 32 位恶意软件。Windows 11 目前仍保留 WoW64，微软未公布移除计划。以上内容均来自这篇二手报道，尚未获得其他来源验证，且该系统仍是尚未发布的计划版本。

telegram · zaihuapd · 11月23日 03:03

**「背景：WoW64 是什么」** WoW64（Windows 32-bit on Windows 64-bit）是 64 位 Windows 中的兼容子系统，使 32 位应用能在 64 位系统上运行。按需功能（Features on Demand，FoD）则允许管理员在需要时再安装系统组件。多家媒体报道称，这是首次有 Windows Server 版本默认不带 WoW64，不过这些报道同样基于微软在 Ignite 上的说法，计划细节仍有待微软进一步确认。

**「影响」** 仍在服务器上运行 32 位应用、安装程序或管理工具的管理员和软件维护者，需要在升级到 Windows Server 2028 前清点相关依赖。如果确实需要，应在部署流程或镜像中把按需安装 WoW64 的步骤写进去，避免上线后才发现应用无法启动。距离发布还有约一年，具体行为仍应以微软正式文档为准。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.windowscentral.com/microsoft/windows-11/microsoft-is-removing-32-bit-app-support-from-the-next-version-of-windows-server-wow64-subsystem-to-become-optional-component-to-reduce-malware-attack-surface">Windows Server 2028 to remove 32-bit app support for improved ...</a></li>
<li><a href="https://winaero.com/windows-server-2028-will-not-support-32-bit-apps-by-default/">Windows Server 2028 will not support 32-bit apps by default</a></li>

</ul>
</details>

**标签**: `#Windows Server 2028`, `#WoW64`, `#32-bit apps`, `#attack surface`, `#Microsoft Ignite`

---

<a id="item-tech-news-7"></a>
### [谷歌据称搭建“Mirror Dimension”模拟互联网测试 Chrome AI 代理](https://www.landian.news/archives/128701.html) ⭐️ 5.5/10

据蓝点网报道（经 Telegram 频道转述），谷歌为 Chrome 的 AI 代理搭建了名为 Mirror Dimension 的模拟互联网，在隔离环境中测试代理打开网站、搜索浏览、登录、加购和完成任务等操作。报道称其中包含数千个模拟网站，每名工程师单独隔离测试，每天运行超过 1000 个测试案例，重点防御恶意网页的提示词注入等攻击。该内容为二手转述，未附谷歌官方来源，测试方法、覆盖范围和防御效果均未披露。

telegram · zaihuapd · 11月23日 01:30

**「背景：浏览器代理与提示词注入」** 浏览器 AI 代理会代替用户打开网页、登录、加购并完成任务，因此要读取并处理大量不受信任的网页内容。恶意网页可借此植入隐藏指令，即提示词注入，诱导代理偏离用户意图。若直接在真实网站上测试，可能带来真实的安全风险。谷歌官方博客称，Mirror Dimension 是一个合成版网络，用来在逼真的在线环境中安全地测试代理，不会造成真实世界的安全风险。

**「影响」** 如果报道属实，这说明谷歌在让 Chrome 代理操作真实网站之前，会先在可控环境中复现登录、购物等高风险流程，并检验其对恶意网页指令的抵御能力。不过由于缺乏谷歌一手说明和实测结果，目前不能据此判断 Chrome AI 代理的安全性，使用者和开发者应等待官方文档或独立评估。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/security/mirror-dimension-for-agents/">Mirror Dimension for Agents: Evaluating Browser-Use Agents ...</a></li>

</ul>
</details>

**标签**: `#Chrome AI agent`, `#prompt injection`, `#agent security testing`, `#Google`, `#browser sandbox`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [美股科技股大跌，中韩及台湾推出稳市措施](https://news.bjd.com.cn/2026/11/22/12039852.shtml) ⭐️ 8.0/10

据报道,美国 AI 和科技股周五大幅抛售,纳斯达克指数单日下跌 5.28%,费城半导体指数下跌近 11%。中国内地、韩国和中国台湾随后宣布了稳定股市的措施。

telegram · zaihuapd · 11月22日 13:24

**「背景」** 据观察者网报道，此轮抛售源于市场对人工智能投资热潮放缓的担忧。融资保证金是投资者借钱买股时需先缴纳的自有资金比例，降到 80%后，100 万元保证金最多可融资 125 万元。

**「影响」** 据报道,台湾自 11 月 23 日起禁止平盘以下卖空,并将融券保证金比例从 130%提高到 150%;韩国自 11 月 24 日起 3 个月内放宽上市公司每日回购订单数量限制。这些措施会直接影响当地的卖空交易、融资融券交易和公司回购操作。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.guancha.cn/GuoJi%C2%B7ZhanLue/2026_11_21_909399.shtml">AI 恐慌爆发，华尔街震荡，美国 科 技 股 跌 入熊市</a></li>
<li><a href="https://finance.eastmoney.com/a/202611223936948742.html">重磅时刻！ A 股 迎三大“新政”！ 影响几何？ 最 新解读来了 _ 东方财富网</a></li>

</ul>
</details>

**标签**: `#美股科技股`, `#纳斯达克`, `#半导体指数`, `#亚洲股市`, `#市场稳定措施`

---

<a id="item-finance-news-2"></a>
### [超级厄尔尼诺海温破纪录，粮食援助面临压力](https://www.wired.com/story/how-this-years-super-el-nino-will-worsen-global-hunger/) ⭐️ 6.0/10

据气候学家 Zeke Hausfather 称，截至 10 月，衡量厄尔尼诺强度的中热带太平洋升温已达 3.5℃，超过此前约 2.75℃的纪录，预计初冬峰值约为 4℃。世界粮食计划署（WFP）8 月警告，本轮厄尔尼诺可能在 2027 年底前使额外 4900 万人陷入急性粮食不安全，总数达 2.74 亿（预测）。

telegram · zaihuapd · 11月22日 14:09

**「背景」** 厄尔尼诺是赤道中东太平洋海水异常变暖的自然气候现象，常引发干旱和洪涝，从而冲击农业与渔业。世界粮食计划署（WFP）在 2026 年 8 月预计，这轮厄尔尼诺可能在 2027 年底前使至少 4900 万人陷入急性粮食不安全，总数升至约 2.74 亿。

**「影响」** 全球援助资金 2025 年比 2022 年峰值低 30%，援助机构应对旱情的能力受限；例如索马里遭遇类似旱情时，WFP 能覆盖的人数从 1000 万降至不足 100 万。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wfp.org/news/world-food-programme-ramps-preparedness-and-response-plans-el-nino-threatens-push-tens">World Food Programme ramps up preparedness and response plans...</a></li>
<li><a href="https://news.un.org/en/story/2026/08/1168079">Strengthening El Niño to push 49 million more people into acute hunger</a></li>

</ul>
</details>

**标签**: `#El Niño`, `#food insecurity`, `#humanitarian aid funding`, `#World Food Programme`, `#climate risk`

---

<a id="item-finance-news-3"></a>
### [蚂蚁集团领投 Simplexity Robotics 1 亿美元融资](https://www.bloomberg.com/news/articles/2026-11-22/ant-group-bets-on-simplexity-to-thrive-in-china-s-humanoid-race) ⭐️ 5.0/10

据彭博报道，杭州具身智能公司 Simplexity Robotics 完成 1 亿美元 pre-A 轮融资，由蚂蚁集团领投，投后估值 16 亿美元；公司董事长向彭博确认了该消息。

telegram · zaihuapd · 11月23日 02:02

**「背景」** 具身智能是指把 AI 装进机器人等实体中，让它通过感知环境来完成动作。彭博此前报道，2025 年全球约 1.3 万台人形机器人出货中，中国厂商占绝大多数；该公司今年 3 月披露的投后估值已超过 10 亿美元。

**「影响」** 这家成立于 2025 年 7 月的公司，此前称半年内完成五轮融资、累计约 20 亿元人民币，投后估值已超 10 亿美元；彭博称，新资金将用于与宇树、优必选等更成熟的厂商争夺市场。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.bloomberg.com/news/articles/2026-01-08/chinese-firms-dominated-global-humanoid-robot-shipments-in-2025">Chinese Firms Dominated Global Humanoid Robot Shipments in 2025</a></li>

</ul>
</details>

**标签**: `#humanoid robotics`, `#venture funding`, `#Ant Group`, `#embodied AI`, `#China tech`

---