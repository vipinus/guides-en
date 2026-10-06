# 02 · Which connection method suits which situation

One LeoTun account has six connection methods: Private network (Tailscale), Cisco (AnyConnect), OpenVPN, Proxy (web proxy), Hiddify, and Router. Each method has the situations it suits best, and this article gives answers by situation: first by the device you use, then by the network you are on, and finally by what you want to do. Each situation comes with a recommendation, the reason, and an alternative. Remember one thing: six methods on one account; there is always one that suits your network.

## By device: what you go online with

- One phone, business trips and travel: Cisco or Hiddify. Cisco connects as soon as you enter the address in the official app and is the most stable; Hiddify is imported by scanning a QR code and is faster when packet loss is high. Alternative: Private network.
- Your own computer (Windows, Mac): Hiddify or Private network. Hiddify is fast and has a built-in split-routing switch; Private network stays online after a single login. Alternative: Cisco.
- A company-issued computer, no administrator rights: web proxy. You only install one browser extension, it needs no administrator rights, and it does not touch the company's network settings.
- iPhone, old devices: Cisco. It connects with the system's built-in VPN or the official client, no configuration import is needed, and compatibility is the best.
- NAS (Synology, QNAP), Linux servers: OpenVPN. Import one .ovpn file and it connects automatically at boot; most of these devices come with a client built in.
- TVs, set-top boxes, game consoles, an elderly relative's phone: Router. Anything connected to the Wi‑Fi goes through the line, and nothing needs to be installed on the device. All three account plans can use it.
- Many devices for a whole family or an office: Router, configured once and effective for all; if you also want to reach the NAS at home from outside, add Private network.

## By network environment: what network you are on

- Dormitory or campus networks, company networks that restrict UDP: Cisco. It runs over TLS, the same as opening an HTTPS website, and is the most stable on restricted networks; Hiddify, Private network and OpenVPN all run over UDP and will be slow or drop.
- Broadband that often drops, weak Wi‑Fi signal: web proxy. It works per request with no long-lived connection, so by design there is no connection to drop.
- Broadband in old residential compounds, mobile data, high packet loss: Hiddify. Its protocol is designed to resist packet loss and gives the best speed on such networks.
- The computer is already connected to a company VPN: web proxy. Two whole-device VPNs running together fight over network settings; the web proxy only handles the browser, so they do not interfere with each other.
- China Mobile, Great Wall and other broadband, or cross-border links that are always unstable: any method, choosing a China-region entry point. The client connects only to an address inside China and we handle the cross-border leg, so it is not affected by cross-border interference.

## By purpose: what you want to do

- You are overseas and want to watch Chinese video: any whole-device method (Cisco, Hiddify, Private network, OpenVPN, Router) with the China region selected; use Router for the TV at home. Do not use the web proxy for video: it cannot reach the device's own network channel, so the video site may still see you as overseas.
- Games, voice and video calls: Hiddify, Private network or Router, choosing the region with the lowest latency. The web proxy only handles the browser; games and calling apps do not go through it.
- Office work and looking things up, browser only: the web proxy is the least hassle; if you need to connect to internal company systems, first confirm whether the company VPN can run alongside ours, and if it cannot, use the web proxy.
- Servers, scripts, the command line: OpenVPN; on a Linux desktop you can also use Private network or Hiddify.
- Reaching the NAS or cameras at home from outside: Private network. Devices on the same account can reach each other, with no need to open ports on the router.

## Quick reference for the six methods: best for / not suited to

- Private network (Tailscale) — best for: multiple devices, logging in once and forgetting about it, reaching home devices from outside. Not suited to: networks that restrict UDP (it can only rely on relays, which are slow), running alongside another VPN.
- Cisco AnyConnect — best for: restricted networks, company computers, iPhone, old devices; the best compatibility. Not suited to: people inside China who do not want all traffic to go through the line (a separate split-routing script has to be run).
- OpenVPN — best for: NAS, Linux servers, OpenWrt routers; import one file and it connects automatically at boot. Not suited to: everyday use on phones and computers, where it is less convenient than Cisco and Hiddify; networks that restrict UDP.
- Web proxy — best for: no administrator rights, already connected to a company VPN, broadband that often drops. Not suited to: video apps, games, calls; it only handles the browser.
- Hiddify — best for: those who want speed, networks with high packet loss; import by scanning a QR code, the same app on five platforms, built-in split routing. Not suited to: networks that restrict UDP.
- Router — best for: a whole family, an office, devices that cannot install a client; the firmware has split routing built in and updates automatically. Not suited to: people with only one device who are often out (you still need to install a client when you go out).

