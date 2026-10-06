# 05 · How to send a Linux server and command-line tools through the line

On Linux there are two routes to the line; choose by need. To send the whole machine through it (pulling Docker images, running services that need an overseas network, unattended operation), use OpenVPN: one configuration file placed in /etc/openvpn/client/ and started at boot. To send only a few commands through it (git, pip, npm, curl), use the web proxy: put the proxy address into the http_proxy environment variable and the rest of the traffic is untouched. On desktop Linux you can also import it in NetworkManager. This article covers all three, with how to write the password file and the commands for verifying.

## Route one: the whole machine through the line (OpenVPN)

1. Install the client: Debian / Ubuntu sudo apt install openvpn, Fedora sudo dnf install openvpn, Arch sudo pacman -S openvpn.
2. Log in to this site and, on the OpenVPN page, click a region's flag to download the .ovpn. The configuration Linux receives does not have the account and password built in (NetworkManager does not accept files with built-in credentials), so create a separate password file: two lines, the first your email for this site, the second your password, chmod 600.
3. Copy the .ovpn to /etc/openvpn/client/<region>.conf, and add the path of the password file after auth-user-pass in the file.
4. sudo systemctl enable --now openvpn-client@<region>. Check the status with systemctl status openvpn-client@<region>, and verify that curl -s https://ipinfo.io/country shows the region you chose.
5. To change region, download another configuration and enable another unit; run only one at a time.

## Route two: only command-line tools through the line (web proxy)

The proxy address given on this site's Proxy page, together with your account and password, can be put straight into environment variables: export https_proxy=https://username:password@proxy-address export http_proxy=$https_proxy. Special characters in the password have to be URL-encoded. After that, curl, wget, git, pip and npm all go through the line in this terminal, and other programs are not affected.

The Docker daemon does not read shell environment variables; write it into Environment= in /etc/systemd/system/docker.service.d/proxy.conf and restart docker. For apt, write Acquire::https::Proxy in /etc/apt/apt.conf.d/proxy.conf.

This route does not drop, needs no root, and does not change routes. It suits company servers and cases where you only want to speed up pulls; it applies only to programs that honour the proxy variables, and the rest of the traffic is untouched.

## Route three: NetworkManager on desktop Linux

1. Install network-manager-openvpn-gnome (one click on this site's OpenVPN page can open the software centre).
2. Settings → Network → VPN → "+" → Import from file, choose the .ovpn, enter your email and password for this site, and save.
3. Switch the VPN on and off from the top bar or the tray. To connect automatically at boot, tick "Automatically connect to VPN" in the settings of the wired/wireless connection.

## Verifying and troubleshooting

- Check the exit: the country in curl -s https://ipinfo.io is the region you chose.
- Check DNS: in resolvectl status, the DNS of the VPN interface should be the one pushed by the line; if it leaks, add dhcp-option DNS to the configuration or use the update-systemd-resolved script.
- AUTH_FAILED: the password file is wrong or the account has expired; if you changed your password, update the password file.
- TLS handshake timeout: UDP to the server is not getting through; switch region or network. On a cloud server, the security group has to allow outbound UDP.
- The server is in China and Chinese sources should connect directly: once OpenVPN is connected, all outbound traffic goes through the line. Change the apt / pip / npm sources to Chinese mirrors, or use route two instead so that only specific commands go through it.

## Things to know

- One Linux machine counts as one device and shares the simultaneous-online quota with your other devices (Personal 2 devices, Family 4 devices, Enterprise 8 devices); the web proxy in route two is counted per connection and is included as well.
- The configuration file and the password file are equivalent to your account; do not commit them to a git repository or put them into an image.
- After you change your password the old configuration stops working immediately; this is the revocation mechanism by design. Updating the password file is enough.
- When running the line on a cloud server, follow the provider's terms of use; the line records only connection duration and total traffic.

## FAQ

**Why does the Linux configuration not have the account and password built in?** When NetworkManager imports a configuration it does not accept a file with built-in credentials and reports an import failure, so the copy issued for Linux has you fill them in yourself; with the systemd method, write them into the password file.

**Can only Docker go through the line?** Yes: set the proxy variables for the Docker daemon alone (route two); or run a container with OpenVPN in it (gluetun) so that specific containers go through the line.

**What about the Private network (Tailscale) on Linux?** The official script installs it in one line, and tailscale up --login-server=<this site's control server> logs in. It suits cases where you need to reach this machine from outside, or want to set it up once and have it always online; for merely speeding up pulls, OpenVPN or the proxy is simpler.

**Is it the same for OpenWrt on a router?** On OpenWrt, install luci-app-openvpn and upload the .ovpn, and the whole LAN goes through the line; a router with this site's firmware does not need this, just log in to your account.

## Further reading

- [OpenVPN page: client downloads and configuration files](https://7d24hrs.com/openvpn?utm_source=github&utm_content=overseas-access-05)
- [How to use OpenVPN and when to choose it](https://7d24hrs.com/guides/openvpn-setup?utm_source=github&utm_content=overseas-access-05)
- [How to send a Synology or QNAP NAS through the line](https://7d24hrs.com/guides/nas-openvpn?utm_source=github&utm_content=overseas-access-05)
- [What the web proxy is and when to use it](https://7d24hrs.com/guides/web-proxy?utm_source=github&utm_content=overseas-access-05)

Website version of this article (also in Traditional Chinese and English): https://7d24hrs.com/guides/linux-server?utm_source=github&utm_content=overseas-access-05

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=overseas-access-05) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=overseas-access-05) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
