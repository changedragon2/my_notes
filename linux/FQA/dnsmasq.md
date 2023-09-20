#### dnsmasq: failed to create listening socket for port 53: Address already in use

1. If you like to know what service is runing, do please:
```shell
# check what's listening on port 53 (domain)
sudo ss -lp "sport = :domain"
# It's usually systemd-resolved 
```

2. Edit dnsmasq configuration
```shell
# open configuration with your text editor
sudo vi /etc/dnsmasq.conf
# uncomment this line and change port to 5300
port=5300
# start dnsmasq service
sudo systemctl start dnsmasq
# enable service when reboot
sudo systemctl enable dnsmasq
```
