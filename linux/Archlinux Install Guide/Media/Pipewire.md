## 安装
与 jack 一样， PipeWire 内部没有实现连接逻辑，监视新流并将它们连接到适当的输出设备或应用程序的负担留给了称为会话管理器的外部组件，此处安装的是 wireplumber
```shell
sudo pacman -Syu --needed pipewire wireplumber
# for 32bit support
sudo pacman -S --needed lib32-pipewire
```

PipeWire可以用作音频服务器，类似于PulseAudio和JACK，安装 pipewire-alsa 以通过 PipeWire 使用 ALSA API 路由所有应用程序，安装 pipewire-jack 提供 jack 支持
```shell
sudo pacman -Syu --needed pipewire-audio pipewire-alsa pipewire-jack
# for 32bit support
sudo pacman -S --needed lib32-pipewire-jack
```