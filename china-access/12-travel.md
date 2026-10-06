# 12 · How to set up for business trips and travel

For a short trip abroad or a business trip back to China you do not need a router or to study protocols: install the Cisco client (Cisco Secure Client) on your phone, try connecting once before you leave, and it works as soon as you land. The two directions are the same thing: abroad, when you need Google, company email and maps, choose a nearby overseas region; back in China, when you want to watch Chinese video and log in to online banking, choose the China region. This article covers ten minutes of preparation before you leave, two common pitfalls of hotel and airport networks, and how to use online banking and payment apps.

## Ten minutes before you leave

1. Install Cisco Secure Client on your phone (App Store / Google Play, or the installer from the Cisco page on this site), log in to this site and click a flag to copy a region's address and enter it, then connect once with your account and password for this site to confirm it works.
2. Copy the addresses of two more regions and save them in the client: one near your destination and one as a backup. The network there will be different, and the best region is often not the same.
3. Note down the three domains (7d24hrs.com → 7x24btc.com → anyfq.com) and the entry to at least one support group, so that you can find someone if something goes wrong in a place where you do not know the network.
4. Install one on your laptop as well, or use the web proxy extension; when a company computer cannot install a client, it still works.

## After you land

- If you have switched to a local SIM or turned on roaming, the client just connects and no reconfiguration is needed; if the roaming data itself already leaves the country, connecting to the line is only for fixing the exit region.
- Abroad, when you need Google, Gmail, company email and maps: choose a nearby overseas region for the best speed.
- Back in China, when you want to watch Tencent Video and iQIYI, listen to NetEase Cloud Music or log in to online banking: choose the China region. Chinese sites go out from a China IP and overseas sites still land overseas, so connecting to the China region while in China does not stop you from carrying on with Gmail.
- If an overseas region will not connect from inside China: switch region, switch to mobile data, and if that still fails switch to Hiddify or OpenVPN; blocking of the three protocols is independent of one another.

## Two pitfalls of hotel, airport and café networks

- Login portal (captive portal): after connecting to the Wi‑Fi, complete authentication in the browser first, then turn on the line. A client set to connect automatically will try before authentication and fail; wait a moment or reconnect manually.
- UDP restrictions: quite a few hotel and airport networks throttle or block UDP. Cisco runs over TLS and is not affected, which is also why Cisco is the first recommendation for travel; if you are using Hiddify or Private network and it is slow or drops, switch to Cisco.

## Online banking, payments, 12306

These apps record the login IP, and jumping back and forth between overseas and China is what triggers risk control most easily. When you need to get something done, connect to the China region first and then open the app; when you are done, quit the app and then disconnect. While travelling, do not use the same online bank while switching frequently between the two kinds of network.

SMS verification codes that never arrive have nothing to do with the line; it is a roaming issue with the phone number. Before you leave, turn on roaming for your Chinese number or change to a plan that can receive codes overseas.

## FAQ

**The trip is only a few days. Do I need to buy a month?** No. Claim the 24-hour free trial, or top up credits and pay by the day: the Personal plan costs 1 credit a day, about 0.32 US dollars a day, which fits a few days well.

**Can my phone and laptop connect at the same time?** Yes. Depending on the plan, one account has 2 / 4 / 8 devices online at the same time (Personal / Family / Enterprise), and the Personal plan is exactly one phone plus one laptop.

**Why is Cisco recommended for travel rather than Hiddify?** On an unfamiliar network the biggest worry is restricted UDP. Cisco runs over TLS, the same as visiting an HTTPS website, and gets through almost anywhere; Hiddify is faster on networks with high packet loss, but does not work when UDP is restricted. Installing both and switching when one does not work is the most reliable.

**Will using the China region abroad make local sites slower?** Local sites are smoothest on a direct connection: disconnect once you have finished with the Chinese content, or connect only when needed.

## Further reading

- [Cisco AnyConnect download and setup](https://7d24hrs.com/anyconnect?utm_source=github&utm_content=china-access-12)
- [How overseas students should set up a China-bound VPN](https://7d24hrs.com/guides/students?utm_source=github&utm_content=china-access-12)
- [How to contact us and how not to lose touch](https://7d24hrs.com/guides/stay-in-touch?utm_source=github&utm_content=china-access-12)
- [China-bound VPN: free or paid](https://7d24hrs.com/guides/free-vs-paid?utm_source=github&utm_content=china-access-12)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/travel?utm_source=github&utm_content=china-access-12

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=china-access-12) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=china-access-12) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
