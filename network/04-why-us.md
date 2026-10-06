# 04 · How we differ from other VPNs

VPNs on the market fall roughly into three kinds: big international brands aimed at users worldwide, the "airport" services known in Chinese-speaking circles (resold subscription proxies), and all sorts of free software. LeoTun has run its own servers since 2007 and does only one thing: keeping the connection stable in both directions for users in mainland China and for overseas Chinese. This article does not boast about being "the fastest and most secure"; instead it sets us side by side with the three kinds of product, item by item, showing where we have the advantage and where we pay a price, so you can see clearly before paying.

## Our positioning in one sentence

We are a service **optimised specifically for the mainland China network environment**, not a reseller of international lines. The quality of the international exits of China Telecom, China Unicom and China Mobile differs greatly; we tune for each carrier separately and give different region recommendations. We have landing nodes inside China, so that users with mediocre broadband also have a stable entry point. We keep adjusting ports and protocols as the network environment in China changes, rather than setting things up and leaving them.

Conversely, when overseas Chinese need to reach services in China, they simply select the China region with the same account: Chinese sites go out from a China IP, while sites outside China still land outside China. Reaching China from abroad and reaching overseas services from China are two directions of the same thing.

## Compared with big international brands

- Their strengths: dozens of countries worldwide, thousands of servers, mature apps, independently audited no-logs claims. If you are in Europe or America and only want encryption on public Wi‑Fi or to watch another country's streaming media, they are a good choice.
- Their weaknesses: the product is not designed for the Chinese network. The signature of a proprietary protocol is fixed, and once it is identified inside China the whole app stops working; they have no landing nodes inside China, so for watching Chinese video from abroad they either lack the feature or use Hong Kong or Taiwan IPs, which Tencent Video and iQIYI block all the same.
- What we do: use only standard protocols (AnyConnect, OpenVPN, Hiddify, Tailscale, HTTPS web proxy), with clients that come from the vendors or the open-source community. What gets blocked can only be a particular address, and changing the address is enough; the client will not be taken down.
- The price we pay: only 24 regions, and far fewer servers than the big brands; no fancy app, and configuration takes a few more clicks (we cut this step as short as possible with QR-code scanning and one-click import); no third-party audit report; what we record and do not record is written on the About page, and we rely on spelling it out rather than on a stamp of approval.

## Compared with "airport" services

- Strengths of airport services: cheap, many nodes, usable as soon as you paste a subscription link, and people who like tinkering with clients enjoy the freedom.
- Weaknesses of airport services: most are individuals or small teams renting overseas machines and reselling traffic, with no landing in China of their own, and exit quality varies with the rented lines; disappearing with the money, renaming and shutting down are common, and paying for a year does not mean you get to use the full year; clients are almost entirely left to users to work out for themselves, and nobody is responsible when something goes wrong.
- What we do: the machines are our own, and the China exits are our own real-name-registered machines at mainland cloud providers; one account has six connection methods, and the whole-device router solution and the 24-hour support group are things airport services do not have; we have operated from 2007 to today, and accounts, validity periods and prices did not change before or after the rename.
- The price we pay: the unit price is higher than airport services (Personal plan $4 per month, Family plan $8, Enterprise plan $16); we do not offer hundreds of nodes for you to pick from. Behind each region the system picks the least busy machine; you choose the region, not the machine.

## Compared with free software

- Strengths of free: it costs nothing, and is enough for looking something up now and then.
- Weaknesses of free: mainland exit bandwidth is billed by usage, so a free service can only keep going by crowding users together, by throttling, or by selling data; browser-extension types only proxy web requests, and video, apps and system DNS do not go through them; installers of unknown origin are a risk in themselves, see "How to spot risky VPN software".
- What we do: the 24-hour free trial needs no credit card and is for checking the goods; pay-by-day (credits) is for occasional users; when a friend you invite pays, you get 30 days, which is a long-term source of free time.
- The price we pay: there is no permanently free plan. That is determined by the cost structure, and we do not pretend we can do it.

## Six connection methods, one account

