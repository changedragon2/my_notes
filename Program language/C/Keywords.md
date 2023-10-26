#### Keywords
|  auto  | break  | continue |  const   |  char  | case  |    do    | default |
|:------:|:------:|:--------:|:--------:|:------:|:-----:|:--------:|:-------:|
| double |  else  |   enum   |  extern  |  for   | float |   goto   |   int   |
|   if   |  long  |  return  | register | signed | short |  struct  | switch  |
| static | sizeof |  typeof  | unsigned | union  | void  | volatile |  while  |
#### auto
automatic variables can only be accessed within the function/block they are declared.
自动变量是在函数或块内的默认存储变量，也称为局部变量，只能在函数或块内访问
```C
auto int trash;
```

#### break/continue
the break statement is used to terminate the innermost loop
break 语句终止最内层的循环
continue 语句跳过本次循环

#### switch, case, default
```C
switch (Expression) {
    case '1':
        // operation 1
        break;
    case '2':
        // operation 2
        break;
    default:
        // default operation to be executed
}
```

#### int
整型
声明并定义一个整型变量 (声明是定义的子集，定义是声明的超集)
```C
int a;
```

#### char
declare a character variable 定义字符变量
```C
char chr = 'X';
```

#### double, float
定义浮点类型
the double and float are datatypes used to declared decimal type varibles
double have 15 decimal digit, and float only have 7
```C
double num;
float length = 3.75;
```

#### short, long, signed, unsigned
| Datatype               | Memory(bytes) | Range                                           | Format |
| ---------------------- | ------------- | ----------------------------------------------- | ------ |
| short int              | 2             | -2^15 ~ 2^15-1 (-32,768 ~ 32,767)               | %hd    |
| unsigned short int     | 2             | 0 ~ 2^16-1 (0 ~ 65,535)                         | %hu    |
| int                    | 4             | -2^31 ~ 2^31-1 (-2,147,483,648 ~ 2,147,483,647) | %d     |
| unsigned int           | 4             | 0 ~ 2^32-1 (0 ~ 4,294,967,295)                  | %u     |
| long int               | 4             | -2^31 ~ 2^31-1 (-2,147,483,648 ~ 2,147,483,647) | %ld    |
| unsigned long int      | 4             | 0 ~ 2^32-1 (0 ~ 65,535)                         | %lu    |
| long long int          | 8             | -2^63 ~ 2^63-1                                  | %lld   |
| unsigned long long int | 8             | 0 ~ 2^64-1                                      | %llu   |
| signed char            | 1             | -2^7 ~ 2^7-1 (-128 ~ 127)                       | %c     |
| unsigned char          | 1             | 0 ~ 2^8-1 (0 ~ 255)                             | %c     |
| long double            | 16            | 3.4E-4932 to 1.1E+4932                          | %lf    |

#### void
the keyword void means nothing
函数返回类型为void时，被视为没有返回值

#### const
the const keyword defines a variable who's value cannot be changed 定义常量
```C
const int a = 5;
```

#### do, while
循环
do-while loop
while loop
do-while 循环先执行一次，然后检查条件
while 循环先检查条件再决定是否执行
```C
do {
    // operation
} while(condition);
```
```C
while (condition) {
    // operation
}
```

#### for
循环
```C
for (int a; a < 5; a++) {
    // operation
}
```

#### if-else
选择语句
the if-else statement is used to make decisions
```C
if (condition 1) {
    // operation
}
else if (condition 2) {
    // operation
}
...
else if (condition n) {
    // operation
}
else {
    // operation
}
```

#### enum
枚举
```C
/* define enum type(user-defined datatype) week */
enum week {Sun, Mon, Tue, Wed, Thu, Fri, Sat};
/* define variable day with week type */
enum week day;
/* variable day have value zero, which is the index of constant Sum in week */
day = Sum;
```

#### extern
声明
The extern keyword is used to declare a variable or a function that has a external linkage outside of the file declaration
变量或函数声明时编译器不会为其分配内存，而定义会分配内存
声明可以多次，而定义只能一次
```C
extern int a;
extern int function_name(void);

/* 声明函数时 extern 省略不写为隐式声明，编译器会自动添加extern */
int function_name(void);
/* 声明变量时 extern 省略不写会被视为定义变量，编译器会为其分配内存 */
```

#### goto
跳转
It's used to jump from anywhere to anywhere within a function
goto 语句跳转到标签处执行
```C
lable_name:
    /* code */

goto lable_name;
```

#### sizeof
sizeof is a keyword that gets the size of an expression (variable, array, pointer etc.)
获取表达式的字节大小
```C
int a;
printf("size of int a is %d\n", sizeof(a));
```

#### register
register variables tell the compiler to store variables in the CPU register instead of memory
告诉编译器将该变量储存在CPU中的寄存器中，而不是储存在内存中，以获取更快的访问速度，用于频繁访问的变量
```C
register char x = 'c';
```

#### static
静态
函数内部定义的静态变量的值会一直保留直到程序结束
函数外部定义的静态变量只能在该文件中被访问
```C
#include <stdio.h>

void print_num() {
    static int a = 0;
    a++;
    printf("%d\n", a);
}

int main(void)
{
    print_num(); // print 1
    print_num(); // print 2
    print_num(); // print 3
    return 0;
}
```

#### struct
结构体
```C
struct Person {
    int age;
    char name[20];
    float height;
};
```

#### typedef
define  a data type with a new name, make code more readable
给数据类型起一个别名
```C
typedef int status;
status print_num(void);
```

#### union
联合体
与结构体类似，但联合体中的变量会共享内存位置
```C
union Todo {
    int number;
    char *list[10];
};
```

#### volatile
volatile变量不会被优化
```C
volatile int a;
```
