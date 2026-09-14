---
layout: default
title: "Horizon Summary: 2026-09-14 (EN)"
date: 2026-09-14
lang: en
---

> From 37 items, 2 important content pieces were selected

---

1. [Homebrew 7.0.0 ships native macOS GUI, stricter sandboxing and built-in vulnerability scanning](#item-1) ⭐️ 9.0/10
2. [Why Google Still Serves Scam Ads: A Hacker News Debate](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Homebrew 7.0.0 ships native macOS GUI, stricter sandboxing and built-in vulnerability scanning](https://brew.sh/2026/09/13/homebrew-7.0.0/) ⭐️ 9.0/10

Homebrew released version 7.0.0, introducing an official native macOS graphical interface alongside faster installs and upgrades, stricter sandboxing, built-in vulnerability checking with a security advisory database. The release also drops support for macOS 10.15 Catalina and older, demotes Intel Macs to Tier 3, and switches the Linux sandbox from Bubblewrap to Landlock. Homebrew is the de facto package manager for macOS and a widely used tool on Linux, so a major-version release affects millions of developers and CI pipelines that depend on it. The official GUI lowers the barrier for less terminal-savvy users, while the security features and breaking platform changes signal a broader shift in how package managers handle supply-chain risk and legacy hardware. Intel Macs are moved to Tier 3, meaning they will no longer receive new precompiled bottles and effectively fall back to building from source, while any macOS 10.15 Catalina or earlier system can no longer run Homebrew at all. On Linux the sandbox implementation changes from Bubblewrap to Landlock, a kernel-level access-control mechanism that lets unprivileged processes restrict their own filesystem access.

telegram · zaihuapd · Sep 13, 11:23

**Background**: Homebrew is a package manager that installs, updates and removes software on macOS and Linux, roughly analogous to apt or yum, and it has long relied on the command line via the brew command. Homebrew classifies platforms into support tiers, where Tier 3 means a configuration still receives support but no new prebuilt binaries. Sandboxing here refers to restricting what a build or installed program can access, and Landlock is a stackable Linux security module that lets even unprivileged processes impose permanent, self-applied limits on file and network access.

<details><summary>References</summary>
<ul>
<li><a href="https://docs.brew.sh/Installation">Homebrew Documentation: Installation</a></li>
<li><a href="https://docs.linuxkernel.org.cn/security/landlock.html">Landlock LSM：内核文档 — Linux 内核文档</a></li>
<li><a href="https://github.com/containers/bubblewrap">GitHub - containers/bubblewrap: Low-level unprivileged sandboxing tool used by Flatpak and similar projects · GitHub</a></li>

</ul>
</details>

**Tags**: `#homebrew`, `#package-manager`, `#macos`, `#open-source`, `#security`

---

<a id="item-2"></a>
## [Why Google Still Serves Scam Ads: A Hacker News Debate](https://www.atomic14.com/2026/09/13/why-is-google-still-serving-dodgy-ads) ⭐️ 8.0/10

A post on the blog atomic14.com titled &quot;Why is Google still serving dodgy ads?&quot; sparked a large Hacker News discussion, scoring 541 points with 259 comments. The thread collected firsthand accounts from publishers and users, including one commenter who said AdSense had been stuffing thousands of scam pop-ups into their site from hosts such as azurewebsites.net, herokuapp.com, netlify.app and digitaloceanspaces.com — domains Google refuses to let them block. The discussion points at a structural problem in online advertising: the largest ad network in the world is also a major distribution channel for scams, and it controls both the inventory and the blocking tools publishers are allowed to use. If regulators adopt strict liability for ad platforms — as many commenters demanded — the economics and legal exposure of Google&\#x27;s ad business would change substantially, affecting publishers, advertisers and ordinary users who are the actual targets of the scams. Publishers report being unable to block the infrastructure domains hosting the bad creatives because Google classifies services like netlify.app, herokuapp.com and azurewebsites.net as &quot;TLDs&quot; rather than blockable domains, while scammers simply rotate to a fresh subdomain each day \(e.g. abc123.netlify.app\). Other commenters described a flood of AI-generated YouTube ads for fake free-electricity devices, anti-aging products and hand-carved birdhouses, and speculated that Google leans on user reports while auto-rejecting them until a volume threshold is reached.

hackernews · iamflimflam1 · Sep 13, 17:37 · [Discussion](https://news.ycombinator.com/item?id=49686445)

**Background**: Google Ads and AdSense form a two-sided marketplace: advertisers bid for placements and publishers host those placements in exchange for a revenue share, with Google taking a cut in the middle. &quot;Dodgy ads&quot; here means scam or deceptive creatives, a subset of the broader problem known as ad fraud — deliberately deceptive impressions, clicks or conversions that extract money from the ad ecosystem, often using identity fraud and bot traffic. In the United States, platforms are broadly shielded from liability for third-party content, while regulations such as the EU&\#x27;s Digital Services Act push toward obligations to remove illegal content quickly — the tension at the heart of calls for &quot;strict liability.&quot;

<details><summary>References</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ad_fraud">Ad fraud</a></li>
<li><a href="https://www.eff.org/deeplinks/2022/05/platform-liability-trends-around-globe-recent-noteworthy-developments">Platform Liability Trends Around the Globe: Recent Noteworthy...</a></li>

</ul>
</details>

**Discussion**: The tone was overwhelmingly critical of Google. One commenter claimed someone who had spent over $100M on Google Ads said the company is juicing revenue in unprecedented ways, attributing it to AI pressure and a desire to cash in before AI erodes the ad business; others called Google &quot;complicit&quot; and demanded strict liability, noting that pre-web newspapers would never have run ads this fraudulent. A minority offered a more forgiving structural explanation, suggesting there are simply more ads than can be reviewed, so Google relies on reports and automated thresholds.

**Tags**: `#Google Ads`, `#ad fraud`, `#online advertising`, `#platform liability`, `#Hacker News`

---