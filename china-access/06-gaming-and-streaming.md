# 06 · China-server games and live streaming

## Games: you can log in, but latency is high

Most China-server games do not block overseas IPs; the problem is latency. If you are in Europe or North America, the physical distance to servers in China brings a fixed base latency, and on top of that come jitter and packet loss on the cross-border link, which show up as stuttering and disconnections.

What "acceleration" does is this: it sends your traffic over a better line to China, reducing detours and packet loss. It turns a jittery, lossy connection into a stable one, and for most games that is the difference between playable and unplayable.

## How to choose an entry point

The region you choose is the country where the traffic lands: for China-server games choose the **China region**, and what goes out is a China IP. Do not choose regions such as Germany or France that are relayed through a third party; they do not carry UDP, and games basically cannot connect. Test several, and judge by the latency shown in the game.

## Choosing a protocol

Games are sensitive to packet loss, so prefer protocols that run over UDP and avoid relayed regions that do not support UDP. TCP-type protocols retransmit when packets are lost, and latency jumps badly.

## Live streaming

Douyin, Kuaishou, Douyu and Huya differ in how they restrict overseas IPs; most can be watched, but with limited resolution. Switching to a China IP unlocks the full set of resolution options. Live streaming is sustained high-bitrate traffic, so choose an entry point with plenty of bandwidth.

## Real-name verification

China-server games require real-name verification. This is an account-level requirement that has nothing to do with IP, and changing the IP does not solve it.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=china-access-06) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=china-access-06) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
