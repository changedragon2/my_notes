#### hyprpaper
1. install
```shell
sudo pacman -S hyprpaper
```
2. configuration
```shell
sudo nvim ~/.config/hypr/hyprpaper.conf
```

``` contents
preload = {/path/to/wallpaper}
# use xrandr to get current monitor name
wallpaper = {monitor},{/path/to/wallpaper}
```