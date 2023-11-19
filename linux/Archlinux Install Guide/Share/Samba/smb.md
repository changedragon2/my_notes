#### Install
```shell
sudo pacman -S samba
```

#### Configuration
1. get sample conf
```shell
sudo mkdir -p /etc/samba/ && wget "https://git.samba.org/samba.git/?p=samba.git;a=blob_plain;f=examples/smb.conf.default;hb=HEAD" -O /etc/samba/smb.conf
```
2. add a user
```shell
sudo smbpasswd -a smb_user
```
list  smb user with
```shell
sudo pdbedit -L -v
```
change smb user password
```shell
sudo smbpasswd smb_user
```
create anonymous user
```shell
sudo useradd guest_user -s /bin/nologin
# add these in /etc/samba/smb.conf
#...
[global]
security = user
map to guest = bad user
guest account = guest

[guest_share]
    comment = guest share
    path = /tmp/
    public = yes
    only guest = yes
    writable = yes
    printable = no
```
enable symlink follow then, restart smb.service.
```shell
# /etc/samba/smb.conf
#...
[global]
   follow symlinks = yes
   wide links = yes
   unix extensions = no
```
