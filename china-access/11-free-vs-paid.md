# 11 · China-bound VPN: free or paid

Do the sums first: the most expensive part of a China-bound line is the bandwidth at the mainland exit, which cloud providers inside China charge for by traffic, and not cheaply. A free option cannot work magic. It can only pick one of three: squeeze many people onto one machine, set limits on traffic and time, or earn the money back from your data and ads. This does not mean free can never be used; for looking something up now and then it is enough. But for following series, doing online banking or setting things up for family, a month of a paid line usually costs less than a cup of coffee, and the time it saves is worth far more than that.

## Three reasons free nodes keep dropping

- Crowded: hundreds or thousands of people share one machine and one cross-border line. It is fine during the day, and from 8 to 11 pm Beijing time everyone is left spinning.
- Capped: it cuts off when the traffic runs out, cuts off when the time runs out, holds the speed below 1080p, and pops up a window halfway through asking you to pay. These are really trial versions of paid products that just do not say so.
- Sold: it keeps going by injecting ads, collecting browsing history, or using your device as someone else's exit node. This is especially common with free "China-bound" browser extensions.

## Two more pitfalls of free options that you cannot see

First, the exit is not necessarily in the mainland. Quite a few free "China-bound" nodes are in fact Hong Kong, Taiwan or Japan addresses. They can open Chinese web pages, but Tencent Video and iQIYI still show a copyright restriction, and online banking also treats you as overseas. Look up where the IP is registered once after connecting and you will know.

Second, IPv6 and DNS are not handled. Free options almost never reject IPv6 inside the tunnel, and when your device has IPv6 the video site still sees an overseas address. This is the most common reason for "it is clearly connected but I still cannot watch"; see "What to do when Tencent Video shows a copyright restriction notice abroad".

## When free is enough, and when you should pay

Enough: occasionally opening a Chinese web page to look something up or read the news, with no demands on speed or stability, and without logging in to any account on it.

Time to pay: you want to watch series and listen to music, log in to online banking or Alipay, set it up for the TV and the elderly at home, or grab tickets at a fixed time. What these situations need is "it works every time", and a free option cannot give that.

A simple test: if you would be annoyed when it drops, it is time to pay.

## How much to spend

LeoTun's Personal plan is 4 US dollars a month and includes 24 regions, 2 devices online at the same time, and all connection methods — AnyConnect / OpenVPN / Hiddify / web proxy — and it can also be used with a router. The Family and Enterprise plans cost 2 times and 4 times the Personal plan respectively. Regions, lines and connection methods are exactly the same on all three plans, and the only difference is the number of devices online at the same time (4 and 8).

If you do not want to buy by the month, there are two routes: first claim the 24-hour free trial (no credit card needed, once per account) and try it once at the evening peak; or pay by the day. After topping up credits, the Personal plan costs 1 credit a day, and 25 credits cost 8 US dollars, which works out at about 0.32 US dollars a day; buying just a few days before a trip back to China fits well.

When a friend you invite signs up and pays for the first time, your validity is extended by 30 days, with no limit on the number of people. This is a long-term source of free time.

## How to check the goods before paying

1. Claim the trial, connect to the China line, and look up whether the IP is registered in mainland China.
2. Open an IPv6 test page and confirm that IPv6 is unavailable or is also a mainland address.
3. Play one episode in 1080p after 8 pm Beijing time and see whether it buffers repeatedly.
4. Switch to another China exit and try once more, to confirm it was not luck.
5. See whether it uses standard protocols (AnyConnect, OpenVPN, Hiddify): the clients come from the vendor or the open-source community, and if the provider folds the configuration can still be used elsewhere; with a proprietary app, once it is taken down there is nothing left.

## FAQ

**Is there a China-bound VPN that is truly free and also stable?** Not one that is stable long-term; the cost structure decides that. Stable and free exists only in the trial period of a paid product. Using it to check the goods is right; counting on it for long-term use is not realistic.

**Will a free VPN steal my passwords?** It cannot see HTTPS content inside the tunnel, but it can see which domains you visit and can inject content into plaintext pages. Free proxies of the browser-extension kind have even broader permissions. Do not log in to online banking on a free line.

**Which is better value, paying by the day or by the month?** If you use it 12 days or more a month, monthly is better value; if you use it a few days now and then, by the day is. Credits do not expire, and one top-up lasts a long time.

**Does the trial require a credit card?** No. Claim it on the home page after signing up: 24 hours with all features, once per account.

**I paid and it still drops. What do I do?** Switch region first, then switch connection method (all three protocols can be used on the same account); if it still does not work, read the troubleshooting guide or contact support. Part of the point of paying is that someone is responsible.

## Further reading

- [Pricing and free trial](https://www.leotun.com?utm_source=github&utm_content=china-access-11)
- [How to choose a China-bound VPN](https://www.leotun.com/guides/choose-china-vpn?utm_source=github&utm_content=china-access-11)
- [What to do when Tencent Video shows a copyright restriction notice abroad](https://www.leotun.com/guides/overseas-video?utm_source=github&utm_content=china-access-11)
- [How overseas students should set up a China-bound VPN](https://www.leotun.com/guides/students?utm_source=github&utm_content=china-access-11)

Website version of this article (also in Traditional Chinese and English): https://www.leotun.com/guides/free-vs-paid?utm_source=github&utm_content=china-access-11

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=china-access-11) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=china-access-11) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
