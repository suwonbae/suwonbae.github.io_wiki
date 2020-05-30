---
layout  : wiki
title   : VMD - variable to string
summary : Loading a command-line argument and naming a filename with a prefix string
date    : 2020/05/30 01:05:43
updated : 2020/05/30 01:15:42
tag     : vmd tcl arguments string
toc     : true
public  : true
parent  : [[VMD]]
latex   : false
---
* TOC
{:toc}

```tcl
set ind 1
puts file${ind} #returns 'file1'
```

```tcl
set ind [lindex $argv 0]
set filename xyz${ind}
puts $filename #returns 'xyz1' given 1 as the command-line argument
```
