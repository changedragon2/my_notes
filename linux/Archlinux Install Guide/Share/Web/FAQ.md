1. 中文字符乱码
```shell
sudo vi /etc/httpd/conf/httpd.conf
# locate this line
ServerRoot "/etc/httpd"
# add these lines
AddDefaultCharset utf-8
IndexOptions +Charset=UTF-8
AddCharset UTF-8 .utf-8
#
```