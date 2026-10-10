---
layout: default
title: "Horizon Summary: 2026-10-10 (EN)"
date: 2026-10-10
lang: en
---

> From 38 items, 3 important content pieces were selected

---

1. [Cloudflare Acquires Deno, Ending Independent Runtime Development](#item-1) ⭐️ 9.0/10
2. [YouTuber Builds Flock-Style Camera to Track Police, Says Cops Visited](#item-2) ⭐️ 8.0/10
3. [Telegram Desktop Flaw Allows One-Click Theft of Arbitrary Files](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare Acquires Deno, Ending Independent Runtime Development](https://deno.com/blog/cloudflare) ⭐️ 9.0/10

Cloudflare has announced it is acquiring Deno, and per the announcement it will maintain the Deno runtime for one more year with monthly bug-fix and security releases, after which it will end its own development of the runtime. The code will remain open source, with the company explicitly inviting others to continue it — meaning that unless another party steps in, Deno effectively becomes unsupported. Deno is one of the most visible alternatives to Node.js, so the end of its independent development significantly reshapes the JavaScript/TypeScript runtime landscape and concentrates further power in Cloudflare, which already owns the workerd runtime. Developers and companies that built on Deno or Deno Deploy now face an uncertain migration path and a runtime with no vendor roadmap. The one-year commitment covers only monthly bug fixes and security updates, not new features, so no further innovation should be expected from the runtime itself. Because Deno stays open source, a third party could fork and continue it, and the acquihire brings Ryan Dahl&\#x27;s team into Cloudflare, where its security model could potentially be absorbed into workerd.

hackernews · ilreb · Oct 9, 13:03 · [Discussion](https://news.ycombinator.com/item?id=50019911)

**Background**: Deno is a JavaScript and TypeScript runtime released in 2018 by Ryan Dahl, the original creator of Node.js, designed to fix Node&\#x27;s perceived shortcomings: secure by default \(no file or network access without explicit permission\), TypeScript support with no configuration, and a built-in standard library. Cloudflare is a major CDN and edge-computing company whose Workers platform runs on workerd, an open-source JavaScript/WASM runtime also built on the V8 engine. An acquisition like this one, often called an &quot;acquihire,&quot; typically means the buyer is mainly acquiring the team and technology rather than a product it intends to keep operating.

<details><summary>References</summary>
<ul>
<li><a href="https://blog.logrocket.com/dev/what-is-deno/">What is Deno , and how is it different from Node.js? - LogRocket Blog</a></li>
<li><a href="https://www.fullstack.com/labs/resources/blog/what-is-deno">What is Deno ? | FullStack Blog</a></li>
<li><a href="https://www.punyakrit.dev/blogs/js-runtime">JavaScript Runtime | Developer Blog | Punyakrit Singh Makhni</a></li>

</ul>
</details>

**Discussion**: Sentiment in the discussion is overwhelmingly sad and resigned: commenters say the headline really means &quot;Deno development effectively shut down via a Cloudflare acquihire,&quot; welcome the one-year runway but mourn the loss of the innovation that Node later borrowed from. Several argue Deno lost its way once npm compatibility and VC pressure took priority over Ry&\#x27;s original first-principles vision, others hope workerd will adopt Deno&\#x27;s permission-based sandboxing, and many frame this as part of a broad wave of developer-tooling consolidation by big AI and cloud vendors.

**Tags**: `#Deno`, `#Cloudflare`, `#JavaScript runtime`, `#acquisition`, `#open source`

---

<a id="item-2"></a>
## [YouTuber Builds Flock-Style Camera to Track Police, Says Cops Visited](https://gizmodo.com/youtuber-says-cops-paid-him-a-visit-after-he-built-flock-style-camera-to-track-cops-2000824306) ⭐️ 8.0/10

A YouTuber built a Flock-style automated license-plate-reading camera aimed at tracking police vehicles, and says law enforcement officers visited him after he did so. Gizmodo reported the incident, which drew 421 points and 231 comments on Hacker News. The episode inverts the usual direction of automated license-plate surveillance, showing that the same technology police use to watch the public can be turned back on them. It feeds a broader debate over whether anyone — including the government — should be allowed to run mass vehicle tracking, and what legislation would be needed to constrain it. The camera is a DIY replication of the ALPR hardware sold by Flock Safety, whose network is used by more than 7,000 law enforcement agencies. Commenters noted an asymmetry at the heart of the case: Flock is designed to be searchable by law enforcement rather than by ordinary citizens, so a private individual tracking and publishing police movements is not a straightforward mirror image of Flock&\#x27;s intended use.

hackernews · gumby · Oct 9, 21:06 · [Discussion](https://news.ycombinator.com/item?id=50026555)

**Background**: ALPR stands for automated license-plate recognition: AI-powered cameras that photograph every passing vehicle and store details such as plate number, location, date and time, letting users search historical movement patterns. Flock Safety, an Atlanta-based company, has built one of the largest such networks in the United States, marketed as a public-safety tool but criticized as a mass surveillance system. Civil-liberties groups and projects like the open-source DeFlock map out where these cameras are installed.

<details><summary>References</summary>
<ul>
<li><a href="https://builtin.com/articles/flock-cameras">Flock Cameras Explained: What They Track and Why It Matters | Built In</a></li>
<li><a href="https://deflock.org/">DeFlock is an open-source project that maps license plate readers ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number- plate recognition - Wikipedia</a></li>

</ul>
</details>

**Discussion**: Commenters largely saw the story as a case of the surveillance balance of power shifting, with one noting that if police can watch citizens, citizens can watch police. Several pointed to New Hampshire&\#x27;s law — which bans collecting every plate for later analysis, requires deleting non-hit images within three minutes, and forbids uploading non-hit imagery off the device — as a model, while others argued the cleanest fix is to bar everyone, government included, from this kind of tracking. Sentiment was broadly critical of ALPR expansion, with some frustration that little is being done politically and a few joking proposals such as an &quot;OpenFlock&quot; that tracks city council members who voted for the cameras.

**Tags**: `#surveillance`, `#privacy`, `#ALPR`, `#Flock`, `#civil-liberties`

---

<a id="item-3"></a>
## [Telegram Desktop Flaw Allows One-Click Theft of Arbitrary Files](https://telegram.me/zaihuapd/44307) ⭐️ 8.0/10

Telegram Desktop versions below 7.2.9 contain a serious vulnerability \(CVE-2026-107181\) that lets an attacker silently steal arbitrary files after a user clicks a crafted tg:// link, with no confirmation prompt shown. The flaw stems from an unescaped semicolon in the link that is treated as a separate IPC command, and a fix has already been released in version 7.2.9. Because Telegram Desktop is a widely used messaging client, a single malicious link could expose highly sensitive data such as SSH keys, browser sessions, and crypto wallets to remote attackers. The low interaction cost — just one click — and broad install base make this an immediately actionable threat for users who have not yet updated. The vulnerability abuses Telegram Desktop&\#x27;s single-instance IPC mechanism: an unescaped separator in the tg:// link is parsed as a distinct command, and combined with the interpret: handler it can read and exfiltrate arbitrary files off disk, including session files. Reported exploitation in the wild and a confirmed fix in 7.2.9 make upgrading, avoiding unusual tg:// links, and enabling a local passcode the recommended mitigations.

telegram · zaihuapd · Oct 9, 09:51

**Background**: tg:// is Telegram&\#x27;s custom URL scheme that lets external links trigger actions inside the desktop and mobile apps, such as opening a chat or joining a group. Telegram Desktop uses a single-instance IPC \(inter-process communication\) channel so that when a second link is opened, it is forwarded to the already-running app instance as a command. CVE-2026-107181 abuses this channel: because a separator character in the link was not properly escaped, part of the link could be interpreted as an extra IPC command, and the interpret: directive could then be used to load and send a local file. The flaw was assigned a CVE and fixed in Telegram Desktop 7.2.9.

<details><summary>References</summary>
<ul>
<li><a href="https://beaksec.github.io/posts/telegram-desktop-one-click-account-takeover/">Telegram Desktop: one-click account takeover via IPC... | beaksec</a></li>
<li><a href="https://dbu.gs/vulnerability/CVE-2026-107181">CVE-2026-107181 — Telegram Telegram Desktop | dbugs</a></li>

</ul>
</details>

**Tags**: `#security`, `#vulnerability`, `#Telegram`, `#CVE`, `#privacy`

---