# 08 · How to confirm you are really connected, and which region you are exiting from

The client showing "Connected" does not mean the websites you visit see the VPN's address. The easiest way to check is right in this site's top bar: the "Current network" field shows **you as this site sees you right now** — which country, which province/state and which network you are coming out of. This article covers how to read that field, how to compare before and after connecting, how to tell whether each of the six connection methods is connected, what the red, yellow and green lights in the region list mean, and a few things you can check yourself when it is "connected but still showing local".

## What "Current network" in the top bar shows

| Position | Content |
|---|---|
| At the front | The flag of the country where the exit is; replaced by a Wi‑Fi icon when the country cannot be identified |
| In the middle | The province/state name, shown in the interface language (the US, Canada, Australia and so on use common abbreviations such as CA, ON, NSW); Hong Kong, Macau and Singapore show the region name directly |
| At the end | The network name: China's three major carriers, the education network and so on are shown in the Chinese interface as short names such as 电信 (China Telecom), 移动 (China Mobile), 联通 (China Unicom) and 教育网 (education network); the rest show their English brand name (e.g. Comcast, Bell) |

- **When the province/state cannot be found, only "flag · network name" is shown.** The country name is not used as a filler; the flag tells you the country.
- On a computer, hover the mouse over this field and it pops up the full organisation name, province/state, country code and **exit IP**. This IP is shown only to you, and it is the most useful thing to have when you contact support.
- Chrome / Edge on Windows have no flag font, so the flag appears as two letters (e.g. JP, US). The meaning is the same.
- On a computer it appears in the top bar only after you log in; on a phone it is shown without logging in.

## Compare before and after connecting to tell at a glance

1. **With the VPN off**, open this site and take a look: it should be the carrier of your home broadband or mobile data, and the flag should be the country you are in.
2. **Connect the VPN** and go back to the browser: the flag changes to the region you chose, and the network name usually changes to the name of a data centre or cloud provider rather than your home carrier.
3. If the two are the same, this browser is not going through the VPN when it visits this site. See "Connected, but still showing local" below.

**There is no need to keep refreshing the page.** This field re-checks automatically when you switch back to the browser window, checks a few more times within a few seconds after it detects a network change, and also updates every ten seconds or so while the page is open. If you still see the old value right after connecting, wait ten seconds or so or switch windows; if it still has not changed, refresh manually.

**When you are in China and have chosen a "China entry point"**, it is normal for the top bar to show a foreign country: the China entry points use split routing, so Chinese websites go out from inside China and foreign websites land via the overseas route. This site is overseas, so naturally what is shown is the overseas end.

## How to tell whether each connection method is connected

| Method | What to look at in the client | Does this site's top bar change |
|---|---|---|
| Cisco (AnyConnect) | The client shows "Connected" | Yes. Once Cisco is connected, all traffic goes through the VPN |
| Hiddify | The client shows connected | It changes in global mode; under "auto routing" it depends on the list |
| OpenVPN | The client shows connected | Yes. By default all traffic goes through the VPN |
| Private network (Tailscale) | The client is online, **and** a region is selected as the Exit Node | It changes only when an exit is selected; with None selected, devices can only reach each other and traffic does not go through the VPN |
| Proxy (web proxy) | There is no "connected" state; look at which region mode is selected in the extension icon | Only the browser with the extension installed changes; the "auto switch" rules may make this site go direct |
| Router | In the admin page, the account status is normal and the expiry date is shown | Look from a device connected to this router's Wi‑Fi; in split-routing mode it depends on the list |

Split routing means that websites on the list go through the VPN and everything else goes direct. If the top bar shows local while split routing is on, it does not necessarily mean you are not connected: **switch to "global" temporarily and look again**. If it changes, the VPN is working and this site is simply not on the list.

## The red, yellow and green lights in the region list

On the Cisco, Hiddify, Proxy and OpenVPN pages there is a small light under each region's flag, and the same light appears before the exit names in the Private network client. It is graded automatically by the average real-time bandwidth of each server in that region, and updates about once a minute:

