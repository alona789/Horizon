---
layout: default
title: "Horizon Summary: 2026-08-01 (EN)"
date: 2026-08-01
lang: en
---

> From 38 items, 9 important content pieces were selected

---

1. [OpenAI&\#x27;s Astra Achieves New Results on Ten Long-Standing Math Problems](#item-1) ⭐️ 9.0/10
2. [Google&\#x27;s Reader Shutdown and Its Role in RSS Decline](#item-2) ⭐️ 8.0/10
3. [NetBSD 11.0 Released with Enhanced NPF Firewall and Fast-Booting MicroVM Kernel](#item-3) ⭐️ 8.0/10
4. [Canada Signs UN Cybercrime Convention, Critics Warn of Surveillance](#item-4) ⭐️ 8.0/10
5. [DeepSeek V4 Flash 0731: 304B Model Delivers Top Value with Agentic Boost](#item-5) ⭐️ 8.0/10
6. [How Symmetric Are the Insides of a Go Network?](#item-6) ⭐️ 8.0/10
7. [VLM Benchmarks Reward Empty Radiology Reports, Erase Rare Clinical Terms](#item-7) ⭐️ 8.0/10
8. [Major Labels Propose Barring AI Songs from Official Charts](#item-8) ⭐️ 8.0/10
9. [Microsoft CEO confirms Copilot &\#x27;super app&\#x27; launching this year](#item-9) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI&\#x27;s Astra Achieves New Results on Ten Long-Standing Math Problems](https://openai.com/index/ten-advances-in-mathematics/) ⭐️ 9.0/10

OpenAI reported that an internal version of its next model, Astra, produced new results on ten open problems in mathematics and theoretical computer science, with proofs formalized in the Lean proof assistant. The problems had seen no major progress for at least a decade, and the work was done with human collaboration. This marks a major milestone in using AI as a research collaborator in mathematics, potentially accelerating discovery on problems that have resisted human effort for decades. It also raises important questions about attribution, verification, and the future role of human mathematicians. OpenAI says each problem cost less than $2,000 in token usage at GPT-5.6 Sol prices to generate the arguments. The results are not yet peer-reviewed; the team has released Lean 4 formalizations in the openai/ten-proofs repository, a paper, and an LLM-generated PDF reconstructing the reasoning.

telegram · zaihuapd · Aug 1, 07:59

**Background**: The ten problems include the existence of non-sofic groups, a counterexample to Connes&\#x27; rigidity conjecture, high-dimensional sphere packing, arithmetic circuit lower bounds, quantum parallel repetition, the hardness of the nearest vector problem, and multicolor Ramsey numbers. Sofic groups are finite approximations of infinite groups, and whether non-sofic groups exist has been a central open question in geometric group theory since Gromov introduced the concept. Lean is an interactive proof assistant that can mechanically verify mathematical proofs, making them more reliable and reproducible.

<details><summary>References</summary>
<ul>
<li><a href="https://mathoverflow.net/questions/513821/existence-of-non-sofic-groups">gr.group theory - Existence of non sofic groups - MathOverflow</a></li>
<li><a href="https://en.wikipedia.org/wiki/Lean_%28proof_assistant%29">Lean (proof assistant) - Wikipedia</a></li>
<li><a href="https://vibemathed.com/problem/non-sofic-groups-exist">Existence of Non-Sofic Groups - VibeMathed</a></li>

</ul>
</details>

**Discussion**: Mathematicians online are reacting with a mix of awe and existential unease, with some comparing the moment to &\#x27;Deep Blue&\#x27; and others describing a &\#x27;profound spiritual crisis&\#x27; in essays like Kirwin Hampshire&\#x27;s &\#x27;The Dark Night of Mathematics.&\#x27; On MathOverflow, a starting PhD student noted the claimed result on non-sofic groups and expressed interest in related open problems.

**Tags**: `#AI research`, `#mathematics`, `#OpenAI`, `#formal verification`, `#breakthrough`

---

<a id="item-2"></a>
## [Google&\#x27;s Reader Shutdown and Its Role in RSS Decline](https://openrss.org/blog/how-google-helped-destroy-adoption-of-rss-feeds) ⭐️ 8.0/10

The article contends that Google, primarily through the shutdown of Google Reader in 2013, played a decisive role in the collapse of RSS adoption. The piece sparked a lively discussion on Hacker News about Google&\#x27;s responsibility and the fate of the open web. RSS is a decentralized, open standard that lets users control their news consumption; its decline contributed to the dominance of centralized platforms and algorithmic feeds. Understanding this history matters for debates about internet decentralization, platform power, and content distribution. Google launched Reader in 2005 and closed it on July 1, 2013, citing declining usage—a justification many users found dubious because Google was pushing Google+ at the time. Mozilla also removed Live Bookmarks and RSS subscription support in Firefox 64, further weakening native RSS capabilities in browsers.

hackernews · pudgywalsh · Aug 1, 18:07 · [Discussion](https://news.ycombinator.com/item?id=49136821)

**Background**: RSS \(Really Simple Syndication\) is a standardized web feed format that allows users to subscribe to website updates and read them in a single aggregator, such as a news reader. Google Reader, launched in 2005, was one of the most popular RSS aggregators and served as a platform for many other apps. Its shutdown on July 1, 2013, removed a mainstream gateway to RSS for millions of users, accelerating the shift toward social media and centralized news distribution.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/RSS">RSS</a></li>
<li><a href="https://en.wikipedia.org/wiki/Google_Reader">Google Reader</a></li>

</ul>
</details>

**Discussion**: Commenters expressed nostalgia for the early-2000s internet and anger at Google&\#x27;s &\#x27;declining usage&\#x27; excuse, noting it was promoting Google+ at the time. Several pointed to Mozilla&\#x27;s removal of Live Bookmarks as another blow, while others recommended alternatives like NetNewsWire instead of relying on Google products.

**Tags**: `#RSS`, `#Google`, `#Web History`, `#Internet`, `#Decentralization`

---

<a id="item-3"></a>
## [NetBSD 11.0 Released with Enhanced NPF Firewall and Fast-Booting MicroVM Kernel](https://blog.netbsd.org/tnf/entry/netbsd_11_0_released) ⭐️ 8.0/10

NetBSD 11.0 has been officially released, introducing major updates such as layer 2 and user/group filtering in the NPF firewall, a new MICROVM kernel for x86 that boots in about 10 ms, and broad hardware support improvements. This release strengthens NetBSD&\#x27;s position as a versatile open-source operating system by adding modern firewall capabilities and an ultra-fast booting microVM kernel, making it more attractive for cloud, virtualization, and embedded scenarios in comparison to Linux and other BSDs. The NPF firewall now supports layer 2 filtering as well as filtering by user and group, and the new MICROVM kernel is designed to boot in approximately 10 ms with the entire VM fitting into about 10 MB. The release also includes numerous hardware and driver improvements across supported platforms.

hackernews · jaypatelani · Aug 1, 17:56 · [Discussion](https://news.ycombinator.com/item?id=49136736)

**Background**: NetBSD is a free, open-source Unix-like operating system renowned for its portability across a wide range of hardware architectures. NPF is NetBSD&\#x27;s BSD-licensed stateful packet filter firewall, comparable to Linux&\#x27;s iptables or FreeBSD&\#x27;s pf. The MICROVM kernel is a lightweight kernel specifically built for rapid virtual machine startup, a concept demonstrated by projects like smolBSD.

<details><summary>References</summary>
<ul>
<li><a href="https://ostechnix.com/build-10mb-netbsd-vms-boot-10ms-smolbsd/">Build 10MB NetBSD VMs That Boot in 10ms Using... - OSTechNix</a></li>
<li><a href="https://www.wikiwand.com/EN/NPF_%28firewall%29">NPF ( firewall ) - Wikiwand</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters questioned the current status of the BSDs versus Linux and whether Wine can run Windows software on NetBSD. Some praised the value of layer 2 NPF filtering and the 10 ms microVM boot, while others observed that the release announcement seemed almost apologetic about open issues.

**Tags**: `#NetBSD`, `#BSD`, `#operating-system`, `#release`, `#firewall`

---

<a id="item-4"></a>
## [Canada Signs UN Cybercrime Convention, Critics Warn of Surveillance](https://www.michaelgeist.ca/2026/07/a-surveillance-treaty-in-disguise-the-trouble-with-canadas-quiet-decision-to-sign-the-un-cybercrime-convention/) ⭐️ 8.0/10

Canada quietly signed the United Nations Convention against Cybercrime in May 2026, a move critics describe as a surveillance treaty in disguise. The signing makes Canada one of 76 participants, but ratification has not yet occurred. If ratified, the treaty could expand cross-border access to electronic evidence and affect digital privacy rights for Canadians. It also signals Canada&\#x27;s alignment with a convention that human rights organizations have criticized for potential surveillance abuses. The convention was proposed by Russia and adopted by the UN General Assembly in December 2024. Several Western nations, including Australia, the EU, and the UK, have also signed, but the treaty&\#x27;s impact remains limited until formal ratification.

hackernews · iamnothere · Aug 1, 14:19 · [Discussion](https://news.ycombinator.com/item?id=49134694)

**Background**: The United Nations Convention against Cybercrime, also known as the Hanoi Convention, is the first comprehensive global treaty on cybercrime. It aims to strengthen international cooperation in sharing electronic evidence for serious crimes, but human rights groups have raised concerns about potential surveillance and privacy violations.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/United_Nations_Convention_against_Cybercrime">United Nations Convention against Cybercrime - Wikipedia</a></li>
<li><a href="https://www.unodc.org/unodc/en/cybercrime/convention/home.html">United Nations Convention against Cybercrime</a></li>
<li><a href="https://www.unodc.org/unodc/en/cybercrime/convention/text/convention-full-text.html">UN Cybercrime Convention - Full Text</a></li>

</ul>
</details>

**Discussion**: Commenters acknowledged that signing does not equal ratification, noting that countries like Australia, the EU, and the UK have also signed. Some praised Michael Geist for his investigative work on privacy, while others observed that Canada signs most UN instruments, and one commenter reflected on the signaling games inherent in international politics.

**Tags**: `#privacy`, `#surveillance`, `#cybercrime`, `#digital-rights`, `#policy`

---

<a id="item-5"></a>
## [DeepSeek V4 Flash 0731: 304B Model Delivers Top Value with Agentic Boost](https://simonwillison.net/2026/Jul/31/deepseek-v4-flash-0731/#atom-everything) ⭐️ 8.0/10

DeepSeek released DeepSeek-V4-Flash-0731, a 304B-parameter model \(167GB on Hugging Face\) with substantially enhanced agentic capabilities. It is priced at $0.14 per million input tokens and $0.27 per million output tokens, and Artificial Analysis ranks it ahead of the larger 428B-parameter MiniMax M3. The model appears to be the best value-per-intelligence option currently on the market, beating far more expensive competitors on the Artificial Analysis Intelligence Index versus cost-per-task chart. This reinforces the trend of cost-effective open-weight models putting pressure on premium-priced frontier models. Simon Willison&\#x27;s testing showed that output quality depends heavily on the reasoning effort setting: the default level produced poor results in his pelican illustration test, while setting reasoning\_effort to &quot;high&quot; via OpenRouter yielded much better output. The model is available on Hugging Face as deepseek-ai/DeepSeek-V4-Flash-0731.

rss · Simon Willison · Jul 31, 23:59

**Background**: Agentic capabilities refer to an AI model&\#x27;s ability to reason, plan, act, and interact autonomously to complete complex, multi-step tasks, rather than merely generating single-shot responses. The Artificial Analysis Intelligence Index is a model-level score that aggregates multiple benchmarks—including reasoning and knowledge tests—to measure overall intelligence. DeepSeek is a Chinese AI lab known for releasing powerful open-weight models at aggressive prices, and V4 Flash is the latest addition to its V4 family.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2503.23037">[2503.23037] Agentic Large Language Models, a survey</a></li>
<li><a href="https://mitsloan.mit.edu/ideas-made-to-matter/agentic-ai-explained">Agentic AI, explained | MIT Sloan</a></li>
<li><a href="https://artificialanalysis.ai/models">Comparison of AI Models across Intelligence , Performance, and Price</a></li>

</ul>
</details>

**Tags**: `#deepseek`, `#llm`, `#model-release`, `#ai`, `#cost-effective`

---

<a id="item-6"></a>
## [How Symmetric Are the Insides of a Go Network?](https://www.reddit.com/r/MachineLearning/comments/1vcrki2/how_symmetric_are_the_insides_of_a_go_network_r/) ⭐️ 8.0/10

The author of the open-source Go engine KataGo has posted a new ML interpretability study analyzing how much the network&\#x27;s internal representations are symmetric under board rotation and reflection, despite training only with stochastic 8-fold data augmentation. The writeup notes that one finding was unexpected. Understanding whether neural networks can automatically discover symmetries could improve how we design architectures and augmentation strategies for domains with known invariances. It also contributes to interpretability research for superhuman game-playing models. The study is written to be accessible to non-ML readers, and the accompanying code is linked from the same repository. The writeup was largely produced with AI assistance, but with detailed human direction and feedback.

reddit · r/MachineLearning · /u/icosaplex · Aug 1, 16:18

**Background**: Go is a board game whose rules are symmetric under rotation and reflection: any position evaluated after an 8-fold transformation should be equivalent. KataGo, a strong open-source Go engine trained primarily via self-play, does not enforce this symmetry in its neural network architecture; instead, it relies on stochastic 8-fold data augmentation during training. This study investigates whether the network automatically develops orientation-invariant concepts or memorizes separate representations for each rotation/reflection.

<details><summary>References</summary>
<ul>
<li><a href="https://katagotraining.org/">KataGo Distributed Training</a></li>

</ul>
</details>

**Tags**: `#ML interpretability`, `#Go`, `#neural networks`, `#symmetry`, `#KataGo`

---

<a id="item-7"></a>
## [VLM Benchmarks Reward Empty Radiology Reports, Erase Rare Clinical Terms](https://www.reddit.com/r/MachineLearning/comments/1vcipzz/vlms_can_score_well_on_benchmarks_while_silently/) ⭐️ 8.0/10

A new paper by Parikh et al. shows that standard evaluation metrics for vision-language models in chest X-ray report generation reward repetitive, clinically empty templates and silently erase rare but clinically meaningful terms. The authors introduce a framework to measure clinical terminology erasure and the introduction of biased terms. Because these flawed metrics are used to validate medical AI, models that score well on benchmarks may produce clinically useless or misleading reports. This work exposes a hidden failure mode in high-stakes radiology AI and could reshape how medical report generation models are evaluated. The authors observed that reports described as &\#x27;normal&\#x27; or written as repetitive templates receive high scores under benchmark metrics, while clinically meaningful rare words are erased. They further hypothesize that such semantic erasure stems from inference strategies that systematically suppress clinical terminology to minimize generation risk.

reddit · r/MachineLearning · /u/ade17\_in · Aug 1, 09:27

**Background**: Vision-language models \(VLMs\) are increasingly used to generate radiology reports from chest X-rays. Standard evaluation metrics such as BLEU and ROUGE are based on n-gram overlap with reference texts, so they tend to reward repetitive, conservative language and can miss whether critical clinical findings are mentioned. This paper highlights a &\#x27;terminology erasure&\#x27; problem and proposes a framework for quantifying it, complementing existing clinical-aware metrics like RaTEScore.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/pdf/2603.01625">Measuring What VLMs Don&#x27;t Say: Validation Metrics Hide Clinical ...</a></li>
<li><a href="https://aclanthology.org/2024.emnlp-main.836/">RaTEScore: A Metric for Radiology Report Generation - ACL ...</a></li>
<li><a href="https://www.emergentmind.com/topics/weighted-association-erasure-wae">Weighted Association Erasure in Clinical NLP</a></li>

</ul>
</details>

**Tags**: `#Vision-Language Models`, `#Medical AI`, `#Evaluation Metrics`, `#Radiology`, `#Bias`

---

<a id="item-8"></a>
## [Major Labels Propose Barring AI Songs from Official Charts](https://www.theverge.com/ai-artificial-intelligence/973741/ai-music-major-record-labels-charts) ⭐️ 8.0/10

Universal Music, Sony Music, and Warner Music jointly proposed that AI-generated songs must be &\#x27;substantially human-authored&\#x27; to qualify for official music charts. The proposal has received support from IFPI, but no chart operator has immediately adopted it. This marks a significant policy shift in how the music industry treats AI-generated content, moving from simple labeling to formal eligibility rules. If adopted, it could set a precedent for AI regulation and copyright enforcement across the creative industries. The proposal goes beyond earlier AI music labeling schemes from RIAA and IFPI by also requiring that AI services be legitimately licensed, training data be copyrighted, and that no chart manipulation or streaming fraud occurs. Key terms such as &\#x27;substantially human-authored&\#x27; remain vaguely defined, and neither Sony nor Universal responded to requests for comment.

telegram · zaihuapd · Aug 1, 02:53

**Background**: Music charts like the Billboard Hot 100 or the UK Official Charts determine commercial success and industry recognition. The International Federation of the Phonographic Industry \(IFPI\) represents the global recorded music industry, while the Recording Industry Association of America \(RIAA\) is the US trade body; both had previously proposed labeling AI-generated music. The new proposal shifts the debate from transparency towards defining human authorship and content eligibility.

**Tags**: `#AI music`, `#copyright`, `#music industry`, `#regulation`, `#charts`

---

<a id="item-9"></a>
## [Microsoft CEO confirms Copilot &\#x27;super app&\#x27; launching this year](https://www.theverge.com/tech/972927/microsoft-copilot-super-app-confirmed) ⭐️ 8.0/10

Microsoft CEO Satya Nadella confirmed on the company&\#x27;s quarterly earnings call that a Copilot &\#x27;super app&\#x27; will launch this year, merging chat, coding, and agentic capabilities for both consumer and commercial use. He said the company will fold these experiences, including code features, into one super app this quarter. This signals Microsoft&\#x27;s push to unify its AI offerings into a single entry point, which could reshape how developers and enterprises access AI-powered coding and automation tools. It also intensifies competition with OpenAI, which recently launched ChatGPT Work to combine ChatGPT and Codex. The super app is expected to integrate the Copilot chatbot, GitHub Copilot, Copilot Cowork, and Autopilot systems. Microsoft reported quarterly revenue of $90 billion, driven mainly by AI and cloud, though specific product details remain high-level.

telegram · zaihuapd · Aug 1, 13:18

**Background**: Copilot is Microsoft&\#x27;s AI assistant embedded across Windows, Microsoft 365, and developer tools, while GitHub Copilot specifically assists with code. Agentic AI refers to systems that can pursue goals and take actions autonomously. Copilot Cowork automates tasks such as sending emails, scheduling meetings, and creating documents, while Autopilots are always-on agents that work in the background without needing repeated prompts.

<details><summary>References</summary>
<ul>
<li><a href="https://www.ibm.com/think/topics/agentic-ai">What is Agentic AI? | IBM</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365-copilot/cowork">Copilot Cowork: Automate Tasks and Workflows | Microsoft</a></li>
<li><a href="https://www.microsoft.com/en-us/microsoft-365/blog/2026/06/02/introducing-microsoft-scout-your-always-on-personal-agent/">Introducing Microsoft Scout: Your always-on personal agent | Microsoft 365 Blog</a></li>

</ul>
</details>

**Tags**: `#Microsoft`, `#Copilot`, `#AI`, `#Agentic`, `#Super App`

---