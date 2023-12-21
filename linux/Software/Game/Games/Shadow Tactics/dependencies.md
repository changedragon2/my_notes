for amd
1. enable multilib in pacman.conf
2. install amd driver and 32bit sound system packages

#### FAQ
1. libGL.so.1: cannot open shared object file: No such file or directory
```shell
# install glu
sudo pacman -S --needed lib32-glu
```
2. libXcursor.so.1: cannot open shared object file: No such file or directory
```shell
# install 32bit libxcursor
sudo pacman -S --needed lib32-libxcursor
```
3. libXrandr.so.2: cannot open shared object file: No such file or directory
```shell
# install 32bit libxrandr
sudo pacman -S --needed lib32-libxrandr
```