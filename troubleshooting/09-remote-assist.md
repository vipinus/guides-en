# 09 · Having support look at your computer and router remotely

Some problems cannot be made clear even after a dozen rounds of screenshots back and forth in the group, yet support can pinpoint them in two minutes by looking directly at the screen. This article covers when remote assistance is worth requesting, what software to use on a computer, how to import this site's server configuration, how to hand the connection details to support safely, what you control during the session, how to take back access afterwards, and what you need to do for a router running this site's firmware.

## When remote assistance is worth requesting

- You have gone through [01 · Checklist for can't connect, slow, and dropped connections](01-cannot-connect-slow-drops.md) once, and asked with the connection method, the region, the exact error text or a screenshot, and the time the problem occurred, and it still cannot be solved.
- You cannot describe the steps themselves: the setting is buried deep, you cannot read the system language, or the error flashes by too fast to capture.
- You are helping a family member with their computer, you are not beside them, and you cannot get it across over the phone.

In the following case **do not use remote assistance**; communicate in text in the group instead:

- Computers centrally managed by a company. Group policy usually forbids running this kind of program, and it may violate company rules.

## What software to use: RustDesk

The website recommends [RustDesk](https://rustdesk.com): it is open source (AGPL-3.0), so the code can be audited by anyone; and when a session starts and when it ends are both decided by your own click. It supports Windows, macOS, Linux, Android and iOS (an iPhone / iPad can only control others; it cannot be controlled).

Download it from the [Contact page](https://www.leotun.com/contact#downloads) under "Download center" → "Remote assistance", or from the official site rustdesk.com. Do not use third-party download sites from search results. Both sides of the session need to install it.

## What to authorise after installing

| System | What to do |
|---|---|
| macOS | In "System Settings → Privacy & Security", tick RustDesk under both "Screen Recording" and "Accessibility", then quit completely and reopen. Granting only one leads to "can see but cannot control" or a completely black screen. If it says "is damaged", see [06](06-antivirus-false-positive.md) |
| Android | When being assisted, tap "Start service" in RustDesk and allow screen recording; for support to be able to tap on your screen, also turn on RustDesk under the system's "Accessibility" |
| Windows / Linux | Usually works straight after installing |

## Connecting to our own server

Remote assistance runs through this site's self-hosted RustDesk server, which also connects reliably from inside China. **Both sides of the session need to import it once**; the two ends can only find each other when they use the same server:

1. Log in to the website first, then on the [Contact page](https://www.leotun.com/contact#downloads) go to "Download center" → "Remote assistance" → "Connect to our server" and click "Copy".
2. On a computer, open RustDesk "Settings → Network", click "Unlock network settings" first, then click "ID/Relay server"; on a phone it is "Settings → ID/Relay server".
3. In the window that pops up, click the clipboard icon at the top right (on a phone tap "Import"). The configuration is filled in automatically; click "OK".

**Do not paste the configuration into the input fields**; that produces "failed to lookup address". This configuration is for use with accounts on this site only. Do not forward it.

## Handing the ID and one-time password to support

Open RustDesk and the main screen shows this machine's ID and a one-time password. Before handing them over, confirm three things:

1. **You asked first.** You described the problem in an official group listed on the [Contact page](https://www.leotun.com/contact?utm_source=github&utm_content=troubleshooting-09), and support decided remote assistance was needed, before moving on to the next step. Our support staff will not approach you on their own, ask you to install remote software, or ask for a connection code; whoever comes asking, verify in the official group first.
2. **Send them only through official support channels**: the human support contacts listed on the Contact page. Any private chat outside the groups claiming to be "LeoTun support" (雷顿（原蓝盾）客服) is not us.
3. **Do not post them in the group.** A group is a place many people can see; an ID plus a password is the same as sticking your computer's key on the door.

## During the session

- Throughout the session you can see what is being done on the screen, and you can disconnect in the RustDesk window at any time.
- If someone asks you to minimise the window, leave the computer, or open online banking or payment apps, **disconnect immediately**.
- When your account password needs to be entered, type it yourself; do not read it out to support.

## Taking back access afterwards

1. Click disconnect in the RustDesk window and confirm the other side has gone offline.
2. Refresh the one-time password so the one you just sent out becomes void.
3. Quit RustDesk. If you no longer need it you can simply uninstall it and download it again next time.

## Routers: what you need to do

For a router running this site's firmware, you do not need to install any remote software on the router or the computer, and you do not need to send the router's admin password to support. All you need to do is:

- Keep the router powered on with the network cable plugged in, and the account logged in on the router.
- Tell support your account, the router model and the symptoms in the official group; support handles the rest.
- Do not repeatedly unplug and restart it while it is being worked on, unless support asks you to.

## FAQ

**Will support message me privately on their own and tell me to install remote software?** No. Whenever someone approaches you unprompted, always verify their identity in the official group first.

**"failed to lookup address" when importing?** Most likely the configuration was pasted into the input fields. Clear those fields, go back to the "ID/Relay server" window and import by clicking the clipboard icon at the top right.

**Connected on macOS but the screen is black, or you can see but cannot control?** The permissions are incomplete. Tick both "Screen Recording" and "Accessibility", then quit completely and reopen.

**What else do I need to do after the session ends?** Disconnect, refresh the one-time password, quit the program. Once these three steps are done, the other side can never connect again.

## Further reading

- [How to use RustDesk remote assistance (website guide)](https://www.leotun.com/guides/rustdesk-certificate?utm_source=github&utm_content=troubleshooting-09)
- [What to do when your Mac says the app "is damaged"](https://www.leotun.com/guides/antivirus-false-positive?utm_source=github&utm_content=troubleshooting-09)
- [Contact page: support groups, human support and email](https://www.leotun.com/contact?utm_source=github&utm_content=troubleshooting-09)
- [05 · How to reach us, and how not to lose touch](05-how-to-reach-us.md)
- [01 · Checklist for can't connect, slow, and dropped connections](01-cannot-connect-slow-drops.md)

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=troubleshooting-09) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=troubleshooting-09) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
