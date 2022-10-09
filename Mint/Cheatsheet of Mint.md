# Linux Mint Cheatsheet

## System Commands

'''
### Distribution Info

neofetch - Neofetch displays information about your operating system, software and hardware in an aesthetic and visually pleasing way.

w – Display who is online

whoami – Who you are logged in as

uname -a – Show kernel information

cat /proc/cpuinfo – CPU information

cat /proc/meminfo – Memory information

df -h – Show disk usage

du – Show directory space usage

free – Show memory and swap usage

'''

'''
### Navigation

pwd – print working directory 

cd – change directory 

mv <path to source directory/file> <path to destination directory/file> - move directory / file 

touch <filename> - create / update file 

ls –la – list contents of directory

cp –avr <path to source directory/file> <path to destination directory/file> - copy directory / file 

mkdir <directory name> - create directory

rm –rf <directory / file name> - delete directory / file

'''

'''
### Viewing

cat <path to file> - view contents of a file

less <path to file> - view contents of a file (screen full at a time with option to scroll backwards)

vi <path to file> - create and open / open file for editing in vi text editor 

tail <path to file> - view last 10 lines of the file 

tail –f <path to file> - view last 10 lines of a changing file (usually a log file) in real time

watch <linux command> - watch the output of a command (refreshes every 2 seconds by default)

more <path to file> - view contents of a file (screen full at a time)

nano <path to file> - create and open / open file for editing in nano text editor

head <path to file> - view first 10 lines of the file

'''

'''
### File and Folder Permissions

##### File Permissions Representations

r w x(owner) r w x(group) r w x(others) 

r (read) – Allows user to view the file – numerical value = 4 

w (write) – Allows user to edit the file – numerical value = 2 

w (write) – Allows user to edit the file – numerical value = 2 

<br>
chmod 777 <path to file> - Owner, group users and other users can read, write and execute the file. 

chmod 700 <path to file> - Owner can read, write and execute the file. Group users and other users do not have any
permission for the file. 


chmod 666 <path to file> - All users can read and write to the file. 

chmod 644 <path to file> - Owner can read and write to the file. Group users and others can only read the file

'''

'''
##### Folder Permissions Representation

d r w x(owner) r w x(group) r w x(others) 

r (read) – Allows user to list the files in the directory – numerical value = 4

w (write) – Allows user to create new files and delete the files in the directory – numerical value = 2

x (execute) – Allows user to change to the directory via cd command – numerical value = 1

chmod 777 <path to folder> - Allows owner, group members and others to list files in directory, create files in
directory, delete files from the directory and to change to the directory.

chmod 755 <path to folder> - Allows owner to list files in directory, create files in directory, delete files from the
directory and to change to the directory. Group members and others can change to the directory and list the files only.

chmod 700 <path to folder> - Allows owner to list files in directory, create files in directory, delete files from the
directory and to change to the directory. Group members and others do not have any permission on the directory. This
makes the directory private to the owner. 


'''



'''
### User Management

adduser <new user name> - create a new user

deluser <existing user name> - remove a user without removing user’s home directory

deluser <existing user name> -remove-home – remove a user with user’s home directory

addgroup <new group name> - create a new group

delgroup <existing group name> - remove a group

passwd – modify password

who – shows list of logged in users

useradd –g <group name> <user name> - add user to a group, group specified will be user’s primary group

useradd –G <group name> <user name> - add user to a group, group specified will be user’s secondary group

usermod –g <group name> <user name> - change user’s primary group

usermod –a –G <group name> <user name> - change user’s secondary group

chown <user name> <file name> - change file’s owner

chgrp <group name> <file name> - change file’s group ownership

'''

'''
### System

hostname - display the hostname of Linux Mint

uptime - displays how long the system has been running

echo $SHELL - displays the current Linux Mint(bash by default)

man <command name> - displays the manual pages of specified command

ps – lists all the processes running in the system 

top - real-time information about Linux system uptime, number of users, system load, number of tasks, and utilization
of system resources 

kill -9 <pid> - kills the process with the specified process id

killall proc – kills all processes named proc*

uname –a - name, kernel version, machine type, network node host name, processor type, OS release, OS version and
other system architecture details

lsb_release –a - LSB version, distributor ID, description of distribution, release number and codename of the
distribution

df –h – display file system and disk space usage

free –m – display amount of free and used system memory

lspci – lists all PCI buses and devices connected to them

lsusb – lists all USB buses and devices connected to them

lshal – lists all the devices that HAL(Hardware Abstraction Layer) is aware about i.e. most of the hardware connected to
your system

lshw – lists hardware present in the system including information about manufacturer, device type and where it is
connected.

'''

'''
### Networking

ping <website/ip address> - to test connectivity or response from a particular IP address or website

traceroute <website/ip address> - trace the network path to a website or IP address.

ifconfig - displays list of all network interfaces

ifconfig <interface> up - enables the specified interface

ifconfig <interface> down - disables the specified interface

iwconfig - displays list of all wireless network interfaces

ssh <user name>@<host name> - login to network host as specified user 

'''

'''
### Installation

apt-get install <packagename> - installs specified application / package

apt-get remove <packagename> - uninstalls specified application / package

apt-get update - updates the Linux Mint / Ubuntu package lists

apt-get upgrade - upgrades the Linux Mint/Ubuntu packages

apt-get -f install - troubleshoots broken packages

apt-get autoremove - automatically removes obsolete packages 

'''

'''
### Installation from source

./configure

make

make install

'''

'''
### Searching

locate <file name> - search the system for the specified file name

grep <pattern> <file name> - searches file for specified pattern

Linux command | grep <pattern> - searches the output of the command for the specified pattern

whereis <command> - shows the locations of the command’s executable file

which <command> - shows the executable which would be run by default for executing the command

'''

'''
### Compression

tar –czvf <archive name>.tar.gz <file name 1> <file name 2>…<file name n> - create a tarball by compressing the
specified files

tar –xzvf <archive name>.tar.gz – extract files from a tarball

tar –cf <archive name>.tar <file name 1> <file name 2>…<file name n> - create a tar archive by compressing the
specified files

tar –xf <archive name>.tar – extract files from a tar archive

gzip <file name> - compresses a file and creates a gzip archive called <file name>.gz

gzip –d <file name>.gz – extracts files from a gzip archive

'''

'''
### Power

poweroff – powers off the system

reboot – reboots the system

echo b > /proc/sysrq-trigger – hard reboot 

'''