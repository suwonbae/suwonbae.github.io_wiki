---
layout  : wiki
title   : How to use HiDPI resolutions
summary : But FHD HiDPI is not activated on my U2719D
date    : 2020/12/21 22:51:05
updated : 2020/12/21 22:56:44
tag     : mac hidpi
toc     : true
public  : true
parent  : [[etc]]
latex   : false
---
* TOC
{:toc}

1. using one-key-hidpi 

2. customization
Ensable HiDPI Mode
```
$ sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool true
```
https://codeclou.github.io/Display-Override-PropertyList-File-Parser-and-Generator-with-HiDPI-Support-For-Scaled-Resolutions/

In order to disable hidpi resolutions
```
$ sudo defaults write /Library/Preferences/com.apple.windowserver.plist DisplayResolutionEnabled -bool NO
```
