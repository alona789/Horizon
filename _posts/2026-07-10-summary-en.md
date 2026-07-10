---
layout: default
title: "Horizon Summary: 2026-07-10 (EN)"
date: 2026-07-10
lang: en
---

> From 35 items, 7 important content pieces were selected

---

1. [Long March 10B achieves world's first net-based rocket recovery at sea](#item-1) ⭐️ 10.0/10
2. [QuadRF: Open-Source Phased-Array RF Visualizer Spots Drones and WiFi Through Walls](#item-2) ⭐️ 8.0/10
3. [Write Code Like a Human Will Maintain It](#item-3) ⭐️ 8.0/10
4. [Musk Reverses, Praises Anthropic, Pledges No Service Cut](#item-4) ⭐️ 8.0/10
5. [Anthropic Web Crawler Scrapes 2800 Pages Per Referral](#item-5) ⭐️ 8.0/10
6. [OpenAI, Google Provide AI Models to Blacklisted Chinese Firms via Singapore](#item-6) ⭐️ 8.0/10
7. [Meta faces $12B EU fine over addictive design](#item-7) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Long March 10B achieves world's first net-based rocket recovery at sea](https://weibo.com/7340734455/R814of1Ki) ⭐️ 10.0/10

On July 10, 2026, China's Long March 10B rocket launched from Hainan Commercial Space Launch Site and successfully achieved the world's first net-based recovery of a rocket first stage at sea, marking China's first controlled recovery of a rocket first stage. This breakthrough establishes China's unique recovery path distinct from SpaceX's landing-leg approach, potentially lowering launch costs and advancing China's reusable rocket technology toward operational missions. The first stage is equipped with 7 YF-100K kerosene/oxygen engines and a hook device, while the recovery ship 'Leader' (25,000-ton DP platform) deployed an '井'-shaped flexible net to catch the rocket. Under fully recovered mode, the rocket's LEO payload is no less than 16 tons, comparable to Falcon 9.

telegram · zaihuapd · Jul 10, 04:36

**Background**: Reusable rockets aim to reduce space access cost by recovering and reusing the most expensive part—the first stage. Previous methods include propulsive landing with landing legs (e.g., SpaceX Falcon 9). China's net-based recovery uses a flexible net on a sea platform to catch the descending stage, eliminating heavy landing legs.

<details><summary>References</summary>
<ul>
<li><a href="https://finance.sina.com.cn/wm/2026-07-10/doc-inihhzsc8353906.shtml">中国开启可回收火箭时代，全球首创的“网系回收”有何玄机？_新浪财经_新浪网</a></li>
<li><a href="https://www.stcn.com/article/detail/4011092.html">中国开启可回收火箭时代，全球首创的“网系回收”有何玄机？</a></li>
<li><a href="https://finance.sina.com.cn/tech/digi/2026-07-10/doc-inihhvka7187715.shtml">全球首次运载火箭网系回收！我国长征十号乙运载火箭成功实现一子级可控回收_新浪科技_新浪网</a></li>

</ul>
</details>

**Tags**: `#航天工程`, `#火箭回收`, `#中国航天`, `#技术创新`

---

<a id="item-2"></a>
## [QuadRF: Open-Source Phased-Array RF Visualizer Spots Drones and WiFi Through Walls](https://www.jeffgeerling.com/blog/2026/quadrf-can-spot-drones-and-see-wifi-through-my-wall/) ⭐️ 8.0/10

Jeff Geerling tested the QuadRF, an open-source phased-array radio built around a Raspberry Pi 5 and FPGA, that visualizes RF signals in the 5-6 GHz range and can detect drones and WiFi sources through walls. This tool democratizes RF sensing, enabling hobbyists and researchers to experiment with beamforming and signal localization without expensive proprietary equipment. It has implications for security, drone detection, and wireless network diagnostics. The QuadRF operates only in the 5-6 GHz band due to its antennas and processing; its RF-core and factory DSP bitstreams are proprietary, but schematics and firmware are open-source. It comes as a kit with a tile and four swappable dual-polarization antennas.

hackernews · speckx · Jul 10, 15:59 · [Discussion](https://news.ycombinator.com/item?id=48861717)

**Background**: RF visualization uses phased-array antennas to steer and focus on radio signals, creating a 2D heatmap of signal strength. Similar to thermal cameras, these devices map invisible RF energy. Drone detection relies on picking up control signals or video transmissions from drones, which typically operate in ISM bands like 2.4 and 5.8 GHz. QuadRF's focus on 5-6 GHz covers the common 5.8 GHz band used by many consumer drones.

<details><summary>References</summary>
<ul>
<li><a href="https://www.jeffgeerling.com/blog/2026/quadrf-can-spot-drones-and-see-wifi-through-my-wall/">QuadRF can spot drones and see WiFi through my wall - Jeff Geerling</a></li>
<li><a href="https://hackaday.com/2026/06/20/seeing-the-world-in-radio-waves-with-the-quadrf/">Seeing The World In Radio Waves With The QuadRF | Hackaday</a></li>
<li><a href="https://www.crowdsupply.com/scale-rf/quadrf">QuadRF | Crowd Supply</a></li>

</ul>
</details>

**Discussion**: The creator (mrtnmcc) answered questions and noted plans to improve UI based on feedback. Some commenters asked about frequency limitations and suggested extending coverage to other bands. Others compared it to thermal cameras or speculated about government capabilities.

**Tags**: `#RF detection`, `#open-source hardware`, `#drone detection`, `#WiFi sensing`, `#maker projects`

---

<a id="item-3"></a>
## [Write Code Like a Human Will Maintain It](https://unstack.io/write-code-like-a-human-will-maintain-it) ⭐️ 8.0/10

The article argues for writing maintainable code with a human maintainer in mind and highlights pitfalls of LLM-generated code that can harm maintainability. As AI-assisted coding becomes widespread, understanding how to preserve code maintainability is crucial for long-term project health and team collaboration. The article and comments discuss using a `/review` command with a checklist, and that LLMs tend to repeat patterns without proper abstraction, leading to overly verbose and copy-pasted code.

hackernews · ScottWRobinson · Jul 10, 13:33 · [Discussion](https://news.ycombinator.com/item?id=48859701)

**Background**: Code maintainability refers to how easily code can be understood, modified, and extended by developers. AI coding assistants like LLMs can generate code quickly but often lack deep understanding of the codebase's architecture, leading to technical debt if not carefully reviewed.

<details><summary>References</summary>
<ul>
<li><a href="https://www.revelo.com/blog/llm-code-generation-2025-trends-predictions-human-data">LLM - Generated Code in 2025: Trends and Predictions</a></li>
<li><a href="https://www.numberanalytics.com/blog/ultimate-guide-code-maintainability">Code Maintainability Best Practices - numberanalytics.com</a></li>
<li><a href="https://dev.to/devcorner/writing-clean-scalable-and-maintainable-code-a-developers-guide-4bep">Writing Clean, Scalable, and Maintainable Code: A Developer's Guide</a></li>

</ul>
</details>

**Discussion**: The comments show a range of opinions: some suggest using specific prompts to guide LLMs, others warn that LLMs produce wrong abstractions and over-comment, and one commenter advocates simply writing code manually to ensure maintainability.

**Tags**: `#software engineering`, `#code maintainability`, `#LLMs`, `#AI-assisted development`, `#code review`

---

<a id="item-4"></a>
## [Musk Reverses, Praises Anthropic, Pledges No Service Cut](https://x.com/i/status/2075278580955685036) ⭐️ 8.0/10

Elon Musk publicly admitted he was wrong about Anthropic, calling them a leader in AI and committing not to remove them from SpaceX servers despite competition. He revealed Anthropic signed a $40 billion contract through 2029 to use xAI's Colossus 1 data center, purchasing 300 megawatts of compute. This shift from Musk signals the intensifying AI infrastructure race, where even rivals become major customers. The $400B contract underscores the massive capital required for frontier AI training and the strategic importance of data center capacity. Anthropic is now one of SpaceX's largest customers as of July 2026. The contract covers the entire capacity of xAI's Colossus 1 data center in Memphis, Tennessee, with monthly payments of $1.25 billion starting May 2025.

telegram · zaihuapd · Jul 10, 02:02

**Background**: Colossus 1 is a hyperscale AI data center built by xAI, operational since July 2024, purpose-built for training large language models like Grok. Anthropic's latest model family, Mythos, with Fable 5 being its most capable widely released model, is focused on advanced reasoning and cybersecurity.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Colossus_(data_center)">Colossus (data center) - Wikipedia</a></li>
<li><a href="https://en.wikipedia.org/wiki/Claude_Mythos">Claude Mythos - Wikipedia</a></li>
<li><a href="https://techcrunch.com/2026/02/28/billion-dollar-infrastructure-deals-ai-boom-data-centers-openai-oracle-nvidia-microsoft-google-meta/">The billion-dollar infrastructure deals powering the AI boom</a></li>

</ul>
</details>

**Tags**: `#AI`, `#Anthropic`, `#Elon Musk`, `#SpaceX`, `#AI Infrastructure`

---

<a id="item-5"></a>
## [Anthropic Web Crawler Scrapes 2800 Pages Per Referral](https://www.businessinsider.com/anthropic-web-bots-crawling-referrals-cloudflare-distillation-2026-7) ⭐️ 8.0/10

Cloudflare data from July 1–7 shows Anthropic's web crawler scrapes about 2800 pages for every one referral visit to content sites, the highest ratio among major AI companies, though improved from early April's 8800:1 and a peak of 24700:1 in early May. This highlights the contentious issue of AI data collection practices, where companies scrape large amounts of web content without proportional traffic referral, raising ethical concerns about fair use and compensation for content creators. The ratio is calculated by comparing the number of pages crawled by Anthropic's bot against the number of referral visits sent to those sites from Anthropic's products. Anthropic has questioned Cloudflare's methodology, stating it cannot verify the calculations and that new search features are increasing referral traffic.

telegram · zaihuapd · Jul 10, 04:25

**Background**: Web scraping is the automated extraction of data from websites using bots. Referral traffic refers to visitors who arrive at a website by clicking a link from another site. AI companies often scrape public web data to train models, but content creators argue this without consent or compensation is unethical. Cloudflare's data provides transparency into these practices.

<details><summary>References</summary>
<ul>
<li><a href="https://economictimes.indiatimes.com/definition/referring-sites">What is Referring Sites? Definition of Referring Sites, Referring ...</a></li>
<li><a href="https://dataforest.ai/glossary/web-scraping-guide">Web Scraping & Crawling Guide... | Glossary by DATAFOREST</a></li>

</ul>
</details>

**Tags**: `#Anthropic`, `#web scraping`, `#AI ethics`, `#Cloudflare`, `#data collection`

---

<a id="item-6"></a>
## [OpenAI, Google Provide AI Models to Blacklisted Chinese Firms via Singapore](https://www.ft.com/content/5d6aafa1-5d47-4585-aa95-6ec06a6cd20f) ⭐️ 8.0/10

OpenAI and Google have been providing advanced AI services to Singapore-based subsidiaries of Alibaba, Baidu, and Tencent, despite these parent companies being included on the US Department of Defense's Section 1260H list of Chinese military companies. This revelation highlights potential loopholes in US export controls on AI models, as the transactions are currently legal under existing restrictions. It could reignite policy debates and lead to stricter regulations on frontier AI software exports. OpenAI suspended API access to an Alibaba-related user after detecting possible model distillation and reported the incident to US authorities. In contrast, Anthropic has a stricter policy that fully prohibits Chinese companies and their overseas entities from accessing its frontier AI models.

telegram · zaihuapd · Jul 10, 09:59

**Background**: Model distillation is a technique to compress a large teacher model into a smaller student model, often used to improve efficiency but could be misused to extract knowledge from restricted models. The Section 1260H list, established by the FY2021 National Defense Authorization Act, identifies Chinese companies that allegedly operate in China's defense industrial base. US export controls on AI aim to prevent adversaries from gaining advanced capabilities, but current rules only restrict direct exports to mainland China, not to overseas subsidiaries.

<details><summary>References</summary>
<ul>
<li><a href="https://www.dentons.com/en/insights/alerts/2026/june/18/dod-expands-section-1260h-chinese-military-companies-list">DoD Expands Section 1260 H “Chinese Military Companies” List</a></li>
<li><a href="https://developer.volcengine.com/articles/7501163741166174259">一文读懂到底什么是“ 模 型 蒸 馏 （ Model Distillation ...”</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#export controls`, `#OpenAI`, `#Google`, `#geopolitics`

---

<a id="item-7"></a>
## [Meta faces $12B EU fine over addictive design](https://www.theverge.com/policy/963872/meta-eu-addictive-design-200b-fine-risk-digital-services-act-dsa) ⭐️ 8.0/10

The European Commission preliminarily found that Meta's Facebook and Instagram violate the Digital Services Act due to addictive design features like infinite scroll and autoplay, and may impose a fine up to $12 billion. This could force Meta to redesign core user interfaces across Europe, setting a precedent for how social media platforms handle addictive design under the DSA. The fine would be up to 6% of Meta's global annual revenue. The EU demands default disabling of addictive features, effective screen time limits, and de-emphasis of engagement-driven algorithms.

telegram · zaihuapd · Jul 10, 14:47

**Background**: The Digital Services Act (DSA) is an EU regulation that imposes obligations on large online platforms to protect users from illegal content and systemic risks, including addictive design. Addictive UI patterns leverage psychological mechanisms to maximize engagement, often at the cost of user well-being. The EU has been increasingly scrutinizing such practices.

<details><summary>References</summary>
<ul>
<li><a href="https://digital-strategy.ec.europa.eu/en/policies/digital-services-act">The Digital Services Act | Shaping Europe’s digital future</a></li>
<li><a href="https://medium.com/from-pixels-to-algorithms/design-that-thinks-for-you-the-psychology-behind-addictive-ui-ux-3176b4a5dc4d">Design That Thinks for You: The Psychology Behind Addictive ...</a></li>

</ul>
</details>

**Tags**: `#Meta`, `#EU regulation`, `#Digital Services Act`, `#addictive design`, `#social media`

---