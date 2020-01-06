---
title: Add progress bars to any command
published: false
description: Tools like gzip and friends are great, but they don't have a progress bar.
canonical_url: https://github.com/Xowap/dev-blog/blob/master/articles/showdev/spybar.md
cover_image: https://thepracticaldev.s3.amazonaws.com/i/7huj3b9zy7m6dyva8amc.jpg
tags:
    - showdev
    - devops
---
Have you ever tried to compress a huge file, waited a bit in front of your terminal and wondered if you should go get a coffee or if it's just about to finish?

After spending some time dealing with huge files and trying to figure out how much I advanced, I ended up discovering tricks that I decided to industrialize. Enter [Spybar](https://github.com/Xowap/Spybar).

![`spybar gzip -c that_big_file.dat`](https://thepracticaldev.s3.amazonaws.com/i/iz3lys4p1q42xki0el0d.gif)

It's a simple Python script that you can get with a

```
pip install spybar
```

If you prefix a command with it, it will start it and display the progress bar. You can also attach to an existing PID. Everything is explained [in the readme](https://github.com/Xowap/Spybar).

This article is however not about the usage of the tool. It's about how it works.

Let's first state that it's only compatible with Linux. It could be that there is some way to do this in other operating systems but this article is not about that.

In Linux, there is a special directory, `/proc` which contains a directory for each running process.

Suppose that you are working on process `42`, you can list all the files open by a process by doing

```
ls -lsh /proc/42/fd
```

When you open a file, in C, you get an integer which is the file handler. All those integers are listed in the `fd` directory. They all are symbolic links to the actual file that they open. Using `ls`, once you've located the file you want, you can note down its number. Suppose that you're interested in number `3`.

There is a different folder which contains some meta-information about those handlers. Which you can simply access by doing

```
cat /proc/42/fdinfo/3
```

You'll get something alike of this:

```
pos:    569573376
flags:  0104000
mnt_id: 28
```

Including the `pos` line which indicates us where exactly the handler is pointing to.

Then you just need to know the size of the file and there you go, you know both the current position and the file size, that's all you need to generate a progress bar.

After doing this for a while I figured that I'd write that little tool so here we are. Thank you for reading!