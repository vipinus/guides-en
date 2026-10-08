# 05 · Private network (Tailscale): installing, logging in to this site's control server, choosing an exit

> Website version (longer): https://www.leotun.com/guides/tailscale-mesh?utm_source=github&utm_content=client-05

The Private network section uses Tailscale (a networking tool built on WireGuard). LeoTun runs its own control server, and you log in with **your account on this site**, which has nothing to do with an official Tailscale account. Log in once and you stay online; the exit region can be changed from the menu at any time. For how it differs from a VPN and who it suits, see [Network guide 03](../network/03-private-network-vs-vpn.md).

## Installing

| Platform | Where to get it |
|---|---|
| Windows / macOS / Linux / Android | The download area on [the Private network page of the website](https://www.leotun.com/mesh?utm_source=github&utm_content=client-05) (served directly by this site, no need to go to the official site) |
| iPhone / iPad | App Store; requires an Apple ID outside the China region (see [Client 06](06-ios-app-store.md)) |

## Logging in

1. **Log out of the official account first** (if you have ever logged in): on a phone, tap your avatar → Log Out; on a computer, run `tailscale logout`. Unless you are fully logged out, the option needed in the next step does not appear.
2. **Point the login at this site**:
   - Phone: on the logged-out screen, tap "⋯" at the top right → Use custom server (called Use an alternate server in some versions), enter the address given on the website's Private network page, and tap Log in.
   - Windows / Linux: copy the `tailscale up --login-server=…` command from the website page and run it in PowerShell / a terminal.
   - macOS: **do not click Log in**. In the Tailscale window, click the arrow on the account row → Account Settings… → Accounts → the small arrow next to "Add Account…" → Add Account Using Alternate Server, paste the address and click Add Account….
3. The browser opens this site's login page automatically; confirm with your account on this site. When you return to the client it is already online.

## Choosing an exit

- Phone: menu → Exit Node, pick a region; it takes effect immediately.
- Computer: tray / menu bar icon → Exit Node submenu; or `tailscale set --exit-node=<region-name>` (`tailscale exit-node list` shows what is available).
- To use no exit, choose None (on the command line, leave the value after the equals sign empty). Only one exit can be used at a time.

## Expiry and device count

- A device's login validity follows the account's expiry date, and it goes offline within a few minutes of expiry; after renewing, just log in once more. No reinstall is needed.
- The number of devices online at the same time depends on your plan (Personal 2, Family 4, Enterprise 8), and the quota is shared with the other access methods; when you exceed your plan's limit, you can temporarily upgrade the account type (the remaining time is converted at equivalent value by price) and switch back when you are done.

## Two cases where another method fits

- With another VPN running on the same device (a company AnyConnect, other mesh networking software): they compete for DNS and routes. This is the reason behind copyright notices when watching Chinese video and company intranets that won't open.
- On a campus / company network that restricts UDP: WireGuard runs over UDP, so it can only go through relays, which is very slow; switch to AnyConnect.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-05) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-05) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
