# 09 · How the router's split routing works

> Website version (longer): https://www.leotun.com/guides/router-smart-split?utm_source=github&utm_content=router-09

They are all called "smart split routing", yet some routers just feel awkward to use. For what split routing is, see [03](03-router-split-routing.md); this article only covers what split routing should do, the symptoms you see when part of it is missing, and how our router does it.

## In one sentence

What split routing should do: each website, **together with its images, video and login**, goes through the VPN or connects directly according to where it is located, and **every device in the house follows the same set of rules**. When only part of this is done, you see the symptoms below.

## Symptoms compared

| What you see | What is going on behind it |
|---|---|
| With split routing on, Chinese websites actually get slower | Chinese websites are mistaken for overseas ones and the whole thing detours abroad and back |
| The web page opens, but video keeps spinning, images do not appear, and login hangs | The list only contains the main site, and the same website's video, images and login take a different path |
| You are abroad with the line for reaching China on, and the video app still says "仅限中国大陆" (mainland China only) | Part of the traffic did not enter the VPN, and the website saw an overseas address |
| It plays on the phone but not on the TV or TV box; one computer simply will not go through the VPN | That device has its own network settings and bypasses the router |
| Banking and payment apps warn of a "login from another location" from time to time | The same app's traffic exits from China one moment and from abroad the next |
| Split routing disappears while you are using it (after a reboot or a reconnect either everything goes through the VPN or nothing does) | The setting was not remembered |

None of these **produces an error**. The router shows "Connected" the whole time, which makes them the hardest to troubleshoot, and many people end up thinking the line is no good.

## What split routing should do

- A website goes one way together with its web pages, images, video and login, without being split up
- When deciding "Chinese or overseas", it stands on the correct side, and Chinese websites take no detour
- Every device in the house follows the same rules, and network settings changed on the device itself cannot get around them
- The direction changes automatically with the chosen region (reaching China from abroad and reaching overseas services from China are two opposite sets of rules)
- The list updates itself, with no need to flash again
- Settings are remembered: unchanged after a reboot or reconnect; and once turned off, it is not quietly turned back on

## Smart split routing on our router

| | How it is done |
|---|---|
| Switch | On by default; choosing a region in China = the direction for reaching China from abroad, choosing an overseas region = the direction for reaching overseas services from China, applied automatically |
| List | Organised by "whole website": the web pages go together with the video, image and login sources they use |
| Chinese websites | In the direction for reaching overseas services from China they connect directly with no detour, at the same speed as without the router |
| Devices at home | Taken over uniformly; network settings changed on the device itself still follow the rules; there is no "back door" around the router |
| Updates | The list and rules update automatically when the router boots |
| Memory | Kept after a reconnect or reboot; once off, it stays off |
| Local network | Printers, NAS and cameras are reached directly as usual |

**The one case that needs your help**: when a phone or browser has an encrypted setting such as "Private DNS" or "Secure DNS" turned on, the device encrypts its own lookups and the router cannot see them. If a device misbehaves, turn off this kind of setting first.

## Verify it yourself

1. You are in China (reaching overseas services): Baidu and Taobao are at normal speed; overseas websites open and video plays.
2. You are abroad (reaching China): pick any episode on Tencent Video or iQIYI and it plays, with no "仅限中国大陆" (mainland China only) message; local bank and shopping websites work as usual.
3. Try every device, especially the TV and TV box; for one that misbehaves, check "Private DNS / Secure DNS" first, then confirm it is connected to this router's Wi‑Fi and not the modem's.
4. A website will not open under split routing: switch to "Global" temporarily. If it opens under Global but not under split routing, it is not on the list yet; send the address to customer service to have it added to the list, and it will be delivered with the automatic update.

## FAQ

**Do I need to turn on smart split routing myself?** No. It is on once you log in to your account and choose a region.

**Do reaching China from abroad and reaching overseas services from China need to be set up separately?** No. The direction is decided automatically by the chosen region.

**Will it affect printers or NAS?** No. Devices on the home network are reached directly as usual.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=router-09) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=router-09) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
