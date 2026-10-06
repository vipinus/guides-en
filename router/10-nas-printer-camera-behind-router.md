# 10 · Will the NAS, printer and cameras behind the router be affected?

Once a VPN router goes in, the first worry is usually the rest of the house: will the NAS, the printer and the cameras still work, and will the NAS drag all its traffic through the VPN?

## The short answer

No. Split routing is on by default: **traffic between devices at home, and traffic to services in China, never enters the tunnel. Only the sites that need the VPN go through it.**

## Three kinds of traffic, three paths

| Traffic | Path | Examples |
|---|---|---|
| Between devices at home | Stays on the local network, never touches the tunnel | Copying files to the NAS, casting to the TV, printing |
| To services in China | Direct, over your own broadband | NAS syncing to a Chinese cloud drive, cameras uploading to a Chinese cloud, domestic downloads |
| To blocked sites | Through the tunnel | YouTube, search, AI tools |

So copying files to the NAS at home runs at full local speed, and its backups to Chinese cloud storage use your whole broadband line without touching the VPN.

When you are abroad and using a China route, the direction is reversed: the Chinese sites on the list go through the tunnel and everything else goes direct. See [03 · What split routing is](03-router-split-routing.md).

## Three common situations

**Reaching the NAS from outside (remote files, phone photo backup)**
Two ways:
- Use the private network (Tailscale): sign the NAS and your phone into the same account and reach the NAS by its device name from anywhere. No public IP and no port forwarding. See [Private network vs VPN](../network/03-private-network-vs-vpn.md).
- Keep doing what you did before (the vendor's remote access, port forwarding). The router does not block it.

**Downloads running on the NAS**
Downloads from Chinese sources go direct and are unaffected. Downloads from overseas sites go through the tunnel and run at tunnel speed. If you do not want downloads using the tunnel, plug the NAS into the upstream router or the modem and it bypasses this router entirely.

**A work laptop that needs the company VPN**
Connect it to the Wi-Fi of the upstream router or the modem, separate from this router. Two VPNs stacked on top of each other usually break access to the company network.

## When one device does not behave

- The device has "Private DNS" or "Secure DNS" turned on. It then looks names up on its own, around the router, and split routing cannot see it. Turn that setting off.
- Check which Wi-Fi it is on. If it is on the modem's Wi-Fi, it never went through this router at all.

## FAQ

**Does the NAS take up a device slot on my account?** No. The router takes one slot, and everything behind it is not counted separately.

**With the whole household on it, will I run out of data?** Accounts have unlimited data, and domestic traffic never enters the tunnel in the first place.

**Can I keep one device off the VPN permanently?** Yes, connect it to the upstream router or the modem. The admin page can also switch the whole router to "Direct" mode, but that applies to everyone at once.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=router-10) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=router-10) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
