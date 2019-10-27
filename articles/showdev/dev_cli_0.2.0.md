---
title: DEV-CLI 0.2.0
published: true
description: More complete API wrapper and new internals
canonical_url: https://github.com/Xowap/dev-blog/blob/master/articles/showdev/dev_cli_0.2.0.md
cover_image: https://thepracticaldev.s3.amazonaws.com/i/3wqyf6zw9c86tm06otk1.jpg
tags:
    - showdev
---

These last days I have been working on a [Retrofit](https://github.com/square/retrofit)-inspired library for Python called [Typefit](https://github.com/xowap/typefit). Since it's clearly not ready for production use yet I'm not doing an introductory post just yet, however as I'm learning to use it in real life I've decided to migrate [DEV-CLI](https://github.com/xowap/dev-cli) into using Typefit.

This new version does not bring any particular feature (nor any feature at all actually), however two changes emerge:

- The internal API wrapper is now type-safe and much more complete
- Instead of some boilerplate code it uses the Typefit API client builder

That is clearly not the news of the year but I also needed to test if this new version of the API works so I had to write an article :)