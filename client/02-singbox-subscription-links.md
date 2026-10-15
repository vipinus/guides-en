# 02 · How to Import a Subscription Link (Hiddify, Clash, Shadowrocket)

> Website version (longer): https://www.leotun.com/guides/singbox-subscription?utm_source=github&utm_content=client-02

The "subscription link" a proxy line provider gives you is simply an HTTPS address from which the client downloads a complete configuration: server, port and credentials are all in it, so nothing has to be typed by hand. LeoTun's Hiddify page gives you the same kind of thing, and gives it in three formats directly, so Hiddify, Clash and Shadowrocket each take their own and nothing needs converting.

## The three buttons in the popup

Log in to the website → Hiddify page → click a region's flag. A QR code pops up, with three buttons below it. The buttons are grouped **by subscription type**, not by operating system, so phone and computer show the same set:

| Clients named on the button | Subtitle | What clicking copies |
|---|---|---|
| Hiddify / sing-box / GUI.for.SingBox / Karing | sing-box subscription | On a phone, the `sing-box://import-remote-profile?url=…` import link, which launches the app; on a computer, the plain `https://…` config URL, for pasting. The configuration already contains routing rules and a rule that rejects IPv6, so there is no need to wrap it in a "subscription template" |
| Clash Meta / Clash Verge / FlClash / Stash / Mihomo Party / Clash Nyanpasu / ClashX Meta / OpenClash | Clash subscription | A Clash-format (YAML) subscription URL, to paste into the client's subscription / profile list |
| NekoBox / Shadowrocket / v2rayN / v2rayNG / Streisand / V2Box / Loon / Egern / Husi / NekoRay / Pharos Pro / Bedlam / Furious / daed / Lumen KVN / Kitty Pro | Share link | One `hysteria2://…` line, carrying the node only, with no routing rules |

- When the names don't fit on one line they scroll in a loop; that is normal.
- **Clicking a button also switches the QR code above to that type**, so the matching client can scan it. When the popup first opens the QR code is the Hiddify / sing-box one, and other clients scanning it directly get "Invalid QR code": click your client's button first, then scan or paste.
- The "Import all regions · auto-select" popup at the top of the page has only the first two buttons, with no share link.

**Subscription conversion**: third-party websites that convert one format into another. LeoTun gives you all three formats directly, so **no conversion is needed**; handing a link that contains your credentials to a conversion site amounts to handing your account to a third party, so don't do it.

## Hiddify / sing-box family: the first button

1. Install Hiddify (Android: the website's download page or Google Play; iOS: App Store; the desktop app covers Windows / macOS / Linux). The sing-box core is built in.
2. Click a region's flag, and the QR code pops up.
3. Phone: tap the first button and switch to Hiddify, which will offer to add it from the clipboard; or use "Scan QR code" in Hiddify on another device. Computer: click the same button, which copies an https:// address, then in Hiddify "+" → "Add from clipboard", and save.
4. Tap connect and allow the VPN permission the first time. To add a region, click another flag; each region is a separate profile.

## Clash family: the second button

For Clash Meta (mihomo), Clash Verge, FlClash, Stash and the like, click the "Clash subscription" button and paste the copied URL into the client's subscription / profile list. No subscription converter is needed.

**Clash-family clients must not use the share link**: they cannot import a single `hysteria2://` line as a profile.

## Other clients: the third button

Click the "Share link" button, then use "Import from clipboard" in NekoBox / Shadowrocket / v2rayN / v2rayNG and so on, or scan the QR code above after clicking the button. A share link carries no rules, so you have to set up routing and IPv6 yourself: if you are overseas and want to watch content from China, route Chinese domains through the node and turn IPv6 off.

The clients listed after v2rayN on the button all support hysteria2, but the share link uses an extended hysteria2 format that a few clients cannot parse; if the import fails or it won't connect, switch to Hiddify.

## Clients that cannot be used

| Client | Why |
|---|---|
| Surge | Supports hysteria2 but only reads its own config format, so none of the three types fit |
| Quantumult X | Does not support this kind of line |
| The original Clash, Clash for Windows | The core lacks hysteria2; use a mihomo-core client instead |

## Does the subscription expire?

- **It does not expire with time.** The token in the subscription URL is tied to your account and keeps working for as long as the account is valid; renewing or changing plan does not require re-importing.
- **Changing your password invalidates the old URL immediately.** This is how you revoke access if a phone is lost or a link leaks; after changing it, scan the code again.
- **After the account expires** the URL returns 401; once you renew, the existing profile doesn't need replacing.
- **Profiles imported before September 2026** lack the rule that rejects IPv6; delete them and import again.

If you have imported it but can't connect, see [Troubleshooting 04](../troubleshooting/04-singbox-import-not-connecting.md).

## FAQ

**What is the difference between a Hiddify subscription and a Clash subscription?** The format differs (JSON vs YAML), and each client does not recognise the other's subscription, but the nodes themselves work with both. LeoTun gives you both directly: Clash-family clients click the "Clash subscription" button and must not use the share link.

**Can one profile contain all regions?** Importing from a flag gives one profile per region, and you switch between them in the client's profile list; that way, a change of address for one region affects only that region. To import all regions outside China at once and let the client choose automatically, click "Import all regions · auto-select" at the top of the page (it has only the sing-box subscription and Clash subscription buttons).

**Can I send the QR code to my family?** The QR code contains your account credentials; whoever you send it to gets your account. Sharing with family is allowed (simultaneous devices by plan: Personal 2, Family 4, Enterprise 8), but don't post it anywhere public; if it leaks, change your password and it stops working.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-02) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-02) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite a friend who pays and you each get 20 Personal-plan days, an ongoing offer
