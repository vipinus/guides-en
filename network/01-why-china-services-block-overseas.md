# 01 · How reaching China from abroad works

## What you see

You are overseas and open iQIYI, Bilibili or NetEase Cloud Music, and you are told "This content is only available in mainland China"; online banking and 12306 simply will not open, or the verification code never arrives.

## There is only one cause: where your IP is registered

When your device goes online, your carrier gives it a public IP address. There is a worldwide register for these addresses that shows which country and which carrier each one belongs to. Chinese video and music platforms buy rights for **mainland China** only and are not legally allowed to stream outside it, so they refuse as soon as they see an overseas IP.

Banks and ticketing sites follow a different logic. For them it is not about copyright but risk control: a login from an overseas IP is treated as high risk and blocked outright.

## The approach to solving it

Make the IP the server sees a mainland China one. This is done by first sending your traffic to a server located in the mainland, which then visits the target site on your behalf. The target site sees that server's IP and lets it through.

That is what a "China-bound line" does: it sends your traffic out from a mainland China IP.

## Three common misconceptions

- **Changing DNS does not help.** DNS only translates domain names into addresses; the target site looks at your source IP, not the DNS you use.
- **A few platforms also look at the system region.** Besides IP, some platforms also check the device language and the app store region; in that case change the system region as well.
- **Speed depends on the quality of the line between the two points.** The cross-border link from overseas to the mainland is the bottleneck, so choosing an entry point that is close to you and has an optimised line to the mainland matters more than the server's own specifications.

## Further reading

- [Which connection method suits which situation](02-choose-your-connection-method.md)
- [Checklist for cannot connect, slow, and dropped connections](../troubleshooting/01-cannot-connect-slow-drops.md)

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=network-01) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=network-01) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; every friend you invite earns you 30 days, an offer with no end date
