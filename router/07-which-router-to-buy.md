# 07 · Should you get a router, and how to choose among the four models

> Website version (longer): https://www.leotun.com/guides/router?utm_source=github&utm_content=router-07

The router approach solves the problem of "too many devices, and some cannot install a client": the VPN is set up once on the router, and the TV, game console, smart speaker and the elderly family member's phone all go through it automatically, with nothing to install. All it takes is a router that can be flashed and ten minutes of flashing. **Personal, Family and Enterprise accounts can all use a router.**

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
| **GL-MT3000** | Portable | $250 | 2 years of Personal service | Dual-band Wi‑Fi 6 with a 2.5G port, slightly larger than a palm | The main router for a small household — TV, streaming box, several phones and computers — and small enough for a backpack |
| GL-AXT1800 | Portable | $300 | 2 years of Personal service | Dual-band Wi‑Fi 6, one gigabit WAN port and two gigabit LAN ports, about the size of the GL-MT3000 | On the move and need to wire two devices at once — a laptop and a TV box, say — as well as use Wi‑Fi |
| GL-MT3600BE | Portable | $350 | 2 years of Personal service | Dual-band Wi‑Fi 7 with two 2.5G ports, about the size of the GL-MT3000 | Phones and laptops that already support Wi‑Fi 7, and you want faster wireless in something you can still carry |
| GL-MT6000 | Desktop | $400 | 2 years of Personal service | Two 2.5G ports plus four gigabit ports, external antennas, the most processing power | Large homes, many devices (a dozen or more), broadband above one gigabit, 4K and console gaming, or a small office. Stays in one place as the only router |

Included months are on the Personal plan; Family gets half and Enterprise a quarter, the same value either way. Free shipping worldwide, usually 3–14 days, returnable within 30 days.

### Quick picks by situation

- A flat or small household where the TV and streaming box need Chinese or overseas video → GL-MT3000
- Mostly at home, but you want to take it on the occasional trip → GL-MT3000
- Portable, with two devices to wire at once → GL-AXT1800
- New phones and laptops with Wi‑Fi 7, and you want the fastest wireless in a portable unit → GL-MT3600BE
- A large home, many devices, broadband above one gigabit, or a shared office → GL-MT6000
- Setting one up for parents who are not technical → GL-MT3000, bought pre-installed: plug it in and it works

## Why the GL-MT3000 is our first recommendation

- **One unit, two roles.** Powerful enough to be a small household's main router, small enough to travel with. It is the only one of the four that does both.
- **It will not date quickly.** Wi‑Fi 6 and a 2.5G port leave headroom over most home broadband.
- **The price is the lowest.** $250 with 2 years of Personal service — the cheapest of the four, $50 less than the GL-AXT1800, yet with a 2.5G port.
- **It is the one we know best.** Our own test unit is this model, new firmware is checked on it first, and the [flashing video tutorial](02-flash-firmware-yourself.md) uses it. When you hit a problem, we have the same device on the desk to compare.

When not to choose it: for a portable unit with two wired ports, the GL-AXT1800; for devices that support Wi‑Fi 7, the GL-MT3600BE; for a large home, many devices or broadband above one gigabit, go straight to the GL-MT6000.

## The three most common problems after getting started

- **Weak Wi‑Fi signal, only 20 dBm**: the firmware sets the wireless power automatically according to the regulations of the country you are in, and it only switches to your country's level after the router has been online once. Right after flashing, plug in a network cable first.
- **Chinese websites become slow** (when you are in China): split routing is off and everything is going through the route. Switch the mode back to split routing: when reaching overseas services from China, by default only blocked sites use the route, while Chinese sites and foreign sites that open fine from China anyway go direct.
- **In China, a foreign website will not open**: under "VPN settings", in the smart split routing section, untick "Blocked sites only" (or switch to "Global" temporarily) and try again; if it then opens, the site is blocked but not yet on the list, so send the address to customer service.
- **Abroad and you want Chinese content**: choose Reverse Split. Reverse split turns the direction round — only mainland Chinese IPs go through the route back to China, and every other site uses your local broadband directly. Chinese video, music and apps see a Chinese address, while local sites and streaming take no detour. The firmware picks the direction from where the router is, so you rarely need to change it. See [03 · Router split routing](03-router-split-routing.md).
- **One device does not go through the VPN, or blocked sites will not open while everything else works**: that device has its own private DNS set (Android "Private DNS", the browser's secure DNS), so the router cannot see which site it is looking up; turn it off.

## FAQ

**Does the router count as one device?** It takes up one slot on the account (by plan: Personal 2, Family 4, Enterprise 8 devices online at the same time), and the devices behind it are not counted separately.

**Can it be used to watch video from China while abroad?** Yes, choose the China region for the line. The router brings the whole local network into the VPN, and the devices' IPv6 and DNS cannot reach the outside, so "copyright restriction" messages appear less often than when a phone connects on its own. See [06](06-unlock-chinese-video-with-router.md).

**Does the firmware have a backdoor?** It is compiled from OpenWrt, with only the component that connects to the VPN and the split routing rules added; the VPN records only connection duration and total traffic for billing, and does not record what you visit.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=router-07) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=router-07) (groups, email and support are all listed there) · Sign up for a 30-minute free trial; invite a friend who pays and you each get 15 credits (about 15 Personal-plan days), valid long-term
