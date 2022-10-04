# Linux Cheat Sheet

## System Commands

### Distribution Information
```
# Debian/Ubuntu
uname -a
lsb_release -a

# CentOS/RedHat
cat /etc/centos-release
cat /etc/redhat-release

# This will provide a lot more information
cat /etc/os-release
```

### Shut down or Reboot
```
shutdown -h now
reboot
```

### Permissions
```
# change the user:group ownership of a file/dir
chown root:git <file_or_dir>

# make a file executable
chmod u+x <file>
```

### Files and Directories
```
# create a new directory and all subdirectories
mkdir -p dir/dir2/dir3

# Send a command's output to file.txt, no STDOUT
ls > file.txt

# Send a command's output to file.txt AND see it in STDOUT
ls | tee /tmp/file.txt

# Search and Replace within a file
sed -i 's/original-text/new-text/g' <filename>
```

### See all set environment variables
```
env
```

## Searching

### File names
```
# search for a file in a filesystem
find . -name 'filename.rb' -print

# locate a file
locate <filename>

# see command history
history

# search CLI history
<ctrl>-R
```

### File contents
```
# -B/A = show 2 lines before/after search_term
grep -B 2 -A 2 search_term <filename>

# -<number> shows both before and after
grep -2 search_term <filename>

# Search on all files in directory (recursively)
grep -r search_term <directory>

# Grep namespace/project/name of a GitLab repository
grep 'fullpath' /var/opt/gitlab/git-data/repositories/@hashed/<repo hash>/.git/config

# search through *.gz files is the same except with zgrep
zgrep search_term <filename>

# Fast grep printing lines containing a string pattern
fgrep -R string_pattern <filename or directory>
```

### CLI
```
# View command history
history

# Run last command that started with 'his' (3 letters min)
!his

# Search through command history
<ctrl>-R


# Execute last command with sudo
sudo !!
```

## Managing resources

### Memory, Disk, & CPU usage
```
# disk space info. The '-h' gives the data in human-readable values
df -h

# size of each file/dir and its contents in the current dir
du -hd 1

# or alternative
du -h --max-depth=1

# find files greater than certain size(k, M, G) and list them in order
# get rid of the + for exact, - for less than
find / -type f -size +100M -print0 | xargs -0 du -hs | sort -h

# Find free memory on a system
free -m

# Find what processes are using memory/CPU and organize by it
# Load average is 1/CPU for 1, 5, and 15 minutes
top -o %MEM
top -o %CPU
```

### Strace
```
# strace a process
strace -tt -T -f -y -yy -s 1024 -p <pid>

# -tt   print timestamps with microsecond accuracy

# -T    print the time spent in each syscall

# -f    also trace any child processes that forked

# -y    print the path associated with file handles

# -yy    print socket and device file handle details

# -s    max string length to print for an event

# -o    output file

# run strace on all puma processes
ps auwx | grep puma | awk '{ print " -p " $2}' | xargs strace -tt -T -f -y -yy -s 1024 -o /tmp/puma.txt
```

## Networking

### Ports
```
# Find the programs that are listening on ports
netstat -plnt
ss -plnt
lsof -i -P | grep <port>
```

### Internet/DNS
```
# Show domain IP address
dig +short example.com
nslookup example.com

# Check DNS using specific nameserver
# 8.8.8.8 = google, 1.1.1.1 = cloudflare, 208.67.222.222 = opendns
dig @8.8.8.8 example.com
nslookup example.com 1.1.1.1

# Find host provider
whois <ip_address> | grep -i "orgname\|netname"

# Curl headers with redirect
curl --head --location "https://example.com"

# Test if a host is reachable on the network. `ping6` works on IPv6 networks.
ping example.com

# Show the route taken to a host. `traceroute6` works on IPv6 networks.
traceroute example.com
mtr example.com

# List details of network interfaces
ip address

# Check local DNS settings
cat /etc/hosts
cat /etc/resolv.conf
systemd-resolve --status

# Capture traffic to/from a host
sudo tcpdump host www.example.com
```

### Package Management
```
# Debian/Ubuntu

# List packages
dpkg -l
apt list --installed

# Find an installed package
dpkg -l | grep <package>
apt list --installed | grep <package>

# Install a package
dpkg -i <package_name>.deb
apt-get install <package>
apt install <package>

# CentOS/RedHat

# Install a package
yum install <package>
dnf install <package> # RHEL/CentOS 8+

rpm -ivh <package_name>.rpm

# Find an installed package
rpm -qa | grep <package>
```

### Logs
```
# Print last lines in log file where 'n'
# is the number of lines to print
tail -n /path/to/log/file
```
