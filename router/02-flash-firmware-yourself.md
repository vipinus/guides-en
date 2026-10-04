# 02 · How to flash the firmware yourself

> Website version (longer, also in Traditional Chinese and English): https://7d24hrs.com/guides/router

This is for people who already have a router whose model is on the supported list. If you are not sure whether your model is supported, look it up on the website's Router page first: more than 1000 models, searchable by brand.

## Steps

1. **Confirm the model and hardware version**: the model on the label on the bottom of the router plus a version number such as v1/v2. Firmware is not interchangeable if the version is off by even one.
2. **Generate the firmware on the website**: after logging in, choose your model on the Router page. The system builds it on demand and emails you a few minutes later when it is ready to download. The download link in the email is valid for 1 day.
3. **Pick the right file**: when flashing from stock firmware, use the `factory` file; when you are already on this firmware and want to upgrade, use the `sysupgrade` file.
4. **Flash it**: upload the factory file under "Firmware Upgrade" on the stock admin page and wait for the reboot. Do not cut the power during this time.
5. **First login**: after flashing, follow the three steps in [Getting started with a pre-installed router](01-plug-and-play-router.md).

## What if the flash goes wrong

Most routers have a recovery mode (hold reset while powering on to enter it) that lets you upload the stock firmware again. Before flashing, download the stock firmware to your computer and keep it.

## When flashing it yourself is not recommended

The model is not on the list, the hardware version does not match, or it is an old router with no recovery mode. In these three cases, buying a pre-installed one is less trouble.

---
Compiled by the [LeoTun](https://7d24hrs.com) team · Questions? Come to the [Telegram group](https://t.me/+NWJN_9yITj9kOWFh) · Sign up for a 24-hour free trial; invite friends and get 30 days for each one, valid long-term
