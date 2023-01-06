
### *NIX Permissions
| sym        | code | desc                   |
|------------|------|------------------------|
| ---        | 0000 | no permissions         |
| -X-X-X     | 0111 | execute                |
| -w-w-w-    | 0222 | write                  |
| -wx-wx-wx  | 0333 | write & execute        |
| -r-r-r-    | 0444 | read                   |
| -r-xr-xr-x | 0555 | read & execute         |
| -rw-rw-rw- | 0666 | read & write           |
| -rwxrwxrwx | 0777 | read, write, & execute |
  

[Linux Distributions Wikipedia](https://en.wikipedia.org/wiki/Linux_distribution)


### Extract Directory of tar.gz files
gunzip -r directory/pathtoallfiles/*

### Extract Directory of .tar files
for f in filename*wildcard.tar; do
tar -xf "$f"
done

### List and delete first 5 files
ls | head -n 5 | rm --

### apt vs apt-get

"apt-get is considered lower level and backend, while apt is designed for humans"
apt and APT are not the same

apt hosts common packages from apt-get and apt-cache. Designed to fix dependecy issues that arise with apt apt-cache and apt-get. 

apt-get installs, updates and removes while apt-cache searches for new packages. apt-get is low-level and configurable.

apt-get + apt-cache + dpkg -l ==> apt

### APT
Advanced Package Tool - collection of tools for managing Debian's packaging system

uses libraries libapt-pkg and libapt-inst

CLI tools apt, apt-get, apt-cache, apt-config, and GUI tool aptitude work with Advanced Package Tool to perform their operational duties of installing, upgrading, and deleting. 

