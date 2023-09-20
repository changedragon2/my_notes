1. install need packages
```shell
sudo pacman -S bluez bluez-utils
```
2. enable bluetooth service
```shell
# start up when boot
sudo systemctl enable bluetooth
# start service right now
sudo systemctl start bluetooth
```
3. console command
```shell
bluetoothctl
```
for gtk interface
```shell
sudo pacman -S blueman
```