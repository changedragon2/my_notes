1. install
```shell
# for GUI(qt based)
sudo pacman -S wireshark-qt
# for cli(terminal based)
sudo pacman -S wireshark-cli
```
2. usage
```shell
# GUI
wireshark
# cli
tshark
```

#### FAQ
1. permission
add user to wireshark group
```shell
# replace {current_username} with your username
sudo usermod -a -G {current_username},wireshark {current_username}
```
relogin(logout and login) or reboot to enable