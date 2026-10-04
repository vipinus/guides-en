# 04 · Hiddify imported but won't connect

> Website version (longer): https://7d24hrs.com/guides/singbox-subscription

Match your error to the table. For how to import in the first place, see [How to use Hiddify subscription links](../client/02-singbox-subscription-links.md).

| Symptom | Cause | What to do |
|---|---|---|
| "Unable to fetch subscription", 401 | The account has expired, or the password was changed (changing the password invalidates old configurations immediately; this is by design) | Log in to the website and check the validity period; after renewing or changing the password, scan the QR code again |
| Import succeeds, connection times out | The address for that region has just been changed, or that entry point is being interfered with by the carrier | Tap "Update subscription" in the client to pull the latest configuration; switch to another region — each region is a separate configuration and they do not affect each other |
| Connected but no internet | The client's own routing rules are sending traffic to "direct" | Change the default outbound to that node, or delete the rules you added yourself |
| Scanning says "Invalid QR code" | The QR code is meant for Hiddify-family clients; or it was scanned from someone else's screenshot | For Shadowrocket / NekoBox / Stash use the "share link"; the QR code contains your own credentials, and someone else's will not work |
| Slow speed | Cross-border congestion at the evening peak | Look at the red, yellow and green lights in the region list on the website and switch to a region with a green light |
| Clicking the import link on desktop does nothing | On Windows / Linux, the sing-box:// deep link cannot always launch the app | Copy the "config URL" (starting with https://) and paste it into Hiddify to import |

## Do I need to re-import after renewing, switching plans, or changing the password

- **Renewing or switching plans (Personal / Family / Enterprise)**: No. The existing configuration keeps working.
- **Changing the password**: The old configuration stops working immediately; scan the QR code again. If you lose your phone or the link leaks, use this to revoke access.
- **Account expired**: The configuration returns 401. After renewing you do not need a new configuration; just reconnect.
- **Imported before September 2026**: The rule that rejects IPv6 is missing, so watching Chinese video from abroad will show a copyright restriction notice. Delete and re-import; see [03](03-ipv6-and-dns-leak.md).

## When to contact support

Tell support three things: the client name and version, the region, and the exact error text or a screenshot.

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
