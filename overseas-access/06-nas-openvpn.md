# 06 · How to send a Synology or QNAP NAS through the line

The NAS is the device at home that most needs the line and gets the least attention: the downloader has to reach overseas resources, Docker has to pull images, Cloud Sync has to sync overseas cloud drives, and Plex has to scrape metadata. A NAS cannot run Hiddify, but Synology and QNAP both come with an OpenVPN client built in — download a .ovpn from this site's OpenVPN page, import it and it connects, and it reconnects automatically at boot. This article covers where the import is on Synology and on QNAP, the key option "Use default gateway", what to do after changing your password, and why "reaching the NAS from outside" is a different matter that calls for the Private network.

## First, tell two things apart

Sending the NAS itself through the line (downloading, pulling images, syncing overseas cloud drives): use OpenVPN, which is what this article covers.

Reaching the NAS from outside (opening shares on a business trip, watching cameras): use the Private network (Tailscale), which puts the NAS and your phone into the same private network; see "Viewing your home cameras and NAS in China from abroad". Leave this job to the Private network — OpenVPN connects the NAS to our line, and the Private network connects you into your home.

## Synology

1. Log in to this site and, on the OpenVPN page, click a region's flag to download the .ovpn file for that region.
2. Control Panel → Network → Network Interface → Create → Create VPN profile → OpenVPN (via importing a .ovpn file), and enter your account email and password for this site.
3. "Use default gateway": ticked, all of the NAS's outbound traffic goes through the line (downloads, Docker and Cloud Sync all benefit); unticked, it only establishes the tunnel and outbound traffic still goes out locally. In the vast majority of cases it should be ticked.
4. Tick "Reconnect when the VPN connection is lost" so that it recovers automatically after the NAS restarts or the line fluctuates. Connect, then try one pull in a package.

## QNAP

1. Download the .ovpn in the same way.
2. QVPN Service → VPN Client → Add → OpenVPN, import the file, and enter the account and password.
3. In the connection settings, tick "Use VPN as the default gateway of the NAS" and automatic reconnection, then connect.

## Which traffic goes through it and which does not

- Goes through: BT and HTTP tasks in Download Station / Download Station, Docker image pulls, Cloud Sync syncing Google Drive / Dropbox / OneDrive, Plex and Emby metadata scraping, and Package Center updates.
- Does not: the traffic of you accessing the NAS within the LAN — it is inside the LAN anyway and is not affected.
- You are in China and want Chinese sites to connect directly: the NAS has no split-routing script, and once OpenVPN is connected all of the NAS's outbound traffic goes through the line. If Chinese download sources are slow, use Chinese mirror addresses in the download tasks, or connect to the line only when you need it.

## Things to know

- The configuration file carries your account, and the password field on the NAS stops working after you change your password: download the .ovpn again and replace it, or change only the password in the VPN profile.
- When the account expires the NAS is disconnected; after renewal it reconnects automatically, and the configuration does not need replacing.
- The NAS counts as one device and shares the simultaneous-online quota with your other devices (Personal 2 devices, Family 4 devices, Enterprise 8 devices).
- The line runs over UDP; a NAS on home broadband will almost never run into UDP restrictions.

## FAQ

**After ticking "Use default gateway", can the NAS still be reached on the LAN?** Yes. LAN traffic does not pass through the gateway; shares, Plex playback and the admin page are all unaffected.

**Plex remote playback is slower after the NAS goes through the line?** Plex remote playback uses the NAS's outbound traffic, so once the default gateway is ticked it takes a detour through the line. For remote playback, reaching the NAS over the Private network is more direct; or connect OpenVPN only when you need to download.

**Can only Download Station go through the line?** Synology and QNAP have no per-app split routing. For fine-grained control, run a download container with OpenVPN in Docker (such as qbittorrent + gluetun) and send only that through the line.

**What about a NAS running a Linux system (TrueNAS, Unraid)?** Do it the Linux way: the openvpn package plus a configuration file placed in /etc/openvpn/client/; see "How to send a Linux server and command-line tools through the line".

## Further reading

- [OpenVPN page: client downloads and configuration files](https://7d24hrs.com/openvpn?utm_source=github&utm_content=overseas-access-06)
- [How to use OpenVPN and when to choose it](https://7d24hrs.com/guides/openvpn-setup?utm_source=github&utm_content=overseas-access-06)
- [Viewing your home cameras and NAS in China from abroad](https://7d24hrs.com/guides/home-camera?utm_source=github&utm_content=overseas-access-06)
- [How to send a Linux server and command-line tools through the line](https://7d24hrs.com/guides/linux-server?utm_source=github&utm_content=overseas-access-06)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/nas-openvpn?utm_source=github&utm_content=overseas-access-06

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=overseas-access-06) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=overseas-access-06) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
