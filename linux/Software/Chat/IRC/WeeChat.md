## Install weechat
archlinux
```shell
linux> sudo pacman -S weechat
```
## Start weechat
```shell
linux> weechat
```

## Connect to Libera.Chat
1. Configuring SASL for WeeChat
    如果还没有连接到 Libera.Chat
    ```shell
    /server add libera irc.libera.chat/6697 -ssl
    ```
    如果已经建立连接或者连接失败并显示 irc: server "libera" already exists, can't add it!，使用以下命令确保SSL/TLS已经启用
    ```shell
    /set irc.server.libera.address "irc.libera.chat/6697"
    /set irc.server.libera.ssl on
    ```
    接下来配置SASL
    ```shell
    /set irc.server.libera.sasl_mechanism PLAIN
    # 已经注册过的用户名 chansteam3
    /set irc.server.libera.sasl_username <Your Name>
    # 密码 qweasdzxc321
    /set irc.server.libera.sasl_password <Your Password>
    /save
    ```
    推荐将密码设置为安全数据（如果已设置了passphrase跳过它）
    ```shell
    /secure passphrase <passphrase>
    /secure set libera_password <password>
    /set irc.server.libera.sasl_password "${sec.data.libera_password}"
    ```
## Usage
1. enable mouse
    ```shell
    # To enable mouse at startup
    /set weechat.look.mouse on
    # To enable mouse now, or use 'alt + m'
    /mouse enable