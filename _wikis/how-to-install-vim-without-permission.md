---
layout  : wiki
title   : Installing Vim without permission
summary : 
date    : 2020/12/23 15:28:30
updated : 2020/12/23 15:31:51
tag     : vim sudo
toc     : true
public  : true
parent  : [[vim]]
latex   : false
---
* TOC
{:toc}

```
$ git clone https://github.com/vim/vim.git
```

```
$ cd vim/src
$ LDFLAGS=-L/sdcc/u/sbae/.local/lib ./configure --prefix=/sdcc/u/sbae/.local/bin
$ make
$ make isntall
```

```
export PATH=$PATH:/sdcc/u/sbae/.local/bin
```
or if you want to have the path ahead of `/usr/bin`

```
export PATH=/sdcc/u/sbae/.local/bin:$PATH
```
