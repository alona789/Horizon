---
layout: default
title: "Horizon Summary: 2026-10-05 (ZH)"
date: 2026-10-05
lang: zh
---

> 从 22 条内容中筛选出 2 条重要资讯。

---

1. [Strata 宣称单张 RTX 4090 可跑 125B 的 Qwen3.8-Flash-Next，速度约 124 token/秒](#item-1) ⭐️ 8.0/10
2. [ARC-AGI-3 Kaggle 榜单分数据报 30 天内从 7% 飙升至 56%](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Strata 宣称单张 RTX 4090 可跑 125B 的 Qwen3.8-Flash-Next，速度约 124 token/秒](https://github.com/Niko1221/Strata) ⭐️ 8.0/10

一个名为 Strata（GitHub 仓库 Niko1221/Strata）的项目发布了新的推理引擎，声称可以在消费级硬件上运行 125B 参数的 Qwen3.8-Flash-Next，包括在单张 RTX 4090 上达到约 100 至 124 token/秒。该项目提供 Windows 与 Linux 一键安装包，在本地主机上暴露兼容 OpenAI/Anthropic 的 API，并可选支持图像输入。 如果这些数字成立，就意味着一个通常需要数据中心级 GPU 的 125B 级混合专家模型，可以在单张消费级显卡上本地服务，这对注重隐私和离线使用的 LLM 场景是实质性进展。同时，它也加剧了本地推理栈（llama.cpp、ds4、Strata）之间的竞争——焦点在于为了速度和显存节省究竟要牺牲多少模型质量。 这一核心宣称存在争议：有评论者对同一份 GGUF 权重和视觉适配器在两种引擎上做了基准测试，结果显示 Strata 下坐标中位误差为 154.8 像素，而 llama.cpp 下仅为 46.5 像素；与此同时，支持者报告在租用的 RTX Pro 6000／RTX 6000 Pro 上运行 4-bit 量化效果良好（prefill 约 1,251 token/秒，decode 最高约 255 token/秒）。另一些人则提醒，量化降到 4-bit 以下往往会明显损害质量，因此这些极端速度可能伴随着真实的精度代价。

hackernews · snehesht · 10月4日 12:51 · [社区讨论](https://news.ycombinator.com/item?id=49953495)

**背景**: Qwen3.8-Flash-Next 是一个规模极大的混合专家（MoE）模型：它并不是为每个 token 激活全部权重，而是把每个 token 路由到一小部分专家上（相关解说视频提到专家数量达 24,576 个），这正是它有可能在有限硬件上运行的原因。像 llama.cpp 这样的本地推理引擎依赖量化——把权重从 16 位压到 4 位甚至更低——以把模型显存占用缩小到消费级显卡能够承载的程度，代价是损失一定的数值精度。Strata 是同领域较新的推理引擎；当不同引擎在完全相同权重上跑出差异很大的基准结果时，通常反映的是算子内核、KV 缓存处理方式以及视觉适配器执行实现的差别。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://github.com/Niko1221/Strata/releases">Releases · Niko1221/ Strata · GitHub</a></li>
<li><a href="https://huggingface.co/Qwen/Qwen3.8-Flash-Next">Qwen / Qwen 3 . 8 - Flash - Next · Hugging Face</a></li>
<li><a href="https://www.youtube.com/watch?v=hJ_Iw2E7cnc">Strata GitHub Explained: How a 125B Qwen3.8-Flash-Next... - YouTube</a></li>

</ul>
</details>

**社区讨论**: 讨论情绪在热情与怀疑之间分化。一位评论者在 RTX 4090、128GB DDR5 和 Ryzen 7950x3d 的机器上复现了约 124 token/秒的结果；另一位则称赞该模型的 4-bit 量化在 RTX 6000 Pro 上表现优异，可支持四路并发流、速度 400+ token/秒；还有一位提醒量化低于 4-bit 可能带来明显的质量退化。最尖锐的反驳来自视觉基准测试：在完全相同的权重下，Strata 的坐标误差约为 llama.cpp 的三倍；此外也有人抱怨该项目在各大 LLM 社区被大量刷屏推广，热度尚待验证。

**标签**: `#local-llm-inference`, `#quantization`, `#consumer-gpu`, `#llm-serving`, `#model-compression`

---

<a id="item-2"></a>
## [ARC-AGI-3 Kaggle 榜单分数据报 30 天内从 7% 飙升至 56%](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/) ⭐️ 8.0/10

r/MachineLearning 上的一篇 Reddit 帖子称，ARC-AGI-3 的 Kaggle 排行榜最高分在过去 30 天内从约 7% 上升到 56%，不过发帖人自己也说明所附的排行榜截图略有滞后。发帖者还声称，在某个评测 harness（评测框架）中运行的小型本地模型已经开始在平均人类水平之上超过该基准。 ARC-AGI 的设计初衷就是「人类容易、AI 困难」，因此其排行榜分数若快速攀升，将动摇「基于抽象推理的能力仍是人类持久优势」这一假设。如果这个数字站得住脚，就说明仅靠评测框架工程加上小型本地模型（而不必依赖前沿规模的大模型），也可能在原本被认为难以企及的任务上取得快速进展。 这一说法仅来自一篇技术细节有限的 Reddit 帖子，且发帖人自己承认排行榜截图已过时，因此 56% 这个数字尚未得到验证。一个关键限制是 Kaggle 参赛者只能使用相对较小的本地模型，这意味着报告的提升很可能来自评测框架的设计与搜索或脚手架策略，而非模型本身的规模。

reddit · r/MachineLearning · /u/we\_are\_mammals · 10月4日 10:24 · [社区讨论](https://www.reddit.com/r/MachineLearning/comments/1wxcd4k/top_arc%CE%B1gi3_scores_on_kaggle_just_went_from_7_to/)

**背景**: ARC-AGI（通用人工智能抽象与推理语料库）是 ARC Prize Foundation 围绕「人类容易、AI 困难」这一原则构建的基准，刻意去除了规模优势与任务特定线索，迫使系统只能从少量示例中推断抽象规则。其最新版本 ARC-AGI-3 被该基金会称为衡量「智能体智能」的基准，至今仍未被攻克。评测 harness（评测框架）是定义评测内容、执行打分并输出结果的标准基础设施——在此类竞赛中，大量创新往往发生在 harness 层面而非模型权重本身；而「小型本地模型」指的是在本地硬件上运行的紧凑型语言模型，而非通过大型云端 API 调用的模型。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arcprize.org/arc-agi">ARC Prize - The only AI benchmark that measures AGI progress.</a></li>
<li><a href="https://arcprize.org/">ARC Prize Foundation is a nonprofit advancing open-source AGI ...</a></li>
<li><a href="https://arize.com/blog/what-is-an-evaluation-harness/">What is an evaluation harness ? Definition &amp; guide - Arize AI</a></li>

</ul>
</details>

**标签**: `#ARC-AGI`, `#Kaggle`, `#AI benchmarks`, `#reasoning`, `#LLM evaluation`

---