---
layout: default
title: "Horizon Summary: 2026-09-14 (ZH)"
date: 2026-09-14
lang: zh
---

> 从 37 条内容中筛选出 2 条重要资讯。

---

1. [Homebrew 7.0.0 发布：官方 macOS 原生图形界面、更严格沙箱与内置漏洞扫描](#item-1) ⭐️ 9.0/10
2. [谷歌为何仍在投放诈骗广告？Hacker News 热议](#item-2) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Homebrew 7.0.0 发布：官方 macOS 原生图形界面、更严格沙箱与内置漏洞扫描](https://brew.sh/2026/09/13/homebrew-7.0.0/) ⭐️ 9.0/10

Homebrew 发布 7.0.0 版本，带来官方 macOS 原生图形界面，并重点提升安装与升级速度，同时引入更严格的沙箱保护、内置漏洞检查与安全公告数据库。该版本还停止支持 macOS 10.15 Catalina 及更早版本，将 Intel Mac 降级为 Tier 3，并将 Linux 沙箱由 Bubblewrap 改用 Landlock。 Homebrew 是 macOS 事实上的包管理器，在 Linux 上也被广泛使用，因此一次大版本更新会影响到数百万开发者以及依赖它的 CI 流水线。官方图形界面降低了对终端不熟悉的用户的使用门槛，而安全能力与破坏性的平台变更也反映出包管理器在供应链风险与老旧硬件支持上的整体转向。 Intel Mac 被降为 Tier 3，意味着它们不再获得新的预编译包（bottle），实质上退回从源码构建；而 macOS 10.15 Catalina 及更早系统则完全无法再运行 Homebrew。在 Linux 上，沙箱实现由 Bubblewrap 改为 Landlock——一种允许非特权进程主动限制自身文件系统访问权限的内核级访问控制机制。

telegram · zaihuapd · 9月13日 11:23

**背景**: Homebrew 是一个在 macOS 和 Linux 上安装、更新与卸载软件的包管理器，作用类似 Linux 上的 apt 或 yum，长期以来主要通过 brew 命令行使用。Homebrew 将平台划分为不同支持层级，其中 Tier 3 表示该配置仍受支持但不再提供新的预编译二进制包。沙箱在这里指的是限制构建过程或已安装程序可以访问的资源，而 Landlock 是一个可堆叠的 Linux 安全模块，允许非特权进程对自身的文件与网络访问施加一旦生效便无法解除的限制。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://docs.brew.sh/Installation">Homebrew Documentation: Installation</a></li>
<li><a href="https://docs.linuxkernel.org.cn/security/landlock.html">Landlock LSM：内核文档 — Linux 内核文档</a></li>
<li><a href="https://github.com/containers/bubblewrap">GitHub - containers/bubblewrap: Low-level unprivileged sandboxing tool used by Flatpak and similar projects · GitHub</a></li>

</ul>
</details>

**标签**: `#homebrew`, `#package-manager`, `#macos`, `#open-source`, `#security`

---

<a id="item-2"></a>
## [谷歌为何仍在投放诈骗广告？Hacker News 热议](https://www.atomic14.com/2026/09/13/why-is-google-still-serving-dodgy-ads) ⭐️ 8.0/10

博客 atomic14.com 发布了一篇题为《Why is Google still serving dodgy ads?》的文章，在 Hacker News 上引发大规模讨论，获得 541 分、259 条评论。讨论中汇集了发布者和用户的第一手经历，其中一位评论者表示 AdSense 长期在其网站上塞入数千条诈骗类弹窗广告，来源域名包括 azurewebsites.net、herokuapp.com、netlify.app 和 digitaloceanspaces.com，而谷歌不允许他们屏蔽这些域名。 这场讨论指向在线广告的一个结构性问题：全球最大的广告网络同时也是诈骗内容的重要分发渠道，而库存和发布者可用的屏蔽工具都由它自己掌控。若监管机构真如众多评论者所呼吁的那样对广告平台施加严格责任，谷歌广告业务的成本结构与法律风险将发生实质变化，并波及发布者、广告主，以及真正被诈骗瞄准的普通用户。 发布者反馈无法屏蔽承载这些恶意创意的底层域名，因为谷歌把 netlify.app、herokuapp.com、azurewebsites.net 这类服务归类为「TLD」而非可屏蔽域名，而诈骗者每天只需换一个新子域（如 abc123.netlify.app）即可绕过。另有评论者描述了 YouTube 上大量 AI 生成的广告，兜售虚假的免费电力设备、抗衰老产品和「手工雕刻」鸟屋，并推测谷歌依赖用户举报，但会先自动驳回举报，直到达到一定数量阈值才处理。

hackernews · iamflimflam1 · 9月13日 17:37 · [社区讨论](https://news.ycombinator.com/item?id=49686445)

**背景**: Google Ads 与 AdSense 构成一个双边市场：广告主竞价购买展示位，发布者在自己的页面上承载这些广告以换取分成，谷歌从中抽成。「dodgy ads」在这里指诈骗性或欺骗性创意，属于更广义的广告欺诈（ad fraud）问题的一部分——即通过刻意欺骗产生的曝光、点击或转化，从广告生态中套取资金，通常伴随身份欺诈和机器人流量。在美国，平台对第三方内容普遍享有免责保护，而欧盟《数字服务法》等法规则要求平台在知悉非法内容后尽快移除，这正是「严格责任」呼声所指向的核心矛盾。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://en.wikipedia.org/wiki/Ad_fraud">Ad fraud</a></li>
<li><a href="https://www.eff.org/deeplinks/2022/05/platform-liability-trends-around-globe-recent-noteworthy-developments">Platform Liability Trends Around the Globe: Recent Noteworthy...</a></li>

</ul>
</details>

**社区讨论**: 整体舆论对谷歌持强烈批评态度。一位评论者称，某位在 Google Ads 上花费超过 1 亿美元的人表示谷歌正以前所未有的方式榨取收入，并将其归因于 AI 竞争压力以及想在 AI 摧毁广告业务之前尽量变现；其他人则直指谷歌「共谋」，要求施加严格责任，并指出网络广告出现之前的报纸绝不会刊登如此诈骗性的广告。也有少数人给出更宽容的结构性解释，认为广告数量远超人工审核能力，因此谷歌只能依赖举报和自动化阈值。

**标签**: `#Google Ads`, `#ad fraud`, `#online advertising`, `#platform liability`, `#Hacker News`

---