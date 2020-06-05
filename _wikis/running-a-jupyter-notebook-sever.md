---
layout  : wiki
title   : Running a notebook server
summary : 
date    : 2020/06/05 01:21:54
updated : 2020/06/05 01:56:23
tag     : jupyter python
toc     : true
public  : true
parent  : [[jupyter]]
latex   : false
---
* TOC
{:toc}

You already have Jupyter notebook installed on both remote and local machines.
In your notebook directory on the remote, type the following commands:
```sh
$ jupyter notebook --no-browser --port=8889
```
In order to tell local notebooks from remote ones, specify port 8889.

On the local,type the following:
```sh
$ ssh -N -f -L localhost:8889:localhost:8889 username:password@remote_server_ip
```

In order to stop notebook server running in background, type the following
```sh
$ jypyter notebook stop 8889
```

The first time you access the remote Jupyter notebook server with "localhost:8889" in your browser, you are asked for token.
Token can be found in the output as you run the jupyter notebook,
```sh
[I 01:43:20.084 NotebookApp] The Jupyter Notebook is running at:
[I 01:43:20.084 NotebookApp] http://localhost:8889/?token=01111111...
```
