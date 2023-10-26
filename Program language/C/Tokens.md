#### Keywords 关键字 
|  auto  | break  |  case  |  const   |  char  | continue |    do    | default |
|:------:|:------:|:------:|:--------:|:------:|:--------:|:--------:|:-------:|
| double |  else  |  enum  |  extern  |  for   |  float   |   goto   |   int   |
|   if   |  long  | return | register | signed |  short   |  struct  | switch  |
| static | sizeof | typeof | unsigned | union  |   void   | volatile |  while  |

#### Identifiers 标识符
1. consist 字母数字和下划线组成
alphabets:    a-z, A-Z
digit:             0-9
underscore:  _
2. rule 只能以字母或下划线开头
Must begin with alphabets or underscore
Shoud not be keywords
Shoud not contain space
Shoud not longer than 31 characters

#### Constants 常量
variables with fixed values 定义后不能被修改

#### String 字符串
an array of characters ended with a null character (```\0```) 以 ```\0``` 结尾的字符数组
C 和 C++ 中字符串一般用双引号，字符用单引号
```C
char string[12] = {'h', 'e', 'l', 'l', 'o', ',', 'w', 'o', 'r', 'l', 'd', '\0'};
char string[12] = "hello,world";
char string[] = "hello,world";
```

#### Special Symbols 特殊符号
brackets []
parentheses ()
braces {}
comma ,
colon :
semicolon ;
asterisk *
assignment operator =
pre-processor #
period .
tilde ~

#### Operators 运算符
1. unary operators 一元运算符
2. binary operators 二元运算符
    arithmetic operators 算术运算符
    relational operators 关系运算符
    logical operators 逻辑运算符
    assignment operators 赋值运算符
    bitwise operators 位运算符
3. ternary operators 三元运算符 e.g. ?