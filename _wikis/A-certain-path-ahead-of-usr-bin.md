---
layout  : wiki
title   : Amending PATH to have a certain path ahead of /usr/bin
summary : 
date    : 2020/12/23 15:11:18
updated : 2020/12/23 15:14:32
tag     : path
toc     : true
public  : true
parent  : [[shell]]
latex   : false
---
* TOC
{:toc}

In your `~/.bash_profile`, add the specific path ahead of `$PATH`.
```
PATH="/sdcc/u/sbae/.local/bin:$PATH"
```

Restart Terminal or `source ~/.bash_profile`
