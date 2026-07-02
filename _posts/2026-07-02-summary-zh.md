---
layout: default
title: "Horizon Summary: 2026-07-02 (ZH)"
date: 2026-07-02
lang: zh
---

> 从 38 条内容中筛选出 10 条重要资讯。

---

1. [Linux 6.9 漏洞：LUKS 挂起未能清除内存中的加密密钥](#item-1) ⭐️ 8.0/10
2. [Podman v6.0.0 发布，带来重大改进](#item-2) ⭐️ 8.0/10
3. [F-Droid 称安卓开发者验证是恶意软件威胁](#item-3) ⭐️ 8.0/10
4. [日本最高法院：AI 不能列为专利发明人](#item-4) ⭐️ 8.0/10
5. [ECTC 2026 亮点：EMIB-T、定制 HBM 与散热](#item-5) ⭐️ 8.0/10
6. [从微分几何视角看哈密顿神经网络](#item-6) ⭐️ 8.0/10
7. [Cloudflare 9 月起默认拦截混合用途 AI 爬虫](#item-7) ⭐️ 8.0/10
8. [OpenAI 提议美国政府持股 5%，可能纳入其他 AI 巨头](#item-8) ⭐️ 8.0/10
9. [花旗禁用 GPT-5.5，多家公司因 AI 成本飙升限制员工使用](#item-9) ⭐️ 8.0/10
10. [Anthropic 洽谈三星代工自研 AI 芯片](#item-10) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Linux 6.9 漏洞：LUKS 挂起未能清除内存中的加密密钥](https://mathstodon.xyz/@iblech/116769502749142438) ⭐️ 8.0/10

Linux 内核 6.9 中的一个漏洞导致在执行 `cryptsetup luksSuspend` 命令时，无法在系统挂起期间从内核内存中清除磁盘加密主密钥，使密钥暴露。 这一安全退化削弱了睡眠期间的磁盘加密保护，使加密数据容易受到冷启动攻击或内存取证。 该漏洞具体影响 `cryptsetup luksSuspend` 操作，这是 Debian 特有的扩展，并非 LUKS 标准的正式组成部分；但所有使用该功能的系统都会受到影响。

hackernews · IngoBlechschmid · 7月2日 15:25 · [社区讨论](https://news.ycombinator.com/item?id=48763035)

**背景**: LUKS（Linux 统一密钥设置）是一种磁盘加密规范，它将主密钥存储在内核内存中以进行实时加密和解密。当系统挂起到 RAM 时，这些密钥通常保留在内存中，但 `luksSuspend` 命令旨在睡眠前清除它们以增强安全性。内核 6.9 的更改意外禁用了这一清除机制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Linux_Unified_Key_Setup">Linux Unified Key Setup - Wikipedia</a></li>
<li><a href="https://www.howtogeek.com/what-is-luks-and-how-does-it-secure-your-linux-file-system/">What is LUKS , and How Does It Secure Your Linux File System?</a></li>
<li><a href="https://www.golinuxcloud.com/how-to-encrypt-hard-disk-partition-luks-linux/">How to Encrypt New Hard Disk (Partition) using LUKS in Linux</a></li>

</ul>
</details>

**社区讨论**: 社区评论指出，该漏洞容易被忽略，因为安全问题通常无声无息。有人认为普通睡眠（不使用 `luksSuspend`）已经使密钥留在内存中，因此额外的保护有限。其他人则强调自动化测试（如 NixOS 测试）对于捕获此类回归的价值。

**标签**: `#Linux kernel`, `#LUKS`, `#disk encryption`, `#security regression`, `#key management`

---

<a id="item-2"></a>
## [Podman v6.0.0 发布，带来重大改进](https://blog.podman.io/2026/07/introducing-podman-v6-0-0/) ⭐️ 8.0/10

Podman 6.0.0 已发布，引入了新的网络改进和增强的 Quadlet 支持，使容器管理更加简单。 此版本巩固了 Podman 作为领先的 Docker 替代品的地位，提供无守护进程、无根执行和与 docker-compose 的无缝兼容，有利于 DevOps 工作流程和容器采用。 值得注意的技术细节包括重新设计的网络栈和改进的 Quadlet 与 systemd 集成，以及社区讨论中强调的性能优化和错误修复。

hackernews · soheilpro · 7月2日 14:23 · [社区讨论](https://news.ycombinator.com/item?id=48762098)

**背景**: Podman 是 Red Hat 开发的开源、无守护进程的容器引擎，符合 OCI 标准。与 Docker 不同，它无需中央守护进程即可运行容器，并支持无根操作以提高安全性。其命令行界面设计为与 Docker 兼容，方便用户迁移。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Podman">Podman - Wikipedia</a></li>
<li><a href="https://www.redhat.com/en/topics/containers/what-is-podman">What is Podman?</a></li>
<li><a href="https://docs.podman.io/">What is Podman? — Podman documentation</a></li>

</ul>
</details>

**社区讨论**: 社区反馈极为积极，用户称赞从 Docker 迁移的便捷性、新的网络功能和 Quadlet。一位用户提到内存效率和无守护进程设计，另一位则对博客文本对比度低提出意见。总体而言，此版本受到热烈欢迎。

**标签**: `#podman`, `#containers`, `#docker alternative`, `#devops`, `#version release`

---

<a id="item-3"></a>
## [F-Droid 称安卓开发者验证是恶意软件威胁](https://f-droid.org/2026/07/01/adv-malware.html) ⭐️ 8.0/10

F-Droid 发布了一篇博文，认为安卓的开发者验证是一种伪装成保护的威胁，并将其比作特洛伊木马等恶意软件。 这篇文章挑战了谷歌对安卓应用分发的控制，并引发了对用户自主性和安全性的担忧，可能影响关于开放移动生态系统的辩论。 该文章使用了强烈的措辞，指责谷歌的行为像“恶意软件供应商”，并将开发者验证与特洛伊木马行为相类比。它还提到了“保持安卓开放”运动。

hackernews · drewfax · 7月2日 03:00 · [社区讨论](https://news.ycombinator.com/item?id=48755965)

**背景**: F-Droid 是一个自由开源的安卓应用商店，只托管自由开源软件。安卓开发者验证要求开发者验证身份并提交应用供审核，F-Droid 认为这限制了用户自由并损害了开源生态系统。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/F-Droid">F-Droid</a></li>

</ul>
</details>

**社区讨论**: 社区评论褒贬不一：一些用户同意并主张切换到 GrapheneOS 或 SailfishOS 等替代系统，而另一些用户则批评文章的语气幼稚且适得其反，认为“保持安卓开放”网站是更好的资源。

**标签**: `#Android`, `#F-Droid`, `#mobile security`, `#open source`, `#Google`

---

<a id="item-4"></a>
## [日本最高法院：AI 不能列为专利发明人](https://japannews.yomiuri.co.jp/science-nature/technology/20260306-314930/) ⭐️ 8.0/10

日本最高法院裁定，人工智能不能作为专利申请中的发明人，维持了发明人必须是自然人的要求。 该裁决确立了明确的法律先例，即 AI 不具备法律人格，从而影响 AI 生成发明的专利申请，并加剧全球关于 AI 与知识产权的辩论。 该案涉及一项将 AI 系统列为专利发明人的申请。法院强调，根据现行专利法，只有人类才能被法律承认为发明人。

hackernews · mushstory · 7月2日 13:43 · [社区讨论](https://news.ycombinator.com/item?id=48761536)

**背景**: 世界各国的专利法通常要求发明人必须是自然人。随着 AI 系统能够独立生成发明，关于 AI 是否能被视为发明人的问题随之产生。该裁决与美国、英国和欧洲的类似决定一致，强化了专利体系以人为中心的性质。

**社区讨论**: 评论者表达了不同观点：有人质疑专利在促进创新方面的有效性，而有人则基于责任归属支持该裁决。还有人担忧发明人可能会将自己列为 AI 生成发明的发明人，从而绕过该裁决。

**标签**: `#AI`, `#patents`, `#law`, `#Japan`, `#intellectual property`

---

<a id="item-5"></a>
## [ECTC 2026 亮点：EMIB-T、定制 HBM 与散热](https://newsletter.semianalysis.com/p/ectc2026) ⭐️ 8.0/10

在 ECTC 2026 上，英特尔展示了其用于 HBM4 集成的 EMIB-T 封装技术，而内存制造商讨论了定制 HBM 和封装挑战。新型微流道冷却和光子互连也成为亮点。 这些进展对于扩展 AI 加速器至关重要，因为它们解决了电源传输、散热和内存带宽限制。封装和互连技术的进步将直接影响下一代 AI 硬件的性能和成本。 英特尔的 EMIB-T 支持 HBM4 及未来的 HBM5，可扩展到 120mm x 180mm 封装，包含超过 38 个桥接片。HBM4 的引脚速度超过 11 Gb/s，提供>2.8 TB/s 带宽。微流道冷却在硅片上直接蚀刻通道，散热效果提升三倍。

rss · Semianalysis · 7月2日 17:25

**背景**: EMIB（嵌入式多芯片互连桥接）是英特尔的一项技术，通过在基板中嵌入小型硅桥接片来连接多个裸片，实现高密度互连。EMIB-T 通过增加硅通孔（TSV）实现垂直供电，支持 AI 加速器等更高功率的芯片。HBM（高带宽存储器）将 DRAM 裸片垂直堆叠并采用宽接口，对于 GPU 和 AI 工作负载至关重要。微流道冷却将液冷通道直接集成到硅片中，实现高效散热，而光子互连则利用光代替电路迹线，以实现更高带宽和更低功耗。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/intels-emib-t-heads-for-fab-rollout-this-year">Intel's EMIB-T packaging technology set for fab rollout this year — as TSMC CoWoS capacity remains limited, EMIB-T is preparing for advanced AI accelerator designs | Tom's Hardware</a></li>
<li><a href="https://en.wikipedia.org/wiki/High_Bandwidth_Memory">High Bandwidth Memory - Wikipedia</a></li>
<li><a href="https://news.microsoft.com/source/features/innovation/microfluidics-liquid-cooling-ai-chips/">AI chips are getting hotter. A microfluidics breakthrough goes straight to the silicon to cool up to three times better. - Source</a></li>

</ul>
</details>

**标签**: `#semiconductor packaging`, `#HBM`, `#photonics`, `#chiplet`, `#cooling`

---

<a id="item-6"></a>
## [从微分几何视角看哈密顿神经网络](https://www.reddit.com/r/MachineLearning/comments/1ukzdnj/hamiltonian_neural_networks_from_a_differential/) ⭐️ 8.0/10

一篇博客文章从微分几何角度介绍哈密顿神经网络（HNN），强调诺特定理以及对称性与守恒定律之间的关系。 这一视角提供了对 HNN 工作原理的更深入理解，将物理原理与机器学习泛化联系起来，可能启发更鲁棒的物理信息模型。 作者加入了交互式可视化，并强调了诺特定理，即每个连续对称性对应一个守恒定律，这一概念在物理信息机器学习中常被忽略。

reddit · r/MachineLearning · /u/FlameOfIgnis · 7月1日 21:55

**背景**: 哈密顿神经网络是一类学习哈密顿动力学的神经网络，能够守恒能量并尊重物理不变量。其灵感来源于哈密顿力学，该力学用位置和动量描述系统。诺特定理将对称性与守恒量联系起来，为机器学习中的泛化提供了理论基础。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://arxiv.org/abs/1906.01563">[1906.01563] Hamiltonian Neural Networks</a></li>
<li><a href="https://greydanus.github.io/2019/05/15/hamiltonian-nns/">Hamiltonian Neural Networks</a></li>

</ul>
</details>

**标签**: `#Hamiltonian Neural Networks`, `#Differential Geometry`, `#Physics-Informed ML`, `#Noether's Theorem`, `#Machine Learning`

---

<a id="item-7"></a>
## [Cloudflare 9 月起默认拦截混合用途 AI 爬虫](https://techcrunch.com/2026/07/01/cloudflares-new-policy-pushes-ai-companies-to-pay-for-publishers-content/) ⭐️ 8.0/10

从 9 月 15 日起，Cloudflare 将默认拦截同时用于搜索索引、AI 问答和训练的混合用途爬虫（包括 Google 的），实际上迫使 AI 公司为使用发布商内容付费。 这项政策转变解决了一个长期漏洞：发布商阻止 AI 爬虫但允许 Googlebot，使 Google 能无偿将抓取内容用于 AI。它可能为网络爬虫生态和 AI 训练的数据补偿模式树立先例。 Cloudflare 特别点名 Google 利用此漏洞——当使用同一用户代理(Googlebot)时，服务器难以区分搜索索引和 AI 训练。该政策仅适用于带广告的页面，并且 Cloudflare 计划未来按实际使用量而非仅抓取量收费。

telegram · zaihuapd · 7月2日 05:37

**背景**: 网络爬虫是系统浏览网站的机器人，通常用于搜索引擎索引。混合用途爬虫指同时执行搜索、AI 问答和模型训练等多项功能的爬虫。发布商长期以来难以在不阻止搜索引擎机器人的情况下阻止 AI 爬虫，Cloudflare 此举提供了技术解决方案。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Web_crawler">Web crawler - Wikipedia</a></li>
<li><a href="https://www.cloudflare.com/learning/bots/what-is-a-web-crawler/">What Is a Web Crawler ? | How Web Spiders Work</a></li>

</ul>
</details>

**标签**: `#Cloudflare`, `#AI Crawlers`, `#Google`, `#Web Scraping`, `#Content Policy`

---

<a id="item-8"></a>
## [OpenAI 提议美国政府持股 5%，可能纳入其他 AI 巨头](https://www.bloomberg.com/news/articles/2026-07-02/openai-proposes-giving-the-us-government-a-5-stake-ft-says) ⭐️ 8.0/10

据彭博社报道，OpenAI 提议让美国政府持有公司 5%的股份，并考虑设立一个统一载体，将 Google、Meta 等其他主要 AI 公司的各 5%股份也纳入其中。 该提案可能重塑 AI 治理，将公共利益与公司利润挂钩，为政府参与科技公司建立先例，并影响 AI 驱动经济收益的分配方式。 据报道，该计划正由 OpenAI CEO Sam Altman 及其他高管内部讨论，但 Google、Meta 等公司是否接受尚不明确，该安排可能引发监管控制和利益冲突方面的担忧。

telegram · zaihuapd · 7月2日 06:02

**背景**: OpenAI 是领先的 AI 研究机构，开发了 GPT 模型和 ChatGPT。该提案出台之际，关于 AI 收益应如何分配的争论日益激烈，有人主张公有制或再分配机制。美国政府持有私营公司股份在美国科技领域罕见，但在战略行业中存在。

**标签**: `#OpenAI`, `#AI政策`, `#美国政府`, `#公司治理`, `#AI产业`

---

<a id="item-9"></a>
## [花旗禁用 GPT-5.5，多家公司因 AI 成本飙升限制员工使用](https://www.404media.co/companies-are-throttling-employees-ai-use-because-its-too-expensive/) ⭐️ 8.0/10

花旗银行于 2026 年 6 月 24 日完全禁用 GPT-5.5、Claude Opus 4.6 和 4.7 等最新模型，理由是这些模型消耗过多 AI 积分。Atlassian 的 AI 月支出飙升至超过 1500 万美元，Adobe 也决定不再续签无限使用 Claude 的合同。 这一趋势凸显了企业在采用前沿 AI 模型时面临的真实成本挑战，可能减缓内部 AI 应用的推广，迫使企业制定更严格的使用政策或寻求更具成本效益的替代方案。 Atlassian 的内部仪表板显示，其 AI 支出从 2025 年 8 月的 500 万美元增至 2026 年 5 月的 1500 万美元以上，公司因此终止了无限使用政策并推出了成本追踪面板。亚马逊此前关闭了鼓励 AI 使用的内部排行榜，员工随后发现了此前未知的 token 使用上限。

telegram · zaihuapd · 7月2日 13:59

**背景**: 企业级 AI 工具如 GPT-5.5 和 Claude Opus 采用基于 token 的定价模式，每次查询消耗一定数量的 token。公司通常为员工提供一定数量的 AI 积分，但昂贵的前沿模型会迅速消耗这些积分，导致意外超支。GPT-5.5 是 OpenAI 于 2026 年 4 月发布的前沿模型，以强大的推理能力著称，但每个 token 的成本也更高。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/GPT-5.5">GPT-5.5</a></li>
<li><a href="https://openrouter.ai/openai/gpt-5.5">GPT - 5 . 5 - API Pricing & Benchmarks | OpenRouter</a></li>
<li><a href="https://www.afternoon.co/blog/token-based-pricing-guide">Token-Based Pricing: How to Account for AI Credits and LLM Usage | Afternoon Blog</a></li>

</ul>
</details>

**标签**: `#AI`, `#enterprise`, `#cost`, `#productivity`, `#news`

---

<a id="item-10"></a>
## [Anthropic 洽谈三星代工自研 AI 芯片](https://www.theinformation.com/articles/anthropic-talks-samsung-manufacture-custom-ai-chip) ⭐️ 8.0/10

Anthropic 已开始开发自研 AI 芯片，并与三星电子就潜在制造合作进行早期洽谈。此举旨在加强对 Claude 模型计算基础设施的控制。 这标志着领先 AI 公司向 AI 硬件垂直整合的趋势，类似 OpenAI 等公司的举措。此举可能减少对第三方芯片供应商的依赖，并针对 Anthropic 特定工作负载优化性能。 该项目仍处于非常早期阶段，相比已推进自研服务器芯片的其他公司，Anthropic 入场时间较晚。三星代工提供先进工艺技术，包括 3nm GAA（全环绕栅极）晶体管。

telegram · zaihuapd · 7月2日 15:57

**背景**: 定制 AI 芯片是专门为加速机器学习工作负载而设计的半导体，比 GPU 等通用芯片更高效。三星代工是全球最大的半导体合同制造商之一，为自研芯片的公司提供制造服务。Anthropic 是 Claude 系列大语言模型的开发者，该模型采用宪法 AI 技术进行训练。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Samsung_Foundry">Samsung Foundry</a></li>
<li><a href="https://semiconductor.samsung.com/foundry/">Foundry Overview | Samsung Semiconductor Global</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_(language_model)">Claude (language model)</a></li>

</ul>
</details>

**标签**: `#AI chips`, `#Anthropic`, `#Samsung`, `#custom silicon`, `#AI hardware`

---