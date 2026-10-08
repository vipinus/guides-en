# 13 · WeChat, Alipay and Chinese Mini Programs

## What you see

You are abroad, and WeChat and Alipay themselves work, but as soon as you touch the **Mini Programs, Official Account articles or Channels** inside them, you get a spinner or a blank screen:

- You open an Official Account post and the images never finish loading
- A Mini Program is stuck on its launch page, or shows "network error"
- In Channels you can scroll to the cover images, but nothing plays when you tap in
- The Citizen Centre, medical insurance and housing provident fund pages in Alipay will not open

## Cause

WeChat's and Alipay's **chat and transfers** run over their own channels, which work worldwide, so you think "the app is fine".

But Mini Programs, Official Account articles and Channels are essentially **web pages**, served by third-party servers, and most of those servers serve only users in China. With your IP abroad, they either give you no content or are so slow that they time out.

So the symptoms are oddly split: you can chat and receive red packets, but you cannot open what is inside.

## What to do

Switch to a China IP and open it again, and it works normally. There are two details that are easy to trip over:

**First, restart the app, do not just reopen the page.** WeChat caches "where it last connected", and refreshing the Mini Program straight after changing IP often still fails. Quitting WeChat completely from the background and going back in has a much higher success rate.

**Second, do not send only the browser through the line.** Mini Programs run inside WeChat, and the browser-extension kind of method cannot reach them. You need the **whole phone**, or at least the WeChat app, to go through the line.

## How to send only WeChat through the line on a phone

Both the Android and iOS clients support "per-app" mode, where you can tick only WeChat and Alipay and keep the other apps on the local network. The benefits are:

- Apps that depend on your **real location**, such as food delivery, ride hailing and maps, are not affected
- It saves battery and data
- Banking apps will not trigger risk control because "the location suddenly changed"

## A common misunderstanding

Some people assume that an Official Account that will not open has been "banned" or that "there is a problem with the account", and so they uninstall and reinstall again and again. That is almost never it: the same article appears immediately once the IP is changed. The test is simple: have a friend in China open the same link and send you a screenshot. If they can see it and you cannot, it is the IP.

---
Compiled by the [LeoTun](https://www.leotun.com?utm_source=github&utm_content=china-access-13) team · Questions? See the [contact page](https://www.leotun.com/contact?utm_source=github&utm_content=china-access-13) (groups, email and support are all listed there) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
