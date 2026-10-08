# 03 · Using Chinese government and public service websites

## What you see

The National Government Service Platform, provincial and municipal government service sites, the electronic tax bureau, social insurance and housing provident fund lookups, CHSI, 12306: from overseas they either will not open, or they open but the verification code never arrives or face recognition fails.

## First work out which layer the problem is on

| Symptom | Cause | Fix |
|---|---|---|
| The page will not open at all, or times out | The site is open only to mainland IPs, or packets are being dropped on the cross-border line | Switch to a China IP |
| It opens, but the phone verification code never arrives | The SMS has to be sent to a Chinese phone number | Keep a Chinese SIM card and turn on international roaming to receive SMS |
| The verification code arrives, but face recognition fails | You are using the version from an overseas app store, or it is the camera permission | Install the Chinese edition of the app and allow the camera |
| You are told "the current network environment is abnormal" | Risk control has detected proxy characteristics | Try again with a different entry region, or use the router option (it looks more like home broadband) |

## 12306 on its own

12306 is extremely sensitive to IP, and from an overseas IP even the home page may not open. After switching to a China IP: registration needs a Chinese phone number, buying a ticket needs a real-name ID document, and payment goes through a Chinese bank card or Alipay. You need all three before you can buy a ticket. During ticket-rush peaks it also limits the request rate of a single IP, so do not open several windows and keep refreshing.

## CHSI and degree verification

CHSI itself is not especially strict with overseas IPs; slowness is the main problem. But its verification SMS is likewise sent only to Chinese numbers. Before doing a degree verification, overseas students should first confirm that their Chinese phone number can still receive SMS.

## One suggestion

Government-type tasks often come up only once or twice a year, and finding a line at the last minute every time is a lot of trouble. Setting up the China-bound line as one fixed entry point and switching back when you are done is less hassle than configuring it again each time.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=china-access-03) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=china-access-03) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
