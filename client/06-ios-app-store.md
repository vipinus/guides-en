# 06 · What to do when iOS won't let you install an app

If you can't find Hiddify, Tailscale or Telegram on your iPhone, or you see "This app is currently not available in your country or region", the app has not disappeared: the App Store is split into storefronts by the region of your Apple ID, and the China storefront does not list most networking apps. On iOS, install from the App Store with a non-China-region Apple ID; the steps are on this page. We recommend registering a new one rather than changing your existing account. Below are the steps, the trick for choosing "None" as the payment method, and why you must never use an account someone else has shared.

## Why this happens

The App Store is split into storefronts by the region of your Apple ID, and different regions list different apps. The China storefront has neither Hiddify nor Tailscale, and Telegram and Discord come and go; Cisco Secure Client and OpenVPN Connect are available in most regions. This is a difference in listings, not a problem with the apps, and an account in another region can install them.

On iPhone, both Hiddify and the private network (Tailscale) on this site are installed from the App Store; just follow the steps below to switch to an Apple ID in another region; the installers for Android, Windows and macOS are provided directly by this site and are not affected.

## Option 1 (recommended): register a new Apple ID outside the China region

1. Sign out of the current App Store account: Settings → your profile at the top → Media & Purchases → Sign Out. This signs you out of the App Store only, not iCloud, so your photos, backups and contacts are not affected.
2. In the App Store, find a free app, tap "Get", and follow the prompt to "Create New Apple ID". Choose any of the United States, Hong Kong, Japan or Singapore as the region, and choose "None" as the payment method. This "None" appears only on the path where you register while downloading a free app; registering directly on the web often doesn't offer it.
3. Sign in to the App Store with the new account, then search for Hiddify, Tailscale and Telegram and download them.
4. Once they are installed you can switch back to your original account; the apps already installed keep working and updating as usual. Switch again whenever you need to install a new app.

## Option 2: change the region of your existing account

Sign in at account.apple.com and change the country or region. You first have to cancel all subscriptions and use up your balance, in some cases you also have to add a local payment method, and changing back is just as much trouble. Not recommended unless you intend to change region for the long term anyway.

## Things you must never do

- Don't use an Apple ID shared by someone else, including "shared accounts" in groups or online. The account owner can lock your device remotely, and a locked iPhone can only be unlocked by them; once two-factor authentication is turned on it cannot be turned off, and the risk and any dispute fall on you. This site's support will not provide any shared account either.
- Don't install configuration profiles of unknown origin or installers "signed with an enterprise certificate". These are common ways of bypassing the store, and also a way in for planting certificates and hijacking traffic.

## After installing

Hiddify: go back to this site's Hiddify page and scan the code or copy the import link. Tailscale: log out of the official account first, then follow the steps on the Private network page to enter this site's control server address. Telegram, Discord: go to this site's Contact page and scan the code to join the group.

## FAQ

**Do I need a credit card to register in another region?** No. On the Option 1 path (registering while downloading a free app) you can choose "None" as the payment method.

**Will the new account affect my iCloud and photos?** No. You switch accounts only in the App Store; iCloud stays on your original account.

**Is it the same on iPad?** Yes, iPadOS follows the same App Store rules.

**Do Android phones have this problem too?** No. The installers for Android, Windows, macOS and Linux are distributed directly by this site and don't depend on an app store.

## Further reading

- [Contact page: client download cards and the three groups](https://www.leotun.com/contact?utm_source=github&utm_content=client-06)
- [Hiddify: import by scanning the code](https://www.leotun.com/singbox?utm_source=github&utm_content=client-06)
- [Private network (Tailscale): login steps](https://www.leotun.com/mesh?utm_source=github&utm_content=client-06)
- [How to contact us and how not to lose touch](https://www.leotun.com/guides/stay-in-touch?utm_source=github&utm_content=client-06)

Website version of this article (also in Traditional Chinese and English): https://www.leotun.com/guides/ios-app-store?utm_source=github&utm_content=client-06

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=client-06) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=client-06) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, an ongoing offer
