---
layout: post
title: 'International Google Nest Unable to Connect to Wi-Fi? Fixing the "Connect to same Wi-Fi" Issue'
description: 'How to fix a Google Nest Mini failing to connect to Wi-Fi with AP Isolation or "Connect to same Wi-Fi" errors on an IndiHome router.'
date: 2024-10-10
author: Aldi Saputra Wahyudi
categories: tutorial
banner:
  image: https://github.com/user-attachments/assets/846533c6-b510-4818-a1f5-cb67833be52d
tags: [tutorial, Smart Home, Google Nest, Networking]
lang: en
locale: en_US
translation_id: google-nest-ap-isolation
is_translation: true
permalink: /en/tutorial/2024/10/10/Google-Nest-Connect-to-same-Wi-Fi.html
top: 1
---

It all started when I had some spare cash lying around and decided to buy a Google Nest to make my life a bit more practical—kind of like having a personal assistant. Before this, I was already using several smart devices like an IndiHome STB (even though I bought a rooted one), smart bulbs, and smart power plugs. Until then, I always controlled everything manually without voice commands—aside from my phone being sluggish, manual control was just faster than waiting for my super slow phone to respond.

In the end, I bought a chalk-colored Google Nest via Tokopedia by sorting from the lowest price. I got it for 400k IDR, full package with the box, and most importantly, brand new! The seller hadn't sold any Google Nest units before, though I figured it wouldn't be a problem since there's a complaint feature if anything goes wrong.

After waiting around 3 days, the package finally arrived. I started setting it up in the afternoon, and after trying for hours, I began to panic—was I just being dense, or was something actually wrong? Sure, I tried setting it up without reading the manual, but if I were that clueless, all my other smart devices wouldn't have worked fine either.

At first, I already felt something was off when the Google Nest showed this message: "This Nest Mini was manufactured for a different country, and may not be compatible with your Wi-Fi network".
I tried watching Google Nest reviews on YouTube and nobody else seemed to get this kind of warning, which made me panic even more.

![Nest Mini was manufactured for a different country](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsqo-gvw0DEraGfjxkFKSUyDNs5YsS9km3BqmKu6AOJc1v9r6nM9EE3CrMxzAFuowaAStHqmcTwJv7tSPHyaq04yjQEbXiJsrcHYDrqNVdNlrQb0Zu_NhdTCv4oinhG2CRyJrzGiv-BCX9/w242-h430/image.png)

When I tried connecting it to Wi-Fi, it showed up, and then gave me these messages: "Connect to same WI-FI", "Your nest mini was setup successfully but can't be found", and "Turn off AP Isolation". That made me wonder if this Nest Mini really wasn't compatible with Indonesian networks—or maybe just IndiHome, since I'm a loyal IndiHome subscriber and hadn't tested it on another ISP.

![Turn OFF AP Isolation!](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg5nJ0HheSPxlpfJyMbFQTsmbUTKxJHNabsuNCGvkZtVsKbNEreuNyc_rs7_NOyP6s89znLFXxsVRTbIU3wx23UXSg2C36DzaOCZspUsfitCQoOqSiMsu1fVq_TPEQZ9El_c0ml_CMOvfwV/w276-h490/image.png)

After doing factory reset – setup – factory reset – setup probably more than 10 times, the result was still nothing!

Eventually, I filed a complaint with the seller, and this is how they replied:

![jawaban seller](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgD-NBCgJrWVhpq6ZYRM6kIV3CagXL_Jr71UjBpzEvOT1vnMONLfdQTrttSMfmzXhwQ6f6l5FBp9kh-VqEva2xmJJTNbeczCEbVByc4J0k6fmF5oVVnO_kO3yV336p6GHLlk8vvvRb7imDR/w417-h284/image.png)

From the seller's reply, I concluded that the seller had no idea either and was just telling me to try the exact steps I had already done beforehand.

As an IT person, I know this AP Isolation issue is a network setting that normally lives in the router configuration. AP Isolation is typically used on public Wi-Fi networks like hotels, airports, and similar places so each user is isolated on a separate path. So I logged into the admin page at `192.168.100.1`, only to find that this HG8245A router didn't expose any AP Isolation setting. Oh, and earlier I also tested it using a mobile hotspot on the Tri provider, and it actually worked! Well, of course—a phone hotspot puts devices on the same local network, right? But there's no way I'm going to leave my mobile hotspot running forever.

Next, I contacted IndiHome via Twitter, and you can probably guess what they told me to do... yep, restart the modem. Obviously that didn't help at all—I asked them to check AP Isolation, and the solution offered was restarting the modem. Even after reaching out via email and Twitter, IndiHome customer support seemed confused by the issue as well and just told me to fill out a troubleshooting form.

Because there was so little info about this Google Nest problem, while waiting on Twitter for IndiHome CS to reply, I searched for "AP Isolation" on Twitter and found someone else with the exact same issue... Finally, I wasn't alone.

After exchanging tweets with Mas Aziz, I asked, "Bro, did IndiHome give you any solution?" and Mas Aziz replied with both the answer and the workaround below:

![sensor karna ga izin yang punya akun guys](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjupYaycW-y2qv2pQYF3hg2vcQYIJwGy3eeTYjsH5iuFbKjTBVyylAbls65g5zLCZ9AKi_XeKEICMEtAB6oLGGxNSJhX2PVtmhR2lQ2tp6x5Q0vtiJfR_cPuR_nmRNAxQjxQnpA9w6Eg384/w519-h219/image.png)

*(Redacted since I didn't ask the account owner's permission, guys.)*

So the solution for this problem is to use a separate router connected behind the IndiHome router.
Up until now, though, I haven't done that for a few reasons: first, electricity cost from running two routers 24 hours a day; second, it just feels odd having two Wi-Fi networks; and third, why on earth would I buy the cheapest Google Nest listing only to end up buying an extra router that costs almost as much as an official Indonesian-warranty Google Nest?

Eventually I had an idea: instead of buying a new router, why not create my own Wi-Fi using my computer? Since I had a spare TP-Link WN727N USB Wi-Fi receiver left over from an old laptop whose built-in Wi-Fi adapter had died, I plugged that receiver into my PC, turned it into a "portable router," and installed Connectify.

![Connectify to Google Nest](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgImb_vnfGvPhL4zB5spamb17pcb880IdHTzinsYP0p7ZTh_za6mV86c205wIEb0iehHb4wGyz-DSD_ecxTRT7Ttfm7rNTxl2hf2WfqIwMgaVZM_fCw276CRLrldYhYuhWwkU-F4JPWugKd/w258-h466/image.png)

In the end, I canceled my Tokopedia complaint, and IndiHome still never had a solution. For a while, my Google Nest could only work whenever my computer was turned on.

## Conclusion and Solution

After experimenting further, I finally found a clean workaround using a dummy Wi-Fi connection.
Suppose the Wi-Fi network you want your Google Nest to connect to has the SSID `'wifialdisaw'`:
1. Turn off the real `'wifialdisaw'` Wi-Fi, then create a hotspot from your phone or Connectify using the exact same SSID, `'wifialdisaw'`, and run through the Google Nest setup again.
2. Once the setup completes and connects successfully, turn off that dummy Wi-Fi and turn the real Wi-Fi back on.
3. Done—your Google Nest will now connect normally to your intended Wi-Fi network.
