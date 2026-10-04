# 02 · Hiddify subscription links, import links and share links: what they are, and whether you need "subscription conversion"

> Website version (longer, also in Traditional Chinese and English): https://7d24hrs.com/guides/singbox-subscription

A Hiddify "subscription" is simply an HTTPS address from which the client downloads a complete configuration: server, port, credentials and routing rules are all in it, so nothing has to be typed by hand. After logging in to the website, LeoTun users get a separate QR code and profile URL for each region.

## Three kinds of link

| Link | What it looks like | Who it is for |
|---|---|---|
| Profile URL (subscription link) | `https://…` | Recognised directly by the official Hiddify app and GUI.for.SingBox. The configuration already contains routing rules and a rule that rejects IPv6, so there is no need to wrap it in a "subscription template" |
| Import link (deep link) | `sing-box://import-remote-profile?url=…` | Tap it to launch the app and add the profile automatically. This is what the QR code contains |
| Share link | `hysteria2://…` | One line of text describing a single node, with no rules. For clients that don't read Hiddify JSON, such as NekoBox, Shadowrocket, Stash and Clash Meta |

**Subscription conversion**: third-party websites that convert one format into another. LeoTun gives you both formats directly, so **no conversion is needed**; handing a link that contains your credentials to a conversion site amounts to handing your account to a third party, so don't do it.

## Phone: scan the code or tap to import in Hiddify

1. Install Hiddify (Android: the website's download page or Google Play; iOS: App Store). The sing-box core is built in.
2. Log in to the website → Hiddify page → click a region's flag, and a QR code appears.
3. On the same phone: tap "Copy import link" and switch to Hiddify, which will offer to add it from the clipboard. On another device: use "Scan QR code" in Hiddify.
4. Tap connect and allow the VPN permission the first time. To add a region, click another flag; each region is a separate profile.

## Desktop: paste the profile URL

1. Install the Hiddify desktop app (Windows / macOS / Linux).
2. On the website, click a flag → "Copy profile URL". The desktop gets an https:// address rather than a deep link, because on Windows / Linux a deep link doesn't always launch the app, whereas pasting works everywhere.
3. In Hiddify, "+" → "Add from clipboard", save, connect.

## Other clients

Click "Copy share link (other clients)", then use "Import from clipboard" in NekoBox / Shadowrocket / Stash / Clash Meta. A share link carries no rules, so you have to set up routing and IPv6 yourself: if you are overseas and want to watch content from China, route Chinese domains through the node and turn IPv6 off.

## Does the subscription expire?

- **It does not expire with time.** The token in the profile URL is tied to your account and keeps working for as long as the account is valid; renewing or changing plan does not require re-importing.
- **Changing your password invalidates the old URL immediately.** This is how you revoke access if a phone is lost or a link leaks; after changing it, scan the code again.
- **After the account expires** the URL returns 401; once you renew, the existing profile doesn't need replacing.
- **Profiles imported before September 2026** lack the rule that rejects IPv6; delete them and import again.

If you have imported it but can't connect, see [Troubleshooting 07](../troubleshooting/04-singbox-import-not-connecting.md).

## FAQ

**What is the difference between a Hiddify subscription and a Clash subscription?** The format differs (JSON vs YAML), and each client does not recognise the other's subscription, but the nodes themselves work with both. For Clash Meta, use the share link.

**Can one profile contain all regions?** At present there is one per region, and you switch between them in the client's profile list. That way, a change of address for one region affects only that region.

**Can I send the QR code to my family?** The QR code contains your account credentials; whoever you send it to gets your account. Sharing with family is allowed (simultaneous devices by plan: Personal 2, Family 4, Enterprise 8), but don't post it anywhere public; if it leaks, change your password and it stops working.

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