Private network (Tailscale): log in once and stay online for good, and switch region from the menu. Cisco AnyConnect: the best compatibility, built into the system or with an official client. OpenVPN: for routers, NAS and Linux. Web proxy: only the browser goes through it, and it does not drop. Hiddify: resists packet loss, with the best speed. Router: whole-device access for TVs, set-top boxes and elderly relatives' devices.

No single method is optimal on every network, so we do not lock you into one: with the same account you switch at any time, from Hiddify to AnyConnect when a campus network restricts UDP, to the web proxy when the broadband is jittery. For how to choose, see "Which connection method suits which situation".

## Pros and cons in the account rules

- Accounts come in three plans, Personal, Family and Enterprise, with 2, 4 and 8 devices online at the same time respectively; regions, traffic and connection methods are the same on all three. There is no limit on how many devices you install on, only on the number of simultaneous connections. When the number online at the same time exceeds the plan's limit, you can temporarily upgrade the account type (remaining time is converted at equal value by price) and switch back when you are done.
- You can switch among the three plans at any time, with remaining time converted at equal value (Family and Enterprise are 2 times and 4 times the Personal price respectively); all three plans support the router, and the Personal plan is enough for a single user.
- Refunds are pro rata by time used and available at any time, and are handled manually; no specific arrival time is promised.
- Speed: we promise smooth YouTube playback, even at the evening peak. If one region is slow, switch region or connection method.
- The Hiddify and OpenVPN configurations carry your account, and changing the password revokes the old configurations. This is a security design, but it also means you have to re-import after changing the password.

## What we do not do

- We do not provide an anonymity service. We record the information needed for billing (email, plan, expiry time, and the duration and traffic of each connection); we do not record what you visit, do not inject ads, and do not sell data; client IPs do not leave our servers. But "not recording content" does not equal "anonymous", and the About page says this clearly.
- We do not make an app. Clients come only from the official upstreams of Cisco, OpenVPN, Hiddify and Tailscale, mirrored as-is without modification, so there is no such thing as "our app got taken down"; the price is one more configuration step than a one-click app.
- We do not pass off Hong Kong or Taiwan nodes as China-bound. The China region means mainland machines; the Hong Kong region was taken offline permanently in August 2026 because the local network environment had deteriorated, and we will not substitute Hong Kong or Taiwan IPs.

## FAQ

**Are you more secure than the big international brands?** The encryption strength is comparable; both use standard protocols. The difference is the trust model: the big brands rely on audit reports, and we rely on spelling out what we record and on not making an app. If you want anonymity, neither side is the answer; that is Tor's territory.

**Why not offer hundreds of nodes like airport services do?** More nodes does not mean more stable. Behind each of our regions there are several machines, and on connecting the system picks the least busy one, so you do not have to run speed tests and pick nodes yourself; when an address is blocked it is replaced automatically, and the address in your client does not need changing.

**Could the price be any lower?** The Personal plan is $4 per month, and the longer you buy the bigger the discount (5% off → 10% off → 20% off); by the day with credits it is about $0.32 a day; when a friend you invite pays, you get 30 more days, with no limit on the number of people. There is no permanently free plan; the cost structure does not allow it.

**How can I verify what you say?** Get the 24-hour trial, connect to the China region at the evening peak and watch an episode on Tencent Video, connect to an overseas region and open YouTube, and check the IP's registered location and an IPv6 test page. The checklist is in "How to choose a China-bound VPN".

**Who were you before the rename to LeoTun?** Before August 2026 we were called ViPiN: the same company, the same team, the same service. Accounts and prices did not change; only the name did.

## Further reading

- [Which connection method suits which situation](https://7d24hrs.com/guides/choose-connection?utm_source=github&utm_content=network-04)
- [How to spot risky VPN software](https://7d24hrs.com/guides/risky-vpn-apps?utm_source=github&utm_content=network-04)
- [China-bound VPN: free or paid](https://7d24hrs.com/guides/free-vs-paid?utm_source=github&utm_content=network-04)
- [About us: how it is built and what we record](https://7d24hrs.com/about?utm_source=github&utm_content=network-04)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/why-us?utm_source=github&utm_content=network-04

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=network-04) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=network-04) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; every friend you invite earns you 30 days, an offer with no end date
