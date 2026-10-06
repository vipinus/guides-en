# 12 · Does the router recover by itself after a power cut or a dropout?

Anyone who has run a do-it-yourself VPN router has probably seen this: one power cut, or a brief broadband outage, and after the reboot everything looks fine but the tunnel never comes back until you go into the admin page and set it up again.

## The short answer

Yes, it recovers by itself. After a power cut and reboot, a broadband dropout, or the tunnel dropping mid-session, the firmware reconnects on its own. No admin page, no signing in again.

## How it does that

The firmware runs a checker all the time that looks at the tunnel about every half minute. When it finds the tunnel down, it reconnects and puts split routing back in place.

During the short gap before the tunnel is back, Chinese sites keep working. The household does not lose internet just because the tunnel is not up yet.

Your settings are remembered too: the region, the split-routing mode and the "Automatically pick the fastest line" switch all survive a reboot or reconnect. If you turned split routing off, it stays off.

## What happens in each case

| What happened | Afterwards |
|---|---|
| Power comes back after a cut | The router boots and the tunnel reconnects by itself |
| Broadband drops and returns | The tunnel reconnects as soon as the line is back |
| The tunnel drops mid-session | The checker notices and reconnects |
| The account expires | Traffic stops using the tunnel, the home network carries on. After renewal it resumes by itself, no need to sign in again |
| We change a server address | The router follows along. Nothing to reconfigure |

## Still not back after a few minutes? Check these

1. **Is the broadband itself working?** Open a Chinese site. If that fails, the problem is the line or the modem, not the tunnel.
2. **Has the account expired?** The tunnel will not connect after expiry. Sign in on the website and check.
3. **Try another region.** Switch region in the admin page. Sometimes one region has a temporary problem.
4. **Restart the router.** Unplug it, wait ten seconds, plug it back in.
5. If none of that helps, send support a screenshot of the status shown in the admin page.

## The very first boot after flashing

The first boot is slower than usual: the firmware checks for component updates and detects the country to set the wireless power. **Plug in a network cable for that first boot.** Weak Wi-Fi before it has been online once is normal.

## FAQ

**Is it usable where power cuts are frequent?** Yes. It reconnects every time the power returns.

**Do I need to reboot the router on a schedule?** No.

**Will component updates interrupt my connection?** No. Updates are checked and downloaded at boot and take effect on the next boot. The router will not restart on you mid-use.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-12) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-12) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
