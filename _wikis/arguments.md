---
layout  : wiki
title   : VMD - command line arguments
summary : Passing argumets so that tcl script can read
date    : 2020/05/27 22:53:47
updated : 2020/05/27 23:14:22
tag     : vmd tcl arguments
toc     : true
public  : true
parent  : [[VMD]]
latex   : false
---
* TOC
{:toc}

```bash
$ vmd -dispdev text -args 1 2 3 4 5 < path-to-script/script.tcl
$ vmd -dispdev text -args < path-to-script/script.tcl 1 2 3 4 5
$ vmd -dispdev text < path-to-script/script.tcl -args 1 2 3 4 5
```

```bash
puts [lindex $argv 0] # returns 1
puts [lindex $argv 1] # returns 2
puts [lindex $argv 2] # returns 3
puts [lindex $argv 3] # returns 4
puts [lindex $argv 4] # returns 5
```
