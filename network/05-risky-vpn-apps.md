# 05 · How to spot risky VPN software

All of your traffic passes through the hands of a VPN app, and it can look at whatever it wants. Two kinds of thing on the market call for particular caution: one is what people in these circles call a "red VPN", which has a regulatory background, demands your real identity in the name of compliance, and hands over the records; the other is the free accelerator of unknown origin, which makes money from your data, your device, or something it plants. What the two have in common is that "it works fine in use"; the problem lies where you cannot see it. Below are ten signals you can verify yourself, what to do if you have already installed one, and a three-minute self-check.

## Why VPN software is riskier than an ordinary app

A VPN works at system level: it gets the traffic of every program on the device, including those you do not know are running in the background. An ordinary app leaks the data it collected itself; a VPN leaks everything you do on that device. So the standard for choosing VPN software must be much stricter than for choosing an ordinary app.

"I used it and nothing happened" is not evidence of safety. Recording, reporting and injection all happen on the server side or in the background and cannot be felt on the user side; when something does go wrong it is often months later, and it cannot be traced back to which piece of software it was.

## Ten signals

- Unknown source: the installer comes through a group chat, a cloud drive or a QR code, with no official website or app store page. A legitimate client comes either from an app store, from the developer's official website, or from a release page where the signature can be checked.
- Asks you to install a root certificate: during installation it asks you to "trust the certificate" or "install the profile" and requires trusting a CA. Once the root certificate is installed, it can open up all your HTTPS traffic, including online banking and email. A normal VPN does not need this step.
- Too many permissions: a VPN asking for contacts, SMS, call logs, precise location, and access to the photo library. A VPN only needs the permission to set up a tunnel; it has no use for the rest.
- Requires real-name registration: signing up needs an ID card, a face scan, or binding a mainland China mobile number. This is how a so-called compliant VPN ties your identity to your traffic records; a legitimate service only needs an email address.
- Proprietary protocol + closed-source client: you can only use its own app, and it supports no standard protocol (AnyConnect, OpenVPN, WireGuard, Hiddify), so you cannot use a third-party open-source client to verify what it actually transmits.
- Free, with no visible source of income: no paid plan, no ads, no business customers, yet it runs year after year. Mainland exit bandwidth is billed by usage, and a service that does not charge always gets it back somewhere else.
- No company, no support, no history: the operating entity cannot be found, there is nobody to contact, the domain was registered less than a year ago, and it frequently changes its name and its shell.
- Abnormal background traffic: the device keeps uploading even when you are not using it, and battery and data drain quickly. It may be using your device as someone else's exit, or syncing your data.
- Its promotion stresses "official", "registered", "legal and compliant" and hints that everything else is illegal: this is the most typical pitch of a "red VPN", and its compliance consists of recording and reporting.
- App store ratings are one-sided, the reviews read alike, and the number of downloads is out of proportion to the number of reviews: they are faked.

## How to verify

1. Look at the protocol: whether the official website states which protocol it uses and whether a third-party client can be used. With a service you can connect to using open-source or standard clients such as OpenVPN, AnyConnect, Hiddify and Tailscale, you can capture packets yourself and see what is transmitted.
2. Look at the permissions: after installing, go to system settings to see which permissions it requested, turn off everything other than VPN, and see whether it still works. If it does not, uninstall it.
3. Look at the certificates: iOS Settings → General → VPN & Device Management; Android Settings → Security → Encryption & credentials → Trusted credentials → User; "Trusted Root Certification Authorities" in the Windows certificate manager. If there is a certificate it installed, delete it and uninstall the app.
4. Check for leaks: after connecting, open a DNS leak test and an IPv6 test page to see whether resolution and address both go through its servers; then open an HTTPS website and see whether the certificate issuer is the original CA.
5. Check the entity: whether the official website has an introduction to the company or team, how many years it has operated, and where support is; whether refund rules are written down; whether the privacy policy states clearly what is recorded.

## What to do if you have already installed one

1. Uninstall the software, then check the locations mentioned above and delete the certificates and profiles it installed.
2. Change passwords: online banking, email, frequently used accounts, especially those you logged in to while using it.
3. For accounts with two-step verification turned on, check the login history and remove any unfamiliar device.
4. If it was installed on a router, restore factory settings and then reflash official or trusted firmware.

## How we let you verify

LeoTun does not make its own app: clients come only from the official upstreams of Cisco, OpenVPN, Hiddify and Tailscale, mirrored as-is without modification, and you can replace the copy downloaded from this site with the official or open-source client at any time. The protocols are all standard protocols and can be verified by packet capture.

Signing up needs only an email address, no phone number and no ID card. What we record and do not record is written on the About page: email, plan, expiry time, and the duration and traffic of each connection are used for billing; we do not record what you visit, do not inject ads, and do not sell data.

We do not install certificates and do not ask for contacts or location. If one day our client asks you to install a root certificate, it is definitely not us.

## FAQ

**Is everything free unusable?** The clients from the open-source community (OpenVPN, Hiddify, Tailscale) are themselves free and trustworthy; the risk lies in a "free service", not in "free software". With a free service, look at what it lives on.

**Is something safe because it is listed in an app store?** Being listed only shows that it passed the store's automated review; it does not mean the server side does not record. Look at permissions, real-name registration, protocol and entity among the ten signals above; the store itself does not check these for you.

**What is a so-called "red VPN"?** The name used in these circles for a VPN that has a regulatory background, requires real-name registration in the name of compliance, and retains records. They usually promote themselves as "official" and "legal" and work normally in use; the problem is that your identity and all your traffic records are tied together.

**How can I tell whether a VPN has recorded my content?** You cannot tell from the user side; you can only look at how many means of verification it gives you: whether the protocol is standard, whether the client is open source, whether the privacy policy is specific, whether the operating entity can be looked up. If it has none of the four, treat it as recording.

**Does router firmware carry this kind of risk too?** Yes; "firewall-bypass firmware" of unknown origin can hijack the entire home network. Flash only official OpenWrt or firmware whose source can be checked; this site's firmware is compiled from OpenWrt, with only the components for connecting to the line and the split-routing rules added.

## Further reading

- [How we differ from other VPNs](https://7d24hrs.com/guides/why-us)
- [China-bound VPN: free or paid](https://7d24hrs.com/guides/free-vs-paid)
- [What to do when Tencent Video shows a copyright restriction overseas](https://7d24hrs.com/guides/overseas-video)
- [About us: how it is built and what we record](https://7d24hrs.com/about)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/risky-vpn-apps

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Join the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; every friend you invite earns you 30 days, an offer with no end date
