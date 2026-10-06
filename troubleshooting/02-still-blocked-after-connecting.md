# 02 · Connected to reach China but still can't watch: what to do

Check in order. Each step takes a minute.

1. **Confirm the exit IP has really changed.** Open a website in your browser that shows where your IP is located and see whether it is mainland China. If not, the VPN has not taken effect; reconnect.
2. **IPv6 and DNS leaks.** If the exit IP is right but the site still judges you to be abroad, most likely the device's IPv6 or local DNS is bypassing the VPN. This is the most common case, and it has its own article: [03 · IPv6 and DNS are the ones that slip through](03-ipv6-and-dns-leak.md).
3. **App cache.** Video and music apps cache the result of their region check. Quit the app completely and open it again; if that does not work, clear the app's data.
4. **App version.** If you installed the international version (iQIYI, WeTV), the content library is different. Switch to the mainland China version.
5. **Where the account was registered.** A few platforms restrict content by the region the account was registered in, regardless of your current IP. In that case the only fix is a different account.
6. **System region and language.** Some apps read the system region. Change the system region to China and try again.
7. **Entry region.** Some content also differs between IPs from different provinces. Switch to another entry point and try again.

## Still not working

Tell support these four things: the target website or app, the exact error text, where your current exit IP is located, and the connection method you use. With these, the problem can be pinpointed in one go.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=troubleshooting-02) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=troubleshooting-02) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
