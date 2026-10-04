# 01 · Cisco AnyConnect: installing, connecting and updating on every platform

> Website version (longer): https://7d24hrs.com/guides/anyconnect-china

AnyConnect is Cisco's enterprise VPN client. Its official name is now **Cisco Secure Client**; it works the same way. You don't need a certificate file or an imported profile: enter the address, your account and your password, and you can connect. For whether it works in China and what to switch to when it won't connect, see [Reaching overseas services from China, guide 02](https://github.com/vipinus/guides-zh-CN/blob/main/chuhai/02-anyconnect-in-china.md) (in Chinese).

## Installing

| Platform | What to install | Where to get it |
|---|---|---|
| Windows 10 and later | Cisco Secure Client 5.x | [The Cisco page on the website](https://7d24hrs.com/anyconnect) |
| Windows 7 / 8 | AnyConnect 4.9 (the last version that supports them; no longer updated) | Same as above |
| macOS | Cisco Secure Client 5.x | Same as above |
| iOS | Cisco Secure Client | App Store; if the store doesn't list it, install the open-source OpenConnect, which uses the same protocol |
| Android | Cisco Secure Client | Google Play, or the APK on the website page |
| Linux | The installer on the website page, or openconnect from your distribution's repository | Same as above |

On Windows there is also the open-source OpenConnect-GUI; the same account works with it.

## Connecting in four steps

1. Open the client and enter the server address in the address field. LeoTun users can **click a region's flag** on the website to copy that region's address.
2. Enter your account (the email you registered with) and your password.
3. Once you see "Connected", open a web page that shows your IP to confirm that your exit is in the region you chose.
4. To change region, use a different address. The client remembers the addresses you have used, so next time you can pick one from the drop-down list.

## Updating

No need to uninstall first: install the new version over the old one and your saved addresses are kept. On a phone, update from the app store. After a major operating system upgrade, update the client first and only then troubleshoot connection problems.

## Common messages

| Message | Meaning |
|---|---|
| Login failed | Wrong account or password, or the account has expired |
| Untrusted server certificate | Most likely the system clock is wrong, or the current network is intercepting encrypted connections; try another network |
| Connection attempt has failed | This address is temporarily unreachable; switch region |

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
