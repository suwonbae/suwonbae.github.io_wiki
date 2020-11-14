---
layout  : wiki
title   : How to install python with no permission
summary : 
date    : 2020/11/13 20:06:39
updated : 2020/11/13 20:41:07
tag     : python
toc     : true
public  : true
parent  : [[python]]
latex   : false
---
* TOC
{:toc}

Python can be installed readily by using apt on ubuntu and Homebrew on macOS. Without package tools such as apt and Homebrew, I would have to compile the codes by myself, which is not difficult either.

First, I download the latested release of Python from the official Python website. I choose tarball to install Python on a Linux system. I extract the tarball, change directory, and then execute the configure script.

```
tar -xf Python-3.?.?.tar.xz
cd Python-3.?.?
./configure
```

Build follows the configuration and I use this command:
```
make install
```

And the build process stops with the following error message.
```
/usr/bin/install -c python /usr/local/bin/python3.8
/usr/bin/install: cannot create regular file `/usr/local/bin/python3.8': Permission denied
make: *** [altbininstall] Error 1
```

If I was working on my personal machine with sudo access, I would just use this command:
```
sudo make install
```

Without sudo access, I have to specify to which path it is to be installed during the configuration.
```
./configure --prefix=/home/suwonbae/.local/
make
make install
```

In order to use my own version of Python, I have to tell explicitly in each python script like:
```
#!/home/suwonbae/.local/bin/python3.8
```
or
specify the path in .bash_profile script like:
```
export PATH=$PATH:/home/suwonbae/.local/bin
```
