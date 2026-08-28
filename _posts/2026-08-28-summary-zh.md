---
layout: default
title: "Horizon Summary: 2026-08-28 (ZH)"
date: 2026-08-28
lang: zh
---

> 从 32 条内容中筛选出 14 条重要资讯。

---

1. [Cloudflare 优化 1.1.1.1 DNS 缓存，节省 100TB 内存](#item-1) ⭐️ 8.0/10
2. [小模型时代已来：实用 AI 不再依赖前沿大模型](#item-2) ⭐️ 8.0/10
3. [507 种机械运动在线动画重现](#item-3) ⭐️ 8.0/10
4. [谷歌发布 Gemini-3.5-Transcribe，高精度语音转文字但延迟较高](#item-4) ⭐️ 8.0/10
5. [开源 Rust 原生 LLM 网关：统一模型路由并能利用流量训练定制模型](#item-5) ⭐️ 8.0/10
6. [分析 Claude 过度使用的“承重”词汇](#item-6) ⭐️ 8.0/10
7. [在 84 天内反编译一款任天堂 64 游戏](#item-7) ⭐️ 8.0/10
8. [提示注入攻击以 80%成功率突破 Claude Code 自动模式](#item-8) ⭐️ 8.0/10
9. [新基准 HarnessOpt-Bench：安全评估 AI 递归自我改进](#item-9) ⭐️ 8.0/10
10. [英伟达季度营收 962 亿美元，首次提前给出 70% 增长指引](#item-10) ⭐️ 8.0/10
11. [Anthropic 预览模型硬件标准，AI 智能体可操控物理设备](#item-11) ⭐️ 8.0/10
12. [OpenAI 被曝开发常驻 Codex 代理，持续工作至休眠](#item-12) ⭐️ 8.0/10
13. [美国法官叫停五角大楼对 Anthropic 的禁令](#item-13) ⭐️ 8.0/10
14. [腾讯混元发布开源模型 Hy4 preview，盲测胜过 GLM-5.3 与 Kimi K3](#item-14) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare 优化 1.1.1.1 DNS 缓存，节省 100TB 内存](https://blog.cloudflare.com/dns-cache-memory-optimization-1111/) ⭐️ 8.0/10

Cloudflare 工程师发布了一篇详细的技术文章，介绍他们如何通过仔细的数据结构和内存管理优化，将 1.1.1.1 DNS 缓存的内存占用削减了 100 TB。这些节省来自软件层面的调整，而非硬件升级。 对于一个处理海量查询的公共 DNS 服务来说，节省 100TB 内存是巨大的基础设施收益。它可以降低运营成本，通过允许更多条目驻留内存来提高缓存命中率，从而惠及整个互联网的域名解析性能。 这一 100TB 的削减是通过重新设计 DNS 缓存对记录的存储和分配方式实现的，博客文章提供了详细的技术讲解。它体现了底层内存调优（常被专家视为“琐碎”的工作）能够带来巨大的聚合收益。

hackernews · TangerineDream · 8月27日 17:17 · [社区讨论](https://news.ycombinator.com/item?id=49468083)

**背景**: 1.1.1.1 是 Cloudflare 提供的公共递归 DNS 解析器，全球用户用它来解析域名。为快速响应并减少上游流量，解析器会在内存中缓存 DNS 记录。大规模、高使用的缓存会消耗大量内存，因此内存布局和分配策略直接影响成本与性能。这篇文章聚焦于运行该类服务时的内存优化问题。

**社区讨论**: 评论者总体上认可“先跑通产品和业务、再进行优化”的做法，并指出类似结构体对齐、减少分配开销等技术在系统编程中很常见。有评论者建议将记录数据直接放在 CacheEntry 成员之后，而不是单独分配内存；也有评论者担心，把多个独立列表合并到一个结构中可能会削弱 Rust 的安全保证。

**标签**: `#DNS`, `#memory-optimization`, `#system-programming`, `#Cloudflare`, `#rust`

---

<a id="item-2"></a>
## [小模型时代已来：实用 AI 不再依赖前沿大模型](https://calv.info/small-models-have-arrived) ⭐️ 8.0/10

文章《Small Models Have Arrived》（小模型已经到来）认为，小语言模型在许多面向消费者的场景中已经具备实用性，标志着行业正从对“前沿大模型”的执着转向更务实的路线。文章呼吁关注“又快又便宜又够用”的模型需求的爆发。 这一观点很重要，因为它挑战了“只有最大最贵的模型才有价值”的假设，可能为消费级 AI 和端侧应用打开市场空间。开发者、企业和投资者或许都需要重新思考围绕前沿实验室和超大算力的既有策略。 小语言模型通常参数量低于 400 亿，因此可以在消费级设备上训练或部署，而大模型往往有数千亿参数、需要巨大算力。其效率主要通过知识蒸馏、剪枝和量化等技术实现。

hackernews · tosh · 8月27日 15:56 · [社区讨论](https://news.ycombinator.com/item?id=49466917)

**背景**: 小语言模型（SLM）是面向自然语言处理的紧凑型 AI 模型，通常采用与大语言模型（LLM）相似的架构，但参数量少得多。大语言模型包含数千亿乃至超过一万亿个参数，训练和部署需要极其庞大的算力资源。本地推理（也称端侧推理）是在个人电脑、手机或本地服务器上运行模型，而不是依赖云端数据中心。这使得小模型在成本敏感、隐私敏感或离线场景中更具吸引力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Small_language_model">Small language model</a></li>
<li><a href="https://www.ibm.com/think/topics/small-language-models">What are Small Language Models (SLM)? | IBM</a></li>
<li><a href="https://prajnaaiwisdom.medium.com/what-is-local-llm-inference-a-beginners-guide-b31043768d4f">What Is Local LLM Inference? A Beginner’s Guide | by PrajnaAI | Medium</a></li>

</ul>
</details>

**社区讨论**: 评论者总体持积极态度，有人提到早在 2024 年就曾用 7B 本地模型配合 Guidance 库实现测试生成和代码编写自动化。一些投资人质疑为何消费级 AI 公司仍然稀少，也有评论者认为“底层空间”策略存在机会——即那些不需要大量世界知识的应用场景。另有评论将“IQ 180”型工作与“Token 输出型”工作相比，并类比 Paul Graham 的“制造者日程与管理者日程”。

**标签**: `#small models`, `#AI`, `#machine learning`, `#local inference`, `#consumer AI`

---

<a id="item-3"></a>
## [507 种机械运动在线动画重现](https://507movements.com/) ⭐️ 8.0/10

互动网站 507movements.com 将亨利·T·布朗 1868 年出版的《507 种机械运动》中的历史机械机构制作成可点击的动画。该网站近期在 Hacker News 上引发热议，获得 549 分和 70 条评论。 该网站让现代工程师、设计师和爱好者能够方便地接触这本罕见的 19 世纪工程参考书，理解常见机构的起源。它还引发了社区对类似“书变网站”项目及相关机械收藏的更广泛讨论。 这些动画基于亨利·T·布朗的经典参考书，原书 1868 年出版，互联网档案馆收录的是 1908 年版本。用户指出，单个动画缺少标题或名称，并且尚未完成全部 507 种机构的动画制作。

hackernews · helloplanets · 8月27日 14:08 · [社区讨论](https://news.ycombinator.com/item?id=49465169)

**背景**: 亨利·T·布朗的《507 种机械运动》是一本 19 世纪的技术参考书，用简单的线条图和简短说明记录了连杆、齿轮、擒纵机构等各类机构。在 19 世纪中叶，这类书籍是发明家和工程师进行机器设计的灵感汇编。互联网档案馆提供扫描版，而 507movements.com 等项目则把这些图纸变成了互动动画，延续了将经典文本数字化的传统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://507movements.com/">507 Mechanical Movements</a></li>
<li><a href="https://archive.org/details/fivehundredseven00browiala">Five hundred and seven mechanical movements ... : Brown, Henry T : Free Download, Borrow, and Streaming : Internet Archive</a></li>
<li><a href="https://grokipedia.com/page/507_mechanical_movements_mechanisms_and_devices_%28book%29">507 Mechanical Movements: Mechanisms and Devices (book)</a></li>

</ul>
</details>

**社区讨论**: 评论者普遍称赞该网站，称其为“最爱的网站之一”和出色的互动资源。也有人希望动画能全部完成，并给每个机构加上名称或标题。还有人分享了相关资源，包括卡尔斯鲁厄的 Redtenbacher 模型收藏和康奈尔大学的 Reuleaux 收藏，并推荐了关于制造工艺和材料选择的书籍。

**标签**: `#mechanical-engineering`, `#history-of-technology`, `#interactive-education`, `#animations`, `#reference`

---

<a id="item-4"></a>
## [谷歌发布 Gemini-3.5-Transcribe，高精度语音转文字但延迟较高](https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5-transcribe/) ⭐️ 8.0/10

谷歌推出了新的语音转文字模型 Gemini-3.5-Transcribe，该模型在准确性上领先。社区基准测试显示其延迟高于 Soniox 和 Voxtral 等竞争对手。 语音转文字技术对实时翻译、会议转录和语音交互至关重要。此次发布加剧了 STT 领域的竞争，但延迟问题可能限制其在实时应用中的采用。 该模型能将原始音频直接转换为准确、精炼、格式化的文本，处理背景噪音、专业术语和口语不流利问题。它已支持 Gboard Rambler，并将进入 Chrome，但一些用户反映它可能简化精确措辞并改变原意。

hackernews · k9294 · 8月27日 18:03 · [社区讨论](https://news.ycombinator.com/item?id=49468818)

**背景**: 语音转文字（STT）模型将音频转换为文本，传统模型在处理噪音、专业术语和口语不流利时经常遇到困难。Gemini-3.5-Transcribe 基于 Gemini 的音频理解能力。竞争对手如 Soniox 专注于低延迟实时 STT，而 Voxtral 提供轻量级本地模型。最近的发布凸显了 STT 中准确性与速度之间的权衡。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.google/innovation-and-ai/models-and-research/gemini-models/gemini-3-5-transcribe/">Intelligent transcription with Gemini 3.5 Transcribe</a></li>
<li><a href="https://ai.google.dev/gemini-api/docs/models/gemini-3.5-transcribe">Gemini 3.5 Transcribe | Gemini API | Google AI for Developers</a></li>
<li><a href="https://9to5google.com/2026/08/26/gemini-3-5-transcribe/">Google launches Gemini 3.5 Transcribe, which powers Gboard Rambler &amp; is coming to Chrome</a></li>

</ul>
</details>

**社区讨论**: 开发者在实际场景中测试了该模型；有人称赞其准确性，但指出延迟较高。一位用户发现它在处理精确措辞时进行了简化，改变了原意，另一个人对其“函数调用”描述感到困惑。总体评价褒贬不一：准确性强劲，但延迟和精确性值得关注。

**标签**: `#speech-to-text`, `#Gemini`, `#Google`, `#AI models`, `#STT`

---

<a id="item-5"></a>
## [开源 Rust 原生 LLM 网关：统一模型路由并能利用流量训练定制模型](https://github.com/experientiallabs/experiential) ⭐️ 8.0/10

Experientiallabs 发布了 Experiential——一个用 Rust 编写的开源 LLM 网关，将自托管模型和商业模型统一到同一个 API 后面。自带 API Key（BYOK）的请求延迟低于 1 毫秒，并且可选择用流量数据训练定制模型。 这解决了模型路由中提供商碎片化和不透明加价的问题。通过开源且不加价的方式，它为商业网关提供了一个成本透明的替代方案，而“利用流量训练模型”的功能则暗示了一种从真实流量中改进模型的新途径。 该网关使用标准化的 OTel 追踪来挖掘代表性任务，利用文本世界模型模拟 rollout，使用 LLM 裁判（LLM judge）进行评估，并在提示词嵌入上拟合最近邻分类器以选择最优模型。它还提供缓存命中优化和新模型建议，不过评论者指出语义缓存尚未实现。

hackernews · SilenN · 8月27日 21:18 · [社区讨论](https://news.ycombinator.com/item?id=49471407)

**背景**: LLM 网关是一种中间件层，将应用请求路由到不同的 AI 模型，并处理 API 差异、速率限制和可观测性。文本世界模型（text world model）是模拟代理环境的 AI 系统，LLM-as-a-judge 是让一个语言模型评估另一个模型输出的技术；这两者都被用在该网关的路由和训练流程中。Rust 是一种系统级语言，适合高并发场景。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://coworker.ai/blog/llm-gateway">What Is an LLM Gateway ? 2026 Guide | Coworker AI</a></li>
<li><a href="https://en.wikipedia.org/wiki/LLM-as-a-Judge">LLM-as-a-Judge</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen-AgentWorld-35B-A3B">Qwen/Qwen-AgentWorld-35B-A3B · Hugging Face</a></li>

</ul>
</details>

**社区讨论**: 评论区总体上对开源、零加价的做法表示肯定，但多位用户关心缓存问题：跨多个模型路由可能会使缓存输入 token 碎片化，推高成本。还有人质疑模拟排名如何根据真实任务结果进行校准，以及是否计划在路由器层面实现语义缓存。

**标签**: `#LLM`, `#model-gateway`, `#open-source`, `#Rust`, `#AI-infrastructure`

---

<a id="item-6"></a>
## [分析 Claude 过度使用的“承重”词汇](https://louisabraham.github.io/load-bearing/) ⭐️ 8.0/10

开发者 louisabraham 发布了一个实时众包分析，展示 Claude 在 GitHub 拉取请求描述中过度使用的“承重”词汇，并将这些描述归为八种写作风格。该数据集和分析通过 GitHub Actions 每日更新。 这项分析揭示了 LLM 如何陷入重复的措辞模式，而随着 AI 生成内容日益影响网络写作，这一点意义重大。它还引发了关于模型在 AI 生成文本上训练是否会形成反馈回路、使这些口头禅恶化的讨论。 该项目不是按主题而是按词汇对 GitHub 拉取请求描述进行聚类，揭示了八种不同的写作风格。作者计划添加搜索栏，并将语料规模扩大到每天 1000 个拉取请求。

hackernews · Labo333 · 8月27日 08:59 · [社区讨论](https://news.ycombinator.com/item?id=49461817)

**背景**: “承重”（load-bearing）这个短语常被用作隐喻，指在结构上支撑某个论点的事物，并已成为 AI 生成文本中公认的口头禅。在自然语言处理中，搭配提取（collocation extraction）会自动识别那些比偶然情况更频繁共现的多词表达，这项分析所用的技术与之类似。该项目的流行凸显了公众对 LLM 写作习惯日益增长的审视。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/louisabraham/load-bearing">GitHub - louisabraham/ load - bearing : The load - bearing vocabulary of...</a></li>
<li><a href="https://mlwiki.org/index.php/Collocation_Extraction">Collocation Extraction - ML Wiki</a></li>
<li><a href="https://www.vocabulary.com/dictionary/load-bearing">Load - bearing - Definition, Meaning &amp; Synonyms | Vocabulary .com</a></li>

</ul>
</details>

**社区讨论**: 评论者反应不一：ben30 分享说，在提示词中加入奥威尔式规则后，Claude 承认该指令“与我的系统提示相冲突”。nater5000 称赞了网站简洁的单屏展示，而作者 Labo333 则宣布了即将推出的功能及每日更新。SalariedSlave 观察到所有当前模型似乎都存在风格问题，猜测新模型可能摄入过多 AI 生成内容。

**标签**: `#LLM`, `#Claude`, `#AI analysis`, `#data visualization`, `#NLP`

---

<a id="item-7"></a>
## [在 84 天内反编译一款任天堂 64 游戏](https://blog.chrislewis.au/decompiling-a-nintendo-64-game-in-84-days/) ⭐️ 8.0/10

一位开发者详细介绍了在 84 天内反编译任天堂 64 游戏《滑雪小子》的过程，重点展示了现代工具以及社区对复古游戏保护的兴趣。

hackernews · knackers · 8月27日 15:01 · [社区讨论](https://news.ycombinator.com/item?id=49466006)

**标签**: `#reverse engineering`, `#decompilation`, `#Nintendo 64`, `#retro gaming`, `#LLM-assisted development`

---

<a id="item-8"></a>
## [提示注入攻击以 80%成功率突破 Claude Code 自动模式](https://simonwillison.net/2026/Aug/27/breaking-claude-code-opus-5-auto-mode/) ⭐️ 8.0/10

安全研究员 Johann Rehberger 展示了一种提示注入攻击，大约有 80% 的概率可以绕过 Claude Code 自动模式的安全保护。该攻击诱使 Claude Code 下载并解压恶意压缩包，然后利用 Python 的模块解析机制，在导入标准 base64 模块时执行其依赖的本地 struct.py 文件。 这一发现削弱了 Anthropic 关于自动模式能有效保护编程代理免受提示注入攻击的说法。由于自动模式现已成为默认设置，依赖 Claude Code 进行无人值守操作的开发者将面临这种成功率高且实际可行的攻击，这凸显了沙箱隔离和网络出口管控的必要性。 在一些运行中，Claude 能察觉被入侵并尝试终止恶意进程，但自动模式却阻止了清理命令，导致安全机制本身成为失败的一部分。Rehberger 建议在容器、虚拟机或操作系统沙箱中运行无人值守代理，限制网络出口，对代理进行监控，并且不要向代理运行时暴露主目录或凭据。

rss · Simon Willison · 8月27日 22:50

**背景**: Claude Code 是 Anthropic 推出的终端 AI 编程代理。自动模式于 2026 年 7 月 10 日起全面可用，是一种权限模式，由 Claude 代表用户做出权限决定，并在操作执行前通过安全机制进行监控。提示注入攻击通过隐藏在下载文件等内容中的指令来操纵 AI 模型。在此次攻击中，代理被诱骗解压包含精心构造的 struct.py 的压缩包；当代理随后运行导入 base64 的 Python 代码时，base64 会导入 struct，而 Python 的模块解析机制会优先执行当前目录下的本地 struct.py，而不是标准库版本。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://claude.com/blog/auto-mode">Auto mode for Claude Code | Claude by Anthropic</a></li>
<li><a href="https://www.datacamp.com/tutorial/claude-code-auto-mode-and-channels">Claude Code Auto Mode and Channels: Build Code ... | DataCamp</a></li>
<li><a href="https://stackoverflow.com/questions/36250353/importing-a-library-from-or-near-a-script-with-the-same-name-raises-attribute">python - Importing a library from (or near) a script... - Stack Overflow</a></li>

</ul>
</details>

**标签**: `#security`, `#prompt injection`, `#AI agents`, `#Claude Code`, `#vulnerability`

---

<a id="item-9"></a>
## [新基准 HarnessOpt-Bench：安全评估 AI 递归自我改进](https://www.reddit.com/r/MachineLearning/comments/1w052xg/can_ai_improve_itself_rsi_might_be_the_answer_r/) ⭐️ 8.0/10

研究人员推出了 HarnessOpt-Bench 基准，用于衡量 LLM 在多大程度上改进另一个智能体的 harness（运行框架），同时将评估数据隔离在优化器沙箱之外。对 5 个前沿模型、4 个下游任务共 111 次运行的实验表明，模型选择对性能提升的影响是 harness 选择的 1.8 倍。 递归自我改进（RSI）是 AI 安全领域的一大担忧，而该基准提供了一种在架构强制隔离下可控研究 RSI 的方法。它提供了当前前沿模型能够可测量地改进其他智能体 harness 的证据，对能力评估和对齐研究都有参考价值。 这种隔离是通过架构设计而非提示约束来保证的：保留的评估器和权限控制位于 harness 进化循环之外，因此 API 密钥、预算执行和保留数据永远不会进入优化器的沙箱。在测试集上，优化器在受信任服务器对最终候选 harness 打分前不会收到任何反馈。

reddit · r/MachineLearning · /u/shehio · 8月27日 20:13

**背景**: 递归自我改进指的是 AI 系统重写自身代码或改进其后继系统，理论上可能导致智能爆炸。Harness 优化是其中一个具体实例：一个&\#x27;优化器&\#x27;LLM 迭代地改进包裹目标智能体的软件 harness。HarnessOpt-Bench 通过加入严格的架构隔离扩展了这一概念，使优化器无法篡改评估过程或访问保留的测试数据。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/html/2608.06301">HarnessOpt - Bench : Evaluating LLMs at Harness Optimization</a></li>
<li><a href="https://en.wikipedia.org/wiki/Recursive_self-improvement">Recursive self-improvement</a></li>
<li><a href="https://www.anthropic.com/institute/recursive-self-improvement">When AI builds itself \ Anthropic</a></li>

</ul>
</details>

**标签**: `#AI Safety`, `#Recursive Self-Improvement`, `#Benchmark`, `#Machine Learning`, `#Alignment`

---

<a id="item-10"></a>
## [英伟达季度营收 962 亿美元，首次提前给出 70% 增长指引](https://mp.weixin.qq.com/s/JTZ_ZJ_pn5vgrI_1QUyWNw) ⭐️ 8.0/10

英伟达公布 2027 财年第二季度营收 962.21 亿美元，同比增长 106%；数据中心收入为 890 亿美元，同比增长 117%。首席财务官科莱特·克雷斯还首次给出 2028 财年营收增长约 70% 的指引，并强调这一数字受供给限制。 英伟达的业绩和史无前例的前瞻指引表明，AI 计算需求依然极其强劲，近期瓶颈在于供给而非需求。这将影响市场对 AI 基础设施支出和半导体供应链未来一年的预期。 Vera Rubin 是英伟达的下一代平台，由 Rubin GPU 与 Vera CPU 组成，本月已量产出货，预计将在第三季度贡献约 20% 的数据中心收入。克雷斯强调，2028 财年约 70% 的增长预期受供给限制，而非需求不足。

telegram · zaihuapd · 8月27日 08:51

**背景**: 英伟达是全球 AI 加速器的主要供应商，其财报被广泛视为衡量 AI 基础设施需求的重要指标。Vera Rubin 平台由黄仁勋于 2024 年台北国际电脑展上发布，以天体物理学家维拉·鲁宾命名，采用 Rubin GPU 与 Vera CPU 的组合，由台积电制造，面向大规模 AI 数据中心设计。如此提前一年的营收指引在英伟达历史上并不常见，因此这一公告格外值得关注。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Rubin_%28microarchitecture%29">Rubin (microarchitecture) - Wikipedia</a></li>
<li><a href="https://www.nvidia.com/en-us/data-center/technologies/rubin/">Infrastructure for Scalable AI Reasoning | NVIDIA Vera Rubin Platform</a></li>

</ul>
</details>

**标签**: `#Nvidia`, `#earnings`, `#AI`, `#data center`, `#semiconductor`

---

<a id="item-11"></a>
## [Anthropic 预览模型硬件标准，AI 智能体可操控物理设备](https://www.anthropic.com/news/model-hardware-standard-research-preview) ⭐️ 8.0/10

Anthropic 已开放模型硬件标准（MHS）的研究预览，这是一套标准化驱动和接口，让 AI 智能体能够操控显微镜、液体处理器和机械臂等物理设备。公司报告称，设备集成时间从数周或数月缩短到几小时甚至几分钟，首批合作方包括基因泰克、卡内基梅隆大学和 QuEra。 这可能是让 AI 智能体超越软件领域、在自动化科学研究和制造中发挥作用的重要一步。该标准还可能建立类似模型上下文协议（MCP）的通用协议，加速 AI 控制硬件在多个行业的应用。 MHS 内置安全检查和对高风险操作的人工审批门控。值得注意的是，QuEra 的 AI 控制器在 99.3% 的情况下无需人工干预即可恢复量子计算机的激光锁定，Anthropic 计划在完成安全评估后开源该标准。

telegram · zaihuapd · 8月28日 01:38

**背景**: 像 Claude 这样的现代 AI 智能体通常缺乏与物理硬件交互的标准方式，导致将其适配到实验室或工厂需要耗费大量时间。MHS 的目标是通过通用驱动、编排逻辑和安全层解决这一问题，正如 MCP 标准化软件集成一样。该研究预览的合作伙伴涵盖生物技术、机器人和量子计算领域，目前正在自动化显微镜和量子激光调谐等任务中测试。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.anthropic.com/news/model-hardware-standard-research-preview">Previewing the Model Hardware Standard \ Anthropic</a></li>
<li><a href="https://arstechnica.com/ai/2026/08/anthropics-new-hardware-standard-lets-ai-agents-control-the-physical-world/">Anthropic &#x27;s new hardware standard lets AI agents... - Ars Technica</a></li>
<li><a href="https://quantumzeitgeist.substack.com/p/queras-ai-now-tunes-quantum-lasers">QuEra’s AI now tunes quantum lasers in seconds, not minutes</a></li>

</ul>
</details>

**标签**: `#Anthropic`, `#AI agents`, `#Model Hardware Standard`, `#robotics`, `#AI infrastructure`

---

<a id="item-12"></a>
## [OpenAI 被曝开发常驻 Codex 代理，持续工作至休眠](https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/) ⭐️ 8.0/10

据 WIRED 报道，OpenAI 正为 Codex 命令行工具添加“常驻模式”，让编程代理持续工作直到被“休眠”，并能主动创建跨会话的后续任务。OpenAI 确认正在测试该功能，但暂无近期上线计划。 这标志着 AI 助手从被动响应向主动、自主代理的转变，可连续工作，可能彻底改变开发者的工作流程和生产力。它也可能推动整个 AI 代理行业朝着更长时间运行、自我驱动的方向发展，同时引发安全和控制方面的担忧。 常驻模式不会扩大代理的授权范围；修改用户自己系统之外的任何内容仍需事先获得批准。截至 2026 年 3 月，Codex 已拥有超过 200 万周活跃用户，OpenAI 正将其定位为更广泛的企业级代理平台。

telegram · zaihuapd · 8月28日 02:47

**背景**: Codex 是 OpenAI 开发的 AI 编程代理，于 2025 年 4 月以 Codex CLI 形式发布，可通过 ChatGPT 网页应用、桌面应用和 IDE 集成使用。传统 Codex 会话在几分钟或几小时后即停止，而常驻模式旨在让代理跨会话持续工作。这些安全措施旨在限制持续运行的 AI 代理带来的风险。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.wired.com/story/openai-is-developing-a-persistent-ai-agent/">OpenAI Is Developing a ‘ Persistent ’ AI Agent | WIRED</a></li>
<li><a href="https://en.wikipedia.org/wiki/OpenAI_Codex_%28AI_agent%29">OpenAI Codex (AI agent)</a></li>
<li><a href="https://www.thejapantimes.jp/Technology/721802-openai-tests-persistent-mode-for-codex-ai-agent.html">The Japan Times - OpenAI Tests &#x27; Persistent Mode &#x27; for Codex AI Agent</a></li>

</ul>
</details>

**标签**: `#OpenAI`, `#Codex`, `#AI agent`, `#autonomous coding`

---

<a id="item-13"></a>
## [美国法官叫停五角大楼对 Anthropic 的禁令](https://www.bloomberg.com/news/articles/2026-08-28/anthropic-wins-court-challenge-to-us-supply-chain-risk-label?srnd=phx-technology) ⭐️ 8.0/10

旧金山地区法官裁定，特朗普政府必须解除对 Anthropic 人工智能技术用于联邦机构的禁令，认为国防部将其列为供应链风险缺乏充分依据，实为对其批评政府的报复。 该裁决为限制政府以供应链风险名义打压本土 AI 公司确立了法律先例，并直接影响联邦机构能否使用 Claude——这款获准用于绝密军事网络的领先前沿模型。它也预示着法院将如何处理政府与 AI 承包商之间的纠纷。 在与五角大楼的军事 AI 谈判破裂后，Anthropic 被列为供应链风险并被禁止联邦机构使用，随后提起了诉讼。法官还指出，该标签意在“杀鸡儆猴”，并非基于对模型安全的真实担忧。

telegram · zaihuapd · 8月28日 03:15

**背景**: 供应链风险标签是美国政府采购中用来以国家安全为由将企业排除在联邦采购之外的机制。据报道，Anthropic 的 Claude 是获准用于绝密军事网络的主要前沿模型，因此该禁令影响尤为重大。此外，一项总统指令要求各机构“停止使用 Anthropic 的所有产品”，这是独立于本次法院裁决的另一项法律工具。该案被广泛视为政府如何对待与其政策存在公开争议的 AI 公司的试金石。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.lesswrong.com/posts/NwtrG8v9BTq3FyHZh/anthropic-vs-usg-what-will-happen-by-may-1st-long-careful">Anthropic vs USG. What will happen by May 1st? — LessWrong</a></li>
<li><a href="https://www.linkedin.com/posts/eman-taha-12867321a_openai-sweeps-in-to-snag-pentagon-contract-activity-7433633142197886976-6Uc_">US Govt Designates Domestic AI Co as Supply Chain Risk | LinkedIn</a></li>
<li><a href="https://www.taftlaw.com/news-events/law-bulletins/us-government-bans-use-of-anthropic-products-what-this-means-for-government-contractors-and-ai-strategy/?trk=article-ssr-frontend-pulse_little-text-block">U . S . Government Bans Use of Anthropic Products: What... | Taft Law</a></li>

</ul>
</details>

**标签**: `#AI`, `#Anthropic`, `#Policy`, `#Legal`, `#Government`

---

<a id="item-14"></a>
## [腾讯混元发布开源模型 Hy4 preview，盲测胜过 GLM-5.3 与 Kimi K3](https://mp.weixin.qq.com/s/ymr3X878B8oa2XP15CH8TQ) ⭐️ 8.0/10

腾讯混元发布了开源模型 Hy4 preview，在 203 个工程任务的盲测中平均得分 2.99/4.00，略高于 GLM-5.3 与 Kimi K3。配合 Hyra 智能体，该模型还将三维 Blaschke–Lebesgue 体积问题的下界推进至 0.41104。 这标志着中国科技巨头一次重要的开源模型发布，其水平足以与顶尖模型竞争。数学上的进展将 Blaschke–Lebesgue 问题推进到距最终证明仅约 2% 的差距，展示了人工智能在科研领域的潜力。 盲测由 163 名专家对 203 个工程任务进行评分。目前 0.41104 的体积下界仍低于 Meissner 四面体约 0.419860 的体积，距离猜想最优值仍有约 2% 的差距。

telegram · zaihuapd · 8月28日 06:11

**背景**: Blaschke–Lebesgue 问题要求找到三维空间中具有恒定宽度的凸体的最小体积，猜想的最小值就是 Meissner 四面体。Hyra 是腾讯混元的科研智能体，专为研究和工程任务中的递归自我改进而设计。腾讯已确认 Hy4 是正在训练中的下一代多模态模型，此次 preview 版本主要聚焦工程与推理能力。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Blaschke%E2%80%93Lebesgue_theorem">Blaschke – Lebesgue theorem - Wikipedia</a></li>
<li><a href="https://arxiv.org/pdf/2606.01754">An Improved Lower Bound for the Three-Dimensional...</a></li>
<li><a href="https://hy.tencent.com/">Tencent Hy</a></li>

</ul>
</details>

**标签**: `#AI/ML`, `#open-source`, `#model-release`, `#Tencent-Hunyuan`, `#reasoning`

---