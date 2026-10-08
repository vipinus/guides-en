# 02 · Does Cisco AnyConnect work in China

> Website version (longer): https://www.leotun.com/guides/anyconnect-china?utm_source=github&utm_content=overseas-access-02

Yes. AnyConnect is Cisco's enterprise VPN protocol. Companies all over the world rely on it for remote work, and the China branches of foreign companies use it every day, so the cost of banning it outright is too high. **What actually gets blocked is one particular server address, not the protocol.** So "does it work" depends on whether the provider has enough addresses and replaces them quickly enough.

## Why it resists blocking better than proprietary VPN apps

| | AnyConnect | Proprietary VPN app |
|---|---|---|
| Traffic signature | Standard TLS, the same as visiting an HTTPS website | Its own protocol, with a fixed signature |
| Once identified | Only that one address stops connecting | The whole app stops working |
| Client | Published by Cisco; the open-source alternative OpenConnect exists on every platform | Gone once it is removed from the app store |

LeoTun runs its own machines in 24 regions. When an address is flagged it is replaced with a new one, the domain name is repointed automatically, and the address saved in your client does not need changing.

## How to install

1. Download the installer for your system from the Cisco page of the website. Windows 10 and later, macOS, iOS, Android and Linux are all covered; Windows 7/8 can only use version 4.9, the last one that supports them.
2. Open the client and enter the server address in the address field — on the website, click a region's flag to copy it.
3. Enter your account and password and connect. No certificate file is needed, and no configuration import.
4. Once you see "Connected", check your exit IP.

## If it will not connect, go in this order

1. **Switch to another region.** If another region connects, only that server is temporarily unreachable.
2. **Switch network.** If broadband fails, switch to mobile data, and vice versa; interference on different carriers is not in sync.
3. **Read the error.** `Login failed` means the account or password, or expiry; `Untrusted server certificate` is most likely a wrong system clock or the current network intercepting TLS, so switch network; only `Connection attempt has failed` means the address is unreachable.
4. **Update the client.** This matters especially after a major system upgrade.
5. **Switch connection method.** The same account can use OpenVPN or Hiddify to connect to the same servers, and blocking of the three protocols is independent of one another; see [02 · Which connection method suits which situation](../network/02-choose-your-connection-method.md).

## Updating Cisco AnyConnect

Cisco has renamed it Cisco Secure Client; it is used the same way. There is no need to uninstall first: install the new version over the old one and the saved addresses are kept. On phones, update in the App Store / Google Play; if the store search does not find it, use the open-source OpenConnect, which uses the same protocol and the same account (for changing the iOS store region, see [Client 06](../client/06-ios-app-store.md)).

## FAQ

**Is slow speed a sign of throttling?** Switch region first: look at the red, yellow and green lights in the region list on the website and pick a green one. If it is still slow, the usual cause is the local broadband: community broadband, or a carrier and region that do not match (China Unicom in the north: Japan or Korea; China Telecom in the south: Southeast Asia or Australia; other providers: the China entry points).

**Why is the same address sometimes good and sometimes bad?** The address is a domain name, and the machines behind it are replaced automatically according to blocking and load. Waiting a minute or two and trying again usually means you caught it mid-switch.

**Does it disconnect by itself after being connected for a long time?** Not because of time. When the account expires the server disconnects you; renew and reconnect.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=overseas-access-02) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=overseas-access-02) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
