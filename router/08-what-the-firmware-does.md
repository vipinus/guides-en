# 08 · After the firmware is installed: what it does on its own, and the few switches you should know

> Website version (longer): https://7d24hrs.com/guides/router-firmware?utm_source=github&utm_content=router-08

After flashing this site's firmware or buying a pre-installed unit, all you need to do is log in to your account on the admin page. This article covers the things the firmware **does on its own** and the few switches you may need to touch; for getting started see [01](01-plug-and-play-router.md), for split routing see [03](03-router-split-routing.md), and for binding and replacing a router see [05](05-mac-binding-and-replacing.md).

## What it does on its own

| What | How it works | What you need to do |
|---|---|---|
| Component and split routing list updates | Checks at boot and downloads any update, which **takes effect at the next boot** | Nothing; changed line addresses and websites added to the list are picked up automatically |
| Wi‑Fi country code | Detects the country it is in once online and sets wireless power and channels automatically | Right after flashing, **plug in a network cable first** so it gets online once; a weaker signal before it has been online is normal |
| Expiry handling | When the account expires it stops going through the VPN; the local network carries on as usual | It recovers automatically after you renew, with no need to log in again |
| Router binding | The first login records this router under the account | Unbind on the website before switching routers |

Only a major version upgrade of the whole firmware requires flashing the sysupgrade file. That happens just a few times a year, and the website will notify you.

## What you may need to touch

- **Split routing mode**: Split routing (default) / Global / Direct. If a website will not open, switch to Global first to verify: if it opens under Global, it is not on the list, so give the address to customer service to have it added; if it will not open under Global either, the problem is with the website itself.
- **Region**: chosen on the admin page. Choose the China region to watch Chinese content from abroad, and an overseas region to reach overseas services from China.
- **Automatically select the fastest line**: located below the region, off by default, and recommended when network quality is poor.

  | | Off (default) | On |
  |---|---|---|
  | Which line is used | Always the region you chose | Automatically picks the line with the lowest latency and little packet loss among the available lines, then re-tests periodically and switches automatically if it gets worse |
  | Exit country | The chosen region | With the China region chosen: picks only among lines in China, and the exit stays in China; with an overseas region chosen: picks among all overseas lines, and **the exit country may differ from the chosen region** (for example, you chose Japan but actually exit from Singapore) |
  | Suited to | Situations that need a fixed country: watching a particular country's streaming services, banks and accounts that are sensitive to region | An unstable home network or a region that often stutters, when you just want speed and do not care which country you exit from |

  When you flip the switch, the admin page shows "Switching automatic selection…" and blocks the page until the switch is complete. The network drops briefly during this time, which is normal. "Current exit" on the admin page shows which line is actually in use.
- **Admin password and Wi‑Fi password**: the factory values are public defaults; change them first thing after logging in.

## TVs, TV boxes and elderly family members' devices

- Just connect to this router's Wi‑Fi or by cable, and the mainland China edition of an app plays right away; the international editions (iQIYI, WeTV) have a different content library, so install the mainland China edition.
- A device is connected but does not go through the VPN: most likely it has its own private DNS set (Android "Private DNS", the browser's secure DNS); turn it off.
- You want a device to always connect directly (a work computer that needs to connect to the company VPN): have it connect to the Wi‑Fi of the upstream router or the modem.

## FAQ

**Can the Personal plan use a router?** Yes. Personal, Family and Enterprise all support a router, with no need to change plans.

**How many device slots does the router take?** One; the devices behind it are not counted.

**Does the firmware have a backdoor?** It is compiled from OpenWrt, with only the component that connects to the VPN and the split routing rules added; the VPN records only connection duration and total traffic for billing.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-08) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-08) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
