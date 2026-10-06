# 03 · Which region is fastest from inside China: by carrier

> Website version (longer): https://7d24hrs.com/guides/pick-region?utm_source=github&utm_content=overseas-access-03

With the same service and the same protocol, speed can differ several times over between regions. The cause is not the server but **the exit route from your carrier to that region**. So when choosing a region, look at the carrier first, then the time of day, and only then the server.

## Try these first, by carrier

| Your network | Try first | Notes |
|---|---|---|
| China Unicom in the north | Japan, South Korea | Unicom's exit to Japan and South Korea is usually the most direct |
| China Telecom in the south | Southeast Asia (Singapore), Australia | Telecom's southbound exit is good |
| China Mobile, Great Wall and so on | China entry | The client connects only to an address inside China, and we handle the cross-border leg, so it is not affected by cross-border interference |
| Mobile data | Differs by carrier; test it separately from broadband | On the same phone, the best region on Wi‑Fi and on mobile data is often different |

LeoTun's region list uses **red, yellow and green lights** to show each region's current load; among several Japan entries, pick the one with the green light.

## Then the time of day

From 8 to 11 pm is the peak. In that period, pick a green-light region or switch connection method; if it is still slow, the usual cause is the local broadband: community broadband, or a carrier and region that do not match, in which case choose again from the table above.

## Finally the protocol

- A network with heavy packet loss (broadband in an old housing estate, mobile data): Hiddify's hysteria2 resists packet loss and is often the fastest.
- A campus network or company network that restricts UDP: hysteria2 runs over UDP and will be throttled; use AnyConnect, which runs over TLS, instead.
- Six methods on one account; there is always one that suits your network.

## A five-minute test

1. Test your local speed once without the line, as the upper limit.
2. Choose two regions from the table above, connect to each once, and open the same speed test site.
3. Test the same two regions again at 9 pm.
4. Take the one that is not bad in either test as your default and the other as your backup.

---
Compiled by the [LeoTun](https://7d24hrs.com?utm_source=github&utm_content=overseas-access-03) team · Questions? See the [contact page](https://7d24hrs.com/contact?utm_source=github&utm_content=overseas-access-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
