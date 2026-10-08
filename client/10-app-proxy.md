# 10 · What to do when Dropbox and other software ask for an HTTP / SOCKS proxy

> Website version (longer): https://www.leotun.com/guides/app-proxy?utm_source=github&utm_content=client-10

**First, how things stand: a proxy has to be encrypted.** Unencrypted proxies (plain HTTP, SOCKS4, SOCKS5) are identified and interfered with on networks in China; after a short while the connection slows down or drops, and the account and password travel in clear text as well. Only encrypted connections stay usable over the long term, so this site's web proxy uses encrypted connections throughout; **for software that accepts only HTTP / SOCKS5, let Hiddify take over the whole machine** (see below).

Standalone software such as Dropbox, Telegram Desktop, Steam, cloud drive clients and developer tools does not read the browser's settings, and its own proxy settings accept only unencrypted HTTP / SOCKS5. The two sides don't match, so entering a proxy doesn't get it connected. The solution is **not to enter a proxy**: use Hiddify to send the whole computer through the line, and set the proxy in the software to "No proxy".

## Why it still won't connect after entering a proxy

| Cause | Explanation |
|---|---|
| Type mismatch | The software offers only HTTP, SOCKS4 and SOCKS5, none of them encrypted; this site's proxy has to be encrypted and can't be entered |
| An unencrypted proxy found online | It connects for a while, then gets interfered with and works only on and off |
| Covers only part of the traffic | In much software only login and sync use the proxy, while updates, calls and LAN sync still connect directly; an HTTP proxy doesn't forward the UDP traffic of games and calls at all |
| Maintained separately in each program | Changing region or password means changing them one by one, and whichever one you miss stops working |

## Recommended approach: let Hiddify take over the whole machine

1. Install Hiddify by following [09 · Installing Hiddify on every platform](09-hiddify-install-all-platforms.md), and import a profile by following [02](02-singbox-subscription-links.md).
2. Connect in "VPN" mode (the default). On Windows, the first connection needs administrator rights.
3. Set the proxy in the software back to "No proxy": in Dropbox, choose "No proxy" or "Auto-detect" under "Preferences → Network → Proxies"; in Telegram Desktop, choose "Disable proxy" under "Settings → Advanced → Connection type". In any other software that has a proxy option, turn it off.
4. Verify: the Dropbox tray icon shows "Up to date" and syncing starts; open a web page that shows your IP in the browser, and the exit is in the region you chose.

With "automatic routing" on, overseas services such as Dropbox go through the line, while WeChat, online banking and Chinese websites connect directly as usual.

## Common software

| Software | How to set it |
|---|---|
| Dropbox | Proxy "No proxy" or "Auto-detect"; if you leave it on "Manual" with some other address, it stays offline once Hiddify is turned off |
| Telegram Desktop | Connection type "Disable proxy"; the built-in MTProto / SOCKS5 layered on top of the tunnel only makes it slower |
| OneDrive, Google Drive, iCloud for desktop | Follow the system network; nothing to set |
| Steam, Epic, Battle.net | No proxy needed; if downloads are slow, switch to a nearer region |
| Zoom, Teams, Slack, Discord | Voice and video are UDP, which only a whole-machine method carries |
| VS Code, JetBrains, Cursor | Follow the system network; clear any proxy set separately inside the tool |

## When you can't install a client (company computer)

- Use the web version of Dropbox and cloud drives: open dropbox.com in a browser with the [web proxy](03-web-proxy-extension.md); you can upload and download, but there is no automatic sync.
- Command-line tools (git, pip, npm, curl) accept an encrypted proxy: put the web proxy address into `https_proxy`; see [Reaching overseas services from China 05 · Linux and the command line](https://github.com/vipinus/guides-zh-CN/blob/main/overseas-access/05-linux-server.md) (in Chinese).
- Other desktop software that accepts only HTTP / SOCKS5 is best used on your own computer or phone; don't install a whole-machine VPN on a company computer for this, as it will trigger the company's security alerts.

## FAQ

**Can you give me a SOCKS5 or HTTP proxy address?** This site's proxy uses encrypted connections throughout; an unencrypted one starts working only on and off before long. Letting Hiddify take over the whole machine is more stable and covers all software at once.

**With Hiddify on, do I still need to enter a proxy in the software?** No. Entering one means going round twice: at best it is slower, at worst it won't connect.

**What about Dropbox on a phone?** Phone apps have no proxy settings. Install Hiddify or use Cisco (AnyConnect); once connected, all apps go through the line.

**Can I do without Hiddify?** Yes. Cisco, the private network and OpenVPN also take over the whole machine, and the software is likewise set to "No proxy". The advantage of Hiddify is built-in routing and better speed on networks with heavy packet loss.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-10) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-10) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
