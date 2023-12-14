GDBus.Error:org.freedesktop.DBus.Error.ServiceUnknown: The name org.freedesktop.Notifications was not provided by any .service files

### 独立使用
1. 安装 daemon
```shell
# install notification-daemon
sudo pacman -S notification-daemon
```
2. 配置
```shell
sudo vim /usr/share/dbus-1/service/org.freedesktop.Notifications.service

[D-BUS Service]
Name=org.freedesktop.Notifications
Exec=/usr/lib/notification-daemon-1.0/notification-daemon
```

### 或安装其他程序
1. dunst
```shell
sudo pacman -S dunst
```