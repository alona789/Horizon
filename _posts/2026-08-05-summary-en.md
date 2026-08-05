---
layout: default
title: "Horizon Summary: 2026-08-05 (EN)"
date: 2026-08-05
lang: en
---

> From 38 items, 11 important content pieces were selected

---

1. [Waymo Expands Driverless Ride-Hailing to Dallas for All Users](#item-1) ⭐️ 8.0/10
2. [DeepSeek V4 Flash Runs on Single AMD MI300X with 256k Context](#item-2) ⭐️ 8.0/10
3. [FedEx&\#x27;s Legitimate Emails Undermine Phishing Detection, Troy Hunt Argues](#item-3) ⭐️ 8.0/10
4. [Oxide Computer Raises $445M in Series D for Rack-Scale Cloud Hardware](#item-4) ⭐️ 8.0/10
5. [Keyv and npm packages compromised in active Shai-Hulud supply chain attack](#item-5) ⭐️ 8.0/10
6. [Xbox outage blocks disc-based games, exposing online DRM dependence](#item-6) ⭐️ 8.0/10
7. [MiniMax-H3 Omni-Modal Model Ported to MLX for Apple Silicon](#item-7) ⭐️ 8.0/10
8. [Huawei Scientist Warns Nvidia Chip Scaling Hits Physical Limit](#item-8) ⭐️ 8.0/10
9. [Google Builds $200B Wall Street Financing Machine for Anthropic AI Chips](#item-9) ⭐️ 8.0/10
10. [China has issued its first mandatory national standard for L3/L4 autonomous driving.](#item-10) ⭐️ 8.0/10
11. [White House Reverses Open-Source AI Stance Amid Silicon Valley Rift](#item-11) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Waymo Expands Driverless Ride-Hailing to Dallas for All Users](https://waymo.com/blog/shorts/dallas-open-to-all/) ⭐️ 8.0/10

Waymo has announced that its driverless ride-hailing service is now open to everyone in Dallas, Texas. This marks the latest expansion of its autonomous vehicle operations into a new major metro area. This expansion brings fully driverless ride-hailing to millions of residents in a large, car-dependent metroplex. It signals Waymo&\#x27;s continued growth across the U.S. and could accelerate competition in the ride-hailing market. Dallas-Fort Worth is one of the largest and most sprawling metro areas in the U.S., with low density and limited public transit. The service is being offered to all customers rather than a waitlist or limited pilot, reflecting confidence in Waymo&\#x27;s technology.

hackernews · xnx · Aug 4, 18:29 · [Discussion](https://news.ycombinator.com/item?id=49172836)

**Background**: Waymo is a subsidiary of Alphabet that develops self-driving car technology and operates a robotaxi service in several U.S. cities. A &\#x27;driverless ride-hailing&\#x27; service means customers can hail a car through an app and ride without any human safety driver behind the wheel. Expanding to Dallas is significant because it requires adapting to local traffic patterns, weather, and road infrastructure.

**Discussion**: Commenters offered a mix of enthusiasm and critical perspectives. Some praised Waymo vehicles as safe and predictable road participants, while a commercial real estate professional argued driverless cars could serve as a highly effective affordable housing policy by reducing parking and transit costs. Others raised concerns about money leaking from the local economy, since profits may leave the region, though some noted local maintenance jobs are still needed.

**Tags**: `#autonomous vehicles`, `#Waymo`, `#ride-hailing`, `#urban mobility`, `#transportation`

---

<a id="item-2"></a>
## [DeepSeek V4 Flash Runs on Single AMD MI300X with 256k Context](https://github.com/ryanzhou/deepseek-v4-flash-mi300x) ⭐️ 8.0/10

A new guide and analysis demonstrates DeepSeek V4 Flash running on a single AMD MI300X at high throughput, while reducing the context length from 1M to 256k tokens. This shows large Mixture-of-Experts models can be served on a single GPU, making DeepSeek V4 Flash more accessible on AMD hardware and potentially lowering deployment costs for high-throughput use cases. The guide reports over 150 tokens per second throughput, but the context window is cut to 256k from the native 1M. The MI300X is an OAM module with 192GB HBM3, and DeepSeek V4 Flash&\#x27;s MoE exports are natively MXFP4 quantized, allowing it to fit in memory.

hackernews · zhoutong · Aug 4, 10:00 · [Discussion](https://news.ycombinator.com/item?id=49166386)

**Background**: DeepSeek V4 Flash is a Mixture-of-Experts \(MoE\) language model with 284B total parameters and 13B activated, supporting a 1M-token context. The AMD MI300X is a CDNA 3-based accelerator with 192GB of HBM3 memory and 5.3 TB/s bandwidth. MoE models activate only a subset of parameters per token, enabling fast inference on a single GPU.

<details><summary>References</summary>
<ul>
<li><a href="https://huggingface.co/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash · Hugging Face</a></li>
<li><a href="https://www.amd.com/en/products/accelerators/instinct/mi300/mi300x.html">AMD Instinct™ MI300X Accelerators</a></li>
<li><a href="https://deepinfra.com/deepseek-ai/DeepSeek-V4-Flash">deepseek-ai/DeepSeek-V4-Flash - Demo - DeepInfra</a></li>

</ul>
</details>

**Discussion**: Commenters generally praised the work and noted practical caveats: the MI300X is only sold as an OAM module \(e.g., an 8-GPU board costing ~250K EUR\), and the PCIe-based MI350P has only 144GB. One user pointed to prior work like DwarfStar that achieves similar results in less memory, while another called the 256k context reduction a very practical tradeoff, comparable to Codex.

**Tags**: `#deepseek`, `#AMD`, `#MI300X`, `#inference`, `#quantization`

---

<a id="item-3"></a>
## [FedEx&\#x27;s Legitimate Emails Undermine Phishing Detection, Troy Hunt Argues](https://www.troyhunt.com/thanks-fedex-this-is-why-we-keep-getting-phished/) ⭐️ 8.0/10

In a 2024 blog post, security researcher Troy Hunt criticized FedEx&\#x27;s legitimate email practices, arguing they train users to accept messages that look exactly like phishing. He highlights how official FedEx emails bypass spam filters yet contain the same red flags found in phishing attacks, undermining users&\#x27; ability to spot scams. This matters because phishing remains a leading attack vector, and when trusted brands send confusing, unexpected email, security awareness training and automated filters lose their value. It shows that email authentication alone cannot solve the human trust problem, and both companies and email providers need to rethink how legitimate mail is designed and delivered. The post centers on domain validation and phishing vectors: FedEx&\#x27;s messages can pass SPF, DKIM, and DMARC checks, yet still arrive with links, attachments, and delivery-notice language that mimic scams. The problem is structural—authentication protocols verify sender identity, not whether a message is malicious, so an authenticated FedEx email can still look identical to a phishing email.

hackernews · stymaar · Aug 4, 21:09 · [Discussion](https://news.ycombinator.com/item?id=49175192)

**Background**: Email authentication protocols like SPF, DKIM, and DMARC use DNS records and cryptographic signatures to prove which systems are allowed to send for a domain, helping receivers block spoofed mail. Phishing detection typically combines automated scanning of content and sender reputation with user vigilance, but it struggles when legitimate senders behave like phishers. This is why a well-authenticated email from a major brand can still confuse both filters and people.

<details><summary>References</summary>
<ul>
<li><a href="https://www.techtarget.com/searchsecurity/answer/Email-authentication-How-SPF-DKIM-and-DMARC-work-together">SPF , DKIM and DMARC : What are they and how do they... | TechTarget</a></li>
<li><a href="https://www.volanea.com/blog/email-authentication-protocols">Email Authentication Protocols : SPF , DKIM and DMARC Guide</a></li>
<li><a href="https://www.expressvpn.com/blog/phishing-detection/">How to detect phishing and prevent scams online</a></li>

</ul>
</details>

**Discussion**: Commenters shared similar real-world examples: one received a legitimate but suspicious FedEx customs notice from an individual employee with a PDF attachment, another found Google&\#x27;s official storage-warning email using the short domain c.gle, and one noted the IRS phone system sounds identical to scam call centers. Several commenters also blamed the proliferation of new generic top-level domains for making phishing links harder for non-experts to judge. Overall, the discussion strongly supported Hunt&\#x27;s argument and added further evidence that legitimate organizations contribute to the phishing problem.

**Tags**: `#security`, `#phishing`, `#email`, `#FedEx`, `#Troy Hunt`

---

<a id="item-4"></a>
## [Oxide Computer Raises $445M in Series D for Rack-Scale Cloud Hardware](https://www.sec.gov/Archives/edgar/data/1795071/000179507126000002/xslFormDX01/primary_doc.xml) ⭐️ 8.0/10

Oxide Computer Company raised $445 million in a Series D round, according to a recent SEC Form D filing. This follows a $200 million Series C round and marks a significant acceleration in funding for the company. This major funding round signals strong investor confidence in rack-scale cloud hardware as a viable on-premises alternative to hyperscale public clouds. It could accelerate Oxide&\#x27;s product delivery and influence how enterprises build private cloud infrastructure. The Series D round is recorded on SEC Form D, following a $200M Series C, a $100M Series B in 2025, and a $44M Series A in 2023. Community discussion raises practical concerns about sales follow-up and whether the company is shipping hardware at scale, despite a well-regarded technical team.

hackernews · depr · Aug 4, 20:13 · [Discussion](https://news.ycombinator.com/item?id=49174407)

**Background**: Oxide Computer Company is a hardware startup focused on rack-scale &\#x27;Cloud Computer&\#x27; systems that unify hardware and software for on-premises data centers, aiming to bring hyperscale cloud architecture in-house. The company unveiled its first commercial product in 2023 and has since attracted multiple funding rounds. Its approach treats the entire rack as a single computer, contrasted with traditional server designs.

<details><summary>References</summary>
<ul>
<li><a href="https://oxide.computer/blog/how-oxide-cuts-data-center-power-consumption-in-half">A rack - scale design that drives data center power efficiency.</a></li>
<li><a href="https://oxide.computer/blog/oxide-unveils-the-worlds-first-commercial-cloud-computer">Oxide Unveils the World&#x27;s First Commercial Cloud Computer</a></li>
<li><a href="https://www.bloomberg.com/profile/company/1776316D:US">Oxide Computer Co - Company Profile and News - Bloomberg Markets</a></li>

</ul>
</details>

**Discussion**: The Hacker News discussion is largely positive about the product concept and the team, with users praising the technical vision and expressing excitement for future episodes of &\#x27;Oxide and Friends.&\#x27; However, some practical concerns emerged: one VP of Engineering said they submitted a sales inquiry and never received a response despite spending $900k/year on AWS, and another commenter questioned whether the company actually ships hardware, citing a lack of public images and deployment stories.

**Tags**: `#funding`, `#hardware`, `#startup`, `#oxide`, `#cloud`

---

<a id="item-5"></a>
## [Keyv and npm packages compromised in active Shai-Hulud supply chain attack](https://www.aikido.dev/blog/keyv-and-friends-compromised-in-npm-supply-chain-attack) ⭐️ 8.0/10

A new wave of the Shai-Hulud worm has compromised Keyv and associated npm packages, including cacheable, and is actively spreading through the npm ecosystem. The worm harvests credentials, publishes itself to every writable npm package, and plants execution hooks in GitHub repositories. Keyv is a widely used key-value storage library with over 1,700 dependent projects, so its compromise can have cascading effects across the JavaScript ecosystem. This attack underscores the systemic risk of supply-chain attacks on open-source dependencies and the urgent need for better security practices. The campaign targets npm packages and has affected more than 400 packages, according to JFrog security research. The worm&\#x27;s capabilities include credential harvesting, self-publication to writable npm packages, and planting of execution hooks in GitHub repositories, making it highly persistent.

hackernews · cimi\_ · Aug 4, 11:01 · [Discussion](https://news.ycombinator.com/item?id=49166874)

**Background**: npm is the largest package registry for JavaScript, with millions of packages and billions of downloads. Shai-Hulud is a self-replicating worm that compromises packages by stealing maintainer credentials and using them to publish malicious versions; it can automatically spread to other writable packages, leading to widespread compromise across the ecosystem.

<details><summary>References</summary>
<ul>
<li><a href="https://research.jfrog.com/post/shai-hulud-is-back-august/">Major Shai Hulud campaign strikes npm again, affecting keyv and 400+ packages - JFrog Security Research</a></li>
<li><a href="https://www.cisa.gov/news-events/alerts/2025/09/23/widespread-supply-chain-compromise-impacting-npm-ecosystem">Widespread Supply Chain Compromise Impacting npm Ecosystem | CISA</a></li>
<li><a href="https://unit42.paloaltonetworks.com/npm-supply-chain-attack/">&quot;Shai-Hulud&quot; Worm Compromises npm Ecosystem in Supply Chain Attack (Updated November 26)</a></li>

</ul>
</details>

**Discussion**: Community sentiment is concerned but proactive, with users sharing mitigation strategies such as using devcontainers to isolate development environments, killing pre-install/post-install hooks for new packages, and using tools like Packj to scan for indicators of compromise. Some also criticized the fragile dependency system and suggested that GitHub could detect and block Shai-Hulud exfiltration repositories.

**Tags**: `#security`, `#npm`, `#supply-chain`, `#open-source`, `#malware`

---

<a id="item-6"></a>
## [Xbox outage blocks disc-based games, exposing online DRM dependence](https://birchtree.me/blog/xbox-goes-down-you-cant-play-games-you-own-on-disc/) ⭐️ 8.0/10

During a recent Xbox network outage, users found they could not play even games they owned on physical discs, because the console requires online authentication before launching them. The incident made visible the always-online DRM that now governs Xbox game ownership. The event demonstrates that physical media no longer guarantees offline access, since &\#x27;owning&\#x27; a disc still depends on Microsoft&\#x27;s servers remaining available. It intensifies the broader industry debate over digital ownership and whether consumers will be able to play their purchased games decades from now. Always-on DRM can fail during server outages even when the content itself is stored locally on the disc. The outage also highlighted that physical discs often function as license keys rather than complete game data, with many titles requiring large downloads before play.

hackernews · surprisetalk · Aug 4, 12:01 · [Discussion](https://news.ycombinator.com/item?id=49167448)

**Background**: Always-on DRM \(or always-online DRM\) is a form of digital rights management that requires a consumer to stay connected to a server to use a product, usually to prevent piracy. It has been controversial because it can inconvenience legitimate buyers and creates a single point of failure when servers go down. In recent years, physical game discs have increasingly been treated as license keys rather than carriers of complete game data, meaning even &\#x27;offline&\#x27; ownership can depend on online authentication.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Always-on_DRM">Always-on DRM</a></li>
<li><a href="https://cardozoaelj.com/2021/09/27/always-online-drm-and-video-games/">Always Online DRM and Video Games - Cardozo AELJ</a></li>
<li><a href="https://houstonianonline.com/its-time-to-say-goodbye-to-physical-games-vertical/">It&#x27;s time to say goodbye to physical games | vertical</a></li>

</ul>
</details>

**Discussion**: Commenters largely expressed frustration and resignation, comparing today&\#x27;s online-dependent gaming with older consoles that could run discs offline and host multiplayer games locally. Some argued the core issue is not physical versus digital media but ownership rights such as permanent access, offline play, resale, and passing games on. One user recounted being forced into an account creation flow just to launch a Steam copy of Halo&\#x27;s Master Chief Collection.

**Tags**: `#DRM`, `#gaming`, `#digital-ownership`, `#Xbox`, `#outage`

---

<a id="item-7"></a>
## [MiniMax-H3 Omni-Modal Model Ported to MLX for Apple Silicon](https://simonwillison.net/2026/Aug/4/minimax-h3-mlx/#atom-everything) ⭐️ 8.0/10

MiniMax released MiniMax-H3, a general-purpose omni-modal generative system that accepts text, images, audio, and video to generate up to 15-second video clips with audio. Two days later, the Python package PipeNetwork/minimax-h3-mlx ported the model to MLX, allowing it to run locally on Apple Silicon; Simon Willison demonstrated it on an M5 Max MacBook Pro. This port makes a cutting-edge omni-modal video generation model accessible to individual developers and creators on local Apple hardware, reducing reliance on cloud APIs. It also highlights the MLX ecosystem&\#x27;s momentum, with new models being adapted for Apple Silicon within days of release. Running the model required downloading roughly 115 GB of model files, and generating one video took just under 45 minutes on Simon Willison&\#x27;s machine. The initial output&\#x27;s audio was &\#x27;weird speech-like garbage&\#x27; because no audio prompt guidance was provided, and MiniMax&\#x27;s prompting guide contains instructions for better results.

rss · Simon Willison · Aug 4, 19:10

**Background**: MLX is an array framework from Apple&\#x27;s machine learning research team, designed for efficient and flexible ML research on Apple Silicon. Omni-modal AI systems can understand and generate multiple data types—text, images, audio, and video—in a unified way. MiniMax-H3 is an open-weights general-purpose multimodal model that can combine these modalities to generate 2K video with native stereo audio, and this MLX port makes such generation possible entirely on-device.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ml-explore/mlx">GitHub - ml-explore/mlx: MLX: An array framework for Apple silicon · GitHub</a></li>
<li><a href="https://www.minimax.io/blog/minimax-h3">MiniMax H3: An Open Model Breaking the Boundaries Between Tasks and Modalities - MiniMax Research | MiniMax</a></li>
<li><a href="https://huggingface.co/MiniMaxAI/MiniMax-H3">MiniMaxAI/MiniMax-H3 · Hugging Face</a></li>

</ul>
</details>

**Tags**: `#AI`, `#MLX`, `#video generation`, `#multimodal`, `#Apple Silicon`

---

<a id="item-8"></a>
## [Huawei Scientist Warns Nvidia Chip Scaling Hits Physical Limit](https://www.bloomberg.com/news/articles/2026-08-04/huawei-s-top-scientist-warns-of-chip-limit-nvidia-will-soon-face) ⭐️ 8.0/10

In late July, Huawei&\#x27;s chief semiconductor scientist Liao Heng gave a rare four-hour public interview warning that Nvidia&\#x27;s approach of adding more compute chips and high-bandwidth memory will eventually hit a physical limit. He also introduced Huawei&\#x27;s LogicFolding framework as an alternative path, with the first phone chip using this framework expected later this year. This warning highlights a growing industry split into two separate semiconductor ecosystems and challenges the dominant scaling approach. As Huawei pushes an alternative architecture to bypass physical limits and U.S. sanctions, the competitive landscape for AI hardware could shift significantly. LogicFolding physically folds and stacks logic circuits into a dual-layer framework, reducing wiring length, load, and propagation delay. Huawei&\#x27;s Tao \(τ\) Scaling Law replaces geometric scaling with temporal scaling that prioritizes signal speed over component size, potentially achieving 55% higher transistor density without EUV lithography.

telegram · zaihuapd · Aug 4, 08:04

**Background**: Moore&\#x27;s Law predicts that transistor density doubles roughly every two years, but geometric shrinking is approaching fundamental physical limits. U.S. sanctions restrict Huawei&\#x27;s access to advanced EUV lithography equipment, so LogicFolding offers a way to increase density and performance without relying on cutting-edge fabrication tools. The Tao \(τ\) Scaling Law is a temporal scaling framework that optimizes how fast data moves across a system rather than how small the components are.

<details><summary>References</summary>
<ul>
<li><a href="https://www.tomshardware.com/tech-industry/semiconductors/huawei-claims-sanctions-busting-breakthrough-with-1-4nm-class-chips-by-2031-claims-55-percent-higher-transistor-density-firm-claims-new-logicfolding-chip-architecture-can-bypass-euv-restrictions-introduces-tau-scaling-law-to-replace-moores-law">Huawei claims sanctions-busting breakthrough with 1.4nm-class chips by 2031, claims 55% higher transistor density — firm claims new LogicFolding chip architecture can bypass EUV restrictions, introduces &#x27;Tau Scaling Law&#x27; to replace Moore&#x27;s Law | Tom&#x27;s Hardware</a></li>
<li><a href="https://www.huaweicentral.com/huawei-logicfolding-architecture-everything-you-need-to-know/">Huawei LogicFolding Architecture: Everything you need to know - Huawei Central</a></li>
<li><a href="https://www.chosun.com/english/industry-en/2026/05/26/Z4I566GOLJAPNOE53763RN7V2E/">Huawei&#x27;s &#x27;Tao Law&#x27; Challenges TSMC, Samsung in Semiconductor Race</a></li>

</ul>
</details>

**Tags**: `#semiconductors`, `#AI chips`, `#Huawei`, `#Nvidia`, `#hardware limits`

---

<a id="item-9"></a>
## [Google Builds $200B Wall Street Financing Machine for Anthropic AI Chips](https://www.ft.com/content/549f2e23-5aa2-49c7-9ea6-a9784ab7087c) ⭐️ 8.0/10

The Financial Times reports that Google has secretly constructed one of the largest infrastructure financing structures ever, worth about $200 billion, to deliver over $150 billion in AI chips to Anthropic. The first transactions closed in June via a special purpose vehicle called Compute SPV, which bought roughly $35 billion in hardware, about one million TPUs and one gigawatt of compute. This unprecedented financing structure lets Anthropic—which has no credit rating—access massive AI compute without putting hundreds of billions of dollars of hardware on its own balance sheet. It also creates a novel risk-sharing model for AI infrastructure involving Google, Broadcom, Apollo, Blackstone, and Morgan Stanley, with implications for how hyperscale AI is funded across the industry. Roughly 80% of the ~$200 billion in contracts is directly tied to chips, with Broadcom buying and helping finance the chips, while Apollo and Blackstone purchase hardware and lease it back to Anthropic. The structure resembles manufacturer financing used by Boeing and GE, and crypto miners are also among the participants sharing risk.

telegram · zaihuapd · Aug 4, 10:52

**Background**: A special purpose vehicle \(SPV\) is a legal shell used to fund huge capital expenditures without consolidating the debt on a sponsor&\#x27;s balance sheet. Google&\#x27;s TPU \(Tensor Processing Unit\) is a custom ASIC designed specifically to accelerate machine-learning workloads, and the Compute SPV&\#x27;s purchases included about one million TPUs representing roughly one gigawatt of compute.

<details><summary>References</summary>
<ul>
<li><a href="https://rondodson.substack.com/p/the-new-shadow-system-ai-finance">The New Shadow System: AI Finance and the SPV</a></li>
<li><a href="https://magdigit.com/ironwood-the-first-google-tpu-for-the-age-of-inference/">Ironwood: The first Google TPU for the age of inference - MagDIGIT</a></li>
<li><a href="https://www.financely-group.com/ai-data-center-finance-sale-leasebacks">AI Data-Center Finance &amp; Sale - Leasebacks</a></li>

</ul>
</details>

**Tags**: `#AI infrastructure`, `#Google`, `#Anthropic`, `#finance`, `#AI chips`

---

<a id="item-10"></a>
## [China has issued its first mandatory national standard for L3/L4 autonomous driving.](https://wap.miit.gov.cn/jgsj/zbys/qcgy/art/2026/art_a1d2072374884287b67048a77560014e.html) ⭐️ 8.0/10

China&\#x27;s Ministry of Industry and Information Technology \(MIIT\) released the mandatory national standard GB 44721-2026, &\#x27;Safety Requirements for Autonomous Driving Systems of Intelligent Connected Vehicles,&\#x27; the country&\#x27;s first mandatory standard for L3 and L4 autonomous driving. It will take effect on July 1, 2027, upgrading the 2024 recommended standard to a binding requirement. This marks a major regulatory milestone: autonomous driving in China shifts from voluntary guidance to mandatory safety requirements, affecting automakers, suppliers, and operators of L3/L4 vehicles. It provides a legal and technical foundation for broader deployment of higher-level autonomous driving on public roads and helps define the safety bar for the industry. The standard applies to M-class \(passenger\) and N-class \(cargo\) vehicles equipped with L3 or L4 systems, and excludes automated parking systems. It builds a safety requirement system around four dimensions: full-lifecycle safety assurance, dynamic driving capability, human-machine interaction and user notification, and multi-dimensional inspection and testing. For L3 systems, it also requires driver takeover capability monitoring.

telegram · zaihuapd · Aug 4, 13:06

**Background**: The standard uses the SAE driving automation levels: L0-L2 are driver assistance, while L3 is conditionally automated driving where the system handles driving under specific conditions but the driver must be ready to take over; L4 is highly automated driving that can operate without driver intervention within an operational design domain. Previously, China issued a recommended \(non-binding\) national standard in 2024; making it mandatory signals policy support for commercializing L3/L4 vehicles. The MIIT announcement states that autonomous driving systems must be at least as safe as a competent and attentive human driver.

<details><summary>References</summary>
<ul>
<li><a href="https://www.autohome.com.cn/news/202608/1316205.html">autohome.com.cn/news/202608/1316205.html</a></li>
<li><a href="https://m.21jingji.com/article/20260804/herald/2ce85d00b1498fe646e9b8d576be5564.html">《智能网联汽车 自 动 驾 驶 系 统 安 全 要 求 》强制性国家标准正式发布 - 21...</a></li>
<li><a href="https://www.tmtpost.com/6496374.html">自 动 驾 驶 ，是忽悠吗？ -钛媒体官方网站</a></li>

</ul>
</details>

**Tags**: `#autonomous-driving`, `#national-standard`, `#regulation`, `#smart-vehicles`, `#L3-L4`

---

<a id="item-11"></a>
## [White House Reverses Open-Source AI Stance Amid Silicon Valley Rift](https://www.nytimes.com/2026/08/04/technology/ai-washington-regulation-whiplash.html) ⭐️ 8.0/10

The White House abruptly reversed its position on regulating open-source AI models, abandoning plans for sanctions and trade blacklists after internal debates and Silicon Valley pushback. On August 4, 2026, it invited tech companies to discuss a new framework focused on competitiveness and pre-release cybersecurity reviews. This policy reversal reshapes the U.S. government&\#x27;s approach to AI regulation, affecting both national security and the global competitiveness of American AI firms. It marks a significant victory for advocates of open-source AI like Nvidia and Meta over OpenAI and Anthropic, which had pushed for restrictions on Chinese rivals. The trigger was the Chinese open-source model Kimi, whose performance rivaled OpenAI&\#x27;s top models. White House chief of staff Susie Wiles and Treasury Secretary Scott Bessent had considered sanctions, while Nvidia CEO Jensen Huang posted on X for the first time in defense of open source and formed a safety coalition with over 230 members.

telegram · zaihuapd · Aug 4, 15:22

**Background**: Open-source AI refers to models whose weights are publicly released, allowing anyone to run, modify, and build on them, which has made them a strategic technology. Kimi is a family of large language models developed by Chinese company Moonshot AI, known for long-context support and competitive performance. The White House debate reflects a broader global struggle over whether to restrict Chinese open-source models for national security or embrace open ecosystems to accelerate innovation.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Kimi_%28chatbot%29">Kimi (chatbot) - Wikipedia</a></li>
<li><a href="https://www.linkedin.com/pulse/open-source-ai-has-become-worlds-most-strategic-heres-luke-lovell-0bcte">Open source AI has become the world&#x27;s most strategic technology.</a></li>
<li><a href="https://huggingface.co/blog/daya-shankar/open-source-llms">Best Open - Source LLM Models in 2026: Coding, Local, Agentic AI ...</a></li>

</ul>
</details>

**Tags**: `#AI regulation`, `#open source`, `#geopolitics`, `#policy`, `#Silicon Valley`

---