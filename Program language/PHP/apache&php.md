#### Apache
确保已经安装 apache 且能正常工作

#### PHP Install
```shell
sudo pacman -S --needed php php-fpm
```

#### Configuration
1. php
```shell
sudo vi /etc/php/php.ini
```
Timezone
```shell
# edit this line to set your timezone e.g. Asia/Shang
date.timezone = "Aisa/Shang"
```
Display errors to debug php code
```shell
# edit this line
display_errors = On
```
SQL
e.g. postgresql  ensure postgresql installed
```shell
# uncomment these lines
extension=pdo_pgsql
extension=pgsql
```
Cache
zend opcache
```shell
# uncomment this line
zend_extension=opcache
```

2. php-fpm
default is ok
```shell
# position
/etc/php/php-fpm.d/www.conf
```

2. apache
Create this config
```shell
sudo vi /etc/httpd/conf/extra/php-fpm.conf

# These lines are the contents
DirectoryIndex index.php index.html
<FilesMatch \.php$>
    SetHandler "proxy:unix:/run/php-fpm/php-fpm.sock|fcgi://localhost/"
</FilesMatch>
```
Enable proxy module and php-fpm config
```shell
sudo vi /etc/httpd/conf/httpd.conf

# uncomment these lines
LoadModule proxy_module modules/mod_proxy.so
LoadModule proxy_fcgi_module modules/mod_proxy_fcgi.so

# add this line
Include conf/extra/php-fpm.conf
```

#### Start
1. start php-fpm.service
```shell
sudo systemctl start php-fpm.service
```
2. start or restart httpd.service

#### Test
create test.php in apache DocumentRoot (e.g. /srv/http)
```shell
sudo vi /srv/http/test.php

# These are the contents
<?php phpinfo(); ?>
```
open this file in your browser
```
# test.php URL
# 80 is the default port for http server
# you need to change the port if you changed it before
http://127.0.0.1:80/test.php
```
[Defaul Local URL](http://127.0.0.1:80/test.php)