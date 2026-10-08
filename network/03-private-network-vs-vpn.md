# 03 · How the Private network (Tailscale) differs from a VPN, and when to use it

> Website version (longer): https://www.leotun.com/guides/tailscale-mesh?utm_source=github&utm_content=network-03

The Private network section uses Tailscale: a networking tool based on WireGuard. LeoTun runs the control server itself, and you log in with your account on this site. It is not the same thing as "connection-type" VPNs such as AnyConnect and OpenVPN.

## Three differences

| | Connection-type VPN (AnyConnect / OpenVPN / Hiddify) | Private network (Tailscale) |
|---|---|---|
| Connection | You tap connect each time, and reconnect after a drop | Log in once and stay online; it recovers automatically when you change networks |
| Exit | Once connected, all traffic goes through the exit | The exit is optional: with none selected, public internet traffic goes out locally and only traffic between devices inside the private network is encrypted; only when you select a region's exit is it equivalent to a VPN |
| Device-to-device access | None | Phones, computers and NAS under the same account can reach each other directly, without port forwarding or a public IP |

## When you should use it

- Multiple devices, and you want to configure once and stay online for good.
- You have a NAS, computer or camera at home to reach from outside: log in to the Private network on both sides and connect directly by device name, as if on the same LAN.
- Devices that need to stay connected for long periods: there is no session timeout.

## When another method suits better

- You only want to use it once, temporarily: importing Hiddify by QR code or installing AnyConnect is quicker.
- The device is already running a company VPN or other networking software: the two fight over DNS and routing, and the symptoms are copyright notices when watching Chinese video and the company intranet failing to open. Use a method that affects only the browser, such as the web proxy.
- Campus / company networks that restrict UDP: WireGuard runs over UDP and can only rely on relays, which are slow; switch to AnyConnect.

## Expiry and number of devices

A device's login validity follows the account's expiry date; it goes offline within a few minutes of expiry, and you just log in again after renewing. The number of devices online at the same time depends on the plan (Personal 2 devices, Family 4 devices, Enterprise 8 devices) and the quota is shared with the other connection methods; when the number online at the same time exceeds the plan's limit, you can temporarily upgrade the account type (remaining time is converted at equal value by price) and switch back when you are done.

For installation and login steps see [Client guide 05](../client/05-tailscale-private-network.md).

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=network-03) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=network-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; every friend you invite earns you 30 days, an offer with no end date
