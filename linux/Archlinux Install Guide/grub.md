1. install grub and efibootmgr
```shell
sudo pacman -S --needed grub efibootmgr
# for detect other system like windows, alos install prober
sudo pacman -S --needed os-prober
```

2. config
```shell
sudo vi /etc/default/grub
# uncomment this line to enable os detect
GRUB_DISABLE_OS_PROBER=false
```
3. generate config
注：在windows中关闭快速启动，才能检测到windows
```shell
# detect other systems
os-prober
# generate grub.cfg
sudo grub-mkconfig -o /boot/grub/grub.cfg
```
