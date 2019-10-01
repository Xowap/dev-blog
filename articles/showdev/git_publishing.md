---
title: Version and automate your dev.to publishing with GitHub Actions
description: What do devs do in the face of adversity? They dev!
tags:
  - showdev
  - tutorial
  - meta
published: true
cover_image: https://thepracticaldev.s3.amazonaws.com/i/cj1cc3jk1n3w1n1yig8o.jpg
canonical_url: https://github.com/Xowap/dev-blog/blob/master/articles/showdev/git_publishing.md
---
I love publishing on [dev.to](https://dev.to/), yet there is a very big problem related to doing this: the web editor is not really dev-friendly since it doesn't allow you to version your content. There is also the constant fear of doing something wrong and losing an article that you wrote within the browser because of stupid computer crash or other kinds of CTRL+Q disasters.

Yet, faced with a challenge, what do devs do? They dev!

First things first, I've created a [GitHub repo](https://github.com/Xowap/dev-blog) to manage all my upcoming Markdown files. Now I've got a place where to store my articles but how do I get them online?

Apparently the hot new thing is GitHub actions. So I created one in my repo! The GitHub interface is surprisingly intuitive for doing so. I'm absolutely no expert on the matter since I wrote [my first action ever](https://github.com/Xowap/dev-blog/blob/master/.github/workflows/publish.yml) about 5 minutes ago, but it's fairly easy to use since that same action published this very article!

In order to be able to publish using GitHub actions, you need some kind of script. I couldn't find anybody who did that (but maybe did I search not enough?) so I created my own tool. Let me introduce [DEV-CLI](https://github.com/Xowap/DEV-CLI)! 🎉 You'll find all the details in the README. You can of course use it right now to publish your Markdown, with or without GitHub actions 😇

I must say that this was a fun evening project. It's still completely experimental and I'd love feedback from other people doing the same thing &mdash; or not doing this if they have alternative workflows!