# 08 · Set up many devices once, and switch phones without starting over

For people with many devices, the most annoying part is configuring every one of them, doing it all again after changing phones, and tapping connect on each device when out and about. The private network removes all of that: each device logs in once with your account on this site and then stays online, with nothing to do after a restart or a change of Wi‑Fi; each device chooses its own exit region, so the laptop can use Japan and the phone the China region without affecting each other; devices under the same account can reach one another, so a laptop away from home can open the shares on the NAS at home directly. A new phone just needs to log in. This article explains how to put a whole household's devices in, how the quota is counted, and how to handle expiry and changing devices.

## What you do only once per device

1. Install the Tailscale client (Android, Windows, macOS and Linux from the download area on this site's Private network page; iPhone / iPad from the App Store, which requires an Apple ID outside the China region).
2. If you have logged in to an official Tailscale account, log out first, then point the login at this site's control server (phone: "⋯" on the logged-out screen → Use custom server; computer: copy the command from the page; macOS: hold Option and click the icon → Debug → Custom Login Server).
3. Confirm in the browser with your account on this site. From then on the device is in the private network and needs no further attention.
4. Choose an exit: each device chooses in its own menu, independently of the others. To use no exit, choose None, which keeps only device-to-device access.

## How simultaneous devices are counted

An account can be installed on any number of devices; the only limit is how many are online at the same time: Personal 2, Family 4, Enterprise 8, sharing one quota with Cisco, Hiddify and the other methods. When you exceed your plan's limit, you can temporarily upgrade the account type (the remaining time is converted at equivalent value by price) and switch back when you are done.

A router counts as one device, and the devices behind it are not counted. One router or NAS at home plus the phone and laptop you carry is usually enough.

## Devices can reach one another

- Each device under the same account has a private network address and can also be reached by device name, with no need for a public IP or port forwarding.
- Opening a shared folder on the home NAS from a laptop away from home, viewing the home video recorder from a phone, or using remote desktop to a home computer all connect directly using private network addresses.
- A home router running this site's firmware can share the whole LAN into the private network, so devices that can't run a client, such as printers and TVs, can also be reached from outside.
- Other customers' devices do not appear in your private network at all; it is not merely that you can't see them.

## Expiry, changing devices, uninstalling

- Account expiry: all devices go offline within a few minutes; after renewing, log in once more on each, and the exit settings are kept.
- Changing phones: log in on the new phone by following the steps above; if it says the limit has been reached, log out on the old phone, or temporarily upgrade the account type and switch back when you are done.
- If you don't want a device to stay in the private network: log out in the client; to force a device offline, contact support.
- Don't run another VPN on the same device at the same time (a company Cisco client, other mesh networking software); they will fight over DNS and routes.

## FAQ

**Can each device choose a different exit region?** Yes, each device chooses its own exit. The laptop can use Japan for video while the phone uses the China region for online banking, without affecting each other.

**Does leaving the private network on all the time drain the battery?** With no exit selected there is almost no traffic; it is used only when communicating with devices in the private network. The battery cost is comparable to the system VPN.

**How do I install it on a home NAS?** Synology and QNAP have a Tailscale package, and Linux systems use the official install script; when logging in, point it at this site's control server in the same way. A router running this site's firmware doesn't need it installed: log in to your account and it is in the private network.

**Why not set up Cisco on every device?** You can, but with Cisco you have to tap connect each time, reconnect after a drop, and change the address to change exit; with many devices the private network is far less effort. A device on a campus network that restricts UDP is the exception; use Cisco on that one.

## Further reading

- [Private network page: download and login steps](https://7d24hrs.com/mesh?utm_source=github&utm_content=client-08)
- [What the private network (Tailscale) is](https://7d24hrs.com/guides/tailscale-mesh?utm_source=github&utm_content=client-08)
- [Viewing your home cameras and NAS in China from abroad](https://7d24hrs.com/guides/home-camera?utm_source=github&utm_content=client-08)
- [What the router firmware can do](https://7d24hrs.com/guides/router-firmware?utm_source=github&utm_content=client-08)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/multi-device?utm_source=github&utm_content=client-08

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=client-08) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=client-08) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
