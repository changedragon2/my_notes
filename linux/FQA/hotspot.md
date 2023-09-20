#### Connection activation failed: IP configuration could not be reserved (no available address, timeout, etc.)
1. check log file
```shell
# use root user
su
# check NetworkManager status
systemctl status NetworkManager
```
2. check and whatch that dnsmasq was used but not installed
```shell
# install dnsmasq
sudo pacman -S dnsmasq
# change port so that will not