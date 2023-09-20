suspend when close computer lid
```shell
sudo vi /etc/systemd/logind.conf
# uncoment this line
HandleLidSwitchExternalPower=ignore
# enable setting
sudo systemctl kill -s HUP systemd-logind
```