| Light | Meaning |
|---|---|
| Green (steady) | Idle |
| Yellow (blinking) | In use |
| Red (blinking) | Busy |
| No light | No data was obtained at the moment; it does not mean the server is down |

On a computer, hover the mouse over the light to see the region's average load.

**What to do when you see a red light:**

- Red does not mean broken; it only means there are many people at that moment. If you are already connected and the speed is good enough, leave it alone.
- If it feels slow, switch to a region with a green light. For Cisco, click another flag on the web page to copy the new address; for Hiddify, import another region's configuration; for Private network, change it in Exit Node; for Proxy, click another region in the extension icon.
- A region has several machines behind it, and the least busy one is picked automatically when you connect. You do not need to, and cannot, pick a machine yourself.
- It is generally crowded from 8 to 11 pm. In this period, switching regions helps more than reconnecting repeatedly. For how to choose a region by carrier, see Further reading.

## Connected, but still showing local

In order of how common they are:

1. **Routing rules make this site go direct.** Hiddify's auto routing, the Proxy extension's "auto switch", and the router's split-routing mode can all keep this site off the VPN. Switch to global temporarily to verify; Proxy users can also add this site to the rules.
2. **The web proxy only covers that one browser.** Looking from another browser or a phone app will of course still show local.
3. **No exit selected in Private network.** Online ≠ going through the VPN; when Exit Node is None, devices can only reach each other.
4. **You are looking from the wrong device.** For the Router option you need to look from a device connected to that router's Wi‑Fi, not a phone connected to the modem's Wi‑Fi or using mobile data.
5. **Another VPN or mesh networking tool is on at the same time.** A company VPN or another provider's accelerator will compete for routes. Keep only one.
6. **It has not refreshed yet.** Wait ten seconds or so, switch windows, or refresh manually once.

## The top bar can only tell you the IP

The top bar looks at the IPv4 address of the connection this site received. If it shows the right thing, that only means this browser went through the VPN when visiting this site:

- **IPv6 and DNS cannot be seen from it.** When the browser visits this site over IPv6, the field is simply not shown; it will not pass off a wrong network as the real one. If a video site still shows a copyright restriction notice, most likely IPv6 or DNS is bypassing the VPN; see [03 · IPv6 and DNS are the ones that slip through](03-ipv6-and-dns-leak.md).
- **Apps cache their region check.** The top bar is looked up fresh every time and is not affected by caching; but video and music apps remember the previous region. Quit completely and reopen; see [02 · Connected to reach China but still can't watch](02-still-blocked-after-connecting.md).

## FAQ

**The "Current network" field in the top bar has disappeared?** On a computer, log in first. If it is still not shown after logging in, most likely this connection went over IPv6 or it cannot be looked up for the moment; wait ten seconds or so or refresh. It would rather show nothing than show something wrong.

**Same region, but a different IP on two connections?** Normal. A region has several machines behind it, and each connection picks the least busy one at that moment. An established connection is not moved elsewhere midway.

**The province shown is not what I expected?** The top bar shows the province/state where the exit IP is located and is only accurate to that level. If the flag matches, the exit is in the country or region you chose.

**What should I report when contacting support?** Hover the mouse over that field in the top bar and send what pops up (including the exit IP) together with the connection method, the region you chose and the time the problem occurred.

## Further reading

- [How to troubleshoot can't connect, slow, and dropped connections](https://7d24hrs.com/guides/connect-issues)
- [Which region is fastest from inside China](https://7d24hrs.com/guides/pick-region)
- [Which scenarios each connection method suits](https://7d24hrs.com/guides/choose-connection)
- [What the web proxy is and when to use it](https://7d24hrs.com/guides/web-proxy)
- [What the router firmware can do](https://7d24hrs.com/guides/router-firmware)
- [What to do when Tencent Video shows a copyright restriction notice abroad](https://7d24hrs.com/guides/overseas-video)

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
