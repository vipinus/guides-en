# 08 · How to choose a China-bound line: where the China IP comes from and where the free ones go wrong

> Website version (longer): https://7d24hrs.com/guides/choose-china-vpn?utm_source=github&utm_content=china-access-08

A China-bound line does only one thing: it makes the requests you send from overseas arrive at Tencent Video, NetEase Cloud Music or your online bank from a **mainland China** IP. So look at two points first: whether the exit really is a mainland IP, and whether any traffic on the device is bypassing it. Speed, price and the client all come after that.

## Where the China IP comes from

The provider must have its own servers inside the mainland. Cloud providers inside China require real-name registration to start a machine and bill bandwidth by usage, so the cost is far higher than for overseas machines. That is why nearly all legitimate China-bound services are paid, and why the number of China exits is limited.

A common substitute is to pass off machines in Hong Kong, Taiwan or Japan as "China-bound". These addresses work for some of Bilibili's Hong Kong, Macau and Taiwan sections, but Tencent Video, iQIYI and Youku still show a copyright restriction, and online banking and 12306 also treat you as overseas. **How to tell: after connecting, look up where the IP is registered; it only counts if it says "China · some province".**

## Five items to check before choosing

| Item | How to check | What failing looks like |
|---|---|---|
| Exit region | Look up where the IP is registered after connecting | Hong Kong, Taiwan, Japan or Korea addresses |
| IPv6 and DNS | Search for "test ipv6" and open a test page | The IPv6 field shows the country you are in → video sites will still block you, see [Troubleshooting 06](../troubleshooting/03-ipv6-and-dns-leak.md) |
| Client | Whether it is a standard protocol (AnyConnect, OpenVPN, Hiddify) | There is only one proprietary app, and once it is taken down you have nothing to use |
| Bandwidth | Play 1080p between 8 and 11 pm Beijing time | Fast during the day, spinning in the evening |
| Multiple devices and router | How many devices per account, and whether a router can connect a whole household | Each device has to be bought separately |

## Why free China-bound lines keep dropping

The problem is not "free" but the cost structure. Mainland exit bandwidth is paid for by usage, and a free service can only pick one of three: squeeze several thousand people onto one machine, so everyone stutters at peak hours; cap traffic and time, so a payment prompt pops up halfway through; or make money some other way, by injecting ads, collecting browsing history, or using your device as someone else's exit.

Free "China-bound" browser extensions have one more blind spot: they only proxy the browser's web requests, and the video player, apps and system DNS do not go through them, which is why "the web page opens but the video will not play" is so common.

For looking something up now and then, free is enough. For following series, listening to music and doing online banking, the time a stable paid line saves is worth far more than the subscription fee. Claim the 24-hour trial first, try it once at the evening peak, and then decide.

## How overseas students, travellers and families should each set up

- **Overseas students**: dormitory networks mostly have IPv6, so use a client that blocks IPv6; for online banking, CHSI and 12306, connect to the China line only when needed and disconnect when you are done, to reduce account risk control.
- **Short trips**: install a Cisco or Hiddify client on your phone and import by scanning the QR code; it works as soon as you land.
- **A whole family living overseas long-term**: connect one router with the firmware flashed to the line, and the TV, set-top box and elderly relatives' phones need no setup; see [Unlocking Chinese video sites with a router](../router/06-unlock-chinese-video-with-router.md).

## A 5-minute self-test

1. Connect to the China line; the IP lookup shows a mainland China province.
2. The IPv6 test page shows it as unavailable, or also as a mainland address.
3. Open any series exclusive to China on Tencent Video; it plays.
4. Play 1080p once more after 8 pm Beijing time; it does not buffer repeatedly.
5. Switch to another China exit and repeat the first three steps.

## FAQ

**Is there a difference between a China-bound VPN and a China-bound accelerator?** No essential difference. An "accelerator" is usually an app customised by a game or video vendor that covers only specific applications; a VPN is a whole-device tunnel.

**Can I watch Tencent Video with a Hong Kong node?** No, the licence covers only the mainland.

**How many devices per account?** With LeoTun, simultaneous connections follow the plan: Personal 2 devices, Family 4 devices, Enterprise 8 devices. A router counts as one device, and the devices behind it are not counted separately. When more are online at once than your plan's limit, you can temporarily upgrade the account type (the remaining time is converted at equivalent value by price) and switch back afterwards.

**Can I use Clash?** Yes. LeoTun provides both a Hiddify configuration address and a hysteria2 share link, and importing the share link into Clash Meta is enough; after importing, set China domains to go through the node, not to "direct".

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=china-access-08) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=china-access-08) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
