### Service
1. 创建服务
```shell
vi /etc/systemd/system/v2ray.service
```
```service
[Unit]
Description=V2Ray Service
Documentation=https://www.v2fly.org/
After=network.target nss-lookup.target

[Service]
User=changedragon2
CapabilityBoundingSet=CAP_NET_ADMIN CAP_NET_BIND_SERVICE
AmbientCapabilities=CAP_NET_ADMIN CAP_NET_BIND_SERVICE
NoNewPrivileges=true
ExecStart=/home/changedragon2/Downloads/v2ray-linux-64/v2ray run
Restart=on-failure
RestartPreventExitStatus=23

[Install]
WantedBy=multi-user.target
```
2. 加载配置
```shell
sudo systemctl daemon-reload
```
3. 将v2ray路径添加到 PATH 环境变量
```shell
sudo ln -s /home/changedragon2/Downloads/v2ray-linux-64/v2ray /usr/bin/v2ray
```
4. 启动服务
```shell
sudo systemctl start v2ray
sudo systemctl enable v2ray
```