1. ensure lsof is installed
```shell
sudo pacman -S --needed lsof
```

```shell
# replace {port} with port number
sudo lsof -i :{port}
```