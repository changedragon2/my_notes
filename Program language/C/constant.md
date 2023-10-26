```C
int a = 5;
int b = 7;
const int fix = 10;
```
1. 指针 本身是一个常量
```C
int *const ptr1 = &a;
```

2. 指针储存的是一个常量
```C
const int *ptr2 = &a;
/* or */
int const *ptr2 = &a;
```

![constant](constant.png)

#### assignment
```C
/* ptr1 是常量，不能更改其值 */
ptr1 = &b;  // ERROR 
/* 可以改变 ptr1 储存地址处的值 */
*ptr1 = 10; // SUCCESS

/* ptr2 是变量指针，可以更改其值 */
ptr2 = &b;  // SUCCESS
/* ptr2 储存的地址的值是常量，不能更改 */
*ptr2 = 10; // ERROR
```

3. 指针本身是一个常量 且 指针储存的也是一个常量
```C
const int *const ptr3 = &a;
/* ptr3 的值 和 其储存地址储存的值都不能更改 */
ptr3 = &b;  // ERROR
*ptr3 = 1;  // ERROR
```