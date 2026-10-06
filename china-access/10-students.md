# 10 · How overseas students should set up a China-bound VPN

What overseas students need is not "a China-bound line that is always connected", but to be able to get a China IP reliably in a few specific situations: following series and listening to music, logging in to online banking and government apps, grabbing tickets, and occasionally checking on devices remotely for family at home. Each situation asks something different of the line, and campus networks have limits of their own. This article explains, situation by situation, what is needed, how to set it up and when to disconnect, and ends with a checklist that can be done in ten minutes before term starts.

## Series, music, live streams: a China IP is all you need, but IPv6 must be closed off

Tencent Video, iQIYI, Bilibili anime, NetEase Cloud Music and QQ Music all judge region by source IP, and connecting to the China line is enough. The pitfall overseas students fall into most often is that campus and dormitory networks commonly have IPv6: the device prefers IPv6, which is not going through the line, so the video site still sees an overseas address and shows "copyright restriction".

The fix is to use a line or client that rejects IPv6 inside the tunnel, or to turn off IPv6 on the device. All three of LeoTun's connection methods already block IPv6 on the line side, with no need to change the device; for detailed troubleshooting see "What to do when Tencent Video shows a copyright restriction notice abroad".

Picture quality depends on cross-border bandwidth. From 8 to 11 pm Beijing time is the peak, which corresponds to morning through midday in Europe and North America; if 1080p keeps spinning in that period, switch to another China exit.

## Online banking, Alipay, government apps: log in over the China line, and disconnect when done

The various banking apps, Alipay, CHSI and the National Government Service Platform differ in how they treat overseas IPs: some refuse the login outright, some put up several extra verification steps, and some let you log in but trigger risk control on a transfer. What they have in common is that they record your login IP, and jumping back and forth between overseas and China is what gets you flagged most easily.

What to do: when you need to do these things, connect to the China line first and then open the app; when you are done, quit the app and then disconnect the line. Do not use the same app while switching frequently between the China line and the local network.

Phone verification codes that never arrive have nothing to do with the line; it is a roaming issue with a Chinese phone number overseas. Before leaving the country, turn on international roaming for the number or change to a plan that can receive codes overseas.

## 12306, concert ticket rushes: connect in advance, and do not switch at payment

12306 sometimes asks for extra verification from an overseas IP, and in a ticket rush one extra verification means the ticket is gone. A few minutes before sales open, connect to the China line, log in and select the passenger details, then submit as soon as the time comes. When payment redirects to Alipay or online banking, keep the line unchanged.

The same reasoning applies to ticketing platforms such as Damai and Maoyan.

## Three limits of campus and dormitory networks

- IPv6: see above; use a line that blocks IPv6.
- UDP restricted or throttled: quite a few campus networks throttle or even block UDP traffic. The hysteria2 that Hiddify uses runs over UDP, and on such networks it is actually less stable than AnyConnect, which runs over TLS; one account can use both, so if UDP does not work, switch to AnyConnect.
- Login portal (captive portal): after connecting to campus Wi‑Fi, complete authentication in the browser first, then turn on the line. If the line client is set to "connect automatically at startup", it will try to connect before authentication and fail; wait a little longer or reconnect manually.

## Going back to China for the holidays: the same account used the other way round

Back in China you need Google, your university email and paper databases; just change the line's region from China to Japan, the United States or a nearby overseas region, and there is no need to change accounts. LeoTun's 24 regions are all in the same account, and reaching China from overseas and reaching overseas from China are two directions of the same thing.

When connecting from inside China, the AnyConnect and Hiddify addresses change automatically to cope with blocking, and the addresses saved in the client do not need to be changed; if it will not connect, switch region or switch protocol.

## Ten-minute setup checklist before term starts

1. Install a client (AnyConnect or Hiddify) on your phone and one on your computer, and log in or import by scanning the QR code on each.
2. Connect to the China line on the dormitory Wi‑Fi and open an IPv6 test page to confirm that IPv6 is unavailable or shows a mainland address.
3. Open Tencent Video and play any episode to confirm that no copyright restriction is shown.
4. Log in to your banking app once to confirm you can get in, then quit the app and disconnect the line.
5. Note down the line provider's support contact; when something goes wrong, read the troubleshooting guide first and then ask.

## FAQ

**Will using a China-bound VPN affect an overseas student's university network account?** No. The line only sends your traffic to a China exit, and what the campus network sees is one encrypted connection. Most universities' usage rules prohibit only infringing downloads and attacks, and personal access to services in your own country is not among them; if you are unsure, take a look at the university's acceptable use policy.

**Can one account be shared with a roommate?** Depending on the plan, one account can have 2 (Personal), 4 (Family) or 8 (Enterprise) devices online at the same time, and sharing with family or roommates is within what the rules allow. But for situations like online banking it is safer for each person to use their own account, to avoid several people switching frequently on the same line and triggering risk control.

**Why is Hiddify slow in the dormitory while AnyConnect is normal?** Most likely the campus network restricts UDP. Hiddify's hysteria2 protocol is based on UDP, and when throttled it shows up as slow or dropping; AnyConnect runs over TLS, the same as visiting an HTTPS website, and is not affected.

**Can I play China-server games over a China-bound line?** You can log in, but latency depends on your physical distance to the China exit. Connecting back to China from North America is usually 150 to 250 milliseconds, which is acceptable for turn-based games and MOBAs and noticeable in shooters.

**Is the account still useful after I graduate and return to China?** Yes. The same account keeps working inside China with an overseas region, for reaching Google, GitHub, your university email and paper databases.

## Further reading

- [What to do when Tencent Video shows a copyright restriction notice abroad](https://7d24hrs.com/guides/overseas-video?utm_source=github&utm_content=china-access-10)
- [How to choose a China-bound VPN](https://7d24hrs.com/guides/choose-china-vpn?utm_source=github&utm_content=china-access-10)
- [AnyConnect client download](https://7d24hrs.com/anyconnect?utm_source=github&utm_content=china-access-10)
- [Hiddify client and subscription import](https://7d24hrs.com/singbox?utm_source=github&utm_content=china-access-10)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/students?utm_source=github&utm_content=china-access-10

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=china-access-10) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=china-access-10) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
