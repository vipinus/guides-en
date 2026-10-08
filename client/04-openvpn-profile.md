# 04 · OpenVPN: download the .ovpn profile, import it and connect; works on routers, NAS and Linux

> Website version (longer): https://www.leotun.com/guides/openvpn-setup?utm_source=github&utm_content=client-04

OpenVPN is a long-established open-source protocol, and almost every operating system, router firmware and NAS ships with a client for it. LeoTun's profile files already include your account, password and encryption material, so you can connect as soon as you import one. For everyday use on phones and computers, AnyConnect or Hiddify is less effort; OpenVPN's value lies in **places that accept only OpenVPN**: OpenWrt routers, Synology / QNAP NAS, Linux servers and older devices.

## Three steps

1. From the table on [the OpenVPN page of the website](https://www.leotun.com/openvpn?utm_source=github&utm_content=client-04), install the client for your system (every platform has the official OpenVPN Connect; on Windows you can also use OpenVPN GUI, and on macOS Tunnelblick).
2. After logging in, **click a region's flag** to download that region's .ovpn. One file per region.
3. Open the file in the client and connect.

| Platform | Notes |
|---|---|
| Windows / macOS / Android / iOS | The profile has the account and password built in; import and connect |
| Linux | System VPN settings → import from file, and enter your website email and password on first connection; command line `openvpn --config file`; to start at boot, put it in `/etc/openvpn/client/` |
| OpenWrt router | Install luci-app-openvpn, upload the .ovpn and enable it; not needed if this site's firmware is preinstalled |
| Synology NAS | Control Panel → Network → Network Interface → Create → VPN → OpenVPN (import the .ovpn); to send the NAS's outbound traffic through the line, tick "Use default gateway on remote network" |
| QNAP NAS | QVPN → VPN Client → Add → OpenVPN, import |

## Users in China: direct connection to Chinese websites

Once connected, traffic to Chinese websites takes a detour. The website provides a "China direct-routing tool": double-click to run it, and Chinese IPs connect directly while everything else goes through the line. It works with both Cisco and OpenVPN. Users overseas should not use it.

## If it won't connect, check in this order

| Log keyword / symptom | Cause | What to do |
|---|---|---|
| AUTH_FAILED | Wrong account or password, or expired | Log in to the website and check the expiry date; if you changed your password, download the profile again |
| UDP times out first, then it connects over TCP | The current network restricts UDP, and it fell back to TCP automatically | Usable but slower; if it is too slow, change network or use AnyConnect instead |
| Both UDP and TCP report TLS handshake failed / key negotiation failed | The network path to the server is down | Switch region or network |
| Error on import | The client is too old (before OpenVPN 2.5) | Update the client |
| Drops suddenly while connected | The account expired and the server disconnected you | Renew and reconnect; the profile doesn't need replacing |

## UDP or TCP

Both are available and you don't have to choose. UDP comes first in the profile, so the client tries UDP first; if UDP is restricted or can't connect, it switches to TCP automatically after a few seconds. UDP has lower latency and is faster; TCP is only a fallback and is noticeably slower across borders. On networks that permanently restrict UDP (some campus and company networks), we recommend using AnyConnect directly.

> Profiles downloaded before 15 September 2026 contain UDP only; download again if you want automatic switching.

## Security

The profile file contains your account and password, which makes it equivalent to the account itself, so don't pass it on; if it leaks, change your password on the website and the old file stops working immediately. The handshake itself is also encrypted: without the key in the profile, a handshake cannot even be started, and the server is invisible to scanners.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-04) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-04) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
