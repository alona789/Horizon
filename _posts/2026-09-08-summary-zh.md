---
layout: default
title: "Horizon Summary: 2026-09-08 (ZH)"
date: 2026-09-08
lang: zh
---

> 从 32 条内容中筛选出 6 条重要资讯。

---

1. [谷歌 InferenceX 推动 TPU 外部化，挑战 NVIDIA CUDA 护城河](#item-1) ⭐️ 8.0/10
2. [仅 417k 参数循环系统自主生成 Bad Apple 视频](#item-2) ⭐️ 8.0/10
3. [LLM 引导的程序进化改进了 10 个圆形填充方案](#item-3) ⭐️ 8.0/10
4. [31,352 次重复基准测试揭示大语言模型性能漂移](#item-4) ⭐️ 8.0/10
5. [华为时隔六年再度发布逻辑折叠技术麒麟 9050 Pro](#item-5) ⭐️ 8.0/10
6. [最高法出台 AI 司法解释，明确换脸与算法杀熟责任](#item-6) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [谷歌 InferenceX 推动 TPU 外部化，挑战 NVIDIA CUDA 护城河](https://newsletter.semianalysis.com/p/tpu-inferencex-full-steam) ⭐️ 8.0/10

据 SemiAnalysis 的一份新报告，谷歌正通过名为 InferenceX 的举措快速向外部客户开放其 TPU 推理技术栈，宣称每美元性能比竞争对手高出最多 50%。报告称该举措正吸引越来越多客户，并涵盖当前 Ironwood 及下一代 TPUv8i 硬件。 如果报告中所说的每美元性能优势属实，将增强 Google Cloud 在 AI 推理领域的竞争力，并直接削弱 NVIDIA 的 CUDA 软件护城河。外部 TPU 客户群的增长可能颠覆 AI 加速器市场，迫使 NVIDIA 以更激进的定价或更开放的软件生态来应对。 该分析特别提到了 Ironwood（谷歌于 2025 年发布的第七代面向推理的 TPU）以及 TPUv8i（代号“Zebrafish”，预计 2026 年底全面上市的高性价比推理加速器）。现有摘要中未说明“最高 50%”优势的具体对比基准，因此参照对象（如 NVIDIA H100、B200 或其他 TPU）尚不明确。

rss · Semianalysis · 9月7日 20:00

**背景**: AI 推理——即运行已训练模型来生成预测——已成为谷歌等云厂商的关键工作负载。谷歌为 AI 工作负载自研张量处理单元（TPU），并长期在内部使用，但如今正越来越多地通过 Google Cloud 等渠道向外部客户提供服务。NVIDIA 的 CUDA 软件生态历史上一直是 AI 开发的事实标准，因此谷歌以高性价比故事推动 TPU 技术栈外部化，是其削弱 NVIDIA 主导地位的更广泛战略的一部分。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/infrastructure-and-cloud/google-cloud/ironwood-google-tpu-things-to-know/">3 things to know about Ironwood, Google&#x27;s latest TPU</a></li>
<li><a href="https://www.servethehome.com/googles-tpuv8s-for-training-and-inference-at-hot-chips-2026/">Google&#x27;s TPUv 8 s for Training and Inference at Hot... - ServeTheHome</a></li>
<li><a href="https://www.nextplatform.com/2025/09/17/google-shows-off-its-inference-scale-and-prowess/">Google Shows Off Its Inference Scale And Prowess</a></li>

</ul>
</details>

**标签**: `#TPU`, `#AI inference`, `#Google Cloud`, `#CUDA`, `#AI accelerators`

---

<a id="item-2"></a>
## [仅 417k 参数循环系统自主生成 Bad Apple 视频](https://www.reddit.com/r/MachineLearning/comments/1wa8rub/generating_bad_apple_autonomously_from_a_single/) ⭐️ 8.0/10

作者训练了一个仅有 417,129 个参数的小型循环动力系统，它能从单一初始潜状态\(h\_0,c\_0\)自主生成整段约 6500 帧的 Bad Apple 视频，完全不需要输入每帧的时间戳。代码、权重和分析工具已发布在 GitHub 上。 这项工作表明，紧凑的循环网络能够学习连续的时间动态，并外推到远超训练时长的范围，从而无需在隐式神经表示中显式加入时间条件。这对视频生成、动力系统研究以及基于 INR 的建模具有技术参考价值。 推理模型采用 4 门 LSTM 式循环转移\(CTF\)，含 16,640 个参数，以及一个 400,361 个参数的帧解码器，在 RTX 4080 上可达到每秒 200 帧以上。训练使用了可学习的潜在教师表、从 2 逐步翻倍到 512 的 rollout 长度课程、状态扰动噪声、二阶差分加速度正则化，以及 AdamW/Muon 优化；尽管只在 512 帧的范围内训练，模型仍能展开完整的约 6,573 步序列。

reddit · r/MachineLearning · /u/SEBADA321 · 9月8日 00:05

**背景**: 隐式神经表示\(INR\)又称神经场，是一种将连续坐标\(如时间与空间位置\)映射为信号值的神经网络，能够紧凑地编码图像、视频和 3D 场景。SIREN 是一种使用正弦激活函数的 INR 架构；此前有项目将 Bad Apple 作为坐标函数\(t,y,x\)映射到像素来记忆。本次工作在此基础上，用循环动力系统取代显式的时间戳输入，使其在时间上自主演化潜状态。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Implicit_neural_representation">Implicit neural representation</a></li>
<li><a href="https://deepwiki.com/vsitzmann/siren/2-siren-architecture">SIREN Architecture | vsitzmann/siren | DeepWiki</a></li>
<li><a href="https://www.emergentmind.com/topics/siren-architecture">SIREN: Sinusoidal Representation Networks</a></li>

</ul>
</details>

**标签**: `#Recurrent Neural Networks`, `#Video Generation`, `#Implicit Neural Representations`, `#Machine Learning`

---

<a id="item-3"></a>
## [LLM 引导的程序进化改进了 10 个圆形填充方案](https://www.reddit.com/r/MachineLearning/comments/1w9xlyi/llmguided_program_evolution_improves_10_bestknown/) ⭐️ 8.0/10

作者使用 LLM 引导的程序进化，从简单的种子求解器开始迭代改进优化算法，在 Packomania csqv 基准上使 N=101 至 114 共 10 个案例的最佳已知半径和提升了 2.4%到 5.4%，共进行了 15 次迭代。LLM 总费用仅为 27.72 美元，Packomania 已独立接受这些结果。 这表明 LLM 引导的程序进化能够以极低成本并经过独立验证地改进公认的优化基准最佳记录。它展示了一条前景广阔且经济高效的自动化算法发现路径，未来可应用于其他困难优化问题。 该方法利用结果记分板和先前尝试的历史来引导 LLM 提出修改，每个候选方案都由独立验证器评分，保留改进、丢弃失败。该系统名为 Discovery Loop，代码、解决方案和论文均已公开，作者特别希望有人对其中的平台期检测停止规则提出评审意见。

reddit · r/MachineLearning · /u/SIGH\_I\_CALL · 9月7日 16:54

**背景**: 圆形填充（circle packing）是一个经典的几何与优化问题，目标是在容器内互不重叠地放置圆形；Packomania 上的 csqv 变体要求最大化单位正方形内 N 个可变大小圆形的半径总和。LLM 引导的程序进化是一种让大语言模型在演化循环中根据实测性能提出算法级代码修改的技术，而不是直接求解目标问题。Packomania 是知名的公开记录库，用于追踪最佳已知填充结果，因此被其独立接受的改进更具可信度。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2609.05093v1">LLM-Guided Program Evolution for Circle Packing:Breaking 10 ...</a></li>
<li><a href="https://arxiv.org/abs/2403.11446">[2403.11446] LLM Guided Evolution -- The Automation of Models ... LLM Guided Evolution - The Automation of Models Advancing ... GitHub - clint-kristopher-morris/llm-guided-evolution: LLM ... LLM Guided Evolution - The Automation of Models Advancing Models LLM Guided Evolution - The Automation of Models Advancing Models llm-guided-evolution/README.md at main · clint-kristopher ...</a></li>
<li><a href="https://packomania.com/">Packomania (52C17)</a></li>

</ul>
</details>

**标签**: `#LLM`, `#program evolution`, `#optimization`, `#circle packing`, `#AI for science`

---

<a id="item-4"></a>
## [31,352 次重复基准测试揭示大语言模型性能漂移](https://www.reddit.com/r/MachineLearning/comments/1w9llr4/measuring_llm_performance_drift_observations_and/) ⭐️ 8.0/10

AI Stupid Level 团队发布了一套纵向基准测试方法论，利用对 49 个模型的 31,352 次重复评分测量来检测大语言模型的性能漂移，将评估视为时间序列测量而非静态排行榜快照。 静态排行榜分数会误导对 API 模型的判断，因为同名模型背后的行为会因基础设施、配置或版本变化而逐日改变。该研究量化了时间变化，并促使社区将漂移视为可测量现象，从而提高大模型评估的可信度。 该分析覆盖 49 个模型和 31,352 次重复评分；日内分数的标准差为 2.80 分，而日间每日中位数的标准差为 8.43 分。作者对基准配置进行版本化，以执行式评估替代 LLM 评审，将可用性故障与有效结果区分开，并对生成的时间序列应用变点检测。

reddit · r/MachineLearning · /u/ionutvi · 9月7日 07:44

**背景**: 大语言模型性能漂移指模型随时间推移表现变差或以不同方式运行的现象。对于通过 API 提供的模型，稳定模型名称背后的接口可能因提供商更新基础设施、配置或版本而发生改变。传统基准测试只是静态快照，而纵向基准测试则以模型自身过去的行为为基线持续测量，以便检测漂移。相关的实践指南以及“冻结、确定性”的纵向基准套件都强调版本跟踪，以避免把变化错误归因于模型能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.fiddler.ai/blog/how-to-monitor-llmops-performance-with-drift">How to Monitor LLMOps Performance with Drift Monitoring | Fiddler AI Blog</a></li>
<li><a href="https://medium.com/@tsiciliani/drift-detection-in-large-language-models-a-practical-guide-3f54d783792c">Drift Detection in Large Language Models: A Practical Guide | by Tony Siciliani | Medium</a></li>
<li><a href="https://github.com/jmeadlock/milo-bench">jmeadlock/milo-bench: Frozen, deterministic, longitudinal benchmark ...</a></li>

</ul>
</details>

**标签**: `#LLM`, `#benchmarking`, `#performance drift`, `#ML evaluation`, `#API models`

---

<a id="item-5"></a>
## [华为时隔六年再度发布逻辑折叠技术麒麟 9050 Pro](https://www.news.cn/20260907/adf46c5c003240d28cc3cf6de54f9b5f/c.html) ⭐️ 8.0/10

华为于 2026 年 9 月 7 日在广州发布 Mate XT 2 三折叠手机，首发搭载麒麟 9050 Pro 芯片。这是华为首款采用逻辑折叠技术的高性能芯片，也是继 Mate 40 之后时隔六年推出的全新旗舰麒麟处理器。 该芯片结束了华为旗舰麒麟芯片六年的更新空窗期，表明其在先进制造受限的背景下正走出一条差异化技术路线。若逻辑折叠技术确实达到宣称的性能提升，将对传统制程微缩路径形成挑战，并加剧先进封装与三维集成领域的竞争。 麒麟 9050 Pro 在单芯片内将逻辑单元分层排布，并加入垂直互连通道，以缩短信号传输路径、降低时延。该芯片还支持按场景调度 CPU 核心，并搭载达芬奇架构 NPU，可在端侧运行总参数达 300 亿、激活参数为 20 亿的全模态大模型。

telegram · zaihuapd · 9月7日 08:20

**背景**: 逻辑折叠技术是华为 2026 年 5 月在上海举行的 ISCAS 2026 上随“韬\(τ\)定律”一起提出的，属于三维集成电路与先进封装范畴，主张以“时间缩微”替代传统的“几何缩微”。由于华为在外部限制下难以获得最先进制程产能，这类封装和架构创新便成为其维持芯片竞争力的重要技术路线。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/%E9%80%BB%E8%BE%91%E6%8A%98%E5%8F%A0%E6%8A%80%E6%9C%AF/67870423">逻辑折叠技术_百度百科</a></li>
<li><a href="https://www.ithome.com/0/999/337.htm">华为 Mate XT 2 非凡大师全新展翼三折叠手机发布：首发 麒 麟 9050 Pro ...</a></li>
<li><a href="https://www.sohu.com/a/1028674003_100085330">深度解读华为逻辑折叠技术:并非3D堆叠而是全新突破枷锁技术路线</a></li>

</ul>
</details>

**标签**: `#Huawei`, `#semiconductor`, `#Kirin chip`, `#chip technology`, `#announcement`

---

<a id="item-6"></a>
## [最高法出台 AI 司法解释，明确换脸与算法杀熟责任](https://www.cnr.cn/news/20260907/t20260907_527806795.shtml) ⭐️ 8.0/10

9 月 7 日，最高人民法院发布共 5 部分 24 条的人工智能纠纷案件司法解释。解释明确，未经同意用 AI 制作可识别的人脸、声音可能构成人格权侵权，算法杀熟、AI 冒充他人代言等行为需承担相应民事责任。 这是中国首个系统规定 AI 纠纷民事责任的司法解释，为法院处理换脸、算法杀熟等案件提供了明确法律依据。它将促使 AI 开发者和平台加强用户授权与合规建设，也为消费者维权提供了更清晰的途径。 司法解释共 24 条、分 5 部分，还涉及自动驾驶、知识产权等问题。意见明确，AI 冒充他人代言诱导消费的，可依法支持惩罚性赔偿请求，并规制利用 AI 实施&\#x27;网络开盒&\#x27;&\#x27;人肉搜索&\#x27;等侵害隐私权的行为。

telegram · zaihuapd · 9月7日 09:32

**背景**: &\#x27;大数据杀熟&\#x27;指平台通过数据分析对同一商品或服务向不同客户展示不同价格，老客户反而比新客户支付更高价格；该现象自 2018 年起引发广泛关注，已被个人信息保护法和电子商务法所禁止。&\#x27;网络开盒&\#x27;是一种新式网络暴力，指非法获取并公开他人隐私信息（如姓名、住址、联系方式）以进行骚扰，通常比传统&\#x27;人肉搜索&\#x27;更具攻击性。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://baike.baidu.com/item/%E5%A4%A7%E6%95%B0%E6%8D%AE%E6%9D%80%E7%86%9F/22456755">大数据杀熟_百度百科 算法滥用风险的监管现状与趋势探析-以“大数据杀熟”为视角 - 今日头条 算法加持下大数据“杀熟”？ - 知乎 算法厌恶背后：从伪装广告到大数据杀熟，用户为何感觉被收割？ 从程序员的角度出发：大数据杀熟，到底是什么原理？怎么反制？ 揭秘：为什么被杀熟的总是你？算法早已给你贴上了“待宰”标签</a></li>
<li><a href="https://xinwen.bjd.com.cn/content/s6669b8d8e4b035c6ca5eaf35.html">比“人肉搜索”更恶劣！ 焦点访谈起底新式 网 暴“ 开 盒 挂人”</a></li>

</ul>
</details>

**标签**: `#AI regulation`, `#China`, `#deepfake`, `#algorithmic discrimination`, `#legal compliance`

---