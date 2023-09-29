#### install
```shell
# xorg server input
sudo pacman -S xorg-server xorg-xinput
```
#### configuration
1. install start script
```shell
# xorg start script
sudo pacman -S --nedded xorg-init
# cp start script to ~/.xinitrc
cp /etc/X11/xinit/xinitrc ~/.xinitrc
```
2. modify start script
```shell
# modify .xinitrc
nvim ~/.xinitrc
# comment these line
#twm &
#xclock -geometry 50x50-1+1 &
#xterm -geometry 80x50+494+51 &
#xterm -geometry 80x20+494-0 &
#exec xterm -geometry 80x66+0+0 -name login

# add your windows manager here, such as dwm
# exec {your-wm}
exec dwm
```
3. start  xorg server with command startx
```shell
startx
```
4. install other xorg app
```shell
sudo pacman -S --needed xorg-xkill xorg-xhost xorg-xauth xorg-xrefresh xorg-xsetroot
```