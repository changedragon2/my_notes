#### Intro
授权非特权应用程序访问特权操作的权限
#### Install
1. polkit
```shell
sudo pacman -S --needed polkit
```
2. authentication agent
```shell
lxqt-policykit
```
3. autostart
```
# add to .xinitrc or other autostart script
lxqt-policykit-agent
```