# 01 · Which services need an overseas IP, and how the line works

The test is the mirror image of reaching China from abroad: when the service sees that your source IP is in mainland China, or you cannot reach its servers at all, it will not open, is downgraded, or is extremely slow. The table below is organised by purpose.

| Category | Examples | What happens without the line | What you need besides an IP |
|---|---|---|---|
| Work | Google Workspace, Slack, Zoom, Teams, Notion | Will not open, or keeps cutting out | A company account |
| Development | GitHub, npm, Docker Hub, PyPI sources other than mirrors, Stack Overflow | So slow that it times out | Nothing |
| AI | ChatGPT, Claude, Gemini | Will not open | The account's country of registration, a phone number |
| Research | Google Scholar, paper databases, university email | Will not open, or extremely slow | A university account |
| Gaming | Steam overseas regions, PSN, Switch eShop, overseas servers | The store will not open, high latency | An account for that region's servers |
| Video and music | YouTube, Netflix, Disney+, Spotify | Will not open | A paid account, and the account's region has to match the IP |
| Social | X, Instagram, Telegram, Discord, WhatsApp | Will not open | A phone number |

## An important distinction

**"Needing an overseas IP" and "needing an overseas account" are two different things.** For GitHub and YouTube, changing the IP is enough; Netflix needs a paid account with a matching region; registering for ChatGPT needs an overseas phone number that can receive a verification code. The line solves "can it be opened"; the account is up to you.

## How the line works

Your traffic is first encrypted and sent to an overseas server, which then accesses the destination. What the destination sees is that server's IP. There are three ways to do it: a client, the web proxy, and a router. For how to choose, see [Which connection method suits which situation](../network/02-choose-your-connection-method.md).

## Three common misconceptions

- **Changing DNS does not help.** Failing to connect is a path problem, not a resolution problem.
- **Speed depends on the line between the two points.** Going out from China, the bottleneck is the cross-border link and your carrier's exit, so choosing the region matters more than the server's specifications; see [03](03-which-region-is-fastest.md).
- **While you are using Chinese apps, not everything has to go through the line.** Turn on split routing: Chinese sites connect directly and overseas sites go through the line, so neither takes a detour; see [Router split routing](../router/03-router-split-routing.md).

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=overseas-access-01) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=overseas-access-01) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
