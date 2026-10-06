# 07 · Should you get a router, and how to choose among the four models

> Website version (longer): https://7d24hrs.com/guides/router?utm_source=github&utm_content=router-07

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

- **Flash it yourself**: you already have a router supported by OpenWrt (more than 1000 models). The firmware is compiled online on the website and you receive the link by email in 3 to 5 minutes; then follow [02 · Flashing the firmware yourself](02-flash-firmware-yourself.md) step by step (it has a video). Suited to people who are comfortable doing technical setup themselves and want to save the cost of a device.
- **Buy a ready-made unit**: we ship a GL.iNet with the firmware already flashed; for the three steps out of the box see [01](01-plug-and-play-router.md). Suited to people who do not want to tinker, or as something for family members who are not technical.

With either route the firmware updates its components by itself, with no need to flash again; and when line addresses change you do not need to change the configuration either.

## Four routers, matched to how you will use them

| Model | Type | Price | Included | What it is | Best for |
|---|---|---|---|---|---|
| GL-MT300N-V2 | Mini | $200 | 12 months of service | Palm-sized and USB-powered (a power bank can run it); 2.4 GHz Wi‑Fi only, 100 Mbps ports | One person travelling: hotel Ethernet or hotel Wi‑Fi, a phone and laptop browsing and watching 1080p. Not suited to being the main router at home |
| **GL-MT3000** | Portable | $300 | 24 months of service | Dual-band Wi‑Fi 6 with a 2.5G port, slightly larger than a palm | The main router for a small household — TV, streaming box, several phones and computers — and small enough for a backpack |
| GL-MT6000 | Desktop | $400 | 24 months of service | Two 2.5G ports plus four gigabit ports, external antennas, the most processing power | Large homes, many devices (a dozen or more), broadband above one gigabit, 4K and console gaming, or a small office. Stays in one place as the only router |
| GL-XE3000 | Mobile | $400 | 24 months of service | Built-in 5G/4G and battery; a SIM card makes it a standalone network, and it also takes Ethernet | Places without fixed broadband: camper vans, job sites, trade shows, short lets; or a backup for the home line |

Included months are on the Personal plan; Family gets half and Enterprise a quarter, the same value either way. Free shipping worldwide, usually 3–14 days, returnable within 30 days.

### Quick picks by situation

- Travelling alone, staying in hotels, on a budget → GL-MT300N-V2
- A flat or small household where the TV and streaming box need Chinese or overseas video → GL-MT3000
- Mostly at home, but you want to take it on the occasional trip → GL-MT3000
- A large home, many devices, broadband above one gigabit, or a shared office → GL-MT6000
- No broadband, or you are on the road most of the time → GL-XE3000
- Setting one up for parents who are not technical → GL-MT3000, bought pre-installed: plug it in and it works

## Why the GL-MT3000 is our first recommendation

- **One unit, two roles.** Powerful enough to be a small household's main router, small enough to travel with. It is the only one of the four that does both.
- **It will not date quickly.** Wi‑Fi 6 and a 2.5G port leave headroom over most home broadband. The mini has only 2.4 GHz Wi‑Fi and 100 Mbps ports, which becomes the bottleneck at home.
- **The price works out.** $300 with 24 months of Personal-plan service, against $200 with 12 months for the mini. Counting the included service, the extra $100 buys a clearly better device plus another year.
- **It is the one we know best.** Our own test unit is this model, new firmware is checked on it first, and the [flashing video tutorial](02-flash-firmware-yourself.md) uses it. When you hit a problem, we have the same device on the desk to compare.

When not to choose it: for a large home, many devices or broadband above one gigabit, go straight to the GL-MT6000; with no fixed broadband, the GL-XE3000; if it is only for one person on trips and price matters most, the GL-MT300N-V2 is enough.

## The three most common problems after getting started

- **Weak Wi‑Fi signal, only 20 dBm**: the firmware sets the wireless power automatically according to the regulations of the country you are in, and it only switches to your country's level after the router has been online once. Right after flashing, plug in a network cable first.
- **Chinese websites become slow** (when you are in China): split routing is off and everything is going through the route. In the split settings choose Forward Split: Chinese IPs go direct and everything else uses the route.
- **Abroad and you want Chinese content**: choose Reverse Split. Reverse split turns the direction round — only mainland Chinese IPs go through the route back to China, and every other site uses your local broadband directly. Chinese video, music and apps see a Chinese address, while local sites and streaming take no detour. The firmware picks the direction from where the router is, so you rarely need to change it. See [03 · Router split routing](03-router-split-routing.md).
- **One device does not go through the VPN**: that device has its own private DNS set (Android "Private DNS", the browser's secure DNS); turn it off.

## FAQ

**Does the router count as one device?** It takes up one slot on the account (by plan: Personal 2, Family 4, Enterprise 8 devices online at the same time), and the devices behind it are not counted separately.

**Can it be used to watch video from China while abroad?** Yes, choose the China region for the line. The router brings the whole local network into the VPN, and the devices' IPv6 and DNS cannot reach the outside, so "copyright restriction" messages appear less often than when a phone connects on its own. See [06](06-unlock-chinese-video-with-router.md).

**Does the firmware have a backdoor?** It is compiled from OpenWrt, with only the component that connects to the VPN and the split routing rules added; the VPN records only connection duration and total traffic for billing, and does not record what you visit.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-07) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-07) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
