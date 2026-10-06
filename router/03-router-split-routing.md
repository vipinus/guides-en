# 03 · What router split routing is

> Website version (longer): https://7d24hrs.com/guides/router-firmware?utm_source=github&utm_content=router-03

## In one sentence

Set up the VPN on the router, and every device in the house goes through it automatically once connected to Wi-Fi. Devices that cannot install a client, such as TV boxes, game consoles and printers, can use it too.

## What problem split routing solves

If all traffic goes through the VPN, you run into two problems: local websites become slow (they take a detour), and local devices become unreachable (printers, NAS and the router admin page are all on the local network, but the traffic has been sent out).

Split routing works by giving the router a list: domains on the list go through the VPN, and everything else connects directly. Chinese websites direct and overseas websites through the VPN, or the other way round, depending on where you are and which side you want to reach.

## Three modes

| Mode | Where traffic goes | When to use it |
|---|---|---|
| Global | Everything goes through the VPN | Temporarily, when troubleshooting |
| Split routing | Listed domains go through the VPN, the rest connects directly | Day to day |
| Direct | Nothing goes through the VPN | When you do not need it for a while |

## Pitfalls

- **A website will not open under split routing**: first check whether it is on the list. Websites not on the list connect directly, and if that website could not be opened in the first place, split routing will not help. Switch to "Global" temporarily to verify.
- **The printer or NAS cannot be reached after connecting**: this means local network addresses are being sent out as well. Check whether the split routing rules exclude private ranges such as 192.168.x.x.
- **Router performance** sets the ceiling. An old router's CPU maxes out on encrypted traffic, which shows up as the whole household slowing down. In that case the VPN line is not the problem.

## One account, one router

Most services bind the router to the account (by MAC address). One account can be bound to only one router, and you must unbind before switching routers. This is the usual way of preventing accounts from being resold.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-03) team · Got questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
