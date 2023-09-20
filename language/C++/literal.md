###### 定义整数
```code
# decimal
int a = 20;
# octal
int a = 024;
# hexadecimal
int a = 0x14;
```
###### 定义类型
```code
# character and character string literal
```

| Prefix |           Meaning            |   Type   |
|:------:|:----------------------------:|:--------:|
|   u    |     Unicode 16 character     | char16_t |
|   U    |     Unicode 32 character     | char32_t |
|   L    |        wide character        | wchar_t  |
|   u8   | utf-8 (string literals only) |   char   |

---
```code
# integer literals
```

|  Suffix  | Minimum Type |
|:--------:|:------------:|
|  u or U  |   unsigned   |
|  l or L  |     long     |
| ll or LL |  long long   |

---
```code
# floaing-point literals
```

| Suffix |    Type     |
| ------ |:-----------:|
| f or F |    float    |
| l or L | long double |
