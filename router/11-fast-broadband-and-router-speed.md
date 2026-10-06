# 11 · Gigabit or 2 Gbps broadband with a router: what decides the speed

Home broadband keeps getting faster, so the question comes up a lot: my line is gigabit, or even 2 Gbps, so what will I get through a VPN router?

## The short answer

For the traffic that goes through the tunnel, the speed is decided by the leg that leaves China. **The bottleneck is not your home line, it is the leg that leaves China.** We promise smooth YouTube playback. The exact speed depends on the things below.

Traffic to Chinese services does not use the tunnel and still runs at your full broadband speed. See [10 · Will the NAS, printer and cameras be affected?](10-nas-printer-camera-behind-router.md)

## Four things that decide the speed

**1. The cross-border leg**
International capacity is shared by everyone and has nothing to do with how fast your home plan is. 8 to 11 pm Beijing time is the national peak; in that period pick a green-light region. If it is still slow, the usual cause is the local broadband (community broadband, or a carrier and region that do not match; see the next point). See [Why it is sometimes fast and sometimes slow](../network/06-why-sometimes-fast-sometimes-slow.md).

**2. Your carrier and the region you pick**
Each carrier leaves China by a different path, and picking the right region matters more than anything else:
- China Unicom in the north: try Japan and Korea first
- China Telecom in the south: try Southeast Asia first
- Other carriers: try the China relay regions first

**3. The router itself**
Traffic has to be encrypted before it enters the tunnel, and that is work for the router's processor. The models differ a lot:
- GL-MT300N-V2 (mini): 100 Mbps ports. Fine for 1080p on a phone or laptop, not a match for a fast line
- GL-MT3000 (portable): handles a small household. The first router for most people
- GL-MT6000 (desktop): 2.5G port. For many devices, 4K and game consoles

With a fast line and a busy household, choose the MT3000 or MT6000, not the mini.

**4. The last few metres at home**
Wire the TV and the desktop wherever you can. Wi-Fi in a crowded apartment block suffers heavy interference, and a lot of "the line is slow" turns out to be inside the home.

## When it feels slow, try these in order

1. Switch region. Try two or three and find the one that holds up at this time of day.
2. Turn on "Automatically pick the fastest line" in the admin page. It picks the line with the lowest latency and loss and switches when that changes. Note that the exit country may then differ from the region you chose.
3. Put the device you watch video on onto a cable.
4. Check whether it is only this one site. If other sites are fast at the same moment, the slow one is the far end's problem.

## How to know before you buy

Sign up and take the 24-hour free trial, no credit card needed. Connect at the time of day you use it most, the evening for instance, and watch a YouTube video in HD. What you see on a phone or laptop is close to what the router will give you. Decide about the router after that.

## FAQ

**Why not just tell me how many megabits?** Because the number is different for every person and every hour. We promise smooth YouTube playback, even at the evening peak, provided your broadband is good: China Unicom in the north or China Telecom in the south. Shared community broadband (小区宽带) is the exception. Taking the 24-hour free trial and trying it once yourself is the most accurate test.

**The speed test site shows a low number, but video plays fine?** That is normal. Speed test servers have busy and quiet moments of their own, and two tests a minute apart can differ by a factor of two. Judge by the thing you actually want to do.

**Will a more expensive router make it faster?** Only if the router is the bottleneck, for instance a mini model on a fast line. When the bottleneck is the cross-border leg, a new router does nothing and a different region does.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-11) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-11) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
