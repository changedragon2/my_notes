hello.c 源文件
```C
#include <stdio.h>

int main()
{
    printf("hello, world\n");
    return 0;
}
```
[hello.png](hello.png)
```
linux> gcc -o hello hello.c
```
![gcc_en](gcc_en.png)
![[Drawing 2023-07-09 13.33.30.excalidraw]]
gcc 编译器驱动读取源文件 hello.c，将其翻译为可执行目标文件 hello
该翻译过程可分为四个步骤：
1. 预处理阶段 (Preprocessing phase)
    ```sh
    # 使用gcc
    gcc -o hello.i -E hello.c
    # 或者使用预处理器 cpp
    #cpp -o hello.i hello.c
    ```
    编译前的预处理，修改以‘#’ 开头的语句，通常以 .i 作为生成文件的后缀
    * 如 "#include <stdio.h>" 将替换成头文件'stdio.h' 的内容并插入源文件中，
    * 如 "#define PI 3.14" ，会将源文件中所有 PI 替换成 3.14
    hello.c 预处理生成 hello.i 文件
2. 编译阶段 (Compilation phase)
    ```shell
    gcc -o hello.s -S hello.i
    ```
    编译器将经过预处理的源文件翻译成汇编语言
    hello.i 编译生成 hello.s 文件
3. 汇编阶段 (Assembly phase)
    ```shell
    gcc -o hello.o -c hello.s
    # 或直接使用汇编器 as
    #as -o hello.o hello.s
    ```
    汇编器将汇编语言翻译成机器语言
    hello.s 汇编生成 可重定位目标程序 hello.o
4. 链接阶段 (Linking phase)
    ```shell
    gcc -o hello hello.o
    # 或直接使用链接器 ld
    #ld -o hello hello.o
    ```
    链接器处理并链接程序所需要的函数库，形成可执行文件