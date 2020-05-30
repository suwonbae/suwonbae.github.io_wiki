---
layout  : wiki
title   : how to update git on mac
summary : Apple's git to the official distro of Git
date    : 2020/05/29 05:00:16
updated : 2020/05/30 00:52:29
tag     : 
toc     : true
public  : true
parent  : [[git]]
latex   : false
---
* TOC
{:toc}

Typing the following command shows the version of the git.
```
$ git --version
```

```
git version 2.20.1 (Apple Git-117)
```

Let's switch to an official distro of git.

```
$ brew intall git
```

Typing the following must comes back with the latest version of git you just installed with Homebrew.
```
$ /usr/local/bin/git --version
```

```
git version 2.26.2
```

Git can be used as is with the path specified. However, it is not good to type the whole path every time you want to use git.

```
$ echo 'export PATH=/usr/local/bin:$PATH' >> ~/.bash_profile
```

```
$ source ~/.bash_profile
```

```
$ git --version
```

```
git version 2.26.2
```
