# 09 · Installing Hiddify on every platform: Windows, macOS, Linux, Android, iOS

The client used by the Hiddify section of this site is the open-source Hiddify, which has the sing-box core built in, so nothing else needs configuring once it is installed. All five platforms use the same app, but the hurdles on first launch differ: on Windows it may be blocked or deleted by antivirus software, on a Mac you may be told it "is damaged" and you also have to authorise a network extension, on Linux you have to run an authorisation command before VPN mode works, and on iPhone it can't be found in the China storefront. This article covers, for each platform, where to download it, how to install it and what to do on first launch, and ends with the shortest steps for importing a subscription and connecting.

## Where to download

| Platform | Installer | Where to get it |
|---|---|---|
| Windows | Installer (.exe), x64 only | Download area of the Hiddify page |
| macOS | .dmg, one package for both Apple silicon and Intel | Download area of the Hiddify page |
| Linux | .deb (Debian / Ubuntu family), x64 only | Download area of the Hiddify page |
| Android | .apk, in two builds: ARM64 and x86-64 | Download area of the Hiddify page, or Google Play |
| iPhone / iPad | Hiddify Proxy & VPN on the App Store | App Store; requires an Apple ID outside the China region |

The download area of the Hiddify page automatically recommends the package for your current system, and the packages for other systems are listed below it. Next to each row there is also an "Official site" icon pointing to Hiddify's official release page, so you can compare versions. The three desktop systems (Windows, macOS, Linux) also have video tutorials.

The desktop installers are unmodified mirrors of Hiddify's official release packages, not altered or repackaged. Before allowing one through you can check it yourself: upload the installer to VirusTotal and take a look; for how, see [Troubleshooting 06](../troubleshooting/06-antivirus-false-positive.md).

## Windows

1. Download the installer from the download area of the Hiddify page and double-click to install. (In our current tests Windows Security does not flag it; if the antivirus software you have installed does, see the FAQ at the end of [Troubleshooting 06](../troubleshooting/06-antivirus-false-positive.md).)

## macOS

1. Download the .dmg from the download area of the Hiddify page, open it and drag Hiddify into "Applications".
2. In "Finder" → "Applications", hold Control and click the Hiddify icon, choose "Open", then click "Open" again in the dialog.
3. If it still won't open: "System Settings" → "Privacy & Security", click "Open Anyway" in the "Security" section and enter your password to confirm.
4. If you are told it "is damaged and can't be opened": the file is not damaged; the system's Gatekeeper is blocking it. Open "Terminal", run the command below, press Return and enter your login password, then open Hiddify again:

```bash
sudo xattr -dr com.apple.quarantine /Applications/Hiddify.app
```

This command only removes the quarantine flag that marks the file as downloaded, and applies to this one app only. **Do not** use `sudo spctl --master-disable` to turn Gatekeeper off for the whole machine.

The first time you click connect after installing, the system will also ask you to authorise a "network extension". If you skip this step the icon keeps spinning and it never connects:

- **macOS 15 Sequoia and later**: "System Settings" → "General" → "Login Items & Extensions", scroll to "Extensions" at the bottom, switch the view to "By Category", click the ⓘ next to "Network Extensions", turn on the switch for Hiddify, and enter your password or use your fingerprint when prompted.
- **macOS 13 Ventura / 14 Sonoma**: first launch Hiddify and click connect once, and "System Extension Blocked" will pop up; then go to "System Settings" → "Privacy & Security", scroll down to "System software from developer … was blocked from loading", click "Allow" and enter your password.

On a company-issued Mac, if these buttons are greyed out, a device management policy has locked them; ask IT, or use the Cisco, OpenVPN or private network clients instead.

## Linux

1. Download the .deb from the download area of the Hiddify page and double-click to install it with the software centre, or open a terminal in the download directory and run (Debian, Ubuntu and their derivatives):

```bash
sudo apt install ./downloaded-file-name.deb
```

2. Connecting straight after installation reports "operation not permitted" and VPN mode won't start, because the official deb does not have this permission once installed. Open a terminal and run the command below to authorise Hiddify, then reopen Hiddify:

