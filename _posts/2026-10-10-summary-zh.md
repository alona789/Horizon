---
layout: default
title: "Horizon Summary: 2026-10-10 (ZH)"
date: 2026-10-10
lang: zh
---

> 从 38 条内容中筛选出 3 条重要资讯。

---

1. [Cloudflare 收购 Deno，独立运行时开发即将终结](#item-1) ⭐️ 9.0/10
2. [YouTuber 自制 Flock 式摄像头追踪警车，称遭警察上门](#item-2) ⭐️ 8.0/10
3. [Telegram Desktop 曝一键窃取任意文件漏洞](#item-3) ⭐️ 8.0/10

---

<a id="item-1"></a>
## [Cloudflare 收购 Deno，独立运行时开发即将终结](https://deno.com/blog/cloudflare) ⭐️ 9.0/10

Cloudflare 宣布收购 Deno，根据公告，Cloudflare 将在未来一年内继续维护 Deno 运行时，每月发布包含错误修复和安全更新的版本，一年后将停止自己对 Deno 运行时的开发。代码仍会保持开源，官方也明确欢迎其他人接手继续开发——也就是说，除非有其他团队接手，Deno 实际上将不再获得支持。 Deno 是 Node.js 之外最受关注的 JavaScript/TypeScript 运行时之一，其独立开发的终结会显著改变运行时生态格局，并进一步把话语权集中到已经拥有 workerd 运行时的 Cloudflare 手中。基于 Deno 或 Deno Deploy 构建的开发者与企业，如今面临不确定的迁移路径，以及一个不再有厂商路线图的运行时。 这一年的承诺只覆盖每月的错误修复与安全更新，不包含新功能，因此不应期待运行时本身再有创新。由于 Deno 仍然开源，第三方可以通过 fork 继续开发；同时这次人才收购把 Ryan Dahl 的团队带进了 Cloudflare，其安全模型有可能被 workerd 吸收。

hackernews · ilreb · 10月9日 13:03 · [社区讨论](https://news.ycombinator.com/item?id=50019911)

**背景**: Deno 是 Node.js 原作者 Ryan Dahl 于 2018 年发布的 JavaScript 与 TypeScript 运行时，初衷是修正 Node 的不足：默认安全（未经显式授权不能访问文件或网络）、无需配置即可使用 TypeScript，以及内置标准库。Cloudflare 是重要的 CDN 与边缘计算公司，其 Workers 平台运行在同样基于 V8 引擎的开源 JavaScript/WASM 运行时 workerd 之上。像这样的收购通常被称为“人才收购”（acquihire），意味着买方主要买的是团队与技术，而不是一个打算继续运营的产品。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://blog.logrocket.com/dev/what-is-deno/">What is Deno , and how is it different from Node.js? - LogRocket Blog</a></li>
<li><a href="https://www.fullstack.com/labs/resources/blog/what-is-deno">What is Deno ? | FullStack Blog</a></li>
<li><a href="https://www.punyakrit.dev/blogs/js-runtime">JavaScript Runtime | Developer Blog | Punyakrit Singh Makhni</a></li>

</ul>
</details>

**社区讨论**: 讨论区的情绪以惋惜和无奈为主：有评论认为这个标题的实质就是“Cloudflare 通过人才收购让 Deno 开发实际上关停”，大家一方面庆幸还有一年的缓冲期，另一方面惋惜失去了 Node 后来也借鉴过的那些创新。不少人认为，自从把 npm 兼容性置于 Ryan 最初的第一性原理愿景之上、并受风投压力影响后，Deno 就已经偏离方向；也有人希望 workerd 能吸收 Deno 基于权限的沙箱机制；还有很多人把此事看作大型 AI 与云厂商整合开发者工具浪潮的一部分。

**标签**: `#Deno`, `#Cloudflare`, `#JavaScript runtime`, `#acquisition`, `#open source`

---

<a id="item-2"></a>
## [YouTuber 自制 Flock 式摄像头追踪警车，称遭警察上门](https://gizmodo.com/youtuber-says-cops-paid-him-a-visit-after-he-built-flock-style-camera-to-track-cops-2000824306) ⭐️ 8.0/10

一名 YouTuber 仿照 Flock 的车牌识别摄像头自建了一套设备，用来追踪警用车辆，并称事后有执法人员上门找他。Gizmodo 报道了这一事件，相关讨论在 Hacker News 上获得 421 分和 231 条评论。 这一事件把自动车牌识别监控的方向颠倒过来，说明警方用来监视公众的技术同样可以被反过来用于监视警方。它进一步推动了更广泛的争论：是否应允许任何一方（包括政府）进行大规模车辆追踪，以及需要什么样的立法来加以限制。 这台摄像头是对 Flock Safety 所售 ALPR 硬件的自制复刻，而 Flock 的网络已被 7000 多个执法机构使用。评论者指出了本案核心的不对称性：Flock 的设计初衷是供执法部门检索，而非供普通公民使用，因此个人追踪并公开警方行踪，并不能简单等同于 Flock 的既定用途被反用。

hackernews · gumby · 10月9日 21:06 · [社区讨论](https://news.ycombinator.com/item?id=50026555)

**背景**: ALPR 是自动车牌识别的缩写，指由 AI 驱动的摄像头拍下每一辆经过的车辆，并存储车牌号、位置、日期和时间等信息，使使用者能够检索历史行车轨迹。总部位于亚特兰大的 Flock Safety 建成了美国规模最大的此类网络之一，它被宣传为公共安全工具，但也被批评为大规模监控系统。民权组织和 DeFlock 等开源项目则致力于绘制这些摄像头的部署位置。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://builtin.com/articles/flock-cameras">Flock Cameras Explained: What They Track and Why It Matters | Built In</a></li>
<li><a href="https://deflock.org/">DeFlock is an open-source project that maps license plate readers ...</a></li>
<li><a href="https://en.wikipedia.org/wiki/Automatic_number-plate_recognition">Automatic number- plate recognition - Wikipedia</a></li>

</ul>
</details>

**社区讨论**: 评论者大多把这则新闻视为监控权力平衡发生变化的案例，有人指出既然警察可以监视公民，公民也可以监视警察。一些人援引新罕布什尔州的法律作为范本——该法禁止收集所有车牌以供日后分析、要求对“未命中”的车辆图像在三分钟内删除、并禁止将未命中的图像上传离开设备——另一些人则认为最彻底的解决办法是禁止包括政府在内的任何一方进行此类追踪。整体情绪对 ALPR 的扩张持批评态度，有人对政治上迟迟没有行动感到不满，也有人半开玩笑地提议做一个“OpenFlock”，专门追踪那些投票支持在本市安装摄像头者的市议员行踪。

**标签**: `#surveillance`, `#privacy`, `#ALPR`, `#Flock`, `#civil-liberties`

---

<a id="item-3"></a>
## [Telegram Desktop 曝一键窃取任意文件漏洞](https://telegram.me/zaihuapd/44307) ⭐️ 8.0/10

Telegram Desktop 7.2.9 以下版本存在严重漏洞（CVE-2026-107181），用户点击精心构造的 tg:// 链接后，系统文件可在毫无确认提示的情况下被悄悄窃取。该漏洞源于链接中未转义的分号被当作独立的 IPC 命令处理，官方已在 7.2.9 版本中修复。 由于 Telegram Desktop 是一款广泛使用的即时通讯客户端，一条恶意链接就可能让远程攻击者获取 SSH 密钥、浏览器会话和加密钱包等高度敏感的数据。攻击只需一次点击、交互成本极低，加之用户基数庞大，这对尚未升级的用户而言是一个需要立即处置的威胁。 该漏洞滥用了 Telegram Desktop 的单实例 IPC 机制：tg:// 链接中未转义的分隔符被解析为一条独立命令，配合 interpret: 处理器即可读取并外泄磁盘上的任意文件，其中也包括会话文件。鉴于已有在野利用报告且 7.2.9 已确认修复，建议尽快升级、警惕异常 tg:// 链接并启用本地密码。

telegram · zaihuapd · 10月9日 09:51

**背景**: tg:// 是 Telegram 的自定义 URL 方案，允许外部链接在桌面端和移动端应用中触发操作，例如打开某个聊天或加入某个群组。Telegram Desktop 采用单实例 IPC（进程间通信）通道，以便在打开第二条链接时把它作为命令转发给已在运行的实例。CVE-2026-107181 正是滥用了这一通道：由于链接中的分隔符未被正确转义，链接的一部分可被解析为额外的 IPC 命令，再借助 interpret: 指令加载并外发本地文件。该缺陷已被分配 CVE 编号，并在 Telegram Desktop 7.2.9 中修复。

<details><summary>参考链接</summary>
<ul>
<li><a href="https://beaksec.github.io/posts/telegram-desktop-one-click-account-takeover/">Telegram Desktop: one-click account takeover via IPC... | beaksec</a></li>
<li><a href="https://dbu.gs/vulnerability/CVE-2026-107181">CVE-2026-107181 — Telegram Telegram Desktop | dbugs</a></li>

</ul>
</details>

**标签**: `#security`, `#vulnerability`, `#Telegram`, `#CVE`, `#privacy`

---