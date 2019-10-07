---
title: What CAPTCHA do you use?
description: I'm tired of training Google's AI, do we have other CAPTCHA options out there?
published: true
tags:
  - webdev
  - discuss
canonical_url: https://github.com/Xowap/dev-blog/blob/master/articles/discuss/what-captcha-do-you-use.md
cover_image: https://thepracticaldev.s3.amazonaws.com/i/8ss50puzgvxb5ympmi4t.jpg
---

Anybody that has been on the web long enough knows that it is crawling with bots and nasty stuff just trying to spam you from all the possible channels. That's why CAPTCHA were invented.

It quickly became a hurdle for developers to create such elements since you constantly need to do something up to speed to beat AI. The folks at reCAPTCHA quickly understood that and provided a great CAPTCHA service.

What was pretty smart about it is that instead of generating stupid text they would use a state-of-the-art OCR to read scanned books and whenever they found something that the OCR could not read (thus that a bot could not read) then they would ask humans to read it in the form of a CAPTCHA. Genius!

Google quickly understood that this is a huge opportunity to get free labor doing all the classification and training of your AI and bought reCAPTCHA a few years later.

Now my problem is the following: I'm sick of working for Google for free and there is no way that I make my users work for Google for free.

Most of the time I avoid CAPTCHAs by having a logic that just allows for bots to register/do whatever without hurting the real users. But sometimes you can't have that.

Does anyone know any other form of Turing test that would be:

- Very quick
- Non-intrusive
- Not a SaaS

Thanks everyone for your feedbacks!