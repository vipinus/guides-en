# 06 · What to do when your Mac says the app "is damaged"

> Website version (longer, also in Traditional Chinese and English): https://7d24hrs.com/guides/antivirus-false-positive

The conclusion first: the file is not broken, and nobody has tampered with it. When double-clicking Hiddify on a Mac shows "is damaged and can't be opened" or "the developer cannot be verified", it is the system's Gatekeeper blocking an app that **has no Apple signature and notarization** — the desktop client we distribute does not currently have a purchased signature.

Installing Hiddify on Windows no longer triggers a virus alert in our current tests. If the antivirus software you have installed flags it anyway, follow the same order here: verify first, then allow.

## Why it gets blocked

- **The installer is not signed.** Apple's developer signing and notarization must be applied for in the name of a company or registered business, with real-identity verification. We are still weighing the cost and trade-offs, so for now macOS sees the installer as coming from an "unidentified developer". That is exactly what Gatekeeper is blocking — **it is not blocking the content, but the fact that it "does not recognise the publisher"**.
- **Files downloaded from a web page are tagged with a quarantine flag.** When macOS sees this flag it checks for a signature and notarization, and refuses if there is none. The message sometimes says "is damaged" and sometimes "the developer cannot be verified"; the cause is the same.

What we do: the desktop client is an **unmodified mirror** of the upstream open-source project's release package. We do not alter it, repackage it or inject anything; we only host it on our own download site to make downloading easier.

## Verify it yourself first; do not allow it blindly

Allowing an app means the system stops checking it, so the order is verify first, then allow.

**Upload it to VirusTotal for a second check.** Drag the installer onto [virustotal.com](https://virustotal.com/gui/home/upload). A few heuristic engines flagging it while the mainstream vendors all pass it is the typical pattern of a false positive. If most mainstream engines flag it, **do not install it** — come straight to us.

Continue only after it passes the check. If you are unsure, contact support first and we will check the download site.

## Three ways to allow it, from narrowest to broadest

After double-clicking you may see ""Client name" is damaged and can't be opened. You should move it to the Trash", or "cannot be opened because the developer cannot be verified". The three steps below go from narrowest to broadest; **if the first step works, do not use the third**.

1. Find it under "Applications" in Finder, Control-click the icon (or right-click), choose "Open", and click "Open" once more in the dialog that appears. This is a one-time allowance for this one app only.
2. If the right-click menu has no usable "Open", go to "System Settings" → "Privacy & Security" and scroll down to the Security section. You will see ""Client name" was blocked from use because it is not from an identified developer". Click "Open Anyway" on the right and enter your password to confirm.
3. If the message is "is damaged", the first two steps usually do not work, because the system could not even read a signature. Open "Terminal" and run `sudo xattr -dr com.apple.quarantine` followed by the app's path (usually a `.app` under `/Applications/`), press Return, enter your login password, then open the app again. What this command does is remove the quarantine flag that marks the download source.

On first launch the system will also ask for your password to authorise installing a network extension. The app can take over traffic only after you agree.

A few reminders:

- Use the `xattr` command **only on files whose source you have already verified**; see the previous section for how to verify.
- **Do not** use `sudo spctl --master-disable` to turn Gatekeeper off globally. That switches off protection for the whole machine, whereas right-click Open affects only one app.
- Since macOS 15 Apple has tightened the right-click Open path, and in most cases you have to go through the "System Settings" step. This is a change in system behaviour, not a problem with our package.
- Company-issued Macs are often managed by an MDM profile, and all three steps above may be disabled. Do not force it; use the signed options below.

## Don't want to allow it? Use one of these three

They use clients that the vendors themselves have signed and notarized, which **work on macOS with a double-click** and show none of the messages above. The account is the same one, with no extra payment:

- **Private network (official Tailscale client)**: vendor-signed, works as soon as it is installed, suitable for leaving on long-term
- **OpenVPN Connect**: an installer signed by OpenVPN itself; just import the configuration
- **Cisco Secure Client**: an enterprise-grade client, fully signed, already installed on many company computers

## FAQ

**Does your program actually contain a virus?**
No. It is an unmodified mirror of the upstream open-source project's official release package. But you should not just take our word for it; the method for checking it yourself is given above: upload it to VirusTotal and look at how the engines' verdicts are distributed.

**Why not buy a signature?**
We are evaluating it. Apple developer signing and notarization and Windows code-signing certificates must all be applied for in the name of a company or registered business, with real-identity verification; the registration details are publicly searchable in most regions; and there is an annual fee. It is a trade-off between cost and the way we operate. When there is a conclusion it will be updated here.

**Will it still be flagged on Windows?**
At present, in our tests the security centre built into Windows no longer flags the Hiddify installation. If the antivirus software you have installed flags it anyway, upload it to VirusTotal for a second check first, and once it passes, set Hiddify's installation directory as trusted in the antivirus software. Do not turn off real-time protection in order to install it.

**It will not open after installing on a Mac. Was the download corrupted?**
No. It will not open because Gatekeeper is blocking on the signature. Handle it with the three ways to allow it above.

**Should I install antivirus software on the Mac to go with it?**
No. What is blocking you on macOS is the system's built-in Gatekeeper, not antivirus software. Installing third-party antivirus will not make this message go away, and may add new blocks.

**Does this problem occur on phones?**
On iOS, installing from the App Store, the problem does not exist. Android occasionally warns about unknown sources; just allow it.

---

Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