## Choosing a region by your broadband

The same method can differ in speed several times over between regions; the reason lies in your carrier's outbound line to that region, not in the server. China Unicom in the north: try Japan and Korea first. China Telecom in the south: try Southeast Asia (Singapore, Malaysia, Thailand, the Philippines, Indonesia) or Australia first. Other broadband (China Mobile, Great Wall and so on): try the China-region entry point first.

The red, yellow and green lights in the region list show each region's live load; among several Japan entries, pick the one with the green light. From 8 to 11 pm is the nationwide peak; in that period pick a green-light region or switch connection method. If it is still slow, the usual cause is the local broadband (community broadband, or a carrier and region that do not match).

## Split routing: direct inside China, through the line for overseas

Only users who are in mainland China need split routing; overseas users use global mode, and turning split routing on would actually send some sites the long way round. In Hiddify you switch to "Auto split routing" in the client, in the web proxy you switch to "Split routing" in the extension, true split routing is on the router, where the firmware has it on by default; with Cisco and OpenVPN all traffic goes through the line once connected, and the split-routing script from the "Cisco" section is available; the Private network sends the whole device through the line.

If a site will not open under split routing, first switch to "Global" temporarily to check: if it opens under global, it is not on the list; if it does not open under global either, the problem is with that site itself.

## How to switch when it does not work

1. Switch region first. If another region connects, that server is just temporarily unreachable.
2. Then switch network. If broadband does not work, switch to mobile data, and vice versa; interference on different carriers does not happen at the same time.
3. Then switch method. If those running over UDP (Hiddify, Private network, OpenVPN) do not work, switch to Cisco, which runs over TLS; if whole-device methods keep dropping, switch to the web proxy. Blocking of the different protocols is independent of one another.
4. If it still does not work, see the troubleshooting guide, or ask in the support group, and include the connection method, region, the exact error text and the time.

## FAQ

**Which of the six methods is fastest?** On networks with high packet loss, Hiddify is fastest; on clean networks there is little difference, and the bottleneck is the region and the time of day, not the method.

**Which one for gaming and voice calls?** Hiddify, Private network or Router, choosing the region with the lowest latency. The web proxy only handles the browser; games and calling apps do not go through it.

**Can the six methods be used at the same time?** On different devices, yes; all methods on the same account share the simultaneous-online quota (Personal 2 devices, Family 4 devices, Enterprise 8 devices). Do not run two whole-device methods at the same time on the same device (for example Private network and Cisco), as they will fight over network settings.

**Do I have to choose between a router and a client?** No. Use the router at home and turn on the client on your phone when you go out; each counts as one device.

**Which one for Linux?** Private network, OpenVPN and Hiddify all have Linux clients; Cisco on Linux uses the open-source OpenConnect; OpenVPN on Linux requires entering the account and password on the first connection. For servers and NAS, OpenVPN is the least hassle.

## Further reading

- [How we differ from other VPNs](https://7d24hrs.com/guides/why-us?utm_source=github&utm_content=network-02)
- [What the Private network (Tailscale) is](https://7d24hrs.com/guides/tailscale-mesh?utm_source=github&utm_content=network-02)
- [How to use OpenVPN and when to choose it](https://7d24hrs.com/guides/openvpn-setup?utm_source=github&utm_content=network-02)
- [What the web proxy is and when to use it](https://7d24hrs.com/guides/web-proxy?utm_source=github&utm_content=network-02)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/choose-connection?utm_source=github&utm_content=network-02

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=network-02) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=network-02) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; every friend you invite earns you 30 days, an offer with no end date
