# LeoTun Knowledge Base

How cross-border access works, how to set up each client, routers and home networks, and troubleshooting. One topic per article, in plain language. Maintained by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=readme) team.

Other languages: [简体中文](https://github.com/vipinus/guides-zh-CN) · [繁體中文](https://github.com/vipinus/guides-zh-TW)

## Free time, always available

| How to get it | What you get |
|---|---|
| Claim the free trial after signing up | 24 hours with every feature, no credit card |
| Invite a friend who signs up and pays for the first time | +30 days on your expiry date (+15 days on Family, +7.5 days on Enterprise), once per friend, no limit on the number of friends |

Website: <https://7d24hrs.com?utm_source=github&utm_content=readme> · Contact us: <https://7d24hrs.com/contact?utm_source=github&utm_content=readme>

## Contents

### [Reaching China from Abroad · Everything that needs a China IP](china-access/)

When you are overseas, many Chinese services refuse you because your IP is not in mainland China: video, music, government services, banking, ticket booking, games. One article per situation, explaining clearly **why you are blocked, how to fix it, and what other pitfalls there are**.

| Article |
|---|
| [01 · Which services need a China IP](china-access/01-what-needs-a-china-ip.md) |
| [02 · Watching Chinese video from abroad](china-access/02-watch-chinese-video-abroad.md) |
| [03 · Using Chinese government and public service websites](china-access/03-government-and-public-services.md) |
| [04 · Online banking, mobile banking and payments](china-access/04-banking-and-payments.md) |
| [05 · Music, podcasts and audiobooks](china-access/05-music-and-audio.md) |
| [06 · China-server games and live streaming](china-access/06-gaming-and-streaming.md) |
| [07 · Viewing your home cameras in China from abroad](china-access/07-home-camera-abroad.md) |
| [08 · How to choose a China-bound line: where the China IP comes from and where the free ones go wrong](china-access/08-how-to-choose-a-china-access-line.md) |
| [09 · Verification codes that never arrive, and Chinese phone numbers](china-access/09-sms-code-and-china-phone-number.md) |
| [10 · How overseas students should set up a China-bound VPN](china-access/10-students.md) |
| [11 · China-bound VPN: free or paid](china-access/11-free-vs-paid.md) |
| [12 · How to set up for business trips and travel](china-access/12-travel.md) |
| [13 · WeChat, Alipay and Chinese Mini Programs](china-access/13-wechat-alipay-miniprograms.md) |
| [14 · Setting things up for elderly relatives abroad: install once, then leave it alone](china-access/14-help-parents-abroad.md) |
| [15 · Online courses, exam registration and degree verification](china-access/15-online-courses-and-exams.md) |

### [Overseas Access Guides · Using Overseas Services from Inside China](overseas-access/)

You are in China, and the overseas services you need for work, development, research, gaming and streaming will not open or are extremely slow. One situation per article, with a clear account of **what you need, how to choose, and what the pitfalls are**.

| Article |
|---|
| [01 · Which services need an overseas IP, and how the line works](overseas-access/01-what-needs-an-overseas-ip.md) |
| [02 · Does Cisco AnyConnect work in China](overseas-access/02-anyconnect-in-china.md) |
| [03 · Which region is fastest from inside China: by carrier](overseas-access/03-which-region-is-fastest.md) |
| [04 · Using a company computer: no administrator rights, already on the company VPN](overseas-access/04-office-laptop.md) |
| [05 · How to send a Linux server and command-line tools through the line](overseas-access/05-linux-server.md) |
| [06 · How to send a Synology or QNAP NAS through the line](overseas-access/06-nas-openvpn.md) |
| [07 · Accessing AI tools (ChatGPT, Claude, Gemini and others)](overseas-access/07-ai-tools.md) |
| [08 · Searching the literature, downloading papers, submitting manuscripts](overseas-access/08-academic-research.md) |

### [Network Guides](network/)

A clear explanation of the **principles** behind cross-border access, **how to choose among the six connection methods**, how we differ from other providers, and how to spot risky software. No jargon pile-ups.

| Article |
|---|
| [01 · How reaching China from abroad works](network/01-why-china-services-block-overseas.md) |
| [02 · Which connection method suits which situation](network/02-choose-your-connection-method.md) |
| [03 · How the Private network (Tailscale) differs from a VPN, and when to use it](network/03-private-network-vs-vpn.md) |
| [04 · How we differ from other VPNs](network/04-why-us.md) |
| [05 · How to spot risky VPN software](network/05-risky-vpn-apps.md) |
| [06 · Why it is sometimes fast and sometimes slow](network/06-why-sometimes-fast-sometimes-slow.md) |
| [07 · Which problems the line solves, and which need another fix](network/07-when-you-do-not-need-us.md) |
| [08 · Choosing among the three account plans, renewal and payment](network/08-account-tiers-and-payment.md) |
| [09 · What to do when you run out of device connections](network/09-not-enough-devices.md) |

### [Client Guides · Installation and Setup](client/)

Step-by-step instructions for **installing and connecting** each access method: Cisco AnyConnect, Hiddify, the web proxy extension, OpenVPN and the private network (Tailscale), plus what to do when iOS won't let you install an app, how to install Telegram / Discord, how to set up many devices once, and what to do when software such as Dropbox asks for a proxy. For which method to choose, see [Which connection method suits which situation](network/02-choose-your-connection-method.md); if it is installed but won't connect, see [Troubleshooting](troubleshooting/).

| Article |
|---|
| [01 · Cisco AnyConnect: installing, connecting and updating on every platform](client/01-anyconnect-install.md) |
| [02 · Hiddify subscription links, import links and share links: what they are, and whether you need "subscription conversion"](client/02-singbox-subscription-links.md) |
| [03 · Web proxy: set up the ZeroOmega extension in two steps](client/03-web-proxy-extension.md) |
| [04 · OpenVPN: download the .ovpn profile, import it and connect; works on routers, NAS and Linux](client/04-openvpn-profile.md) |
| [05 · Private network (Tailscale): installing, logging in to this site's control server, choosing an exit](client/05-tailscale-private-network.md) |
| [06 · What to do when iOS won't let you install an app](client/06-ios-app-store.md) |
| [07 · Installing Telegram and Discord](client/07-install-telegram-discord.md) |
| [08 · Set up many devices once, and switch phones without starting over](client/08-multi-device.md) |
| [09 · Installing Hiddify on every platform: Windows, macOS, Linux, Android, iOS](client/09-hiddify-install-all-platforms.md) |
| [10 · What to do when Dropbox and other software ask for an HTTP / SOCKS proxy](client/10-app-proxy.md) |

### [Router and Home Network Guides](router/)

Put every device in the house on the VPN at once: getting started with a pre-installed router, flashing firmware yourself, how split routing works, TVs and elderly family members, binding and replacing a router.

| Article |
|---|
| [01 · Getting started with a pre-installed router](router/01-plug-and-play-router.md) |
| [02 · Flashing the firmware yourself: from stock to ours, step by step (with video)](router/02-flash-firmware-yourself.md) |
| [03 · What router split routing is](router/03-router-split-routing.md) |
| [04 · For elderly family members and the TV](router/04-family-tv-and-router.md) |
| [05 · MAC binding and replacing a router](router/05-mac-binding-and-replacing.md) |
| [06 · Unlocking Chinese video sites from abroad with a router](router/06-unlock-chinese-video-with-router.md) |
| [07 · Should you get a router, and how to choose among the four models](router/07-which-router-to-buy.md) |
| [08 · After the firmware is installed: what it does on its own, and the few switches you should know](router/08-what-the-firmware-does.md) |
| [09 · How the router's split routing works](router/09-real-vs-fake-split.md) |
| [10 · Will the NAS, printer and cameras behind the router be affected?](router/10-nas-printer-camera-behind-router.md) |
| [11 · Gigabit or 2 Gbps broadband with a router: what decides the speed](router/11-fast-broadband-and-router-speed.md) |
| [12 · Does the router recover by itself after a power cut or a dropout?](router/12-after-power-cut-or-dropout.md) |

### [Troubleshooting Guide](troubleshooting/)

A checklist to work through in order when something goes wrong: can't connect, slow, dropped connections; still blocked after turning on the route back to China; IPv6 and DNS leaks; Hiddify imported but not connecting; and finally, how to reach us. Installation topics have moved to the [Client Guide](client/).

| Article |
|---|
| [01 · Checklist for can't connect, slow, and dropped connections](troubleshooting/01-cannot-connect-slow-drops.md) |
| [02 · Connected to reach China but still can't watch: what to do](troubleshooting/02-still-blocked-after-connecting.md) |
| [03 · Connected, but the video site still shows a copyright notice: IPv6 and DNS are the ones that slip through](troubleshooting/03-ipv6-and-dns-leak.md) |
| [04 · Hiddify imported but won't connect](troubleshooting/04-singbox-import-not-connecting.md) |
| [05 · How to reach us, and how not to lose touch](troubleshooting/05-how-to-reach-us.md) |
| [06 · What to do when your Mac says the app "is damaged"](troubleshooting/06-antivirus-false-positive.md) |
| [07 · After switching phones, switching computers, or reinstalling the system](troubleshooting/07-new-phone-new-computer.md) |
| [08 · How to confirm you are really connected, and which region you are exiting from](troubleshooting/08-am-i-connected.md) |
| [09 · Having support look at your computer and router remotely](troubleshooting/09-remote-assist.md) |
| [10 · How to communicate effectively with AI support](troubleshooting/10-ask-ai-support.md) |

Questions are welcome in this repository's [Discussions](https://github.com/vipinus/guides-en/discussions).

> The Chinese knowledge base has two more sections about China-specific situations (reaching Chinese services from abroad, and reaching overseas services from inside China); they are not translated. These articles are translated from the Chinese edition; where the two differ, the Chinese edition is authoritative.

## License

Text is licensed under [CC BY 4.0](LICENSE). Please credit the source and keep the link when republishing.
