---
title: Batch installing fonts in multiple subdirectories
author: 'Devon Zuegel'
tags: ['mac', 'fonts', 'batch', 'install', 'command line']
collection: posts
date: 'February 2 2015'
img: 'http://i.stack.imgur.com/o76m6.png'
---

I'm a digital pack rat, especially when it comes to fonts. Every time I see a nice typeface, I immediately forget whatever it is I'm actually reading and instead dig into the source code, find its name, and search the corners of the web for a a free copy. It doesn't help that my favored form of procrastination is scrolling through pages upon pages of fonts on sites like [MyFonts.com](https://www.myfonts.com/) and [FontSquirrel.com](http://www.fontsquirrel.com/). The result is that I frequently find myself with a mess of directories containing `.ttf` and `.otf` files.

The sad hangover to my binge is actually getting the fonts into Font Book. Macbooks have no easy way to get multiple fonts into Font Book all at once, leaving you with the painful and humiliating task of installing them by hand, one by one. It's particularly unpleasant when the files are in multiple subfolders, which is the common format of the downloaded bundles I love so much.

Luckily, it's easy to install all fonts within the subfolders of a directory from the command line.

![](http://i.imgur.com/u7Om82G.png =50x)

``` bash
find ~/Desktop/New\ Fonts/ -name "*.ttf" -exec cp -iv {} /Library/Fonts \;
```