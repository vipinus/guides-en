# 03 · Web proxy: set up the ZeroOmega extension in two steps

> Website version (longer): https://www.leotun.com/guides/web-proxy?utm_source=github&utm_content=client-03

The web proxy sends only **this browser** through the line; other programs on the system are left alone. There is no client to install, no administrator rights are needed, and there is no "connected" state, so by design there is no connection to drop. It suits a company computer, a machine already connected to a company VPN, or cases where you want just one browser to use the line. For when to use it and when a VPN is required, see [Network guide 02](../network/02-choose-your-connection-method.md).

## Two steps

1. **Install the extension**: install ZeroOmega (the continuation of SwitchyOmega) in Chrome / Edge / Firefox. [The Proxy page on the website](https://www.leotun.com/httpproxy?utm_source=github&utm_content=client-03) has the install link for each browser.
2. **Import**: log in to the website and, on the Proxy page, click the flag of the region you want (or click "Copy import link for all regions" to import every region at once); that copies the settings link. Open the extension's "Import/Export", paste it into "Restore from online", and click "Restore". Regions, addresses and encryption method are imported in one go, with nothing to type by hand.

After that, click the extension icon and pick a region, then enter your website account and password in the login box the browser shows. To change region, click another one in the icon's menu; to go back to a direct local connection, switch to "Direct".

## For these cases, use a whole-machine method

- Video and music apps and players: most don't use the browser's proxy, so you get "web pages open but videos won't play".
- Phone apps, games and desktop software. The proxy settings in software such as Dropbox accept only unencrypted HTTP / SOCKS5, whereas in practice a proxy has to be encrypted, so this site's web proxy cannot be entered there. Use Hiddify to take over the whole machine instead; see [10](10-app-proxy.md).
- Watching Tencent Video or iQIYI from overseas: video sites also check IPv6 and DNS, which the web proxy does not cover; use a whole-machine VPN.

## FAQ

| Symptom | Cause |
|---|---|
| The login box keeps popping up | The account has expired or the password is wrong |
| Some sites won't open while others are fine | The "auto switch" rules in the extension have sent them direct; try global proxy mode once |
| In China, only HTTPS sites open | Plain HTTP gets rewritten in transit, and only encrypted connections get through; almost all sites are HTTPS nowadays |
| Slow | Switch region; the proxy and the VPN use the same set of servers |

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-03) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
