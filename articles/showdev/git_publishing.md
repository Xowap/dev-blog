---
title: Version and automate your dev.to publishing with GitHub Actions
description: What do devs do in the face of adversity? They dev!
tags:
  - showdev
  - tutorial
published: false
canonical_url: https://github.com/Xowap/dev-blog/blob/master/articles/showdev/git_publishing.md
---
I love publishing on [dev.to](https://dev.to/), yet there is a very big problem related to doing this: the web editor is not really dev-friendly since it doesn't allow you to version your content. There is also the constant fear of doing something wrong and losing an article that you wrote within the browser because of stupid computer crash or other kinds of CTRL+Q disasters.

Yet, faced with a challenge, what do devs do? They dev!

I've created a [GitHub repo](https://github.com/Xowap/dev-blog) to manage all my upcoming Markdown files.

Apparently the hot new thing is GitHub actions. I don't know yet how this works since I'm writing this article to find out and you'll notice that this paragraph will be changed to explanations in the final version of the article.

In order to be able to publish using GitHub actions, you need some kind of script. I couldn't find anybody who did that (but maybe I searched bad?) so I created my own tool. Let me introduce [DEV-CLI](https://github.com/Xowap/DEV-CLI)! 🎉 You'll find all the details in the README.

And then... Who knows? This article is still in beta.