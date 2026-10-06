# 04 · Using a company computer: no administrator rights, already on the company VPN

A company computer has three restrictions: you cannot install unapproved software, you have no administrator rights, and it is often already connected to the company VPN. A whole-device VPN here either cannot be installed or fights with the company VPN. The right tool is the web proxy — a browser extension that sends only this browser's requests through the line, while the company intranet, the email client and the company VPN all stay exactly as they are, and no administrator rights are needed. This article covers how to set it up, what it can do, what not to do, and how to get along with the company's IT policy.

## Why the web proxy

- No client to install: it is only a browser extension, and most companies allow extensions but not software.
- No administrator rights: the extension runs in user space and does not change the system's network settings.
- Coexists with the company VPN: the company VPN takes over the system routes, while the web proxy sits only at the browser layer, so the two do not interfere; company intranet pages keep going through the company VPN.
- By design there is no connection to drop: the proxy works per request with no long-lived connection, so you do not notice jitter on the company network either.

## Set up in two steps

1. Install the ZeroOmega extension (the continuation of SwitchyOmega) in the browser; this site's Proxy page has the install link for each browser.
2. Log in to this site and, on the Proxy page, click "Copy extension restore link", then paste it into "Import/Export" → "Restore from online" in the extension. Regions and addresses are imported in one go; after that, click the extension icon and pick a region, and enter your account and password for this site in the login box the browser shows.
3. We recommend a separate browser profile (or a different browser) dedicated to the proxy, with the work browser kept local, so the two do not mix.

## What it suits, and which situations call for another method

- Yes: looking things up, opening Google, GitHub, Stack Overflow, overseas documentation sites, the web version of ChatGPT, and web mail.
- Use another method: video apps, desktop software and command-line tools do not use the browser's proxy settings by default (for the command line, you can put the proxy address into the http_proxy environment variable; see the Linux article).
- Use another method: watching Chinese video sites (for users overseas) — video sites also check IPv6 and DNS, which the web proxy does not cover; that situation needs a whole-device VPN.

## Getting along with IT policy

Everything on a company computer may be audited by the company, and extensions are no exception. Read the company's acceptable use policy first: what most companies prohibit is unapproved software and bypassing security policy, and a browser extension accessing external websites is usually in a grey area; if you are not sure, ask IT.

Do not install a whole-device VPN (Cisco, Private network, Hiddify) on a company computer to get around company policy: they change the system routes, which triggers alerts in endpoint management software and also carries company intranet traffic out. The web proxy affects only one browser and carries the least risk.

Keep work accounts and personal accounts apart: do not log in to company accounts in the browser that uses the proxy, and do not log in to personal accounts in the company browser.

## FAQ

**What if the company forbids installing extensions?** Then use your own phone or personal computer. Do not use portable software of unknown origin to get around the controls.

**Will the extension see my company intranet traffic?** No. Under the split-routing rules, company intranet domains connect directly and do not pass through the proxy; in global mode they are merely sent to the proxy server and back, and what the proxy sees is the domain name, not the content. To be safe, give the proxy its own browser profile.

**Does the proxy still work while the company VPN is on?** Yes, the two do not conflict. A very small number of company VPNs force all traffic through the company exit and disable proxy settings; in that case the extension reports that it cannot connect, and the only option is to turn off the company VPN.

**Is it the same on a company Mac?** The same; the Chrome, Edge and Firefox extensions all have Mac versions. Safari does not have this extension, so use a different browser.

## Further reading

- [Proxy setup page: extension install and restore link](https://7d24hrs.com/httpproxy?utm_source=github&utm_content=overseas-access-04)
- [What the web proxy is and when to use it](https://7d24hrs.com/guides/web-proxy?utm_source=github&utm_content=overseas-access-04)
- [How to send a Linux server and command-line tools through the line](https://7d24hrs.com/guides/linux-server?utm_source=github&utm_content=overseas-access-04)
- [Which connection method suits which situation](https://7d24hrs.com/guides/choose-connection?utm_source=github&utm_content=overseas-access-04)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/office-laptop?utm_source=github&utm_content=overseas-access-04

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=overseas-access-04) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=overseas-access-04) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
