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

It started when I had some spare cash lying around and bought a Google Nest to make things a bit more convenient, like having a personal assistant. Before this, I was already using a few smart devices such as an IndiHome STB (even though I bought a rooted one), smart lights, and smart power plugs. Up until then, I always controlled them manually without voice commands. Besides my phone being sluggish, doing it manually was simply faster than waiting for my slow phone to respond.

I ended up buying a chalk-colored Google Nest on Tokopedia, sorting listings from the lowest price. I got a brand-new, full-box unit for 400k IDR. The seller hadn't sold any Google Nest units before, though I wasn't worried since Tokopedia has a complaint feature if anything went wrong.

After waiting about 3 days, the package arrived. I started setting it up in the afternoon, and after hours of trying, I began to panic. Did I miss something obvious, or was something actually broken? I did skip the manual, sure, but all my other smart devices worked fine.

Right from the start, something felt off when the Google Nest showed this message: "This Nest Mini was manufactured for a different country, and may not be compatible with your Wi-Fi network".
I watched several Google Nest reviews on YouTube and nobody else seemed to run into that warning, which made me panic even more.

![Nest Mini was manufactured for a different country](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgsqo-gvw0DEraGfjxkFKSUyDNs5YsS9km3BqmKu6AOJc1v9r6nM9EE3CrMxzAFuowaAStHqmcTwJv7tSPHyaq04yjQEbXiJsrcHYDrqNVdNlrQb0Zu_NhdTCv4oinhG2CRyJrzGiv-BCX9/w242-h430/image.png)

When I tried connecting it to Wi-Fi, it showed up and then gave me these prompts: "Connect to same WI-FI", "Your nest mini was setup successfully but can't be found", and "Turn off AP Isolation". That made me think this Nest Mini might really not support Indonesian networks, or maybe just IndiHome, since I'm a loyal IndiHome user and hadn't tried another ISP.

![Turn OFF AP Isolation!](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEg5nJ0HheSPxlpfJyMbFQTsmbUTKxJHNabsuNCGvkZtVsKbNEreuNyc_rs7_NOyP6s89znLFXxsVRTbIU3wx23UXSg2C36DzaOCZspUsfitCQoOqSiMsu1fVq_TPEQZ9El_c0ml_CMOvfwV/w276-h490/image.png)

After running factory reset, setup, factory reset, setup more than 10 times, I still got nowhere.

Eventually, I filed a complaint with the seller, and this was their reply:

![jawaban seller](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgD-NBCgJrWVhpq6ZYRM6kIV3CagXL_Jr71UjBpzEvOT1vnMONLfdQTrttSMfmzXhwQ6f6l5FBp9kh-VqEva2xmJJTNbeczCEbVByc4J0k6fmF5oVVnO_kO3yV336p6GHLlk8vvvRb7imDR/w417-h284/image.png)

From that response, I figured the seller didn't know either and was just telling me to try the exact steps I had already gone through.

As an IT guy, I knew AP Isolation is a network feature that normally lives in the router settings. It is typically used on public Wi-Fi in hotels, airports, and similar places to keep each user isolated on a separate path. So I logged into the admin panel at `192.168.100.1`, only to find that the HG8245A router didn't expose any AP Isolation setting. Earlier, I also tested it using a mobile hotspot on the Tri network, and it worked right away. Of course it did, since a phone hotspot keeps all connected devices on the same local network. Still, I obviously couldn't keep tethering from my phone forever.

Next, I reached out to IndiHome via Twitter, and you can probably guess what they told me to do... yep, restart the modem. That obviously did nothing when I was asking them to check AP Isolation. Even after contacting customer support via email and Twitter, they seemed just as confused by the problem and told me to submit a troubleshooting form.

Because information on this Google Nest issue was so scarce, while waiting on Twitter for IndiHome CS to reply, I searched Twitter for "AP Isolation" and found someone with the exact same problem. Finally, I wasn't the only one.

After trading replies with Mas Aziz, I asked, "Bro, did IndiHome give you any solution?" and he replied with both the answer and the workaround below:

![sensor karna ga izin yang punya akun guys](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEjupYaycW-y2qv2pQYF3hg2vcQYIJwGy3eeTYjsH5iuFbKjTBVyylAbls65g5zLCZ9AKi_XeKEICMEtAB6oLGGxNSJhX2PVtmhR2lQ2tp6x5Q0vtiJfR_cPuR_nmRNAxQjxQnpA9w6Eg384/w519-h219/image.png)

Censored since I didn't ask the account owner's permission, guys.

So the fix is to connect a separate router behind the IndiHome router.
Up until now, I haven't done that for a few reasons: first, the power cost of running two routers 24/7; second, having two Wi-Fi networks feels awkward; and third, why buy the cheapest Google Nest listing only to spend almost the price of an official Indonesian-warranty unit on another router?

Then I had an idea: instead of buying a router, why not spin up my own Wi-Fi using my PC? I had a spare TP-Link WN727N USB Wi-Fi receiver left over from an old laptop with a broken built-in Wi-Fi adapter. I plugged it into my PC, turned it into a "portable router," and installed Connectify.

![Connectify to Google Nest](https://blogger.googleusercontent.com/img/b/R29vZ2xl/AVvXsEgImb_vnfGvPhL4zB5spamb17pcb880IdHTzinsYP0p7ZTh_za6mV86c205wIEb0iehHb4wGyz-DSD_ecxTRT7Ttfm7rNTxl2hf2WfqIwMgaVZM_fCw276CRLrldYhYuhWwkU-F4JPWugKd/w258-h466/image.png)

In the end, I canceled my Tokopedia complaint, and IndiHome never came up with a fix. Up until then, my Google Nest could only run when my PC was turned on.

## Conclusion and Solution

After some trial and error, I finally found a solution using a dummy Wi-Fi connection.
Suppose the Wi-Fi network you want your Google Nest to join has the SSID `'wifialdisaw'`.
Turn off the real `'wifialdisaw'` Wi-Fi, create a phone hotspot or Connectify network with the exact same SSID (`'wifialdisaw'`), and run through the Google Nest setup again.
Once setup finishes and it connects successfully, turn off the dummy Wi-Fi and turn the real Wi-Fi back on.
Done. Your Google Nest should now connect normally to your intended Wi-Fi network.
