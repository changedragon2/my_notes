#### Install
```shell
sudo pacman -S --needed postgresql
```

#### Initial configuration
1. switch to user postgres with privilege elevation program like su, sudo
```shell
sudo -iu postgres
# or use su
# su -l postgres
```
then the prompt would like this 
[postgres]$
2. initialize db
```shell
[postgres]$ initdb -D /var/lib/postgres/data
# or
# initdb --locale=C.UTF-8 --encoding=UTF8 -D /var/lib/postgres/data --data-checksums
```
3. start/enable service
```shell
sudo systemctl start postgresql
# enter this for auto start when boot
sudo systemctl enable postgresql
```
4. create user/database
```shell
# if the postgresql user have the same name as the linux user, then you can access postgresql database without to login
[postgres]$ createuser --interactive

# if you don't grant your new user database creation privilege, add '-U postgres' as an argument for below command
createdb mydatabasename
```
5. access database shell
```shell
psql -d mydatabasename
```
some helpful command:
get help
```shell
\help
```
list all database
```shell
\l
```
connect to particular database
```shell
\c mydatabasename
```
list all users and their permission levels
```shell
\du
```
show summary information about all tables in the current database
```shell
\dt
```
exit/quit psql shell
```shell
\q
# or press Ctrl+d
```
see all meta-commands
```shell
\?
```