```bash
echo /usr/share/hiddify/lib | sudo tee /etc/ld.so.conf.d/hiddify.conf && sudo ldconfig && sudo setcap cap_net_admin,cap_net_raw+ep /usr/share/hiddify/hiddify
```

3. **Run it again after every Hiddify upgrade**: the authorisation is attached to the program file, and an upgrade replaces the file, so the authorisation is lost.

The deb package is x64; on ARM Linux devices use OpenVPN, and the same account works.

## Android

1. Download the .apk from the download area of the Hiddify page. The page automatically recommends the architecture for your phone; the vast majority of phones are ARM64. If you can use Google Play, you can also install it straight from the store.
2. If a prompt about "unknown sources" or a warning from security software appears during installation, allow it.
3. The first time you tap connect, the system asks for VPN permission; tap allow.

## iPhone / iPad

1. Search for "Hiddify" in the App Store and install it; it is free.
2. If you can't find it, or you see "This app is currently not available in your country or region": on iOS, install from the App Store with a non-China-region Apple ID (Hiddify is in the United States, Hong Kong, Taiwan, Japan and Singapore storefronts). We recommend registering a new one: in the App Store, tap "Get" on any free app → "Create New Apple ID", choose a region such as Hong Kong or the United States, and choose "None" as the payment method. You switch accounts only in the App Store, and iCloud is not affected. For the full steps, see [06 · What to do when iOS won't let you install an app](06-ios-app-store.md).
3. The first time you tap connect, the system asks for VPN permission; tap allow.

**Do not** use an Apple ID shared by someone else; they can lock your device remotely.

## After installing: import a subscription and connect

1. Log in to the website and open the Hiddify page.
2. Click the flag of the region you want and a QR code pops up; or click "Import all regions · auto-select" at the top of the page to import all regions outside China at once and let the client choose automatically. **The China region is imported separately**: for watching video or using online banking in China from abroad, click the China flag to import it.
3. Phone: tap "Copy import link", then switch to Hiddify and add it as prompted, or scan the code with Hiddify on another device. Computer: click "Copy config URL (to paste)", then in Hiddify click "+" → "Add from clipboard".
4. Click connect.

For the difference between the three kinds of link, how to import into other clients, and whether a subscription expires, see [02 · Hiddify subscription links](02-singbox-subscription-links.md). If you have imported it but can't connect, see [Troubleshooting 04](../troubleshooting/04-singbox-import-not-connecting.md).

## FAQ

**Have you modified the installers?** No. The desktop installers are unmodified mirrors of Hiddify's official release packages. Every row on the Hiddify page has a link to the official release page, so you can compare versions yourself, and you can also upload the file to VirusTotal to double-check.


**I have already run the xattr command on my Mac and it still won't connect?** Most likely the "network extension" has not been authorised; follow the macOS section above and turn on the switch for Hiddify in System Settings.

**After upgrading Hiddify on Linux, VPN mode has stopped working again?** That is expected; run the authorisation command once more after upgrading.

**Can it be used on ARM Windows or Linux computers?** Yes, with another access method such as OpenVPN, and the same account works; the Hiddify desktop packages are currently x64.

**Don't want to bother with the allow-through steps?** Cisco (Cisco Secure Client), OpenVPN (OpenVPN Connect) and the private network (Tailscale) are all vendor-signed clients; they are not flagged by antivirus software and a Mac does not say they are "damaged", and the account is the same one.

## Further reading

- [Hiddify page: client downloads and QR codes for each region](https://7d24hrs.com/singbox?utm_source=github&utm_content=client-09)
- [How to import a Hiddify subscription link](https://7d24hrs.com/guides/singbox-subscription?utm_source=github&utm_content=client-09)
- [Client flagged by antivirus / Mac says it is damaged: verify first, then allow](https://7d24hrs.com/guides/antivirus-false-positive?utm_source=github&utm_content=client-09)
- [What macOS "network extension" authorisation is and how to allow it](https://7d24hrs.com/guides/macos-network-extension?utm_source=github&utm_content=client-09)
- [What to do when iOS won't let you install an app](https://7d24hrs.com/guides/ios-app-store?utm_source=github&utm_content=client-09)

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=client-09) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=client-09) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
