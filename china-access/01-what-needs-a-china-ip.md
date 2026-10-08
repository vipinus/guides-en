# 01 · Which services need a China IP

There is only one test: when the service sees that your source IP is not in mainland China, it refuses you or gives you a reduced service. The table below is ordered by how strictly you are blocked.

| Category | Examples | What happens without a China IP | What is checked besides IP |
|---|---|---|---|
| Video | iQIYI, Tencent Video, Youku, Mango TV, some anime series on Bilibili | You are told it is only available in the mainland, or you can only watch free content | App store region, where the account was registered |
| Music | NetEase Cloud Music, QQ Music, Kugou | Large numbers of songs are greyed out and cannot be played | Nothing |
| Government services | The National Government Service Platform, provincial government service sites, tax, social insurance, housing provident fund | The page will not open, or the verification code never arrives | Phone number, face recognition |
| Education | CHSI, the academic degree site, university academic administration systems | Will not open, or extremely slow | Nothing |
| Travel | 12306, airline websites | Will not open, payment fails | Phone number, payment |
| Finance | Online banking, mobile banking, Alipay, WeChat Pay | Login is stopped by risk control, transfers fail | SIM card, device fingerprint, face |
| Games | China-server PC and mobile games | You can log in, but latency is high and you get disconnected | Real-name verification |
| Daily life | Meituan, Ele.me, DiDi, some Taobao features | Location errors, orders fail | Location, phone number |
| Live streaming | Douyin, Kuaishou, Douyu | Cannot be watched in some regions | Nothing |

## One important distinction

**"Needs a China IP" and "needs a Chinese phone number" are two different things.** Video and music only look at IP, and changing the IP is enough. Government services, banking and ticket booking, besides IP, also need you to receive an SMS verification code and pass face recognition. IP solves "whether it will open"; the verification after that depends on your own Chinese phone number and ID documents.

## Ways to solve the IP problem

Send the traffic first to a server in the mainland, which then visits the target. There are three ways to do this: a client, the web proxy, or a router. For how to choose, see [Which connection method suits which situation](../network/02-choose-your-connection-method.md) in the sister repository.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=china-access-01) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=china-access-01) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
