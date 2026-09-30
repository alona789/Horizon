---
layout: default
title: "Horizon Summary: 2026-09-30 (EN)"
date: 2026-09-30
lang: en
---

> From 41 items, 4 important content pieces were selected

---

1. [OpenAI launches GPT-6.1 Sol: near-Astra intelligence at one-fifth the price](#item-1) ⭐️ 8.0/10
2. [PS5 Relapse Exploit Jailbreaks Firmware 7.00–13.60](#item-2) ⭐️ 8.0/10
3. [Privacy Analysis of Web and Mobile Conversational AI Agents](#item-3) ⭐️ 8.0/10
4. [Anthropic: Z.ai&\#x27;s GLM-5.3 Can Autonomously Launch Cyberattacks](#item-4) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [OpenAI launches GPT-6.1 Sol: near-Astra intelligence at one-fifth the price](https://openai.com/index/introducing-gpt-6-1-sol/) ⭐️ 8.0/10

OpenAI released GPT-6.1 Sol, a point upgrade to GPT-6 Sol that the company says approaches GPT-6 Astra on agentic coding, computer use, and professional tasks while costing only one-fifth of Astra&\#x27;s standard price. It matches GPT-6 Sol&\#x27;s $2/$10 per million input/output token pricing but raises the cached-input discount from 90% to 95%, bringing cached input to $0.10 per million tokens, and is accessible via the API as gpt-6.1-sol as well as through ChatGPT paid tiers and Amazon Bedrock. The release signals that price-performance, not raw capability, has become the primary competitive battleground among frontier labs, putting pressure on rivals such as Anthropic as well as on OpenAI&\#x27;s own cheaper alternatives. For developers running agentic and coding workloads where cached context dominates token spend, a 50% cut in cache pricing translates directly into lower operating costs. According to Artificial Analysis, GPT-6.1 Sol scores just one point below GPT-6 Astra on its Intelligence Index at less than a quarter of Astra&\#x27;s cost per task, and OpenAI says the model makes fewer factual errors and respects explicit restrictions and user intent more reliably than GPT-6 Sol. The model arrives only about a week after GPT-6 Sol, and some coverage notes it is not yet available in every ChatGPT surface, with the API remaining the primary developer path.

hackernews · crorella · Sep 29, 17:06 · [Discussion](https://news.ycombinator.com/item?id=49896586)

**Background**: OpenAI&\#x27;s GPT-6 family is tiered, with Astra as the flagship frontier model and Sol as a cheaper, lower-capability variant; the naming echoes the earlier GPT-5.6 line, which shipped in Luna, Terra, and Sol variants. GPT-6 Astra has been positioned as state of the art in coding, math, and computer/browser navigation, but at a price that is prohibitive for high-volume agentic use. A point release like GPT-6.1 Sol is OpenAI&\#x27;s way of closing much of the gap to the flagship while keeping costs low enough for everyday developer workloads.

<details><summary>References</summary>
<ul>
<li><a href="https://openai.com/index/introducing-gpt-6-1-sol/">Introducing GPT - 6 . 1 Sol | OpenAI</a></li>
<li><a href="https://artificialanalysis.ai/articles/gpt-6-1-sol-replaces-gpt-6-sol-after-just-7-days-with-near-astra-intelligence">GPT-6.1 Sol replaces GPT-6 Sol after just 7 days, with near-Astra ...</a></li>
<li><a href="https://openrouter.ai/openai/gpt-6.1-sol">GPT - 6 . 1 Sol - API Pricing &amp; Providers | OpenRouter</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters were largely skeptical: several reported that GPT-6 Sol was a regression from Sol 5.6 and said they had switched to Anthropic&\#x27;s Opus 5.5, doubting that a one-week-later point release would change much. One top comment argued the real headline is the 95% cached-input discount, since cheaper cache yields far more mileage on coding agents, while others questioned whether $200/month tiers are justifiable when DeepSeek is far cheaper with negligible perceived intelligence differences; one commenter framed the shift to token-price competition as ominous for the industry and investors.

**Tags**: `#OpenAI`, `#GPT-6.1`, `#LLM`, `#AI pricing`, `#model release`

---

<a id="item-2"></a>
## [PS5 Relapse Exploit Jailbreaks Firmware 7.00–13.60](https://github.com/ntfargo/Relapse-Exploit) ⭐️ 8.0/10

A public exploit chain called &quot;Relapse&quot; has been released for PlayStation 5 consoles running firmware versions 7.00 through 13.60, chaining a WebKit JavaScriptCore browser vulnerability with a kernel exploit to reach a jailbreak environment. The repository, published by ntfargo, performs a browser-stage attack using JSC info leaks and a structured clone object pool mismatch to corrupt a typed array, then escalates with an address leak and an aio\_multi\_wait use-after-free race to establish kernel read/write and load ELF payloads. This is a broad jailbreak affecting a wide firmware range, meaning many retail PS5 and PS5 Pro units still on store shelves may be vulnerable, which opens the door to homebrew apps, game backups, and other capabilities Sony does not officially allow. It arrives amid growing debate over digital game ownership, giving users a practical \(if unofficial and potentially illegal\) way around restrictions such as the inability to back up saves to USB. The exploit supports firmware 7.00 through 13.60, but consoles updated on September 16 are reportedly not compatible, so not every PS5 owner can use it. It provides an ELF loader, letting users run homebrew payloads once the jailbreak is achieved, and community members speculate Sony may respond by disabling JIT in WebKit to shrink its attack surface.

hackernews · therepanic · Sep 29, 15:44 · [Discussion](https://news.ycombinator.com/item?id=49895304)

**Background**: WebKit is the browser engine used by Safari and many embedded browser views, and JavaScriptCore \(JSC\) is its JavaScript engine, which can be targeted by memory-corruption bugs to achieve code execution inside the browser sandbox. A jailbreak typically chains two or more exploits: a userland or browser-stage bug to escape the sandbox, and a kernel-stage bug to gain full control of the operating system. The PS5 runs a heavily locked-down, Sony-controlled system that blocks unapproved software and, unlike earlier PlayStation consoles, restricts backing up game saves to external media.

<details><summary>References</summary>
<ul>
<li><a href="https://github.com/ntfargo/Relapse-Exploit">GitHub - ntfargo/ Relapse - Exploit : Exploit chain for PS 5 7.00 - 13.60</a></li>
<li><a href="https://www.superpsx.com/ps5-relapse-jailbreak-13-60-and-lower-complete-guide/">PS 5 Relapse Jailbreak 13.60 and Lower – Complete Guide</a></li>
<li><a href="https://decrypt.co/379583/sony-ps5-jailbreak-digital-games-ownership">Someone Finally Jailbroke the PS5—Just After Sony Said Players Don’t Own Their Games - Decrypt</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters focused on practical use, with one asking whether they can finally back up game saves to USB after losing a year of Minecraft progress to data corruption, highlighting frustration over PS Plus cloud-only backups. Others speculated that veteran console-hacking groups likely hold additional zero-days for bootloader-level escapes, and one suggested Sony might disable JSC&\#x27;s JIT to reduce the attack surface; some wished the release had waited until GTA 6, while another hoped it would enable running Steam PC games on PS5.

**Tags**: `#PS5`, `#exploit`, `#security`, `#WebKit`, `#jailbreak`

---

<a id="item-3"></a>
## [Privacy Analysis of Web and Mobile Conversational AI Agents](https://jorgegarciaherrero.com/wp-content/interactivos/20260916-Prompt-like-a-butterfly-sting-like-a-tracker-%28clean%29.pdf) ⭐️ 8.0/10

A new research paper titled &quot;A Privacy Analysis of Web and Mobile Conversational AI Agents&quot; \(published at jorgegarciaherrero.com\) systematically examines the privacy risks of conversational AI agents across web and mobile platforms, focusing on prompt leakage, pre-submission data exfiltration, and weak URL-based access controls. The paper, summarized on Hacker News under the phrase &quot;Prompt like a butterfly, sting like a tracker,&quot; reached 408 points and 130 comments. The findings suggest that everyday interactions with mainstream AI chat assistants—typing a draft, pasting a document, or sharing a session link—can leak sensitive content to analytics or tracking infrastructure before the user ever hits send. With LLM assistants now embedded in browsers, phones, and enterprise workflows, this raises direct questions for both end users and teams evaluating the privacy posture of commercial AI products versus locally run open models. Commenters highlighted concrete technical vectors: ChatGPT&\#x27;s web client reportedly sends unfinished prompts to a \`conversation/prepare\` endpoint before submission, potentially to pre-warm caches but also exposing writing cadence and evolving ideas, while Perplexity exposes full conversations to anyone holding a session URL because it treats a UUID in the URL as a privacy guarantee. These are classic examples of broken access control and insecure direct object reference \(IDOR\) patterns, and the paper also compares how much risk stems from the agent itself versus the surrounding platform APIs and permissions.

hackernews · damaru2 · Sep 29, 09:03 · [Discussion](https://news.ycombinator.com/item?id=49890226)

**Background**: Conversational AI agents are chat-based assistants \(such as ChatGPT, Perplexity, or Gemini\) that maintain a session with the user and often run in a browser or mobile app with access to platform permissions. &quot;Prompt leakage&quot; is a recognized LLM security category—OWASP lists system prompt leakage as LLM07:2025—referring to unintended exposure of hidden instructions or user input, while &quot;pre-submission exfiltration&quot; echoes earlier web research such as the USENIX &quot;Leaky Forms&quot; study, which found email and password fields being harvested by trackers before the form was ever submitted. URL-based access control failures, including IDOR, occur when a resource is protected only by an unguessable-looking identifier rather than real authorization checks.

<details><summary>References</summary>
<ul>
<li><a href="https://genai.owasp.org/llmrisk/llm07-insecure-plugin-design/">LLM07:2025 System Prompt Leakage - OWASP Gen AI Security Project</a></li>
<li><a href="https://portswigger.net/web-security/access-control">Access control vulnerabilities and privilege escalation | Web Security Academy</a></li>

</ul>
</details>

**Discussion**: Hacker News commenters largely confirmed and extended the paper with firsthand reports: one described ChatGPT periodically shipping unfinished prompts, another noted Perplexity equating a UUID in the URL with privacy, and a third linked it to the OpenAI training-data controversy over unpublished drafts in private Codex sessions, arguing &quot;open models have to win.&quot; Others asked how much risk comes from the agent versus the underlying platform APIs, and one invoked the Simpsons &quot;Milhouse tells Willie everything&quot; joke to capture how readily users confide in these assistants.

**Tags**: `#privacy`, `#conversational-ai`, `#llm-security`, `#web-tracking`, `#research-paper`

---

<a id="item-4"></a>
## [Anthropic: Z.ai&\#x27;s GLM-5.3 Can Autonomously Launch Cyberattacks](https://www.anthropic.com/research/glm-5-3-and-the-spread-of-advanced-cyber-capabilities) ⭐️ 8.0/10

Anthropic published an evaluation concluding that Z.ai&\#x27;s open-weight GLM-5.3 can autonomously build and execute end-to-end cyberattacks, succeeding in 50 of 410 ExploitBench attempts — close to the 56 successes it recorded for its own Claude Mythos Preview. The report also says GLM-5.3&\#x27;s safety guardrails can be bypassed with simple methods, with simulated tests succeeding 64% to 100% of the time. The finding suggests that autonomous offensive cyber capability is no longer confined to closed frontier models, since an openly downloadable model now performs at near-parity with a leading proprietary system. It sharpens the debate over open-weight releases, because any safety alignment baked into the model can be stripped out by whoever downloads it, potentially widening the pool of actors able to run automated attacks. The headline numbers reflect relatively low absolute success rates — 50 of 410 attempts for GLM-5.3 versus 56 for Claude Mythos Preview — so the capability is best described as partial rather than reliable autonomy. Anthropic adds that because GLM-5.3 ships with open weights, users can fine-tune or modify the model to weaken its refusal behaviour, and that its guardrails already fall to straightforward bypass techniques with 64%-100% success in simulated testing.

telegram · zaihuapd · Sep 29, 23:58

**Background**: ExploitBench is a benchmark and workbench used by security researchers to develop, test and score vulnerability-exploitation code across many bug classes, so a higher success count implies a model can get further through the chain from finding a bug to weaponising it. Open weights means a model&\#x27;s trained parameters — the numeric values learned during training — are published for anyone to download and run, which is different from open source because the training data and code need not be released. A jailbreak is a prompt crafted to make a model produce output its safety training was designed to refuse; it is an alignment failure rather than a software exploit, which is why it survives even when the model itself is not compromised.

<details><summary>References</summary>
<ul>
<li><a href="https://www.datalearner.com/benchmarks/exploitbench-jun-aug-2026">ExploitBench (Jun–Aug 2026)... | DataLearnerAI</a></li>
<li><a href="https://en.wikipedia.org/wiki/Open_weights">Open weights - Wikipedia</a></li>
<li><a href="https://casrai.org/dictionary/term/jailbreak-llm">LLM Jailbreak: How Prompts Bypass Guardrails — CASRAI</a></li>

</ul>
</details>

**Tags**: `#AI safety`, `#cybersecurity`, `#LLM`, `#open weights`, `#Anthropic`

---