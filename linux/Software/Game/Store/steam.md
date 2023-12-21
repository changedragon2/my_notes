### Enable Multilib
```shell
sudo vim /etc/pacman.conf

# uncomment these lines
[multilib]
Include = /etc/pacman.d/mirrorlist
```
update
```shell
sudo pacman -Syu
```

### Make Driver is installed
1. nvidia
[nvidia-driver](obsidian://open?vault=my_notes&file=linux%2FArchlinux%20Install%20Guide%2FDriver%2FNVIDIA)
2. amd
[amd-driver](obsidian://open?vault=my_notes&file=linux%2FArchlinux%20Install%20Guide%2FDriver%2FAMD)

### Install
```shell
sudo pacman -S steam
```