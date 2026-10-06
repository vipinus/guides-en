# 06 · Unlocking Chinese video sites from abroad with a router

## Why use a router instead of installing a client on every device

- TVs, TV boxes, projectors and game consoles cannot install a client, so a router is the only way.
- With many people at home, setting up every device for every person is not realistic; set up the router once and it takes effect as soon as a device connects to Wi-Fi.
- Split routing is done on the router, so local websites and local devices keep connecting directly; only Chinese video domains go through the line for reaching China, and speed is not affected.

## What you need

| Item | Notes |
|---|---|
| A supported router | A pre-installed one works out of the box; if you flash it yourself, see [How to flash the firmware](02-flash-firmware-yourself.md) |
| An account | Personal, Family and Enterprise accounts all support the router feature. After signing up, claim the free trial first to verify the whole process: a new account is on the Personal plan, with a 24-hour trial |
| An upstream network | The modem or router you already have at home; the new router goes behind it |

## Done in five steps

1. Connect the new router's WAN port to the upstream network, plug in the power and wait one minute.
2. Connect your phone to the new router's Wi-Fi, open the admin address `http://192.168.11.1`, and log in to your account.
3. Choose **Split routing** as the mode. Chinese video domains are on the list and will automatically go through the line for reaching China.
4. Switch the TV and the TV box over to this Wi-Fi, or connect them by cable to a LAN port on the new router.
5. Open iQIYI, Tencent Video or Yangshipin (CCTV); if it plays normally, you are done.

## The list is public

The video domains on the split routing list are maintained in a public repository: <https://github.com/vipinus/openwrt-2026-video-domains>. If a platform will not play, you can check whether its domain is on the list, and submit an entry if it is not.

## Picture quality and bandwidth

1080p needs a steady 5 Mbps, and 4K needs 25 Mbps or more. The cross-border link is the bottleneck; if it is not enough at evening peak hours, lower the picture quality. For the entry region, pick one that is close to you and has a good route to mainland China; try a couple, and judge by whether playback stutters.

## FAQ

- **It plays on the phone but not on the TV**: the TV is still connected to the old Wi-Fi, or the app on the TV is the international edition.
- **Some platforms play and some do not**: that platform's domain is not on the split routing list. Switch to "Global" temporarily to verify, then submit it to the list repository.
- **The whole household slows down on an old router**: the CPU cannot keep up with encrypted traffic; switch to a model with better performance, see [Getting started with a pre-installed router](01-plug-and-play-router.md).

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-06) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-06) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
