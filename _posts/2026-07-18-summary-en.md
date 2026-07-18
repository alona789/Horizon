---
layout: default
title: "Horizon Summary: 2026-07-18 (EN)"
date: 2026-07-18
lang: en
---

> From 33 items, 11 important content pieces were selected

---

1. [LG monitors silently install software via Windows Update without consent](#item-1) ⭐️ 9.0/10
2. [Trump considers FINRA-like watchdog to review top AI models](#item-2) ⭐️ 9.0/10
3. [GPT-5.6 Solves 30-Year Convex Optimization Conjecture with a Prompt](#item-3) ⭐️ 8.0/10
4. [Kimi K3 Achieves Frontier Performance via Distillation](#item-4) ⭐️ 8.0/10
5. [Fable 5 vs GPT-5.6 Sol: Does /goal Help on NP-Hard?](#item-5) ⭐️ 8.0/10
6. [TP-Link Kasa cameras leaked GPS location via unauthenticated UDP for 6 years](#item-6) ⭐️ 8.0/10
7. [Alleged AI Slop Wins $25K DeepMind Kaggle Prize](#item-7) ⭐️ 8.0/10
8. [Doubao Phone Drops GUI Automation, Embraces MCP](#item-8) ⭐️ 8.0/10
9. [Meta May Rent AI Compute to Anthropic in Potential $10B Deal](#item-9) ⭐️ 8.0/10
10. [TSMC Announces A14 Process Technology for 2028 Production](#item-10) ⭐️ 8.0/10
11. [SF Orders Apple and Google to Remove 'Nudify' Apps](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [LG monitors silently install software via Windows Update without consent](https://videocardz.com/newz/lg-monitors-silently-install-software-through-windows-update-without-user-consent) ⭐️ 9.0/10

LG monitors automatically install software such as 'LG Customer Support' or 'LG Update' without user consent when connected via HDMI, leveraging Windows Update's driver delivery mechanism. This occurs in the background with no user interaction required. This silent installation poses a significant security and privacy risk as the software has full system access, no sandboxing, and can potentially serve as a supply-chain attack vector. It affects all Windows users who connect an LG monitor. The software installs immediately when an LG monitor is plugged in, even if the user already had an older LG monitor. It runs at every system boot. Workarounds include disabling automatic download of device apps via Group Policy or Device Installation Settings.

hackernews · baranul · Jul 18, 10:21 · [Discussion](https://news.ycombinator.com/item?id=48956688)

**Background**: Windows Update can automatically download and install driver updates, including associated software, to ensure devices function properly. This feature is intended for convenience but can be exploited by hardware vendors to push unrelated or potentially unwanted software. Supply-chain attacks occur when a trusted distribution channel is used to deliver malicious or unwanted software, as highlighted by this incident.

<details><summary>References</summary>
<ul>
<li><a href="https://support.microsoft.com/en-US/Windows/Hardware/Drivers/automatically-get-recommended-and-updated-hardware-drivers">Automatically get recommended and updated hardware drivers</a></li>
<li><a href="https://en.wikipedia.org/wiki/Supply_chain_attack">Supply chain attack - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters expressed strong concern, noting that Windows is ultimately responsible for allowing automatic installation without consent. Some provided group policy workarounds and emphasized that this could be exploited by malware. Others pointed out the irony that monitors are now a vector for unwanted software.

**Tags**: `#security`, `#windows`, `#privacy`, `#supply-chain-attack`, `#lg`

---

<a id="item-2"></a>
## [Trump considers FINRA-like watchdog to review top AI models](https://www.bloomberg.com/news/articles/2026-07-17/us-considers-creating-finra-like-watchdog-to-vet-top-ai-models) ⭐️ 9.0/10

The Trump administration is considering creating an independent AI oversight body modeled after the Financial Industry Regulatory Authority (FINRA) to vet the safety of top AI models, led by Treasury Secretary Scott Bessent and under review by White House Chief of Staff Susie Wiles. This proposal could shift AI regulation from ad hoc government interventions to a structured framework combining industry self-regulation and government oversight, directly affecting the release processes of leading AI firms like OpenAI and Anthropic and addressing concerns from both Wall Street and Silicon Valley. The new agency would report to the Securities and Exchange Commission (SEC); notably, Anthropic and OpenAI previously objected to government requests to modify or delay their latest models. The plan aligns with recommendations from Google DeepMind CEO Demis Hassabis, though President Trump has not yet reviewed it and details remain subject to change.

telegram · zaihuapd · Jul 18, 05:45

**Background**: FINRA is an independent regulatory body overseen by the SEC that protects investors and ensures market integrity in the U.S. securities industry. The proposal aims to apply a similar model to AI safety, giving Wall Street and Silicon Valley a larger voice in jointly setting security standards, rather than relying on temporary government controls.

<details><summary>References</summary>
<ul>
<li><a href="https://zh.wikipedia.org/zh-hans/美国证券法">美国证券法 - 维基百科，自由的百科全书</a></li>
<li><a href="https://www.oanda.com/bvi-ft/lab-education/invest_us_stock/finra/">FINRA是什麼？介紹其成立宗旨與功能所在 - OANDA Lab</a></li>
<li><a href="https://lazarusalliance.com/zh-CN/什么是FINRA合规性/">什么是 FINRA 合规性？ - Lazarus Alliance, Inc.</a></li>

</ul>
</details>

**Tags**: `#AI监管`, `#政策`, `#特朗普政府`, `#FINRA`, `#AI安全`

---

<a id="item-3"></a>
## [GPT-5.6 Solves 30-Year Convex Optimization Conjecture with a Prompt](https://old.reddit.com/r/math/comments/1uxj3cy/after_openais_cdc_proof_announcement_gpt56_used_a/) ⭐️ 8.0/10

OpenAI's GPT-5.6 model solved a 30-year-old open problem in convex optimization by using a single prompt, marking a demonstration of LLMs contributing to mathematical research. This shows that advanced AI can tackle long-standing mathematical problems, potentially accelerating discovery and shifting the role of human researchers toward more creative work. The problem involves proving an upper bound on the complexity of convex optimization over Lipschitz functions on a spherical domain, a niche but recognized conjecture. The model used was Sol Pro, not Ultra, according to Reddit clarification.

hackernews · mbustamanter · Jul 18, 13:00 · [Discussion](https://news.ycombinator.com/item?id=48957779)

**Background**: Convex optimization is a subfield of mathematical optimization focusing on minimizing convex functions over convex sets, with many polynomial-time algorithms. However, some specific problem classes remained open for decades. GPT-5.6 is a large language model capable of reasoning and generating proofs when suitably prompted.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Convex_optimization">Convex optimization - Wikipedia</a></li>
<li><a href="https://whatdoesmeanings.com/general/gpt-5-6-used-a-prompt-to-close-a-30-year-gap-in-convex-optimization/">GPT-5.6 Used A Prompt To Close A 30 - Year Gap In Convex ...</a></li>
<li><a href="https://pulseaugur.com/cluster/149817-gpt-5-6-solves-30-year-convex-optimization-problem">GPT-5.6 Solves 30 - Year Convex Optimization Problem · PulseAugur</a></li>

</ul>
</details>

**Discussion**: The community generally validated the result's importance, noting the problem is more niche than OpenAI's cyclic double cover proof but still a real contribution. Some discussed the implications for mathematical research, suggesting it may eliminate low-hanging fruit while requiring human creativity for novel approaches. There was also clarification that Sol Pro was used, not Ultra, prompting curiosity about the difference between models.

**Tags**: `#AI`, `#convex optimization`, `#mathematical research`, `#LLM applications`, `#open problem`

---

<a id="item-4"></a>
## [Kimi K3 Achieves Frontier Performance via Distillation](https://stephen.bochinski.dev/blog/2026/07/18/the-kimi-k3-moment/) ⭐️ 8.0/10

Chinese lab Moonshot AI released Kimi K3, a 2.8 trillion parameter model that achieves frontier-level performance through knowledge distillation, raising debates about the inevitability of such advancements and their geopolitical impact. This event shows that distillation can enable fast catch-ups by non-frontier labs, potentially accelerating AI competition and prompting stricter national security measures. It challenges the assumption that frontier models require massive resources and original research. Kimi K3 uses the novel Kimi Delta Attention mechanism and supports a 1M-token context window. Distillation involves training a smaller 'student' model to replicate the outputs of a larger 'teacher' model, reducing cost while retaining performance.

hackernews · sbochins · Jul 18, 17:32 · [Discussion](https://news.ycombinator.com/item?id=48960218)

**Background**: Knowledge distillation is a model compression technique where a small model learns from a large model's predictions, enabling efficient deployment. Moonshot AI is a Chinese company known for long-context models, and Kimi K3 is their latest flagship, designed for frontier tasks like software engineering and reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_(chatbot)">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://platform.kimi.ai/docs/guide/kimi-k3-quickstart">Kimi K3 - Kimi API Platform</a></li>
<li><a href="https://www.linkedin.com/pulse/knowledge-distillation-how-large-language-models-learn-fahim-ahamed-2inie">Knowledge Distillation in AI : How Large Models Train Smaller</a></li>

</ul>
</details>

**Discussion**: Commenters debated whether distillation undermines original research, with some arguing it's an inevitable step just like how frontier labs distilled human knowledge. Others shared mixed practical experiences: one user found Kimi K3 slower and less efficient than alternatives, while another speculated that geopolitical frustrations drive support for the model despite technical flaws.

**Tags**: `#AI`, `#Distillation`, `#Frontier Models`, `#Geopolitics`, `#Performance Comparison`

---

<a id="item-5"></a>
## [Fable 5 vs GPT-5.6 Sol: Does /goal Help on NP-Hard?](https://charlesazam.com/blog/fable-5-gpt-5-6-sol-goal/) ⭐️ 8.0/10

A blog post compares Anthropic's Fable 5 and OpenAI's GPT-5.6 Sol on an NP-hard problem, testing whether the /goal directive improves model performance on complex reasoning tasks. This evaluation sheds light on how advanced LLMs handle structured problem-solving and whether goal-setting directives enhance their reasoning, which is relevant for AI research and practical applications in optimization. The blog notes that the /goal directive works better for single-track investigations or small-scale scatter/gather, while ultra mode (with parallel investigators and adversarial review) may be superior for broader search strategies.

hackernews · couAUIA · Jul 18, 11:00 · [Discussion](https://news.ycombinator.com/item?id=48956879)

**Background**: NP-hard problems are notoriously difficult to solve optimally, and LLMs are increasingly tested on such tasks to gauge reasoning ability. The /goal directive is a prompt feature that instructs the model to focus on a specific objective, potentially improving performance on tasks requiring sustained attention and strategic planning. Both Fable 5 and GPT-5.6 Sol represent the latest generation of frontier AI models from Anthropic and OpenAI, respectively.

<details><summary>References</summary>
<ul>
<li><a href="https://www.anthropic.com/claude/fable">Claude Fable \ Anthropic</a></li>
<li><a href="https://openai.com/index/previewing-gpt-5-6-sol/">Previewing GPT-5.6 Sol: a next-generation model | OpenAI</a></li>

</ul>
</details>

**Discussion**: Community members noted that GPT models have excelled in optimization competitions, suggesting an inherent advantage. Others shared experiences that Claude models sometimes forget long-context instructions, and the /goal directive might help mitigate that issue. One commenter found the chart confusing due to an inverted y-axis.

**Tags**: `#AI`, `#LLM`, `#NP-hard`, `#benchmark`, `#problem-solving`

---

<a id="item-6"></a>
## [TP-Link Kasa cameras leaked GPS location via unauthenticated UDP for 6 years](https://github.com/BadChemical/IoT-Vulnerability-Research-Public/blob/main/TP-Link_Kasa_EC71/Kasa_EC71.md) ⭐️ 8.0/10

Security researcher BadChemical disclosed that TP-Link Kasa EC70 v4 and EC71 v4 cameras continuously broadcast their precise GPS coordinates via unauthenticated UDP packets on the local network, a flaw that has existed for six years. This vulnerability allows any local network attacker to pinpoint a user's exact location without any authentication, posing a severe privacy risk. It highlights the ongoing security shortcomings in IoT devices and the need for better design practices. The GPS data is broadcast over UDP, which is connectionless and unencrypted, enabling passive eavesdropping. The vulnerability requires the attacker to be on the same local network; however, if the device is set to DMZ, it could be exposed to the internet.

hackernews · BadChemical · Jul 17, 21:42 · [Discussion](https://news.ycombinator.com/item?id=48952565)

**Background**: TP-Link Kasa cameras are popular smart home security devices. UDP (User Datagram Protocol) is a lightweight network protocol that does not provide authentication or encryption by default. Many IoT devices suffer from similar vulnerabilities due to hardcoded keys or unsecured communication protocols, making them easy targets for LAN-based attackers.

<details><summary>References</summary>
<ul>
<li><a href="https://cybersecuritynews.com/tp-link-cameras-vulnerability/">Multiple TP-Link Cameras Vulnerability Allows Hackers to ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/User_Datagram_Protocol">User Datagram Protocol - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Community comments express concern over IoT security, with some noting that the vulnerability is local-only and less severe if devices are not exposed to the internet. Others criticize the use of AI-generated reports and raise broader issues about unencrypted data leaks to cloud IPs.

**Tags**: `#IoT`, `#security`, `#privacy`, `#vulnerability`, `#TP-Link`

---

<a id="item-7"></a>
## [Alleged AI Slop Wins $25K DeepMind Kaggle Prize](https://www.reddit.com/r/MachineLearning/comments/1uzyf66/did_blatant_ai_slop_just_win_a_25k_usd_deepmind/) ⭐️ 8.0/10

A Reddit post alleges that the $25,000 grand prize winner of the Google DeepMind-sponsored Kaggle competition 'Measuring Progress Toward AGI' is a low-quality submission filled with unfounded claims and nonsensical outputs, escaping proper review. This controversy highlights potential flaws in review processes for high-profile AI competitions, raising concerns about research integrity and the credibility of prestigious awards. The competition asked participants to design new cognitive-science-based AI benchmarks; the winning entry purportedly used LLM alternative viewpoints but resulted in a disorganized submission exceeding the requested format tenfold.

reddit · r/MachineLearning · /u/TheWerkmeister · Jul 18, 15:10

**Background**: Kaggle is a platform for data science competitions owned by Google. The DeepMind-sponsored challenge focused on measuring progress toward AGI through cognitive science tasks. The review process relies on judges, but the poster claims they failed to scrutinize the winning submission.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kaggle">Kaggle - Wikipedia</a></li>
<li><a href="https://www.kaggle.com/competitions">Kaggle Competitions</a></li>
<li><a href="https://cognitiveaibenchmarking.org/">Cognitive-AI Benchmarking - CAB @ CogSci 2023</a></li>

</ul>
</details>

**Tags**: `#Kaggle`, `#DeepMind`, `#AI ethics`, `#research integrity`, `#controversy`

---

<a id="item-8"></a>
## [Doubao Phone Drops GUI Automation, Embraces MCP](https://www.latepost.com/news/dj_detail?id=3648) ⭐️ 8.0/10

ByteDance's Doubao Phone has shifted strategy from GUI automation (screen reading and simulated clicks) to requiring major super apps like Alibaba and Tencent to provide MCP services for integration, and has increased its stock from 30,000 to hundreds of thousands of units. This move signals a major industry shift from brittle GUI automation to cooperative API-based AI agent interoperability, potentially standardizing how mobile AI assistants interact with third-party apps and reducing friction with app developers. The Doubao Phone assistant received its generative AI service approval on July 15, 2025, and the product was first previewed in December 2024 but had to disable capabilities due to bans from WeChat and Taobao. The new approach aligns with similar MCP frameworks being adopted by Apple and Google.

telegram · zaihuapd · Jul 18, 00:29

**Background**: GUI automation involves reading the screen and simulating clicks to operate apps, which is brittle and often blocked by app developers. MCP (Model Context Protocol) is an open standard that allows AI assistants to request data and actions from apps through official APIs, making interactions more reliable and secure. The shift represents a move from adversarial to cooperative integration between AI assistants and app services.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/mobile-next/mobile-mcp">GitHub - mobile-next/mobile-mcp: Model Context Protocol ...</a></li>
<li><a href="https://modelcontextprotocol.io/docs/getting-started/intro">What is the Model Context Protocol (MCP)?</a></li>
<li><a href="https://www.36kr.com/p/3589329638146309">00后大模型实习生「扒光」豆包手机，千字实测揭秘-36氪</a></li>

</ul>
</details>

**Tags**: `#AI assistant`, `#MCP`, `#mobile strategy`, `#Chinese tech industry`

---

<a id="item-9"></a>
## [Meta May Rent AI Compute to Anthropic in Potential $10B Deal](https://www.nytimes.com/2026/07/17/technology/meta-anthropic-ai-computing-power.html) ⭐️ 8.0/10

Meta is in early talks to rent AI computing power to Anthropic in a potential two-year deal worth up to $10 billion, as reported by The New York Times on July 17, 2026. This deal highlights the extreme scarcity of AI compute resources, and for Meta, it could generate new revenue and ease investor concerns about its massive capital expenditures on data centers. Anthropic proposed the deal in June 2026, and Meta is evaluating it; if finalized, Anthropic would pay monthly, and either party could exit early.

telegram · zaihuapd · Jul 18, 01:14

**Background**: AI companies like Anthropic require enormous computing power to train and run large language models, but specialized hardware (e.g., GPUs) is in short supply. Meta has been investing heavily in AI infrastructure, planning up to $145 billion this year, and renting out excess capacity is a strategic way to optimize utilization.

**Tags**: `#AI computing`, `#Meta`, `#Anthropic`, `#data centers`, `#industry news`

---

<a id="item-10"></a>
## [TSMC Announces A14 Process Technology for 2028 Production](https://t.me/zaihuapd/42643) ⭐️ 8.0/10

TSMC announced its next-generation A14 (1.4nm-class) process technology, scheduled for mass production in 2028. Compared to the N2 (2nm-class) process, A14 offers a 15% speed increase at the same power or a 30% power reduction at the same speed, along with over 20% higher logic density. This announcement reinforces TSMC's technological leadership in advanced semiconductor manufacturing, crucial for powering future AI, high-performance computing, and mobile devices. The performance and efficiency gains over N2 will enable more powerful and energy-efficient chips, impacting the entire electronics industry. TSMC also plans an intermediate A16 process with backside power delivery to launch in late 2026. Chairman C.C. Wei confirmed that A14 production scale will be larger than that of the 2nm process, and TSMC is developing new IC assembly technology to complement CoWoS.

telegram · zaihuapd · Jul 18, 05:00

**Background**: TSMC is the world's leading dedicated semiconductor foundry, manufacturing chips for companies like Apple, NVIDIA, and AMD. Process nodes like N2 (2nm-class) use gate-all-around (GAA) nanosheet transistors, offering significant performance and efficiency improvements over previous FinFET technologies. A14 represents the next step beyond N2, continuing the trend of shrinking transistors and enhancing chip capabilities.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/tsmc-begins-quietly-volume-production-of-2nm-class-chips-first-gaa-transistor-for-tsmc-claims-up-to-15-percent-improvement-at-iso-power">TSMC begins quietly volume production of 2nm-class chips — first GAA transistor for TSMC claims up to 15% improvement at ISO power | Tom's Hardware</a></li>
<li><a href="https://xab.info/en/posts/tsmc-a14-performance-surpasses-n2">TSMC Breaks Its Own Records: New A 14 (1.4nm) Process ... - XAB.info</a></li>
<li><a href="https://www.newkerala.com/news/a/tsmc-projects-mass-production-advanced-a14-chips-2028-477.htm">TSMC A 14 Chips Mass Production by 2028</a></li>

</ul>
</details>

**Tags**: `#TSMC`, `#semiconductor`, `#process technology`, `#A14`, `#hardware`

---

<a id="item-11"></a>
## [SF Orders Apple and Google to Remove 'Nudify' Apps](https://techcrunch.com/2026/07/17/apple-and-google-ordered-to-purge-nudify-apps-from-app-stores/) ⭐️ 8.0/10

San Francisco City Attorney David Chiu demanded Apple and Google remove dozens of AI-powered 'nudify' apps from their app stores, citing non-consensual deepfake image generation. Letters warn the companies may have profited millions by allowing these apps to operate without intervention. This action sets a legal precedent for platform responsibility in curbing AI-powered image abuse and deepfake generation. It highlights the ongoing struggle between free expression, technological innovation, and the need to protect individuals from non-consensual sexual content. Apple stated it removed three apps and terminated associated developer accounts, while Google confirmed it suspended five Play Store apps identified in the letter. The Tech Transparency Project had previously warned both companies in January and April 2026 about these apps.

telegram · zaihuapd · Jul 18, 08:45

**Background**: Nudify apps use artificial intelligence to alter photos of individuals, typically women, to create realistic but fake nude images without consent. These tools are part of a broader deepfake ecosystem that enables image-based sexual abuse, including the creation of child sexual abuse material. The growing accessibility of such AI technology has prompted regulatory scrutiny and calls for stricter platform policies.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtransparencyproject.org/articles/apple-and-google-are-steering-users-to-nudify-apps">TTP - Apple and Google Are Steering Users to Nudify Apps</a></li>
<li><a href="https://www.wired.com/story/deepfake-nudify-technology-is-getting-darker-and-more-dangerous/">Deepfake ‘Nudify’ Technology Is Getting Darker—and More Dangerous | WIRED</a></li>

</ul>
</details>

**Tags**: `#AI ethics`, `#deepfakes`, `#app store regulation`, `#privacy`, `#platform responsibility`

---