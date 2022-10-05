[![Businge Scott](https://img.shields.io/badge/Businge%20Scott-Linux-green.svg)]()
[![License: MIT](https://img.shields.io/badge/License-MIT-yellow.svg)](https://opensource.org/licenses/MIT)

# Linux Environment Fundamentals

## Introduction

Undertaken as fullfillment of the action plan to complete a short Linux course focused on linux essentials, file- system, directory structure, the command-line and go through Linux privilege escalation on user and administrative accounts.

## Course

> Introduction to the LPI Linux essentials certification (010 - 150) (by David Clinton on pluralsight)

## Course Modules

 - Introduction to Linux Operating system
 - Finding your way around the Linux system / Linux directories
 - Power of the Command line
 - Security and file permissions 

## Introduction to Linux Operating system

***Advantages of linux***
- Cheaper to own (open source)
- More secure (limited privileges by default, diverse file system architectures, open source thus more eyeballs and helping hands)
- Fewer malware threats 
- used in majority of cloud VMS and famous docker built on linux

***Linux distributions types***

***Popular ones;***
- Android. for mobile.
- Red Heart Enterprise Linux (RHEL). it's an enterprise distros.
- CentOS. this is the community rebuild for RHEL.
- Ubuntu. all round.

***others;***
- kali. this distribution is optimised and enhanced for security.
- Mint. recommended for easy personal use with it’s desktop.
- SUSE - OpenSUSE
- Scientific Linux. this is optimised for science and advanced math.
- Raspbian. meant to be embedded in IOT devices / mini architectures. 

***Package managers;***
-  **apt-get** for online packages and **dpkg** on local packages for Ubuntu, debian, mint.
-  **yum** for online packages and **RPM** for local packages access on Redhat, Fedora, Amazon linux.

## Finding your way around the Linux system / Linux directories

Basic / fundamental commands

lsb_release -a Check linux distribution system.

***Monitoring and Networking***

```

- vmstat to get memory details.

- vmstat -S M to see memory usage in mb's.

- vmstat -a to see active / inactive memory.

- uptime to see system load (cpu) 1min, 5mins, 15mins.

- who to see logged in users and consoles (names and tty.

- whoami - show current logged in user. (name)

- top to display and update sorted info about processes

- netstat -alt to see listening tcp ports.

- netstat -alu to see listening udp ports.

- netstat -alx to see listening sockets.
 
 ```

***Networking***
```
- ip route show - route

- ip addr show - ip config

- ipv6 / ipv4 128 bit and 32 bit addresses

- netstat -i  - interface info

- netstat -r - route info

- DNS - map ip figures to human readable language

- host name - ip to dns

- nslookup - check IP address that's mapped to a domain name
```

***Text and file manipulation***

```

- grep to filter.

- cat to read files sequentially.

- less to paging data of a file.

- head - first 10 lines of a file.

- tail - last 10 lines of a file.

```

***Cmd admin***

```

- mkdir dir_name - create a new directory

- cd dir_name - change to a directory

- touch file_name - create a new file

- vim file_name- open a file to either view or edit with vim

- mv old_file_name new_file_name - rename a file

- cp old_file_name new_file_name - copy content to a file

- date > file_name  - append to a file

- date >> file_name  - Overwrite a file

- ps  - see running processes

- ps aux | grep process_name - filter a particular running process 

- df -h  - check disk space usage

- date - check date (day, time, year, timezone)

- time - check current time

- cd .. - Go back a single step to previous directory

- cd ~  - go to home directory

- man 'command' - checkout details about a manual page.

- sort - organizing output in order

- sort -r  - organize output in reverse order

- ls  - directory listings

- rm - delete

- rmdir - delete dir

- find - locate files

- grep - filter

- cat /etc/shells - List of available shells on the system

- chsh -s /usr/bin/bash - change shell

- sudo - administrative privelages

- apt-get install - install new packages

- apt-get upgrade  - run upgrades on already installed packages

- && - run many commands in sequence e.g apt-get install && apt-get upgrade && ls -l

- !cat !grep  - recall full previous ran command starting with either cat, or grep

```

***Linux directory structure***

```

/   
- Root directory. Everything on the linux system located here.

/home
- Home directories for all users to store their personal files.

/etc
- Contains configuration files required by all programs.

/proc
- Contains information about system process. It's a filesystem with text information about system resources. For example: /proc/uptime
- /proc/{pid} directory contains information about the process with that particular pid.

/tmp
- Directory that contains temporary files created by system and users. Files under this directory are deleted when system is rebooted.
- It's worth noting that files under /var/tmp are considered more important and aren't deleted when a system is rebooted. 

/var
- var stands for variable files.
- Content of the files that are expected to grow can be found under this directory too. 

/dev
- Contains device files that include terminal devices, usb, or any device attached to the system. e.g /dev/tty1, /dev/usbmon0

/bin
- Contains binary executables.Common linux commands you need to use in single-user modes are located under this directory too. e.g ps, ls, ping, grep, cp.

/sbin
- Just like /bin, /sbin also contains binary executables though commands located under this directory are used typically by system aministrator, for system maintenance purpose. e.g iptables, reboot, fdisk, ifconfig,

/usr
- Contains binaries, libraries, documentation, and source-code for second level programs.
- /usr/bin contains binary files for user programs.
- /usr/sbin contains binary files for system administrators.
- /usr/lib contains libraries for /usr/bin and /usr/sbin
- /usr/local contains users programs that you install from source. For example, when you install apache from source, it goes under /usr/local/apache2

/lib
- Contains library files that supports the binaries located under /bin and /sbin

/boot
- Contains boot loader related files. e.g Kernel initrd, vmlinux, grub files are located under /boot

/opt
- opt stands for optional and contains add-on applications from individual vendors.
- add-on applications should be installed under either /opt/ or /opt/ sub-directory.

/mnt
- Temporary mount directory where sysadmins can mount filesystems.

/media
- Temporary mount directory for removable devices. e.g /media/cdrom for CD-ROM; /media/floppy for floppy drives

/srv
- srv stands for service and contains server specific services related data. e.g /srv/cvs contains CVS related data.

```

## Power of the Command line

***Globing*** 
```
cp file*  - all instances 

file? - single instance  

rm file* - deletes all files starting with file
```

***archiving*** 
```
.tar - archive

.zip - zipped with zip algorithm

tar xzf file.tar.gz 

x - extract files from archive

z - compressed or zipped

f - file follows
```

> Bash Scripting 

- command line syntax and simple design  as prerequisite

- functional in nature (inputs, variables and control structures)

- shebang (#!/bin/bash) binary bash

> list packages

- yum list 

- apt list 

- dpkg list

## Security and file permissions 

***Good practices***
```
- log in as normal user.

- create separate user accounts. e.g sudo user add -m scott (add user scott)

- limit each user’s authority.

- sudo to invoke admin rights for a single command. 

- su (switch user)
```

- Reading, writing, and executing are the three main settings in permissions.

- users are placed into a group when their accounts are created.

- All files and directories are "owned" by the person who created them.

- The first column shows current permissions; it has ten slots. The first slot represents the type of file. The remaining nine slots are actually three sets of permissions for three different categories of users.

```
For example:  -rw-rw-r-- 

r — file can be read

w — file can be written to

x — file can be executed (if it is a program)

-(dash) — specific permission has not been assigned
```

- Use the ***chmod*** command to change permissions.
 
- If you are the owner of the file or are logged into the root account, you can change any permissions for the owner, group, and others.

- NB: Remember that file permissions are a security feature. Whenever you allow anyone else to read, write to, and execute files, you are increasing the risk of files being tampered with, altered, or deleted. As a rule, you should only grant read and write permissions to those who truly need them.

```
-rw-rw-r-- 

chmod o+w file
-rw-rw-rw-

chmod go-rw file
-rw-------

chmod a-rwx file
---------- (no permissions for all)

chmod u+rw foo.txt
-rw-------

```
***Identities***
```
u — the user who owns the file (that is, the owner)

g — the group to which the user belongs

o — others (not the owner or the owner's group)

a — everyone or all (u, g, and o)
```

***Permissions***
```
r — read access

w — write access 

x — execute access
```

***Actions***
```
+ — adds the permission

- — removes the permission

= — makes it the only permission
```

Here is a list of user permissions and corrsponding values.

```
g+w — adds write access for the group

o-rwx — removes all permissions for others

u+x — allows the file owner to execute the file

a+rw — allows everyone to read and write to the file

ug+r — allows the owner and group to read the file

g=rx — allows only the group to read and execute (not write)
```

***file***

code | Numerical value| Permissions
------------ | ------------- | ------------- 
-rw-------   |600 | only owner with read and write permissions.
-rw-r--r--   | 644 | only owner with read and write permissions, group and others have read only permissions.
-rwx------   | 700 | only owner with read and write permissions. group and others have no permissions. 
-rwxr-xr-x   | 755 | only owner with read and write permissions, group and others have read and execute only.
-rwx--x--x   | 711 | only owner with read and write permissions, group and others have execute only permissions.
-rw-rw-rw-   | 666 | all can read and write to the file.
-rwxrwxrwx   | 777 | all can read, write and execute to the file.

***directory***

code | Numerical value| Permissions
------------ | ------------- | ------------- 
drwx------ |700 | only user with read and write permissions in this directory.
drwxr-xr-x | 755 | all can read the directory; users and groups have read and execute permissions.

## The MIT License (MIT)

Copyright (c) 2022 [BUSINGE SCOTT [Morbius00]]

> Permission is hereby granted, free of charge, to any person obtaining a copy
> of this software and associated documentation files (the "Software"), to deal
> in the Software without restriction, including without limitation the rights
> to use, copy, modify, merge, publish, distribute, sublicense, and/or sell
> copies of the Software, and to permit persons to whom the Software is
> furnished to do so, subject to the following conditions:
>
> The above copyright notice and this permission notice shall be included in
> all copies or substantial portions of the Software.
