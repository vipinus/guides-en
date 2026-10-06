# 02 · Flashing the firmware yourself: from stock to ours, step by step (with video)

> Video tutorial (about two and a half minutes, English or Chinese narration): https://7d24hrs.com/video/router-flash
>
> Website version: https://7d24hrs.com/guides/router-flash

This is for people who already have a router whose model is on the supported list. You have a router still running its stock system, and we go from opening the website to the whole household being connected — what to click at each step, what you will see, and where people slip up. The demonstration uses a GL.iNet GL-MT3000. Other models follow the same steps; only the stock admin panel looks different. If you would rather not do this yourself, a pre-installed router is less trouble: see [01](01-plug-and-play-router.md). For which model to pick, see [07](07-which-router-to-buy.md).

## Before you start

- **Check that your model is supported.** Sign in, open the **Router** section and find your model by brand. The hardware revision after the model name (v1, v2 and so on) has to match too.
- **Your account must be active.** Personal, Family and Enterprise plans can all use a router.
- **Have a network cable ready.** The router's WAN port goes to your modem or upstream router. While flashing, it is best to connect your computer to the router by cable as well; it is steadier than Wi-Fi.
- **Keep a copy of the stock firmware.** Download the stock firmware for your model from the manufacturer's site, in case you ever want to go back.

## Step 1: Build the firmware on the website

1. Sign in and click **Router** in the navigation bar.
2. Find your model and click **Firmware**, or scroll down to "Build Router Firmware" and pick the model from the brand list.
3. Click **Start Building**.

A few things to know first:

- **A build takes 3 to 5 minutes.** The firmware is made for your account on the spot; it is not a ready-made file. At busy times the build may wait in a queue. The page tells you when that happens — just wait, there is no need to click again.
- **You get an email when it is ready.** The entry under "Recent Builds" changes to "Completed", and a notice arrives in your inbox.
- **The firmware's interface language follows the website language.** If you are using the site in English, the router's admin pages will be in English. For another language, switch the site language first and then build.
- **The download link is valid for one day.** If it expires, simply build again.

## Step 2: Download and extract

1. Under "Recent Builds", click **Download**. You get a zip file.
2. Open your Downloads folder and **extract** it.
3. The extracted folder contains the firmware file.

Which file to use:

| Your router currently runs | Use the file |
|---|---|
| GL.iNet stock system (the case in the video) | ending in `sysupgrade.bin` |
| Another brand's stock system | with `factory` in its name |
| Our firmware already, and you are upgrading | with `sysupgrade` in its name |

If the zip contains only one file, that is the one.

> ⚠️ **This firmware is for you alone.** It carries your account details so that the router can sign in by itself after flashing. Do not send the file to anyone else or share it publicly.

## Step 3: Flash it from the stock admin panel

Using GL.iNet as the example:

1. Connect your computer to the router, open the stock admin panel in a browser (`http://192.168.8.1` on GL.iNet) and sign in with the admin password.
2. In the left menu, open **System** → **Upgrade**.
3. Switch to the **Firmware Local Upgrade** tab.
4. Click the upload area and pick the firmware file you extracted.
5. Wait until verification shows **Pass**.
6. **Switch "Keep Settings" off.** This is the step people miss most often. The two systems do not share a configuration format, and keeping the old settings causes all sorts of odd problems.
7. Click **Install**.

The page changes to "Upgrading and rebooting…" with a progress ring. **It takes two to three minutes. Do not unplug the router or close the page meanwhile.** It is normal for the page to stop loading once the progress finishes — the router is now running a different system, and both its address and its Wi-Fi have changed. See the next step.

Other brands: look for "Firmware Upgrade", "System Upgrade" or "Local Upgrade" in the stock admin panel, upload the file, and again do not keep settings.

## Step 4: Join the new Wi-Fi

After flashing, the old Wi-Fi name is gone and a new one appears:

- **Wi-Fi name: `www.anyfq.com`**
- **Wi-Fi password: `www.anyfq.com`** (the same as the name)

Computers and phones have to **switch to this Wi-Fi** before they can get online or open the router's admin page. A computer connected to the router by cable does not need to switch.

The new admin address is `http://192.168.11.1` (type the leading `http://` yourself).

## Step 5: Wait for it to connect by itself

No sign-in, no region to pick. **As long as your account is active, the router connects by itself within 10 minutes.** Once it has, every device on this Wi-Fi goes through the service automatically — TVs, set-top boxes and game consoles included.

To confirm it is connected, open a site from a device on the router that you normally cannot reach, or look at the status in the admin page.

## Two things worth doing afterwards

1. **Change the default passwords.** The Wi-Fi password and the admin password are public defaults out of the box. Change both in the admin page.
2. **A weak Wi-Fi signal right after flashing is normal.** The router has to get online once and work out which region it is in before it raises the wireless power to the level allowed there. Plug in the network cable and let it go online first.

## Replacing an old router with a new one

An account is bound to one router at a time. If your account was used on another router before:

1. Sign in, open the **Router** section, and under the "Build Router Firmware" heading you will see the model that is **Bound**, with **Unbind** next to it.
2. Click Unbind. You can do this even if the old router is broken or not at hand.
3. Nothing to do on the new router: it **connects automatically** and is bound to your account.

If you flash the new router before unbinding, that is fine too. The new router keeps waiting and connects by itself once you unbind.

More on the rules in [05 · MAC binding and replacing a router](05-mac-binding-and-replacing.md).

## What if my account expires

After expiry the router stops routing through the service, while your home network carries on working as usual. **Once you renew, the router recovers by itself — no need to sign in again, and no need to re-flash.**

## It did not connect by itself — how to check

If it still is not working after ten minutes or so, go through these in order:

1. **Is the broadband itself working?** From a device on the router, open any ordinary website. If that fails, the problem is the cable or the modem: check that the cable in the WAN port is seated properly.
2. **Has the account expired?** Sign in on the website and check the expiry date. After renewing, wait a few minutes.
3. **Is the account still bound to the old router?** In the Router section, look at the bound model. If it is not this router, click Unbind.
4. **Restart the router once.** Unplug it, wait ten seconds, plug it back in and give it two to three minutes.
5. **Sign in manually.** Open `http://192.168.11.1` and log in to the router with username `root` and password `www.anyfq.com`. Then go to **Services** → **VPN**, enter your account email and password, and save.

Still stuck? Ask in the group, and tell us the router model and how far you got in the list above.

## When flashing it yourself is not a good idea

The model is not on the list, the hardware revision does not match, or it is an old router with no recovery mode. In these three cases a pre-installed router is less trouble.

## If the flash goes wrong

Most routers have a recovery mode: unplug the power, hold the reset button while plugging it back in, keep holding for a few seconds, then connect a computer by cable and upload the stock firmware following the manufacturer's instructions. For GL.iNet, search its documentation for "uboot". This is what the stock firmware you saved beforehand is for.

## Common questions

**Does flashing void the warranty?** That depends on the manufacturer. GL.iNet routers are built on an open-source system to begin with and can be flashed back to stock.

**Can I go back to the stock firmware?** Yes. Use the recovery mode described under "If the flash goes wrong" to upload the stock firmware.

**Can one firmware file be used on two routers?** No. Firmware is built per account, and an account is bound to one router at a time.

**Do I need a new build if I change accounts?** No. Sign out in the admin page and sign in with the new account.

**Do future updates need a re-flash?** Routine updates are picked up by the router on its own; you do not have to do anything. Only a major version needs a fresh build and one flash of the sysupgrade file, and the website will announce it when that happens.

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
