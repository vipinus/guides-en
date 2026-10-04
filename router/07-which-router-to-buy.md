# 07 · Should you get a router, and how to choose among the four models

> Website version (longer): https://7d24hrs.com/guides/router

The router approach solves the problem of "too many devices, and some cannot install a client": the VPN is set up once on the router, and the TV, game console, smart speaker and the elderly family member's phone all go through it automatically, with nothing to install. The cost is a router that can be flashed and ten minutes of flashing. **Personal, Family and Enterprise accounts can all use a router.**

## When to use one and when not to

| Use one | Do not use one |
|---|---|
| You have devices at home that cannot install a client, such as a TV box, game console, Apple TV or smart speaker | You only have one phone and one computer and mostly travel for work — installing a client is lighter |
| There are many family members and you do not want to teach them one device at a time | You live in a dormitory or shared flat and do not control the network |
| You have devices that need to stay connected 24 hours a day (NAS, camera upload) | Your main router is a carrier-locked modem and you cannot attach a second router — use a portable router as a compromise |
| An office in China or a whole family steadily reaching overseas services from China, with split routing on the router and nothing for the devices to notice | |

## Flash firmware or buy a ready-made unit

Both routes end up running the same firmware. The difference is who does the flashing and who is responsible when something goes wrong.

- **Flash it yourself**: you already have a router supported by OpenWrt (more than 1000 models). The firmware is compiled online on the website and you receive the link by email in about 5 minutes; for the process see [02](02-flash-firmware-yourself.md). Suited to people who are comfortable doing technical setup themselves and want to save the cost of a device.
- **Buy a ready-made unit**: we ship a GL.iNet with the firmware already flashed; for the three steps out of the box see [01](01-plug-and-play-router.md). Suited to people who do not want to tinker, or as something for family members who are not technical.

With either route the firmware updates its components by itself, with no need to flash again; and when line addresses change you do not need to change the configuration either.

## The four models on sale

| Model | Positioning | Price | Included | Suited to |
|---|---|---|---|---|
| GL-MT300N-V2 | Mini | $200 | 12 months of service | Palm-sized and USB-powered, plug it into the hotel network cable on business trips; 100 Mbps ports, enough for 1080p on a phone or laptop |
| GL-MT3000 | Portable | $300 | 24 months of service | Wi‑Fi 6, can serve a small household and also fits in a backpack; the first router for most people |
| GL-MT6000 | Desktop | $400 | 24 months of service | 2.5G ports and multiple antennas, for many devices, 4K and game consoles; works as the main router with nothing else attached |
| GL-XE3000 | Mobile | $400 | 24 months of service | Built-in 5G/4G and a battery; insert a SIM card and it is a standalone network, for motorhomes, construction sites and temporary housing without broadband |

The included months are counted on the Personal plan; they are halved on the Family plan and quartered on the Enterprise plan, which is equivalent in value, so you do not lose out. Free shipping worldwide, usually arriving in 3–14 days, returnable within 30 days.

## The three most common problems after getting started

- **Weak Wi‑Fi signal, only 20 dBm**: the firmware sets the wireless power automatically according to the regulations of the country you are in, and it only switches to your country's level after the router has been online once. Right after flashing, plug in a network cable first.
- **Chinese websites become slow** (when you are in China): split routing is not on and everything is going through the VPN. With split routing on, Chinese IPs connect directly. If you are abroad watching Chinese content, keep split routing on as well: the Chinese video domains on the list go through the line for reaching China, and everything else connects directly. See [03 · Router split routing](03-router-split-routing.md).
- **One device does not go through the VPN**: that device has its own private DNS set (Android "Private DNS", the browser's secure DNS); turn it off.

## FAQ

**Does the router count as one device?** It takes up one slot on the account (by plan: Personal 2, Family 4, Enterprise 8 devices online at the same time), and the devices behind it are not counted separately.

**Can it be used to watch video from China while abroad?** Yes, choose the China region for the line. The router brings the whole local network into the VPN, and the devices' IPv6 and DNS cannot reach the outside, so "copyright restriction" messages appear less often than when a phone connects on its own. See [06](06-unlock-chinese-video-with-router.md).

**Does the firmware have a backdoor?** It is compiled from OpenWrt, with only the component that connects to the VPN and the split routing rules added; the VPN records only connection duration and total traffic for billing, and does not record what you visit.

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
