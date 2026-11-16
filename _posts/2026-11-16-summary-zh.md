---
layout: default
title: "Horizon Summary: 2026-11-16 (ZH)"
date: 2026-11-16
lang: zh
---

> 从 46 条内容中筛选出 10 条重要资讯。

---

**科技新闻**
1. [美团开源 LongCat-2.5，称全程用华为升腾训练](#item-tech-news-1) ⭐️ 7.5/10
2. [Meta FAIR 与 NYU 研究：多模态 LLM 视觉编码器无需单独预训练，但需视觉专用参数](#item-tech-news-2) ⭐️ 7.0/10
3. [多人世界模型游戏:每位玩家在本地 GPU 上生成自己的 CS:GO 画面](#item-tech-news-3) ⭐️ 7.0/10
4. [cmt 工具称可将 B300 上可分页 cudaMemcpy 吞吐提升约 5 倍](#item-tech-news-4) ⭐️ 6.5/10
5. [美法官驳回美光、三星、SK 海力士 DRAM 价格操纵案撤诉动议](#item-tech-news-5) ⭐️ 6.5/10
6. [Raschka 发布现代 LLM 位置嵌入讲解文章](#item-tech-news-6) ⭐️ 6.0/10
7. [ULA Vulcan 复飞任务失利,据报道 40 颗亚马逊卫星损失](#item-tech-news-7) ⭐️ 6.0/10
8. [C++ 语言服务器 Clice 发布 v1.0,定位为 clangd 的现代替代品](#item-tech-news-8) ⭐️ 6.0/10
9. [无需训练的推理模型提前退出:把线性探针折进 &lt;/think&gt; 输出行](#item-tech-news-9) ⭐️ 6.0/10

**财经新闻**
1. [卢特尼克之子执掌的康托尔减持英伟达，引发利益冲突质疑](#item-finance-news-1) ⭐️ 7.0/10

---

## 科技新闻

<a id="item-tech-news-1"></a>
### [美团开源 LongCat-2.5，称全程用华为升腾训练](https://the-decoder.com/meituan-releases-a-1-6-trillion-parameter-agent-model-that-never-touched-an-nvidia-gpu/) ⭐️ 7.5/10

美团 LongCat 团队在模型正式发布一周后，公开了 LongCat-2.5 的权重，采用可商用的 MIT 许可证。该模型面向需要自主完成冗长多步骤任务（尤其是编程）的智能体，每个 token 激活约 480 亿参数，支持文本、图像和视频输入。官方称其训练全程使用华为升腾加速卡、未使用英伟达 GPU，并称其在 Terminal Bench v2.1 上得分 88.4，略低于 Claude Opus 5 的 89.1。以上均为厂商自述，来源文章未给出架构、训练配置或第三方评测，标题中的“1.6 万亿参数”也只见于链接标题。

telegram · zaihuapd · 11月15日 11:08

**「背景」** LongCat-2.5 是美团 LongCat 团队推出的原生多模态智能体模型，面向长程任务、视觉编程和仓库级代码工作。第三方模型页面称其总参数约 1.6T、每个 token 激活约 48B、上下文窗口为 1M；“1.6T”和 1M 上下文并未出现在原文正文中，且这些页面的可靠性有限，应视为待核实信息。训练全程使用华为升腾、未使用英伟达 GPU 的说法，目前仍是官方自述。

**「影响」** MIT 许可证允许商用，开发者和企业在权重可获取的前提下可自行评估并部署该模型，用于编程智能体场景。但“全程使用升腾训练”和基准得分尚无独立验证，采用前宜先用自己的任务实测，不宜仅凭厂商成绩下结论。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.longcatai.org/">LongCat AI - LongCat - 2 . 5 Native Multimodal Agent Model (1.6T)</a></li>
<li><a href="https://lmspeed.net/model/longcat-2-5">LongCat - 2 . 5 API Pricing &amp; Benchmarks | LMSpeed</a></li>
<li><a href="https://llm-stats.com/models/longcat-2.5">LongCat - 2 . 5 Benchmarks, Pricing &amp; Context Window</a></li>

</ul>
</details>

**标签**: `#LongCat-2.5`, `#open-weight models`, `#Huawei Ascend`, `#agentic coding`, `#Meituan`

---

<a id="item-tech-news-2"></a>
### [Meta FAIR 与 NYU 研究：多模态 LLM 视觉编码器无需单独预训练，但需视觉专用参数](https://www.reddit.com/r/MachineLearning/comments/1xx1k2o/meta_fair_nyu_unbundling_multimodal_vision/) ⭐️ 7.0/10

Meta FAIR 与 NYU 的研究者\(帖子由作者之一发布\)把多模态 LLM 的标准视觉编码器拆成三个选择:单独预训练、仅视觉 token 使用的参数、置于 LLM 之前,并分别做对照实验。研究从零训练了 200 多个模型\(含 LLM\),使用相同数据,且编码器预训练算入同一总算力预算;主要对比采用 Qwen3-1.7B 和 4B 配置\(0.4B 视觉参数\),扩展实验覆盖 0.6B 到 6.4B 骨干,评测为 Cambrian 的 16 个 VQA 基准\(448 px\)和 12 个语言基准。作者报告:对比学习、自监督和两种 captioning 四类预训练的编码器,在算力匹配下至多与随编码器从零联合训练持平;把 MetaCLIP 预训练延长 6.5 倍使 ImageNet 线性探测从 80.4% 升至 84.4%,但 VQA 没有提升。无编码器模型在各规模上均落后,约需 3 倍算力才能追平;让 LLM 获得编码器的参数只改善文本、不改善 VQA。作者提出的“In-fusion”在 LLM 前 8 层加入零初始化的视觉专用注意力投影和 FFN\(文本 token 不使用\),在 1.7B 到 6.4B 上与编码器方案持平,首 token 时间约低 13%;在 1.7B 上放在 1–8 层得到 45.0 VQA\(编码器 44.4\),文本共享这些参数为 42.3,放在最后 8 层为 35.1。以上均为作者自报结果,尚未见独立复现。

reddit · r/MachineLearning · /u/trungh98 · 11月15日 17:38

**「背景:视觉编码器的三重捆绑」** 在多模态大模型中,标准的视觉编码器同时捆绑了三项设计:独立的预训练、仅供视觉 token 使用的专属参数,以及置于 LLM 之前的位置。各实验室的做法并不一致:帖子称 Gemma 4 12B 去掉了编码器,Kimi K3 从头训练编码器,Inkling 2 Small 又重新引入编码器,但这些说法无法由所给材料核实。已发布模型的数据和算力各不相同,也很少把编码器预训练计入总算力,所以难以直接比较。这项研究因此把三项设计拆开,在相同数据和相同总算力下逐项检验。

**「影响」** 若结论成立,设计多模态模型的团队在预算有限时,可以把算力更多投向视觉专用参数,而不是单独预训练编码器,并可考虑 In-fusion 这类将视觉专用权重并入 LLM 的结构来降低首 token 延迟。但实验只覆盖最大约 6.4B 的骨干和小规模视觉容量,能否推广到前沿规模尚不确定,采用前需自行验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2611.17334v1">Unbundling Multimodal Vision Encoding - arXiv.org</a></li>
<li><a href="https://sparsenotes.com/posts/2026/11/papers/unbundling-multimodal-vision-encoding/">Unbundling Multimodal Vision Encoding | Sparse Notes</a></li>

</ul>
</details>

**标签**: `#multimodal-LLM`, `#vision-encoder`, `#ablation-study`, `#Meta-FAIR`, `#pretraining`

---

<a id="item-tech-news-3"></a>
### [多人世界模型游戏:每位玩家在本地 GPU 上生成自己的 CS:GO 画面](https://www.reddit.com/r/MachineLearning/comments/1xx4ta3/we_made_a_multiplayer_game_where_each_players/) ⭐️ 7.0/10

开发者发布了一个免费公测版多人游戏:轻量服务器负责同步游戏状态,每位玩家在本地运行世界模型,根据服务器状态、玩家操作和此前画面,用扩散 Transformer 逐帧生成自己的视角。模型训练自他们上月发布的开放数据集,包含 10 人 CS:GO 机器人对战,约 3958 小时,所有玩家视角与输入以 16 Hz 对齐。目前限制明显:仅有一张小地图、只能使用手枪,细节表现较弱;运行需要 RTX 3080 或更好的显卡,另有实验性的 Mac 版本。以上均为作者在 Reddit 帖子中的自述,未提供架构细节、延迟或画质指标,也没有论文。

reddit · r/MachineLearning · /u/bengal7ion · 11月15日 19:46

**「背景」** 世界模型是指根据历史画面、玩家操作和环境状态预测下一帧的生成式模型，此处用扩散 Transformer 代替传统游戏引擎来绘制画面。多人场景的难点在于，各玩家各自生成的画面需要与同一份游戏状态保持一致，因此该团队先发布了包含全部玩家视角和输入的开放数据集，再让服务器同步状态、由各玩家本地推理出自己的视角。

**「影响」** 对研究者而言,这个数据集提供了多视角对齐的画面与输入数据,可用于训练或复现多人场景下的世界模型。对想试玩的用户,需要 RTX 3080 级别以上的显卡,且画质与原版游戏差距很大。目前尚无独立评测,多人一致性效果只能靠自行试玩来验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://vor.tech/">VOR.TECH — open multiplayer gameplay data for world models</a></li>
<li><a href="https://x.com/v0rt3ch/status/2122031717712085388">vor.tech on X: &quot;1/ We made a playable multiplayer game using ...</a></li>

</ul>
</details>

**标签**: `#world-models`, `#diffusion-transformers`, `#generative-games`, `#open-dataset`, `#multiplayer`

---

<a id="item-tech-news-4"></a>
### [cmt 工具称可将 B300 上可分页 cudaMemcpy 吞吐提升约 5 倍](https://www.reddit.com/r/MachineLearning/comments/1xx2n25/making_cudamemcpy_5x_faster_on_a_b300_p/) ⭐️ 6.5/10

一位 Reddit 作者发布了开源工具 cmt\(仓库名 cudamemcpy-tuner\),用于调优可分页\(pageable\)内存的 cudaMemcpy 传输。作者给出的示例是:在 B300 上用 PyTorch 把 1 GB 的 uint8 张量从 CPU 拷贝到 GPU,吞吐从 10.2 GB/s 提升到 51.5 GB/s,用法是 \`cmt tune -- python bench.py\`。这只是作者自测的单一基准,帖子给出了博客和 GitHub 链接,但摘要内容没有说明具体优化机制。

reddit · r/MachineLearning · /u/makneeee · 11月15日 18:20

**「背景：可分页内存的传输路径」** CUDA 中的可分页（pageable）主机内存不能被 GPU 直接做 DMA，驱动通常要先把数据拷到一块临时的锁页（pinned）缓冲区，再由 DMA 传到 GPU，所以其吞吐常低于直接使用锁页内存的传输（据 tool-1-2 的第三方说明）。PyTorch 中对普通 CPU 张量调用 \`.to\(&quot;cuda&quot;\)\` 默认走的就是这条路径，因此 cmt 针对的是这一类常见但较慢的传输。帖子本身没有说明 cmt 的具体调优机制，上述路径只是对问题成因的一般性背景。

**「影响」** 如果你的 ML 流程大量使用可分页主机内存做 CPU 到 GPU 传输,可以在自己的硬件和数据规模上试用 cmt,与现有基线对比。需要注意,目前证据只覆盖一台 B300、一种 1 GB 的传输,也没有与固定内存\(pinned memory\)方案对比,因此收益能否推广到其他场景还需独立验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://medium.com/@bethe1tweets/cudamemcpy-vs-cudamemcpyasync-b7af8da56b8d">cudaMemcpy () vs cudaMemcpyAsync() | by Pranjali Puranik | Medium</a></li>

</ul>
</details>

**标签**: `#CUDA`, `#GPU performance`, `#cudaMemcpy`, `#memory transfer`, `#open source`

---

<a id="item-tech-news-5"></a>
### [美法官驳回美光、三星、SK 海力士 DRAM 价格操纵案撤诉动议](https://www.tomshardware.com/tech-industry/big-tech/judge-denies-motion-to-dismiss-dram-price-fixing-lawsuit-against-micron-samsung-and-sk-hynix-says-chipmakers-acted-like-hawks-flying-in-formation-finds-evidence-of-dram-collusion-plausible-after-500-percent-price-surge) ⭐️ 6.5/10

美国法官 Noël Wise 驳回了美光、三星和 SK 海力士要求撤销 DRAM 价格操纵集体诉讼的动议。她认为原告已提出新证据，三家厂商的同步行为“更像编队飞行”。原告为 17 名个人和小企业，指控三家公司在一年内四次采取平行动作限制 DRAM 供应，使价格最多上涨 500%。三家公司须在 12 月 7 日前作出回应，案件管理会议定于 2027 年 1 月举行。

telegram · zaihuapd · 11月15日 16:39

**「背景」** 这是一起拟议的集体诉讼，原告指控美光、三星和 SK 海力士限制 DRAM 供应（报道提到削减传统内存产能）以推高价格，三家公司随后联合申请驳回。据 TechPowerUp 报道，北加州联邦地区法院的 Noël Wise 法官于 11 月 14 日驳回该动议。在这一驳回起诉的阶段，法院通常只审查原告的指控是否足以成立、值得进入后续程序，并不认定共谋事实已被证明。

**「影响」** 案件将进入后续程序，三家厂商需要正式回应指控。但该裁定只表明在起诉阶段，原告的串通指控被认为有可能成立，并不是对价格操纵的认定，最终结果仍不确定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://wccftech.com/federal-judge-rejects-memory-makers-defense-samsung-micron-sk-hynix-dram-shortage-lawsuit/">Federal Judge Rejects Memory Makers’ Defense To Advance...</a></li>
<li><a href="https://www.techpowerup.com/354863/samsung-sk-hynix-and-micron-fail-to-get-dram-antitrust-suit-dismissed">Samsung , SK hynix , and Micron Fail to Get DRAM ... | TechPowerUp</a></li>

</ul>
</details>

**标签**: `#DRAM`, `#antitrust`, `#price-fixing`, `#semiconductor industry`, `#memory market`

---

<a id="item-tech-news-6"></a>
### [Raschka 发布现代 LLM 位置嵌入讲解文章](https://magazine.sebastianraschka.com/p/understanding-positional-embeddings) ⭐️ 6.0/10

Sebastian Raschka 的杂志发布了一篇题为《Understanding Positional Embeddings in Modern LLMs》的文章，讲解现代大语言模型中的位置嵌入。目前只有标题和来源可用，没有正文内容，因此文章的具体覆盖范围、深度、示例和结论都无法核实。从标题和讨论来看，这更像是一篇教学性讲解，而不是新研究成果。

hackernews · vismit2000 · 11月15日 12:14 · [社区讨论](https://news.ycombinator.com/item?id=50506376)

**「背景:为什么 Transformer 需要位置编码」** Transformer 的自注意力本身不区分 token 的先后顺序,因此模型需要额外的位置信息。早期的 GPT-2 把可学习的绝对位置向量加到 token 嵌入上,与固定的上下文长度\(最初为 1,024 个位置\)绑定。较新的模型多采用 RoPE\(旋转位置编码\)等方法,部分架构还会部分使用或省略显式位置编码。据搜索结果中对该文的介绍,Raschka 的文章通过图示、少量数学和一个小型 PyTorch 实现来讲解这些方法。

**「社区讨论」** 评论者 programjames 认为，文章侧重位置嵌入的实现，而要真正理解它，需要从群表示论入手：位置嵌入可以看作群表示，这一视角也可用来推导并参数化可学习的嵌入。该评论者举例称，旋转位置编码（RoPE）是平移群的表示，并指出 n 维平移群 ℝⁿ 是阿贝尔群。这是评论者的个人观点，评论内容在提供的文本中被截断，也未经文章内容验证。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://magazine.sebastianraschka.com/p/understanding-positional-embeddings">Understanding Positional Embeddings in Modern LLMs</a></li>
<li><a href="https://daily.dev/posts/understanding-positional-embeddings-in-modern-llms-415mglzuo">Understanding Positional Embeddings in Modern LLMs</a></li>
<li><a href="https://explainx.ai/blog/rope-positional-embeddings-modern-llms-raschka-guide-2026">RoPE and NoPE: What Sebastian Raschka&#x27;s 2026 Positional ...</a></li>

</ul>
</details>

**标签**: `#positional-embeddings`, `#LLM`, `#transformers`, `#RoPE`, `#machine-learning-education`

---

<a id="item-tech-news-7"></a>
### [ULA Vulcan 复飞任务失利,据报道 40 颗亚马逊卫星损失](https://www.space.com/space-exploration/launches-spacecraft/ula-vulcan-centaur-return-to-flight-amazon-leo-internet-satellite-launch) ⭐️ 6.0/10

据报道,ULA 的 Vulcan 火箭在复飞任务中发射失败,所载 40 颗 Amazon Leo\(亚马逊低轨互联网星座\)卫星随之损失。提供的原文内容为空,因此失败发生的具体阶段、原因和调查进展均无从核实。评论中引用的说法称,这是 ULA 20 年历史上首次整次任务失败,但该说法来自评论转引,并非经核实的文章正文。

hackernews · jonbaer · 11月15日 20:37 · [社区讨论](https://news.ycombinator.com/item?id=50510442)

**「背景」** 据 CBS News 报道,此次发射是亚马逊购买的 38 次 Vulcan 任务中的第一次,用于部署与 Starlink 竞争的 Amazon Leo 卫星星座;ULA 此前已用 Atlas 5 火箭执行了 8 次 Leo 发射。据 NY Post 报道,火箭在升空近 10 分钟后出现“异常”,ULA 尚未说明具体原因,表示将展开调查并“尽快恢复飞行”。

**「影响」** 若报道属实,亚马逊 Leo 星座的部署进度可能受到影响,美国政府和商业客户在重型发射服务上对 SpaceX 的依赖也可能加深。不过现有材料没有说明后续发射安排或调查结论,具体影响需等待 ULA 和亚马逊的官方说明。

**「社区讨论」** 多位评论者认为,美国需要不止一家可靠的发射服务商,有人认为 ULA 当初采取保守的设计路线,随后又遇到不少初期问题。另有评论者质疑 ULA 是否像 SpaceX 那样可以通过试飞迭代,还是每次任务都承担全部风险;这些都是个人观点,不是已证实的事实。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://nypost.com/2026/11/15/us-news/ula-loses-40-amazon-leo-satellites-in-total-mission-failure-minutes-after-rocket-launch/">ULA loses 40 Amazon Leo satellites in ‘total mission failure ’ minutes...</a></li>
<li><a href="https://www.cbsnews.com/news/vulcan-rocket-40-amazon-leo-internet-satellites-launch-mishap/">United Launch Alliance loses Vulcan rocket and 40 Amazon Leo ...</a></li>

</ul>
</details>

**标签**: `#ULA Vulcan`, `#launch failure`, `#Amazon Leo`, `#space industry`, `#satellite internet`

---

<a id="item-tech-news-8"></a>
### [C++ 语言服务器 Clice 发布 v1.0,定位为 clangd 的现代替代品](https://ykiko.me/en/articles/2105384023094834022/) ⭐️ 6.0/10

Clice 是一个定位为 clangd 现代替代品的 C++ 语言服务器,其作者发文宣布项目达到 v1.0。本次仅获得文章标题和 Hacker News 评论,没有拿到正文,因此具体的设计细节、基准测试数据和兼容性条件都无法核实。评论显示,文章中似乎展示了 clangd 在 VS Code 中崩溃的情形,结尾还流露出对 AI 时代编程的感伤。

hackernews · molenzwiebel · 11月15日 17:22 · [社区讨论](https://news.ycombinator.com/item?id=50508715)

**「背景」** 语言服务器是为编辑器提供跳转定义、补全和高亮等功能的后台程序，C++ 领域目前最常用的是基于 LLVM/Clang 的 clangd。Clice 同样建立在 LLVM/Clang 之上，但据其项目主页和作者博客介绍，它是从头重新设计的，并移植了 clangd 的部分组件，目标是解决 clangd 与 ccls 多年未解决的架构问题。据 daily.dev 转述，Clice 的做法之一是用类似浏览器的多进程池在隔离的子进程中编译代码，因此单个工作进程在处理不完整代码时崩溃，不会拖垮整个服务器；这是项目方的设计说明，本次未获取原文，也没有独立验证。

**「影响」** 对正在使用 clangd 的 C++ 开发者来说,v1.0 意味着可以重新评估 Clice。有评论者称几个月前它还不够稳定,另一位评论者指出它在与 clangd 相同的位置也会崩溃,所以迁移前最好先在自己的代码库上测试稳定性和索引速度。

**「社区讨论」** 有评论者认为,基于 clang 的索引器在大型代码库上比 Eclipse、Qt Creator 的旧式索引器慢得多,甚至要花数天,因此希望有不依赖 clang 的快速索引器。这是个人经验,不是已验证的基准。另一位评论者则对 Clice 的崩溃截图提出疑问,认为既然展示了问题,似乎应该直接修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/clice-io/clice">GitHub - clice-io/clice: A next-generation C++ language ...</a></li>
<li><a href="https://ykiko.me/en/articles/2105384023094834022/">clice v1.0 Released: Welcome to Modern C++ | ykiko&#x27;s blog</a></li>
<li><a href="https://daily.dev/posts/clice-v1-0-released-welcome-to-modern-c--ca2kgqqeh">Clice v1.0 Released: Welcome to Modern C++ - daily.dev</a></li>

</ul>
</details>

**标签**: `#Clice`, `#C++`, `#language-server`, `#clangd`, `#developer-tools`

---

<a id="item-tech-news-9"></a>
### [无需训练的推理模型提前退出:把线性探针折进 &lt;/think&gt; 输出行](https://www.reddit.com/r/MachineLearning/comments/1xx1xdm/trainingfree_early_exit_for_reasoning_models_a/) ⭐️ 6.0/10

一位 Reddit 用户提出,只修改推理模型输出层\(lm\_head\)中 &lt;/think&gt; 对应的一行权重,就能让模型在已经得出答案后停止“再检查”。做法是用 24 道数学题记录思考过程中每个 token 的隐藏状态,把答案已出现后的段落末尾标为“只是复查”,用线性判别分析\(无梯度训练\)求出区分方向,再按强度 14 加到该行上,所以推理时不需要额外代码,编辑后的权重可在普通运行环境中使用。作者自报的结果样本很小:Qwen3.5-4B 在 8 道未见过的 MATH-500 题上准确率不变、token 减少 54%;在 3 道 AIME 2025 题\(32k 上限\)上,原模型全部耗尽 token,编辑后解出 2 道;DeepSeek V4.1 Flash\(2 比特量化\)为 7/7 对 6/7,token 减少 40%。作者提供了 GGUF 模型、代码和日志,这些结果均为作者自测,尚无独立验证。

reddit · r/MachineLearning · /u/Good-Presentation-23 · 11月15日 17:52

**「背景」** 推理模型在“思考”阶段结束时会输出特殊 token &lt;/think&gt;,而下一个 token 的得分是输出层对应行与隐藏状态的乘积。用隐藏状态上的探针判断是否提前停止推理,已有论文发表\(如帖中引用的 Zhang 等人 2025,arXiv 2504.05419\);作者称自己的新意只是把探针直接并入这一行权重,使推理时无需运行任何额外组件。

**「影响」** 如果结果能够复现,使用 llama.cpp 等标准运行时的用户可以直接换用编辑后的权重文件来降低推理 token 开销,而无需改动推理代码。但探针只在数学题上拟合,智能体场景属于迁移结果,AIME 对比所用的 32k 预算也低于 Qwen 推荐的 81,920,因此在其他任务上使用前需要自行评估是否会过早停止。

**标签**: `#reasoning-models`, `#early-exit`, `#linear-probe`, `#inference-efficiency`, `#LLM`

---

## 财经新闻

<a id="item-finance-news-1"></a>
### [卢特尼克之子执掌的康托尔减持英伟达，引发利益冲突质疑](https://www.cnbc.com/2026/11/13/howard-lutnick-nvidia-jensen-huang-china-cantor-fitzgerald.html) ⭐️ 7.0/10

据 CNBC 对持仓文件的分析，由商务部长卢特尼克之子执掌的康托尔菲茨杰拉德，2025 年 9 月至 2026 年 3 月间申报的英伟达持股数量下降约 49%，从约 350 万股降至 178 万股。与此同时，Axios 报道称卢特尼克多次抵制对涉嫌向中国转运英伟达芯片的公司采取行动；目前没有证据表明存在不当信息共享。

rss · CNBC Finance · 11月15日 19:58

**「背景」** 实体清单是美国商务部管理的出口限制名单，企业一旦被列入，获取美国技术和产品就会受限。财政部长贝森特称，多个部门数月来都主张把涉嫌向中国转运英伟达先进 AI 芯片的新加坡公司 Megaspeed 列入，据英国《金融时报》报道，商务部推迟了这一动作。

**「影响」** 这一事件让外界更加关注美国芯片出口管制的执行是否受到利益冲突影响，尤其是商务部是否将涉事公司列入“实体清单”（受限企业名单）；但目前尚无证据显示康托尔的业务利益影响了卢特尼克的决定。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.ft.com/content/afb6c960-a910-4d67-9588-73ba3bea5b06?syn-25a6b1a6=1">US commerce department delays Megaspeed’s inclusion on trade ...</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#Chip export controls`, `#Cantor Fitzgerald`, `#Howard Lutnick`, `#Conflict of interest`

---