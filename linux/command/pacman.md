## 配置
/etc/pacman.conf
## 源
/etc/pacman.d/mirrorlist
## 使用
**Arch** 为滚动更新，使用 pacman 安装软件时需使用 -Syu 选项，使系统保持最新，避免部分更新
###### 更新系统
```shell
prompt> sudo pacman -Syu
```
###### 安装

1. 从镜像源安装
```shell
prompt> sudo pacman -Syu pkg_name1 pkg_name2 ...
```
2. 安装本地已经编译好的AUR包
```shell
sudo pacman -U pkg_name.pkg.tar.zst
```
###### 搜索
1. 搜索远程数据库（所有包的数据）
```shell
prompt> pacman -Ss pkg_name ...
```
2. 搜索本地数据库（以安装的包的数据）
```shell
prompt> pacman -Qi pkg_name 
```
3. 查看手动安装的包（如AUR, yay, paru）
```shell
prompt> pacman -Qm
```
4. 检查作为依赖项安装的软件包，但现在没有其他软件包依赖于它们
```shell
prompt> pacman -Qtd
```
5. 列出安装的AUR包
```shell
pacman -Qtm
```
###### 设备迁移
1. 备份已安装软件包列表
```shell
prompt> pacman -Qqen > pkglist.txt
# for AUR
prompt> pacman -Qqem > pkglist_aur.txt
```
2. 安装备份
```shell
# 编辑 pkglist.txt（和 pkglist_aur.txt）并删除新系统上不需要的驱动程序。 然后安装任何其他以前安装的软件
prompt> sudo pacman -Syu --needed - < pkglist.txt
```

### 彩蛋
在配置文件中加入 ILoveCandy 使进度条变成吃豆人
```shell
sudo vim /etc/pacman.conf

...
# Misc options
ILoveCandy
...

```