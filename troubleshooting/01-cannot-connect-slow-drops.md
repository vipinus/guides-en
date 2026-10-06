# 01 · Checklist for can't connect, slow, and dropped connections

> Website version (longer): https://7d24hrs.com/guides/connect-issues?utm_source=github&utm_content=troubleshooting-01

Go through it in order. Each step is quick, and most problems are solved within the first four.

## Can't connect

1. **Is your account still valid?** Expiry is the number one cause. Log in to the website and take a look.
2. **Is the device clock correct?** Encrypted connections require the time to be accurate to within a few minutes. Turn on automatic time sync on your phone and computer.
3. **Switch to another region.** It is common for a region's entry point to be temporarily interfered with by the carrier; switching to another one gets you through.
4. **Switch to another connection method.** The same account works with the other methods. If switching gets you through, the protocol is being interfered with; it is not an account problem.
5. **Turn off security software and try again.** Some security software blocks encrypted connections, especially on computers.
6. **Restart the router and the modem.** It is old advice, but it really works.

## Slow

1. **Test your speed without the VPN.** If the local network itself is slow, no VPN route will help, however good it is.
2. **Pick a region by carrier.** China Unicom in the north: try Japan or Korea. China Telecom in the south: try Southeast Asia or Australia. Other broadband providers: try the China entry points.
3. **Check whether it is peak time.** From 8 to 11 pm, pick a green-light region or switch connection method; if it is still slow, the usual cause is the local broadband: community broadband, or a carrier and region that do not match (see the previous step).
4. **Switch protocols.** On a poor network, a protocol with stronger resistance to interference is often faster, because it loses fewer packets.

## Dropped connections

1. **Phone battery-saving policy.** Android's background restrictions kill the client. Add it to the whitelist.
2. **Switching between Wi-Fi and cellular.** The connection is always rebuilt when the network changes. This is normal.
3. **If it keeps dropping, you can switch to the web proxy**, which does not depend on a long-lived connection.

## When to contact support

If you have tried everything above and it still does not work, tell support these three things: the connection method you use, the region, and the exact error text or a screenshot. With these three, most problems can be pinpointed in one go.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=troubleshooting-01) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=troubleshooting-01) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
