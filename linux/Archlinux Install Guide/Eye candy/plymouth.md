### Install
```shell
sudo pacman -S plymouth
```

### Configuration
1. 添加内核参数 splash(启动图形画面) quiet(抑制日志输出)
```shell
sudo vim /etc/default/grub
# 或者直接编辑 /boot/grub/grub.cfg, 在 linux 这一行 后添加参数
...
GRUB_CMDLINE_LINUX_DEFAULT="splash quiet"
...
```
2. 修改 hooks
```shell
sudo vim /etc/mkinitcpio.conf
...
MODULES=(nvidia)
...
HOOKS=(base udev plymouth ...)
...
```
3. 修改主题
```shell
sudo plymouth-set-default-theme -R theme_name
```
每次修改主题，需要重新生成 initramfs, 添加 -R 选项可自动生成
或手动修改 /etc/plymouth/plymouth.conf, 再手动生成 initramfs
默认 plymouth 配置 /usr/share/plymouth/plymouthd.defauts