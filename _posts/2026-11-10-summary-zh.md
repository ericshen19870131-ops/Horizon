---
layout: default
title: "Horizon Summary: 2026-11-10 (ZH)"
date: 2026-11-10
lang: zh
---

> 从 54 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [Anthropic 发布 Claude Fable 5.2 与 Mythos 5.2](#item-tech-news-1) ⭐️ 7.0/10
2. [谷歌发布 TPU 8tx 与 TPU 8i Max 两款新芯片](#item-tech-news-2) ⭐️ 7.0/10
3. [英飞凌宣布在 300 毫米碳化硅晶圆上制出功能性功率器件](#item-tech-news-3) ⭐️ 7.0/10
4. [Show HN：watched.earth 可查询任意地点一周内过境卫星及其影像](#item-tech-news-4) ⭐️ 6.5/10
5. [E-means：声称以约十分之一轮数达到 k-means 效果的聚类算法](#item-tech-news-5) ⭐️ 6.5/10
6. [LingBot-Touch：JEPA 式触觉预训练在检索上大幅超越重建基线](#item-tech-news-6) ⭐️ 6.5/10
7. [SwarmEvolve：用潜空间智能体集群加速 AlphaEvolve 式数学发现](#item-tech-news-7) ⭐️ 6.5/10
8. [欧盟《数字公平法案》泄露草案：限制成瘾设计，游戏虚拟货币须标真实币值](#item-tech-news-8) ⭐️ 6.5/10
9. [Meta 发布轻量模型 Muse Ember，主打低成本智能体任务](#item-tech-news-9) ⭐️ 6.5/10

**财经新闻**
1. [前三季度新能源乘用车出口大增，国内零售下滑](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [Anthropic 发布 Claude Fable 5.2 与 Mythos 5.2](https://www.anthropic.com/claude-fable-and-mythos-5-2) ⭐️ 7.0/10

Anthropic 发布了 Claude Fable 5.2 和 Mythos 5.2，据称强化了编码、推理和视觉能力。两款模型共用底层架构：Fable 面向所有用户，Mythos 需通过网络安全或生命科学验证计划申请。据转述，新版输出速度比 5.1 快约 30%，价格为每百万输入 token 8 美元、输出 40 美元，另有 2.5 倍加速模式。Anthropic 还称，1000 个 Fable 5.2 智能体在约 30 小时内、人工干预很少的情况下完成了费马大定理的形式化，而此前由未发布研究版 Claude 完成同一工作用了 11 天。以上均为厂商自述，我们只看到 Telegram 转述和评论区引文，未见原文全文，也没有独立验证。

hackernews · lairv · 11月9日 18:01 · [社区讨论](https://news.ycombinator.com/item?id=50429068)

**「背景：同一模型的两种发布形态」** 据 Anthropic 的系统卡和产品页介绍，Claude Fable 5.2 与 Mythos 5.2 是同一个底层模型的两种配置。Fable 面向通用场景，并在生物、网络安全等高风险的两用领域加装了额外防护；Mythos 则减少了这些限制，因此两者的结果差异主要出现在 Fable 的防护介入的任务上。需要注意，这些说明来自厂商自己的材料，其中的基准测试和“30 小时形式化证明费马大定理”等说法，目前尚未见到独立验证。

**「影响」** Fable 5.2 对所有用户开放，开发者可以直接在自己的工作负载上对比它与现有模型的效果和成本，Mythos 则要先通过验证计划。有评论者称，在日常编码任务上难以区分 Fable 5.2 与 Opus 5.5，所以是否值得切换，最好用自己的高难度任务实测，不必只看发布方的基准图。

**「社区讨论」** 评论者 postalcoder 认为，Fable 5.2 只有在提示足够有挑战性时才明显优于 Opus 5.5，普通编码任务上几乎看不出差别；advaith08 则称其团队用 Fable 5.2 处理 60 万行的 Fortran 代码，把材料科学计算加速了 36 倍，并公开了结果，但这仍是未经独立复核的个人报告。breakwaterlabs 则质疑发布方的基准对比，指出其拿不同的推理强度档位做比较、在网络安全基准中遗漏了 Carbon，并在某项测试里更换了对照模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://assets.claude.com/27d60918d218125e7504bc7354c4b4626ec56b11.pdf">Claude Fable 5.2 &amp; Claude Mythos 5.2 System Card</a></li>
<li><a href="https://www.anthropic.com/claude/mythos">Claude Mythos \ Anthropic</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#LLM release`, `#Claude`, `#AI benchmarks`, `#AI coding`

---

<a id="item-tech-news-2"></a>
### [谷歌发布 TPU 8tx 与 TPU 8i Max 两款新芯片](https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/tpu-8i-max-and-8tx/) ⭐️ 7.0/10

谷歌宣布推出两款新的张量处理单元（TPU）：TPU 8tx 和 TPU 8i Max。据 Bloomberg 报道（经 Telegram 频道转述），TPU 8tx 面向政府机构和受严格监管的行业，用于处理安全机密数据，并将与 AMD 芯片协同工作；TPU 8i Max 面向超长上下文窗口的 AI 应用，在同一封装内集成两颗 TPU 芯片，以提供更强算力和更大内存容量。所提供材料中没有性能、功耗、价格和上市时间等具体数据，也无法确认这些芯片是否已可供使用。谷歌官方博客的标题称其为“为智能体时代打造”，但正文未提供更多技术细节。

hackernews · \_benx\_ · 11月9日 21:56 · [社区讨论](https://news.ycombinator.com/item?id=50432831)

**「背景：TPU 第八代产品线」** TPU 是谷歌自研的 AI 加速器，长期以来主要在谷歌云内部提供，被视为英伟达 GPU 之外的替代选择。检索结果显示，TPU 8tx 是第八代 TPU 8t（训练型）的改型，TPU 8i Max 则把两颗面向推理的 TPU 8i 芯片封装在一起；这些说法来自谷歌博客摘要和第三方媒体 Wccftech，细节尚未在本材料中得到独立验证。

**「影响」** 对考虑采用 TPU 的企业和机构而言，两款芯片分别针对受监管的机密数据场景和长上下文推理场景，选型时可以按负载类型区分。但目前缺少性能、能效和价格数据，难以与英伟达 GPU 方案比较，建议等官方给出规格、可用区域和定价后再评估。

**「社区讨论」** 有评论者（ur-whale）质疑发布内容缺少每瓦每 token 或每 token 成本数据，也没有与英伟达同价位产品的对比。另一位评论者（mekpro）表示，Colab 上最强的仍是 v6e-1，规模太小，不足以做严肃工作，希望谷歌开放更新的 TPU；还有人（qntty）追问谷歌为何不对外销售这些芯片。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/global-network/tpu-8i-max-and-8tx/">Introducing TPU 8 tx and TPU 8 i Max</a></li>
<li><a href="https://wccftech.com/google-pairs-its-new-tpu-8tx-with-custom-amd-epyc-cpus-hosts-while-the-tpu-8i-max-combines-two-tpu-8i-chips-in-a-single-package-to-offer-phenomenal-compute-and-memory-density/">Google Pairs Its New TPU 8 tx With Custom AMD EPYC CPU Hosts...</a></li>

</ul>
</details>

**标签**: `#Google TPU`, `#AI accelerators`, `#AI infrastructure`, `#agentic AI`, `#hardware`

---

<a id="item-tech-news-3"></a>
### [英飞凌宣布在 300 毫米碳化硅晶圆上制出功能性功率器件](https://www.infineon.com/press-release/2026/infpr202611-028) ⭐️ 7.0/10

英飞凌于 2026 年 11 月 9 日发布新闻稿,称已在 300 毫米碳化硅\(SiC\)晶圆上加工出功能性功率器件,并称这是业界首次。公司将其定位为 300 毫米 SiC 工艺可行性的验证,为宽禁带功率半导体的制造奠定基础。社区评论提到,这项工作主要利用了原本为硅设计的现有 300 毫米设备。目前可见的内容只有新闻稿摘要,没有良率、缺陷密度、量产时间表等数据,因此这只是厂商自述的可行性里程碑,并非已投入量产的产能,也未经独立验证。

hackernews · sshah03 · 11月9日 18:25 · [社区讨论](https://news.ycombinator.com/item?id=50429430)

**「背景：从 200 毫米到 300 毫米碳化硅」** 晶圆直径越大,单片可切出的芯片越多;硅晶圆从 200 毫米转向 300 毫米始于 2000 年代初,据维基百科\(该处标注“需要引用”\)可使单颗芯片成本降低约 30%至 40%。碳化硅\(SiC\)是电动汽车、能源和数据中心电源所用的宽禁带功率半导体材料,其单晶生长困难,晶圆尺寸长期落后于硅。Infineon 称其已在奥地利菲拉赫\(Villach\)工厂把 300 毫米 SiC 晶圆加工成功能性功率器件;此前 Wolfspeed 已宣布制出单晶 300 毫米 SiC 晶圆,但两者的宣称侧重点不同,Wolfspeed 的材料成果面向 AI 数据中心先进封装等用途,并不等同于已量产功率器件。

**「影响」** 如果该工艺日后能以可接受的良率量产,更大的晶圆有望降低每颗 SiC 芯片的成本,惠及电动车、能源和数据中心电源等采购方。但现有证据只能证明可行性,采购方和设计方暂时还不能据此假设会有新的供货或价格;需要等待英飞凌公布良率、产能爬坡节奏和客户送样时间。

**「社区讨论」** 有评论者\(johntb86\)质疑,既然主要使用早已转向 300 毫米的硅工艺设备,为何过渡花了这么久,并推测难点可能在于更大晶锭的生长等少数工艺步骤。另一位评论者\(mercurywells\)则回忆称 Wolfspeed 在今年年初已达到 300 毫米,对“业界首次”的说法提出疑问,但这只是未经证实的个人记忆,评论中未给出依据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Wafer_%28electronics%29">Wafer (electronics) - Wikipedia</a></li>
<li><a href="https://www.techpowerup.com/354619/infineon-starts-worlds-first-300-millimeter-power-silicon-carbide-sic-wafer-production">Infineon Starts World&#x27;s First 300 - Millimeter Power Silicon Carbide ...</a></li>
<li><a href="https://www.wolfspeed.com/company/news-events/news/wolfspeed-unveils-foundation-for-next-generation-ai-data-center-advanced-packaging-leveraging-300mm-silicon-carbide-technology/">Wolfspeed Unveils Foundation for Next Generation AI... | Wolfspeed</a></li>
<li><a href="https://eepower.com/news/wolfspeed-makes-300mm-silicon-carbide-wafer-breakthrough/">Wolfspeed Makes 300 mm Silicon Carbide Wafer Breakthrough...</a></li>

</ul>
</details>

**标签**: `#silicon-carbide`, `#power-semiconductors`, `#semiconductor-manufacturing`, `#Infineon`, `#wide-bandgap`

---

<a id="item-tech-news-4"></a>
### [Show HN：watched.earth 可查询任意地点一周内过境卫星及其影像](https://www.watched.earth/) ⭐️ 6.5/10

开发者在 Show HN 上发布了开源网页应用 watched.earth。用户输入任意地点后，应用会在浏览器中基于 CelesTrak 星历目录运行 SGP4 算法，约半秒内列出过去 7 天内经过该地的卫星，并调取对应过境的 Sentinel-2、Landsat 和 NASA 真实影像。作者称，只有确实存在影像时才会显示“watched”，且不会存储用户位置；约 1.7 万个在轨物体通过 GPU 渲染，每帧求解开普勒方程。作者还称，过境搜索在两极、国际日期变更线和极窄幅宽场景下与暴力搜索对比，漏检为 0，不过这是作者自述，未经独立验证。

hackernews · a585gupt · 11月9日 17:51 · [社区讨论](https://news.ycombinator.com/item?id=50428907)

**「背景」** SGP4 是根据 TLE 等轨道根数预测近地卫星位置的常用传播模型，CelesTrak 公开提供这类星历目录。Sentinel-2 和 Landsat 则是公开的对地观测影像来源。作者还提到，Sentinel-2 元数据中的时间戳常与卫星实际飞越该点的时刻相差 5 到 10 分钟，因此需要做对应处理。

**「影响」** 对关心“哪颗卫星拍过某地”的用户，尤其是规划野外行程的人，这个工具把过境预测和公开影像检索合并到一个界面，省去分别查询多个数据源的步骤。评论者 wnissen 表示，它比自己此前使用的 Copernicus 更易上手。需要注意，它显示的影像仅限 Sentinel-2、Landsat 和 NASA 等公开来源，不涵盖商业卫星或军用卫星的实际拍摄。

**「社区讨论」** 所给评论全部为正面评价：adonovan 称赞其轨道可视化、地面轨迹和过境时间序列等多源数据整合得很好，sixtyj 自称从事地理空间工作，认为它的特别之处在于能看到卫星实际拍下的图像。这些是个人观点，评论中没有对作者的精度和漏检声明做独立验证。

**标签**: `#satellite-tracking`, `#geospatial`, `#SGP4`, `#WebGL`, `#show-hn`

---

<a id="item-tech-news-5"></a>
### [E-means：声称以约十分之一轮数达到 k-means 效果的聚类算法](https://e-means.github.io/) ⭐️ 6.5/10

E-means 是一种被提出的 k-means 替代算法，项目页标题声称它能以约十分之一的迭代轮数（epochs）达到优于 k-means 的聚类效果。本次未能获取页面正文，其算法细节、基准数据和实验条件均无法核实，上述说法只能视为作者的宣称。评论区有开发者在自己的向量索引（IVF）场景中做了初步尝试，报告了不同程度的加速，但这些都是自述的个人测试，未经评审。

hackernews · porridgeraisin · 11月9日 18:45 · [社区讨论](https://news.ycombinator.com/item?id=50429734)

**「背景」** k-means 通常用 Lloyd 算法反复执行“分配样本、更新质心”，每一轮都要遍历整个数据集，因此数据量大时成本很高。聚类是 IVF 等向量索引构建的基础步骤，减少遍历轮数能直接缩短索引构建时间。

**「影响」** 对需要在大数据集上反复聚类的向量索引构建，例如分片拆分后的整体重建，E-means 可能值得在自己的数据上做对比测试。评论显示收益依赖场景：有人在 IVF 索引上报告 GPU 加速，而在球面网格松弛任务中效果反而更差，所以不宜直接替换现有的 k-means 实现。

**「社区讨论」** 评论者的自述结果不一：real\_faxenoff 称在自己的 IVF 索引上获得 146x 的 GPU 加速，kingcauchy 称完整重建索引快了 2.5 倍，但增量插入的总耗时变化不大；jlhawn 则发现它不适合球面网格松弛，认为其优势在于减少对大数据集的遍历次数。shiandow 提出，该更新规则可理解为带摩擦项的期望最大化，并指出它能让质心保持在凸包内，这属于个人理论解读，并非已证实的结论。

**标签**: `#clustering`, `#k-means`, `#vector-indexing`, `#machine-learning-algorithms`, `#optimization`

---

<a id="item-tech-news-6"></a>
### [LingBot-Touch：JEPA 式触觉预训练在检索上大幅超越重建基线](https://www.reddit.com/r/MachineLearning/comments/1xs05uo/latent_prediction_beats_reconstruction_for/) ⭐️ 6.5/10

Robbyant 发布了触觉编码器 LingBot-Touch，已公开推理代码和模型检查点。它采用 JEPA 式自监督训练，预测被遮挡接触区域的潜在表示，而不是重建原始传感器信号。论文称，在相同数据和相同模型规模下，该方法在触觉到视频检索（top-5 召回率）上明显优于 MAE 和 VAE：1K 小时数据时为 32.1% 对 5.6% 和 4.4%；4K 小时时 JEPA 达 49.3%，MAE 低于 9%，VAE 降至 3.1%。在 26 个真实机器人任务、4 种策略的 104 种组合中，冻结编码器特征在 89 种里得分最高；在预训练中未见过的磁式触觉手上，LingBot-VLA 的得分从 57.21 提升到 75.04。以上均为论文自报结果，目前尚无独立复现。

reddit · r/MachineLearning · /u/Zealousideal-War7154 · 11月9日 18:52

**「背景」** JEPA\(联合嵌入预测架构\)式自监督学习不重建原始输入,而是在隐空间中预测被遮挡部分的表示;MAE、VAE 则以重建原始信号为训练目标。触觉信号多为接近零的稀疏背景,仅少数接触点有有效读数,因此重建损失容易被背景主导。LingBot-Touch 的官方资料称,它用模态专用的分词器加共享的 Haptic Transformer,把压阻、磁和视触觉三类传感器的信号统一成一组触觉 token,预训练数据接近 5000 小时。

**「影响」** 该工作的设计细节可供触觉预训练的研究者参考：遮挡比例在 300 步内从 40% 逐步升至 80%（据称一开始就用高遮挡会遮住稀疏信号中所有接触点，导致梯度爆炸），并通过规范化指尖坐标与 5D RoPE，让磁式、压阻式和视触觉三类传感器共用同一个 Transformer。由于代码和检查点已公开，团队可以在自己的触觉或操作任务上验证这些结果，再决定是否采用。需要注意，这些结论目前仅来自论文本身。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Robbyant/lingbot-touch">GitHub - Robbyant/lingbot-touch: Learning Heterogeneous ...</a></li>
<li><a href="https://technology.robbyant.com/lingbot-touch">LingBot-Touch Tactile Foundation Model - Robbyant</a></li>

</ul>
</details>

**标签**: `#tactile-sensing`, `#JEPA`, `#self-supervised-learning`, `#robotics-manipulation`, `#representation-learning`

---

<a id="item-tech-news-7"></a>
### [SwarmEvolve：用潜空间智能体集群加速 AlphaEvolve 式数学发现](https://www.reddit.com/r/MachineLearning/comments/1xrunu7/using_latentagent_swarms_for_math_discovery_and/) ⭐️ 6.5/10

论文作者在 Reddit 上介绍了 SwarmEvolve，这是一个面向数学发现与优化的框架，思路类似 AlphaEvolve：让 LLM 写程序、打分、再迭代改进。它在 Qwen3 8B、14B 和 32B 上运行数百个潜空间推理智能体，智能体不输出文字思考，而是通过共享 KV cache 交换想法。作者声称，该系统约 5 分钟就能达到 OpenEvolve、ShinkaEvolve 和 CodeEvolve 需要 1 小时以上才能达到的分数，仅用 8B 模型就能匹配已知最佳的圆填充结果，并称框架已扩展到 Qwen3.5 和 Muse 模型，表现更好。论文已发布在 alphaxiv，代码标注为“即将开放”；以上结果均来自作者自述，所给文本未提供具体基准细节，也没有独立验证。

reddit · r/MachineLearning · /u/QileHQ · 11月9日 15:30

**「背景:AlphaEvolve 与 LatentMAS」** AlphaEvolve 式的“进化”搜索,是让大模型编写程序、打分,再据此反复改进;原版运行在 Gemini 上,OpenEvolve、ShinkaEvolve、CodeEvolve 等开源实现则被作者描述为通常较慢且成本较高。SwarmEvolve 借鉴了 LatentMAS 的思路:智能体不输出文字形式的推理,而是在潜空间中思考,并通过共享 KV 缓存\(即“潜在工作记忆”\)传递内部表示,据称这种交换是无损的。

**「影响」** 如果论文中的速度与成本优势能被复现，使用开源 AlphaEvolve 式系统的研究者可以用小型开源模型更快做程序搜索，而不必依赖闭源模型或长时间运行。不过代码尚未发布，实际采用前应等待代码和完整基准，核对对比设置是否公平、各任务的评分细节以及算力开销。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.emergentmind.com/papers/2511.20639">Latent Collaboration in Multi - Agent Systems</a></li>
<li><a href="https://www.alphaxiv.org/abs/2511.20639">Latent Collaboration in Multi - Agent Systems | alphaXiv</a></li>

</ul>
</details>

**标签**: `#SwarmEvolve`, `#latent-reasoning agents`, `#AlphaEvolve`, `#multi-agent LLMs`, `#math discovery`

---

<a id="item-tech-news-8"></a>
### [欧盟《数字公平法案》泄露草案：限制成瘾设计，游戏虚拟货币须标真实币值](https://www.mlex.com/mlex/articles/2546584/digital-businesses-face-addictive-design-controls-under-draft-eu-consumer-law) ⭐️ 6.5/10

据 MLex 和 Euronews 报道的一份泄露草案，欧盟《数字公平法案》拟限制成瘾性设计和订阅陷阱：企业须允许用户关闭自动播放、连续使用奖励等诱导强迫或过度使用的功能；在线订阅须提供取消按钮、续费提醒和人工客服，免费试用转为付费前须取得用户明确同意。草案还拟禁止面向未成年人的游戏付费抽奖（loot box）、“付费获胜”和画像广告，并要求游戏虚拟货币标明真实币值。欧盟委员会定于 11 月 11 日提交该法案，同时改革消费者保护合作框架；违规企业最高可被罚全球营业额的 6%。这仍是泄露的草案，两项提案均需欧洲议会和欧盟各国政府同意才能生效，最终条款可能变化。

telegram · zaihuapd · 11月9日 16:42

**「背景」** 《数字公平法案》（DFA）是欧盟为应对在线“暗黑模式”、订阅陷阱等数字消费者保护问题而筹备的立法，欧盟委员会预计于 11 月 11 日连同《消费者保护合作条例》（CPC）的修订一并提出。据 Euronews 报道，泄露草案还拟列出十类操纵性设计“陷阱”的黑名单，并禁止先低价后在结账时才显示不可避免费用的“滴灌定价”。目前内容均来自泄露草案，正式文本仍需欧洲议会和成员国同意，细节可能变化。

**「影响」** 订阅服务、应用和游戏开发商需要提前审视自动播放、连续使用奖励、取消流程和试用转付费等设计，以及面向未成年人的抽奖和虚拟货币定价展示。由于草案尚未通过，具体合规要求要以最终文本为准，但相关企业可以先排查这些功能。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.euronews.com/2026/11/09/eu-to-blacklist-ten-manipulative-online-design-traps-leaked-draft-shows">EU to blacklist ten manipulative online design &#x27;traps&#x27;, leaked draft s...</a></li>
<li><a href="https://www.socialistsanddemocrats.eu/newsroom/digital-fairness-act-progressive-approach-protect-all-consumers-online">Digital Fairness Act : a progressive... | Socialists and Democrats</a></li>

</ul>
</details>

**标签**: `#EU regulation`, `#Digital Fairness Act`, `#dark patterns`, `#consumer protection`, `#gaming monetization`

---

<a id="item-tech-news-9"></a>
### [Meta 发布轻量模型 Muse Ember，主打低成本智能体任务](https://research.meta.ai/blog/muse-ember) ⭐️ 6.5/10

Meta 发布了轻量级模型 Muse Ember，面向复杂推理和智能体任务，支持 100 万 Token 上下文，可处理文本、图像、音频和视频，并能调用工具、执行跨应用工作流及自动修复代码。该模型已通过 Meta Model API 开放，输入价格为每百万 Token 0.10 美元，输出价格为 0.50 美元。Meta 称，其在 Artificial Analysis 智能指数上的表现可媲美 Claude Haiku 5.5，但单任务成本仅为后者的三分之一，并在多项测试中超过 GPT-6 Luna；这些均为 Meta 自己的说法，来源中没有给出详细评测方法，也没有独立验证。

telegram · zaihuapd · 11月9日 23:08

**「背景」** Muse Ember 是 Meta 在 Muse 模型系列中推出的最小、最高效的一款，通过 Meta Model API 按量计费提供。Meta 官方博客称其输入和输出价格分别为每百万 Token 0.10 美元和 0.50 美元，成本对比使用各模型的公开标价；Artificial Analysis 也已列出该模型（Max 推理档位）的页面。需要注意的是，Meta 说明所有对比均在最高推理强度下运行，部分结果来自其内部评测套件，因此“可媲美 Claude Haiku 5.5、单任务成本约三分之一”仍属厂商表述，需以第三方独立数据为准。

**「影响」** 对需要大量调用智能体的开发者来说，Ember 提供了一个低价的 API 选项，值得在自己的真实任务上对比试用。但目前的成本和性能对比只来自厂商公布的数据，而且按评论引用的脚注，其中部分结果来自 Meta 内部评测，因此不宜仅凭这些数据就迁移生产负载。

**「社区讨论」** Hacker News 上的评论对 Meta 的基准成绩持怀疑态度：djacksondev 认为 Muse 系列模型在榜单上看起来接近前沿，实际使用中却不够实用；doodlesdev 则指出，模型的最佳成绩并非来自 Meta 自家的智能体框架，而是来自 mini-swe-agent。另外，simonw 测试了六档推理强度，发现更多推理 Token 并未明显提升 SVG 画作质量，其中“high”档没有返回完整的 SVG；Retro\_Dev 则因找不到开放权重而感到遗憾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://artificialanalysis.ai/models/muse-ember">Muse Ember (Max) Intelligence, Performance &amp; Price Analysis</a></li>
<li><a href="https://research.meta.ai/blog/muse-ember">Introducing Our Smallest, Most Efficient Model: Muse Ember</a></li>
<li><a href="https://dev.meta.ai/docs/pricing-rate-limits">Pricing and rate limits - Meta Model API</a></li>

</ul>
</details>

**标签**: `#Meta Muse Ember`, `#agentic AI`, `#low-cost LLM`, `#long context`, `#model API pricing`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [前三季度新能源乘用车出口大增，国内零售下滑](https://finance.sina.com.cn/tech/roll/2026-10-26/doc-iniwpfnc2438186.shtml) ⭐️ 7.0/10

2026 年前三季度，中国新能源乘用车出口 388.7 万辆，同比增长 138.8%；国内零售 775.8 万辆，同比下降 12.8%。9 月国内新能源乘用车零售同比下降 16.7%，燃油车下降 43%。

telegram · zaihuapd · 11月10日 02:56

**「背景」** 2026 年起，新能源车购置税优惠由全额免征改为减半征收，国家购车补贴也改为按比例补贴，购车成本因此上升；文章把国内需求走弱与这些政策调整以及去年同期的高销量基数联系起来。

**「影响」** 报道称，出口增长已成为车企销量增长的重要支撑，在国内需求走弱时帮助部分抵消压力；不过文中未给出具体车企或出口目的地的数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://post.smzdm.com/p/a03466ww/">2026 ...</a></li>
<li><a href="https://youjia-pc.bdstatic.com/article/9042311325197635062.html">2026 买 车 规则 调 整 ，这些细节不看要多花万元-有驾</a></li>

</ul>
</details>

**标签**: `#新能源车出口`, `#中国汽车市场`, `#国内零售下滑`, `#购置税与补贴`, `#汽车贸易`

---