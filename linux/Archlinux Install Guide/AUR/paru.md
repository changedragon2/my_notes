#### Install
1. ensure base-devel is installed
```shell
sudo pacman -S --needed base-devel
```
2. clone paru
```shell
git clone https://aur.archlinux.org/paru.git
```
3. compile
```shell
makepkg -s
```
4. install
```shell
sudo pacman -U paru*.zst
```
#### Config
1. Edit /etc/pacman.conf
```shell
sudo nvim /etc/pacman.conf
```
2. Uncomment this line
```shell
Color
```