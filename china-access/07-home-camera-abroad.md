# 07 · Viewing your home cameras in China from abroad

> Website version (longer): https://7d24hrs.com/guides/home-camera?utm_source=github&utm_content=china-access-07

## Three cases, each with a different fix

| Which kind your home camera system is | Can you view it directly from overseas | Fix |
|---|---|---|
| Vendor app with cloud (EZVIZ, Xiaomi, TP-Link, Imou and so on) | Mostly yes; in a few regions it is restricted or extremely slow | Switch to a China IP and use the Chinese edition of the app |
| A network video recorder (NVR) that can only be viewed on the home LAN | No, there is no public entry point | Add one device at home to a private network, and have the overseas device enter the home LAN through the private network |
| Vendor app, but the one in the overseas store is a separate system with its own servers | The accounts do not match | Install the Chinese edition of the app and use the Chinese account |

## Case one: vendor cloud

The camera pushes the picture to the vendor's server, and the app pulls it from the server. The line from an overseas network to a Chinese vendor's server is poor, which shows up as slow loading and broken streams. After switching to a China IP you are on a line inside China, and it improves noticeably.

Note that the app of the same name in an overseas store usually connects to overseas servers, and the accounts are not interchangeable. Install the Chinese edition of the app; for store region problems, see the [troubleshooting and installation guide](../client/06-ios-app-store.md).

## Case two: the recorder is only on the LAN

This is the most common case and also the hardest. The NVR has no public IP, and port forwarding mostly cannot be done on home broadband in China. The workable approach is a **private network**:

1. Leave one always-on device at home; a computer, a NAS, a Raspberry Pi or a supported router will all do. Install the private network client on it, add it to your private network, and turn on "share LAN".
2. Add the phone or computer overseas to the same private network as well.
3. From then on the overseas device reaches the NVR directly at its home LAN address, just as if you were at home.

LeoTun's "Private network" is exactly this kind of private network. There is no limit on how many devices you install it on with one account, and the number online at the same time follows the plan: Personal 2 devices, Family 4 devices, Enterprise 8 devices. One device at home plus a few overseas fits the Family plan exactly.

## Case three: the accounts do not match

A device bought in China is bound to a Chinese account, and the app from the overseas store cannot log in to it. The only fix is to install the Chinese edition of the app. Do not re-bind the device, as that will kick your family's account off.

## A privacy reminder

The picture from your home cameras should only flow between your devices and your home. The private network option prefers a direct peer-to-peer connection and only forwards through a relay when a direct connection cannot be made, and the picture is not stored on any server; the vendor cloud option, by contrast, passes through the vendor. In either case do not use "tunnelling tools" of unknown origin, which amounts to handing your home cameras to someone else.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=china-access-07) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=china-access-07) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
