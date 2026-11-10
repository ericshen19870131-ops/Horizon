---
layout: default
title: "Horizon Summary: 2026-11-10 (ZH)"
date: 2026-11-10
lang: zh
---

> 从 55 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Anthropic 发布 Claude Fable 5.2 与 Mythos 5.2](#item-tech-news-1) ⭐️ 8.0/10
2. [GitHub 仓库称消费版 Gemini 或将关联应用中的个人数据交人工标注](#item-tech-news-2) ⭐️ 6.5/10
3. [E-means 聚类算法称以约十分之一轮数达到 k-means 水平](#item-tech-news-3) ⭐️ 6.5/10
4. [加拿大支付协会宣布推出全天候实时支付系统 RTR](#item-tech-news-4) ⭐️ 6.5/10
5. [LingBot-Touch：JEPA 式触觉预训练在检索任务上大幅领先重建方法](#item-tech-news-5) ⭐️ 6.5/10
6. [SwarmEvolve：用潜空间推理智能体集群做数学发现与优化](#item-tech-news-6) ⭐️ 6.5/10
7. [谷歌发布 TPU 8tx 与 8i Max，扩充 TPU 产品线](#item-tech-news-7) ⭐️ 6.5/10
8. [watched.earth：查看过去 7 天飞越任意地点的卫星及其影像](#item-tech-news-8) ⭐️ 6.0/10
9. [Artificial Analysis 榜单显示 Claude Fable 5.2 得 65 分,居当前最高](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [中国延长暂停对美 24%加征关税，保留 10%税率](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Anthropic 发布 Claude Fable 5.2 与 Mythos 5.2](https://www.anthropic.com/claude-fable-and-mythos-5-2) ⭐️ 8.0/10

Anthropic 发布了 Claude Fable 5.2 与 Mythos 5.2，据称强化了编码、推理和视觉能力。两款模型共用底层架构：Fable 面向所有用户，Mythos 需通过网络安全或生命科学验证计划申请。转载内容称，其输出速度比 5.1 快约 30%，价格降至每百万输入 token 8 美元、输出 40 美元，另有 2.5 倍加速模式。官方称 1,000 个 Fable 5.2 智能体在 30 小时内、仅需极少人工干预就完成了费马大定理的形式化；这是厂商的自我报告，本文未见原文全文或独立验证。

hackernews · meetpateltech · 11月9日 18:56 · [社区讨论](https://news.ycombinator.com/item?id=50429906)

**「背景」** 形式化证明是把数学证明写成可由证明助手机械检验的代码，工作量很大。据评论引用的公告，Anthropic 此前由未发布的研究版 Claude 完成同一定理的首次形式化，耗时 11 天，并依赖专门搭建的工具链和人类研究员的指导。

**「影响」** 对开发者而言，Fable 5.2 对所有用户开放，且价格下调，可以直接在自己的任务上与 Opus 5.5 对比。Mythos 需经网络安全或生命科学验证计划申请，相关领域的团队要先走审核流程。是否值得切换，取决于自身任务难度，因为有早期用户反映日常编码差别不大。

**「社区讨论」** 有早期用户 postalcoder 表示，只有把提示的目标定得足够宏大，Fable 5.2 才明显优于 Opus 5.5，普通编码任务上几乎看不出差别。另有评论者质疑基准对比的设置，例如拿 Fable xHigh 对比 Carbon Med，网络安全基准中缺少 Carbon；还有人认为 5.5 在新版本发布前被削弱，但这些都是评论者的看法，未经证实。

**标签**: `#Anthropic`, `#LLM release`, `#multi-agent systems`, `#formal verification`, `#model benchmarks`

---

<a id="item-tech-news-2"></a>
### [GitHub 仓库称消费版 Gemini 或将关联应用中的个人数据交人工标注](https://github.com/thisisme6598/gemini_files/) ⭐️ 6.5/10

一个匿名风格作者发布的 GitHub 仓库声称,谷歌面向消费者的 Gemini 在连接 Gmail、Drive 等应用后,用户的个人文件和邮件可能被送给人工标注人员审阅。该仓库页面未提供可读的技术细节,这一说法目前未经证实,也无法确认是否属于新变化。评论者指出,涉及范围仅限于启用“已连接应用”的消费版 Gemini,而 Workspace 版 Gemini 据称不受人工审核。

hackernews · gf74918 · 11月9日 18:24 · [社区讨论](https://news.ycombinator.com/item?id=50429426)

**「背景:Gemini 的人工审核与关联应用」** 根据 Google 的 Gemini Apps 隐私中心\(经 Android Police 转述\),人工审核员会阅读、标注并处理消费者版 Gemini 的对话;ZDNet 报道称,经人工审核的对话与 Google 账号分开保存,删除活动记录时不会被删除,最长保留三年。第三方对比页面 Ask Safely 还指出,用户一旦关联 Gmail、云端硬盘等应用,Gemini 读取的邮件和文件就适用与聊天数据相同的审核和保留条款。因此该仓库的说法与 Google 已公开的政策基本吻合,但其本身没有提供技术细节,也无法证明有新的数据流向。

**「影响」** 如果你在消费版 Gemini 中授权了 Gmail 或 Drive 等应用,相关内容在被调用后可能和其他消费版 Gemini 数据一样进入人工审核流程。对敏感邮件和文件较多的用户,应先查阅谷歌的消费版数据使用条款与活动记录设置,再决定是否保留这些授权。企业用户则应以 Workspace 管理文档中的不审核承诺为准,而不是依据这个仓库。

**「社区讨论」** 评论者 bri3d 强调,该问题仅限于消费版 Gemini 加已连接应用,Workspace Gemini 仍声称不受人工审核;另一些人如 hek2sch 则认为,凡是有人工审核或标注环节的工具都存在内容被阅读或用于训练的风险。也有用户如 rustyhancock 以亲身体验表示,Gemini 的回答有时明显贴合其邮件内容,但这只是个人观察,并不能证明存在人工审阅。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.zdnet.com/article/dont-tell-your-ai-anything-personal-google-warns-in-new-gemini-privacy-notice/">Don&#x27;t tell your AI anything personal, Google warns in new Gemini ...</a></li>
<li><a href="https://www.androidpolice.com/reasons-you-should-turn-off-gemini-ai-training/">Google Gemini : 4 reasons you should turn off the AI-training mode</a></li>
<li><a href="https://www.asksafely.ai/compare/gemini/">Ask Safely vs Gemini : What Google Does With Your Conversations</a></li>

</ul>
</details>

**标签**: `#gemini`, `#ai-privacy`, `#human-review`, `#google-workspace`, `#data-governance`

---

<a id="item-tech-news-3"></a>
### [E-means 聚类算法称以约十分之一轮数达到 k-means 水平](https://e-means.github.io/) ⭐️ 6.5/10

E-means 是一种被提出的 k-means 替代算法,标题称其可在约十分之一的迭代轮数\(epochs\)内取得优于 k-means 的聚类效果。不过本次只拿到标题和社区评论,没有页面正文,具体基准、实验方法和同行评审情况均无法核实。评论者的自述显示,它在大数据集上可能大幅减少数据遍历次数,但在小规模几何松弛任务中没有优势。

hackernews · porridgeraisin · 11月9日 18:45 · [社区讨论](https://news.ycombinator.com/item?id=50429734)

**「背景：k-means 与 Lloyd 算法」** k-means 是经典的聚类方法，通过 Lloyd 算法反复执行“把点分配给最近的质心、再重新计算质心”来降低簇内方差；每一轮（epoch）都要完整遍历数据集，因此数据量很大时成本很高。搜索结果显示，e-means 的博客称其为 Meta FAIR 开发并开源的 k-means 算法，并与 Lloyd 算法比较了 epoch 数、CPU 时间和 GPU 时间。由于未能获取页面正文，其基准测试和方法细节尚未得到验证。

**「影响」** 对于需要在大数据集上反复运行 k-means 的场景,例如向量检索中的 IVF 索引构建,E-means 可能降低遍历数据的成本,有一定试用价值。但现有证据只有个别用户的非正式测试,采用前应在自己的数据和指标上与标准 k-means 对比,并等待作者的基准和方法细节得到验证。

**「社区讨论」** 用户 real\_faxenoff 称,将该方法改用于自己的 IVF 索引后,在 GPU 上获得 146 倍加速;而 jlhawn 试用于球面二十面体等面积网格的 Lloyd 松弛后发现效果并不更好,认为其优势在于大数据集上所需遍历次数更少。shiandow 则推测其更新规则类似带“摩擦项”的期望最大化\(EM\),并指出该规则能让质心保持在凸包内,但这只是评论者的解读,并非已验证的结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://e-means.github.io/">e - means : 10 x faster k - means at equal loss - Blog</a></li>
<li><a href="https://www.geeksforgeeks.org/machine-learning/clustering-in-machine-learning/">Clustering in Machine Learning - GeeksforGeeks</a></li>

</ul>
</details>

**标签**: `#clustering`, `#k-means`, `#machine-learning`, `#vector-search`, `#algorithms`

---

<a id="item-tech-news-4"></a>
### [加拿大支付协会宣布推出全天候实时支付系统 RTR](https://www.payments.ca/canada-launches-real-time-rail-bringing-247-payment-infrastructure-national-economy) ⭐️ 6.5/10

加拿大支付协会\(Payments Canada\)宣布推出 Real-Time Rail\(RTR\),这是一套面向全国、全天候运行的实时支付基础设施。原文正文未能获取,只有标题和部分评论可供参考,因此 ISO 20022 支持情况、系统架构、可用性和费用等技术细节均无法核实。有评论援引的名单显示,首批活跃参与者包括 Wealthsimple、Questbank、Peoples Trust Company、KOHO、Bank of America 等机构,其中似乎没有加拿大大型银行,但这份名单并不完整,也未经原文证实。

hackernews · ocd · 11月9日 16:00 · [社区讨论](https://news.ycombinator.com/item?id=50427362)

**「背景」** 实时轨道（RTR）是加拿大支付协会（Payments Canada）建设的新一代实时清算与结算系统，用于支持全天候的即时、数据丰富的支付，按计划于 2026 年第四季度启动。据第三方博客文章称，首批直接参与机构先投入生产运行，各合作机构要到 2027 年第三季度才会达到全部交易量，因此这是一个约一年的逐步爬坡过程。

**「社区讨论」** 有评论者认为,RTR 听起来像是把 Interac e-Transfer 的模式变成可供任意银行接入的公共基础设施,并且让 Interac 参与其中是明智之举,但也提醒要看实际推广效果。另一位评论者指出,首批参与者中似乎没有加拿大大型银行,这是对 RTR 覆盖面的主要质疑。还有评论拿美国 FedNow 作对比,称其只有少数银行支持,且收费较高。这些都是评论者的观点和引述,并非已核实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.payments.ca/systems-services/payment-systems/real-time-rail-payment-system">Real - Time Rail payment system | Payments Canada</a></li>
<li><a href="https://blog.fundmore.ai/canada-real-time-rail-comes-into-force-lender-batch-assumptions-just-got-a-deadline">Canada &#x27;s Real - Time Rail Comes Into Force Aug 24. Every...</a></li>

</ul>
</details>

**标签**: `#real-time-payments`, `#fintech`, `#payments-infrastructure`, `#Canada`, `#financial-systems`

---

<a id="item-tech-news-5"></a>
### [LingBot-Touch：JEPA 式触觉预训练在检索任务上大幅领先重建方法](https://www.reddit.com/r/MachineLearning/comments/1xs05uo/latent_prediction_beats_reconstruction_for/) ⭐️ 6.5/10

Robbyant 发布了 LingBot-Touch，一种采用 JEPA 式自监督训练的触觉编码器：它预测被遮挡接触区域的潜在表示，而不是重建原始传感器信号。论文称，在相同数据、相同规模下，触觉到视频检索的 top-5 召回率在 1K 小时数据时为 JEPA 32.1%、MAE 5.6%、VAE 4.4%；4K 小时时 JEPA 达到 49.3%，MAE 低于 9%，VAE 降至 3.1%。在 26 项真实机器人任务、4 种策略的 104 个组合中，冻结的编码器特征在 89 个组合里得分最高；在预训练中从未见过的磁式灵巧手上，LingBot-VLA 的成绩从 57.21 提升到 75.04。推理代码和检查点已公开，但以上数字均来自作者自己的论文，帖子中未提及独立复现。

reddit · r/MachineLearning · /u/Zealousideal-War7154 · 11月9日 18:52

**「背景:JEPA 与触觉预训练」** JEPA\(联合嵌入预测架构\)式自监督学习不重建原始输入,而是预测被遮挡部分的潜在表示;MAE、VAE 等方法则重建原始信号。触觉信号大多是接近零的稀疏背景,仅少量接触点有信息,因此作者认为重建损失很容易下降却没有学到接触特征。LingBot-Touch 由 Robbyant 发布,项目页称其用共享的 Haptic Transformer 统一磁式、压阻式和视觉触觉三类传感器信号,代码仓库目前提供推理用的冻结目标编码器和特征提取工具。

**「影响」** 做触觉或灵巧操作的团队可以直接下载公开的检查点，把冻结特征接入自己的策略，评估其在自家传感器上的效果。其训练设计也值得借鉴：掩码率在 300 步内从 40% 升到 80%，并通过规范化指尖坐标加 5D RoPE，让磁式、压阻式和视觉触觉三类传感器共用一个 Transformer。不过这些结论仍需在其他数据集和硬件上验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Robbyant/lingbot-touch">GitHub - Robbyant/lingbot-touch: Learning Heterogeneous ...</a></li>
<li><a href="https://technology.robbyant.com/lingbot-touch">LingBot-Touch Tactile Foundation Model - Robbyant</a></li>

</ul>
</details>

**标签**: `#tactile-sensing`, `#JEPA`, `#self-supervised-learning`, `#robotic-manipulation`, `#representation-learning`

---

<a id="item-tech-news-6"></a>
### [SwarmEvolve：用潜空间推理智能体集群做数学发现与优化](https://www.reddit.com/r/MachineLearning/comments/1xrunu7/using_latentagent_swarms_for_math_discovery_and/) ⭐️ 6.5/10

SwarmEvolve 是作者在 Reddit 上发布的一篇新论文，提出一种 AlphaEvolve 风格的数学发现与优化框架：用数百个基于 Qwen3 8B、14B、32B 的潜空间推理智能体组成集群，智能体不输出文字形式的思考，而是在潜空间中推理并相互传递 KV 缓存。作者称，该框架在约 5 分钟内就能达到 OpenEvolve、ShinkaEvolve 和 CodeEvolve 需要超过 1 小时才能达到的分数，仅用 8B 模型就能追平已知最佳的圆填充结果，并已扩展到 Qwen3.5 和 Muse 模型，效果更好。这些数据均来自作者自述，帖子中没有给出具体基准细节，也没有独立验证；代码标注为“即将发布”，论文发布在 alphaxiv（2611.08483）。

reddit · r/MachineLearning · /u/QileHQ · 11月9日 15:30

**「背景：AlphaEvolve 与 LatentMAS」** AlphaEvolve 的做法是让大模型编写程序、打分,再据此迭代改进,帖子称它曾找到比 1969 年纪录更快的 4x4 复数矩阵乘法;OpenEvolve、ShinkaEvolve、CodeEvolve 是类似的开源实现。SwarmEvolve 借鉴的 LatentMAS 是 2025 年 11 月提出的免训练框架\(arXiv 2511.20639\),让多个 LLM 智能体不再以文本交流,而是在潜空间中生成隐状态思考,并共享 KV 缓存和隐状态,以减少文本编解码带来的开销。

**「影响」** 如果这些加速结果在代码发布后能够复现，研究者就可以用小型开源模型而非 Gemini 级闭源模型运行进化式程序搜索，降低实验成本。目前尚不能据此选型或替换现有框架，应等待代码和完整基准公开后，再对比各框架在相同任务和算力预算下的表现。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/2511.20639">[2511.20639] Latent Collaboration in Multi-Agent Systems Latent Collaboration in Multi-Agent Systems - arXiv.org GitHub - Gen-Verse/LatentMAS: [ICML 2026 Spotlight] Latent ... LaMAR: Latent Multi-agent Collaboration via KV-Cache ... Paper page - Latent Collaboration in Multi-Agent Systems Latent Collaboration in Multi-Agent Systems | OpenReview Latent Collaboration in Multi-Agent Systems</a></li>
<li><a href="https://github.com/Gen-Verse/LatentMAS">GitHub - Gen-Verse/LatentMAS: [ICML 2026 Spotlight] Latent ...</a></li>

</ul>
</details>

**标签**: `#latent-reasoning`, `#multi-agent-systems`, `#AlphaEvolve`, `#evolutionary-program-search`, `#Qwen3`

---

<a id="item-tech-news-7"></a>
### [谷歌发布 TPU 8tx 与 8i Max，扩充 TPU 产品线](https://www.bloomberg.com/news/articles/2026-11-09/google-escalates-nvidia-rivalry-with-new-versions-of-its-tpu-systems) ⭐️ 6.5/10

据彭博社报道，谷歌宣布推出两款新的 TPU：TPU 8tx 面向政府机构和受严格监管行业，用于处理安全机密数据，并将与 AMD 芯片协同工作；TPU 8i Max 面向超长上下文窗口的 AI 应用，在同一封装内集成两颗 TPU，以提供更强算力和更大内存容量。报道称，谷歌正打破过去约每两年推出一代处理器的节奏，今年连续扩充产品线，并称苹果、Meta、甲骨文和 Anthropic 等已是客户。该来源是对彭博报道的简短转述，未给出基准测试、具体规格、上市时间或定价，产品细节也无法仅凭该条目核实。

telegram · zaihuapd · 11月9日 13:36

**「背景：TPU 8 系列」** TPU（张量处理单元）是谷歌自研的 AI 加速芯片，是其面向英伟达 GPU 的替代方案。据谷歌官方博客，新发布的 8tx 和 8i Max 是对第八代 TPU 产品组合的扩充；另据 Wccftech 报道，8tx 是 TPU 8t 的改款，8i Max 则是将两颗 TPU 8i 芯片封装在一起。

**「社区讨论」** Hacker News 评论更多关注可获得性：有用户希望 Colab 提供新一代 TPU，称目前最强的仍是 v6e-1，不足以做严肃工作；另有用户质疑这些芯片又是外部用户用不上的，并问谷歌为何不直接出售。另有评论指出，谷歌官方博客文章标题称这两款芯片面向“智能体时代”。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/tpu-8i-max-and-8tx/">Introducing TPU 8 tx and TPU 8 i Max</a></li>
<li><a href="https://wccftech.com/google-pairs-its-new-tpu-8tx-with-custom-amd-epyc-cpus-hosts-while-the-tpu-8i-max-combines-two-tpu-8i-chips-in-a-single-package-to-offer-phenomenal-compute-and-memory-density/">Google Pairs Its New TPU 8 tx With Custom AMD EPYC CPU Hosts...</a></li>

</ul>
</details>

**标签**: `#Google TPU`, `#AI hardware`, `#Nvidia competition`, `#AI accelerators`, `#long-context inference`

---

<a id="item-tech-news-8"></a>
### [watched.earth：查看过去 7 天飞越任意地点的卫星及其影像](https://www.watched.earth/) ⭐️ 6.0/10

开源网页工具 watched.earth 允许用户输入任意地点，在浏览器端基于 CelesTrak 星历目录用 SGP4 轨道传播算法，约半秒内找出过去 7 天飞越该地的卫星，并拉取这些过境对应的 Sentinel-2、Landsat 和 NASA 真实影像。作者称，其过境搜索不会漏检，并在极地、对日界线和窄幅宽等情形下与暴力搜索对照，漏检数为 0；页面还用 GPU 每帧求解开普勒方程，绘制约 1.7 万个在轨物体。作者表示，只有存在真实影像时才显示“watched”，且不保存用户位置。上述技术与验证说法均来自作者自述，本次未经独立验证。

hackernews · a585gupt · 11月9日 17:51 · [社区讨论](https://news.ycombinator.com/item?id=50428907)

**「背景」** SGP4 是根据 TLE/轨道根数预测近地卫星位置的常用模型，CelesTrak 则提供公开的卫星轨道数据目录。作者还提到 Sentinel-2 的影像时间戳常与卫星实际飞越该点的时间相差 5–10 分钟，因此需要把过境时刻与影像记录对应起来。

**「影响」** 对地理空间从业者和户外活动规划者来说，这个工具能更方便地查看某地近期有哪些卫星过境，以及能否找到对应的公开影像。有评论者称，它在规划背包徒步时比其使用的 Copernicus 更易用，但这只是个人使用反馈，不代表覆盖范围或精度已得到独立验证。

**「社区讨论」** 多数评论肯定其实用性：一位从事地理空间工作的评论者称，能看到卫星拍摄的确切图像是它区别于其他卫星总览网站之处，另一位认为它在户外行程规划中比 Copernicus 更易获取。也有评论者指控帖子文字由 LLM 生成，并认为违反 HN 规则；这一指控未经证实，也与工具本身的功能无关。

**标签**: `#satellite-tracking`, `#SGP4`, `#geospatial`, `#show-hn`, `#open-source`

---

<a id="item-tech-news-9"></a>
### [Artificial Analysis 榜单显示 Claude Fable 5.2 得 65 分,居当前最高](https://artificialanalysis.ai/models/claude-fable-5-2) ⭐️ 6.0/10

Artificial Analysis 的模型页面显示,Claude Fable 5.2 的综合指数得分为 65,是该榜单目前的最高分。由于未能获取页面正文,产品名称和分数仅来自条目标题与摘要,无法进一步核实。HN 评论者称,相比 Fable 5.1,每项任务的输出 token 从约 11.8 万升至约 27.4 万,其中推理 token 从约 7.1 万增至约 19.2 万,单任务成本约翻倍。这些数字均为评论者的说法,尚未经页面证实。

hackernews · theanonymousone · 11月9日 20:04 · [社区讨论](https://news.ycombinator.com/item?id=50431144)

**「背景：Artificial Analysis 智能指数」** Artificial Analysis 是一家独立的模型评测机构，其“智能指数”（Intelligence Index）把多项评测汇总为单一分数，并同时给出每项任务的成本和耗时，用来对比不同模型。检索到的页面显示，Claude Fable 5.2 的 Max 档得分为 65，同类模型的中位数为 40；该页面还说明模型支持文本和图像输入、输出文本，上下文窗口为 100 万 token，且 5.2 版本共包含 5 个不同档位的模型。需要注意，社区评论里关于 5.1 到 5.2 的 token 用量和成本翻倍的具体数字，目前没有在检索结果中得到证实。

**「影响」** 如果评论中的数据属实,在 Fable 5.2 与其他模型之间做选择的团队,需要把单任务成本和 token 消耗与榜单分数一起评估,而不是只看智能指数。成本敏感的场景可以先在 Artificial Analysis 页面核对实际的单任务成本,再决定是否升级。

**「社区讨论」** 多数评论者关注性价比:rgbrenner 称 Fable 5.2 的单任务成本相比 5.1 翻倍,brachkow 和 schnitzelstoat 则认为智能提升幅度有限而价格过高,schnitzelstoat 同时猜测真实任务上的差距可能比基准更明显。oliwary 持相反的角度,指出 Fable 5.2 的低、中档设置位于「单任务耗时—智能」的帕累托前沿上,在交互速度上更有优势。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/releases/claude-fable-5-2">Claude Fable 5 . 2 Models - Intelligence ... | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/models/claude-fable-5-2">Claude Fable 5 . 2 (max) - Intelligence ... | Artificial Analysis</a></li>
<li><a href="https://artificialanalysis.ai/leaderboards/models">LLM Leaderboard - Comparison of AI models from... | Artificial Analysis</a></li>

</ul>
</details>

**标签**: `#llm-benchmarks`, `#artificial-analysis`, `#inference-cost`, `#anthropic`, `#reasoning-models`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [中国延长暂停对美 24%加征关税，保留 10%税率](https://mp.weixin.qq.com/s/nNxJB3y0YA_2zJvOK6onUQ) ⭐️ 7.0/10

据国务院关税税则委员会公告，自 2026 年 11 月 10 日 13 时 01 分起，中国将在 2 个月内继续暂停实施对美 24%的加征关税，并保留 10%的加征关税税率。公告称，此举是为落实中美两国元首华盛顿会晤达成的共识。

telegram · zaihuapd · 11月9日 04:03

**「背景」** 此次是对现有安排的延期：中国对美加征关税中的 24% 部分暂不执行，另外 10% 仍照常征收，公告称这是为落实两国元首华盛顿会晤的共识。11 月 6 日，中美经贸牵头人刚举行视频通话，讨论如何落实元首会晤共识和经贸磋商成果。

**「影响」** 在这 2 个月内，中国对美国商品的加征关税仍维持在 10%，另外 24%的部分继续暂停实施，涉及对美出口商品的企业面临的关税成本因此不会升至更高水平。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://ru.china-embassy.gov.cn/zgxw/202611/t20261107_12055300.htm">ru.china-embassy.gov.cn/zgxw/202611/t20261107_12055300.htm</a></li>

</ul>
</details>

**标签**: `#中美关税`, `#贸易政策`, `#关税税则委员会`, `#中美关系`, `#国际贸易`

---