# 03 · Connected, but the video site still shows a copyright notice: IPv6 and DNS are the ones that slip through

> Website version (longer): https://www.leotun.com/guides/overseas-video?utm_source=github&utm_content=troubleshooting-03

You have passed step 1 of [02 · Connected to reach China but still can't watch](02-still-blocked-after-connecting.md) — the exit IP checks out as mainland China — yet the site still says "cannot be played due to copyright restrictions". Nine times out of ten there is still a path on the device that does not go through the VPN: **IPv6** or **DNS**. A video site decides where you are from the address it sees, and as long as one path leaks out, what it sees is still overseas.

## Why leaks happen

- Modern devices have both an IPv4 and an IPv6 address, and browsers prefer IPv6. If the VPN only takes over IPv4, IPv6 requests go straight out through your home broadband.
- The browser's built-in "secure DNS", Android's "Private DNS", or another mesh networking tool that is running (Tailscale and the like) will all take over name resolution ahead of the VPN.

"Connected" only means the tunnel has been established. It does not mean all traffic goes through the tunnel.

## Five-step check

1. **Check IPv6.** After connecting, search for "test ipv6" and open a test page. If the IPv6 field shows an address in the country you are in → the problem is here, go to step 2. If both fields show mainland China, or IPv6 is unavailable → go to step 3.
2. **Turn off IPv6, or switch to a client that blocks IPv6.** Windows: in the network adapter's properties, untick "Internet Protocol Version 6". macOS: Network settings → TCP/IP → set IPv6 to "Link-local only". Phone: turn off Wi‑Fi and try once on mobile data; home broadband usually has IPv6, while carrier mobile data often does not.
3. **Check DNS.** Chrome Settings → Privacy and security → turn off "Use secure DNS"; on Android turn off "Private DNS"; quit other VPNs, mesh networking tools and proxy extensions.
4. **Quit the app completely and reopen it; for the web version, clear the site data.** Platforms cache the previous region check.
5. **Switch to another entry point and try again.** The address of a particular exit may have just been flagged by the platform.

## How LeoTun handles it

Since September 2026, all three of LeoTun's connection methods (Hiddify, Cisco AnyConnect, OpenVPN) reject IPv6 directly inside the tunnel and push DNS settings that force resolution inside the tunnel — no settings need to be changed on your device. **Hiddify configurations imported before September do not have this rule. Delete them and scan the QR code to import again.**

The router option does not leak in the first place: the whole LAN goes out through the router, so the devices' IPv6 and DNS never reach the outside.

## Cases that still trigger the notice

| Case | Symptom | Fix |
|---|---|---|
| The exit is not mainland China | The IP lookup shows Hong Kong / Taiwan / Japan | Switch to a China entry point; Hong Kong and Taiwan addresses also count as overseas for Tencent and iQIYI |
| Custom routing rules set the video domains to "direct" | Web pages open, but videos will not play | Change the China domains to go through the node; overseas users should not turn on "direct for China" |
| You are using the web proxy | Works in the browser, not in apps | Watching video needs a whole-device tunnel; the web proxy only covers the browser |

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=troubleshooting-03) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=troubleshooting-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
