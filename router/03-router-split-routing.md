# 03 · What router split routing is

> Website version (longer): https://www.leotun.com/guides/router-firmware?utm_source=github&utm_content=router-03

## In one sentence

Set up the VPN on the router, and every device in the house goes through it automatically once connected to Wi-Fi. Devices that cannot install a client, such as TV boxes, game consoles and printers, can use it too.

## What problem split routing solves

If all traffic goes through the VPN, you run into two problems: local websites become slow (they take a detour), and local devices become unreachable (printers, NAS and the router admin page are all on the local network, but the traffic has been sent out).

Split routing works by giving the router a list: domains on the list go through the VPN, and everything else connects directly. Which way round depends on where you are and which side you want to reach, and is decided automatically by the region you choose:

- **Abroad, with the China region chosen (reaching China)**: Chinese websites and apps go through the VPN, and everything else connects directly.
- **In China, with an overseas region chosen (reaching overseas services)**: by default only blocked websites and services go through the VPN; Chinese websites, and foreign websites that open fine from China anyway (foreign company websites, Apple and Microsoft downloads, game platforms and the like), connect directly with no detour, as fast as without the router.

## Three modes

| Mode | Where traffic goes | When to use it |
|---|---|---|
| Global | Everything goes through the VPN | Temporarily, when troubleshooting |
| Split routing | Listed domains go through the VPN, the rest connects directly | Day to day |
| Direct | Nothing goes through the VPN | When you do not need it for a while |

## Reaching overseas services from China: blocked sites only

Since 14 October 2026, split routing in the direction for reaching overseas services from China sends only blocked websites and services through the VPN by default. It works from a blocked-site list that updates automatically every day, plus services such as Telegram that connect to fixed addresses without looking up a site name. Websites that open fine from China anyway, Chinese or foreign, connect directly.

The switch is on the router admin page under "VPN settings", in the smart split routing section: the "Blocked sites only" checkbox, ticked by default. Untick it to go back to the previous behaviour: Chinese websites direct, everything else through the VPN.

Firmware flashed before October 2026 does not show this checkbox yet; the new default already applies to those routers through automatic updates. To change it, contact customer service, who can do it remotely.

The direction for reaching China from abroad is unchanged.

## Pitfalls

- **A website will not open under split routing**: first check whether it is on the list. Websites not on the list connect directly, and if that website could not be opened in the first place, split routing will not help. Switch to "Global" temporarily to verify.
- **In China, a foreign website will not open**: untick "Blocked sites only" in the smart split routing section (or switch to "Global" temporarily) and try again. If it then opens, the site is blocked but not yet on the list; send the address to customer service.
- **Blocked websites will not open, but everything else works**: the device most likely has an encrypted DNS setting turned on (Android "Private DNS", the browser's "Secure DNS"), so the router cannot see which site it is looking up. Turn that setting off.
- **The printer or NAS cannot be reached after connecting**: this means local network addresses are being sent out as well. Check whether the split routing rules exclude private ranges such as 192.168.x.x.
- **Router performance** sets the ceiling. An old router's CPU maxes out on encrypted traffic, which shows up as the whole household slowing down. In that case the VPN line is not the problem.

## One account, one router

Most services bind the router to the account (by MAC address). One account is bound to one router, and you unbind first when switching routers. That way the account stays yours alone.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=router-03) team · Got questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=router-03) (groups, email and support are all listed there) · Sign up for a 4-hour free trial; invite a friend who pays and you each get 15 credits (about 15 Personal-plan days), valid long-term
