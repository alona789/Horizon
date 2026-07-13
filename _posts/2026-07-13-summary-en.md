---
layout: default
title: "Horizon Summary: 2026-07-13 (EN)"
date: 2026-07-13
lang: en
---

> From 17 items, 5 important content pieces were selected

---

1. [Climate.gov data rescued by open data efforts](#item-1) ⭐️ 8.0/10
2. [LAPD ends Flock contract over privacy concerns](#item-2) ⭐️ 8.0/10
3. [LLM Agents Should Not Be Directly Responsible Individuals](#item-3) ⭐️ 8.0/10
4. [Chain-of-Thought as a Scaling Trap: Latent Reasoning Emerges](#item-4) ⭐️ 8.0/10
5. [GPUHedge cuts serverless GPU cold start p95 latency by 74%](#item-5) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Climate.gov data rescued by open data efforts](https://werd.io/climate-gov-was-destroyed-open-data-saved-it/) ⭐️ 8.0/10

A blog post details how open data initiatives preserved climate.gov data after the site was destroyed, ensuring public access to taxpayer-funded climate information. This event highlights the vulnerability of government data and the critical role of open data communities in preserving scientific information, especially for climate research and policy decisions. The recovery relied on donations from individuals and organizations, raising questions about sustainable funding for ongoing data collection and analysis beyond historical preservation.

hackernews · benwerd · Jul 13, 19:57 · [Discussion](https://news.ycombinator.com/item?id=48897945)

**Background**: Climate.gov is a U.S. government website providing climate data and information. Open data refers to the practice of making data freely available for anyone to access, use, and share. This incident underscores concerns about government data integrity and the need for independent backups.

**Discussion**: Commenters expressed gratitude for the data rescue but questioned long-term relevance and funding, with some arguing that reliance on donations is unsustainable. Others debated trust in government entities for data collection and regulation.

**Tags**: `#open data`, `#climate science`, `#data preservation`, `#government`, `#hackernews`

---

<a id="item-2"></a>
## [LAPD ends Flock contract over privacy concerns](https://techcrunch.com/2026/07/13/lapd-lets-contract-with-surveillance-giant-flock-expire-citing-serious-concerns-over-civil-liberties-and-privacy/) ⭐️ 8.0/10

The Los Angeles Police Department (LAPD) let its contract with surveillance company Flock Safety expire, citing serious concerns over civil liberties and privacy. However, Flock's cameras remain installed and continue to record data that can be sold to other law enforcement agencies. This decision marks a significant step for police accountability, but the persistence of Flock's surveillance network reveals a critical loophole: data collection and resale continue without direct oversight. It underscores the need for stricter regulations on government data purchasing. Flock owns the cameras and poles, so the infrastructure remains operational even after the contract ends, allowing data to be sold to entities like CHP, LASD, FBI, and Palantir. This design makes the exit largely symbolic, as LAPD can still access the data through other means.

hackernews · forks · Jul 13, 15:11 · [Discussion](https://news.ycombinator.com/item?id=48893947)

**Background**: Flock Safety is a manufacturer of automated license plate recognition (ALPR) systems and other surveillance hardware. They sell cloud-connected cameras to police departments and private customers, aggregating license plate readings into a searchable database. Critics argue that this creates a persistent, nationwide surveillance network that undermines privacy and civil liberties.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Flock_Safety">Flock Safety - Wikipedia</a></li>
<li><a href="https://www.flocksafety.com/">Flock Safety</a></li>
<li><a href="https://www.aclu.org/news/privacy-technology/flock-roundup">Flock’s Aggressive Expansions Go Far Beyond Simple Driver Surveillance | American Civil Liberties Union</a></li>

</ul>
</details>

**Discussion**: Community comments express skepticism, noting that Flock's infrastructure is designed to be resilient to political pressure and that data continues to be harvested. Some users question the effectiveness of ALPR in high-crime areas, while others highlight the loophole that government purchasing of data circumvents legal restrictions.

**Tags**: `#privacy`, `#surveillance`, `#law enforcement`, `#data ethics`, `#tech policy`

---

<a id="item-3"></a>
## [LLM Agents Should Not Be Directly Responsible Individuals](https://simonwillison.net/2026/Jul/12/directly-responsible-individuals/#atom-everything) ⭐️ 8.0/10

Simon Willison argues that LLM-powered agents should never be designated as Directly Responsible Individuals (DRIs) because they lack the capacity for human accountability. This argument is significant for software engineering ethics and AI governance, as it challenges the trend of assigning autonomous AI agents decision-making responsibility without human oversight. Willison references the GitLab handbook definition of DRI as the person ultimately accountable for a project's success or failure, and cites an IBM 1979 training slide stating that a computer can never be held accountable and must never make a management decision.

rss · Simon Willison · Jul 12, 23:57

**Background**: The term Directly Responsible Individual (DRI) originated at Apple and is used in organizations like GitLab to designate a single person who is accountable for an initiative. The concept emphasizes human accountability in decision-making. Willison extends this to AI agents, arguing that since machines cannot be held morally or legally accountable, they should not be given DRI status.

<details><summary>References</summary>
<ul>
<li><a href="https://handbook.gitlab.com/handbook/people-group/directly-responsible-individuals/">Directly Responsible Individuals (DRI) | The GitLab Handbook</a></li>
<li><a href="https://simonwillison.net/2026/Jul/12/directly-responsible-individuals/">Directly Responsible Individuals (DRI) | Simon Willison’s Weblog</a></li>

</ul>
</details>

**Tags**: `#management`, `#accountability`, `#AI agents`, `#ethics`, `#software development`

---

<a id="item-4"></a>
## [Chain-of-Thought as a Scaling Trap: Latent Reasoning Emerges](https://www.reddit.com/r/MachineLearning/comments/1uviru5/chain_of_thought_is_a_scaling_trap_the_next_wave/) ⭐️ 8.0/10

A Reddit analysis argues that chain-of-thought reasoning is a scaling trap due to faithfulness and cost issues, and highlights latent reasoning approaches such as Coconut (continuous latent thought), HRM (Hierarchical Reasoning Model), and RecursiveMAS as promising alternatives that avoid serializing intermediate steps into tokens. This shift from explicit token-level reasoning to latent computation could significantly reduce latency and cost in LLM inference, while also enabling deeper reasoning; however, it introduces a 'black box wall' where interpretability is reduced, necessitating new governance layers. The post identifies two practical problems with CoT: faithfulness (traces may not reflect actual computation) and systems cost (serializing reasoning into tokens inflates latency and context usage). It proposes latent recursion as an alternative, where reasoning happens in hidden states, with language output only at the end.

reddit · r/MachineLearning · /u/meowsterpieces · Jul 13, 17:50

**Background**: Chain-of-thought reasoning improves LLM performance on complex tasks by generating intermediate steps in natural language. However, this approach forces the model to 'think out loud' in tokens, which can be inefficient and unfaithful. Latent reasoning methods like Coconut use the last hidden state as a continuous thought, fed back as input without decoding to text, potentially enabling more efficient and deeper reasoning.

<details><summary>References</summary>
<ul>
<li><a href="https://arxiv.org/abs/2412.06769">[2412.06769] Training Large Language Models to Reason in a Continuous Latent Space</a></li>
<li><a href="https://arxiv.org/abs/2506.21734">[2506.21734] Hierarchical Reasoning Model</a></li>
<li><a href="https://arxiv.org/abs/2604.25917">[2604.25917] Recursive Multi-Agent Systems</a></li>

</ul>
</details>

**Tags**: `#LLM reasoning`, `#chain-of-thought`, `#latent reasoning`, `#AI research`

---

<a id="item-5"></a>
## [GPUHedge cuts serverless GPU cold start p95 latency by 74%](https://www.reddit.com/r/MachineLearning/comments/1uvlb6h/gpuhedge_hedging_serverless_gpu_providers/) ⭐️ 8.0/10

GPUHedge is an open-source tool that mitigates cold start latency in serverless GPU providers by hedging requests across multiple providers using speculative execution, reducing p95 latency from 116.6 seconds to 29.4 seconds. This significant latency reduction (74%) improves the user experience for AI inference workloads on serverless GPUs, making serverless GPU computing more practical and cost-effective for applications that require low latency. In benchmarks, GPUHedge used a fixed RunPod to Cerebrium hedge launched after 10 seconds, achieving 0 out of 36 requests over 60 seconds and reducing average active-compute cost from $0.0114 to $0.0083 per request.

reddit · r/MachineLearning · /u/Putrid_Construction3 · Jul 13, 19:20

**Background**: Serverless GPU providers allow users to run AI models without managing infrastructure, but they suffer from cold start latency when GPU instances are freshly allocated, which can take over a minute. Hedging is a technique that sends multiple redundant requests to different providers and uses the first successful response, canceling the others.

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Serverless_computing">Serverless computing - Wikipedia</a></li>
<li><a href="https://www.usenix.org/legacy/event/nsdi09/tech/full_papers/wester/wester_html/">Tolerating latency in replicated state machines through client...</a></li>

</ul>
</details>

**Tags**: `#serverless`, `#GPU`, `#cold start`, `#hedging`, `#latency`

---