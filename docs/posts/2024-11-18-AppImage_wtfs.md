---
title: "appimaged, where were you all this time?"
summary:
authors:
    - Georgi Georgiev
created: 2024-11-18
---

# appimaged, where were you all this time?

**TLDR: There is a daemon [appimaged](https://github.com/probonopd/go-appimage) you can install that watches for new AppImage files in /bin and ~/Downloads and automatically installs them.**

I've been using Linux systems for a while now and honestly, I've never really cared about how applications enter my system as long as I don't have to work too hard for it. I just want to get my work done and I'm okay with any type of packaging system, be it deb packages, AppImages, or Flatpaks, whatever works, works. However, I get annoyed whenever I see ineffincies that could be solved with some small amount of effort. 

One such annoyance is how AppImages get installed - you download it, open a terminal in the download directory, `chmod u+x` the file and then maybe move it to another directory. Why do I need to do all these things, why can't I just download them and use them right away?

To solve this annoyance, I was thinking of making my own daemon which checks for new AppImages in ~/Downloads and does the above things automatically. However, I never got around to, so I just suffered in silence. However, I was reading an online discussion and I read about [appimaged](https://docs.appimage.org/user-guide/run-appimages.html?highlight=daemon#appimaged) a daemon which checks predefined set of directories on the user's system and makes them accessible to the user. This is exactly what I was looking for! I dug around and I found that it's been around [since at least 2018](https://github.com/AppImageCommunity/appimaged). Why is this not part of distros? I know different distributions promote their own way of package distribution but this just makes sense to include.

I saw a [zdnet article](https://www.zdnet.com/article/what-are-appimages-and-how-do-you-use-them-on-linux/) from this year that kind of introduces this application distribution but it doesn't even mention appimaged. Why? 

Anyway, install appimaged and enjoy your AppImages.