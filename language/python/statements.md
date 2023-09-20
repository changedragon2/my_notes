1. if
```python
if condition:
    statements
elif condition:
    statements
else:
    statements
```
example:
```python
# /usr/bin/env python
num = input("Please enter a digit: ")
if num.isdigit():
    num = int(num)
    if num < 0:
        print(num, " is negative")
    elif num == 0:
        print(num, " is equal to zero")
    else:
        print(num, " is positive")
else:
    print(num, "is not digit !!!")
```
output:
```shell
Please enter a digit: 3
3 is positive
```
---
2. for
```python
for variable in something:
```
example:
```python
# /usr/bin/env python
game = { "Terraria":"fun", "PUBG":"not fun", "Stardew Valley":"fun" }
for name, status in game.items():
    if status == "fun":
        print(name, "is fun")
```
output:
```shell
Terraria is fun
Stardew Valley is fun
```