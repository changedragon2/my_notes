1. if
```bash
if condition ; then
    statements
fi
```
or
```bash
if condition
then
    statements
fi
```
---
2. for
```bash
for variable in list
do
    statements
done
```
example:
```shell
for char in a b c
do
    echo "$char"
done
```
output:
```shell
a
b
c
```
---
3. while
```shell
while condition
do
    statements
done
```
---
1. case
```bash
case "$variable" in
    var1 | var2)
        statements ;;
    var3 | ...)
        statements ;;
    *)
        statements ;;
esac
```