详见[zsh](https://zsh.sourceforge.io/Doc/Release/index.html#Top)
### 安装
```shell
# Arch , Manjaro etc.
linux> sudo pacman -S zsh
# Debain , Ubuntu etc.
linux> sudo apt install zsh
```
### 配置文件路径
```shell
# 所有用户
/etc/zsh/zprofile
# 当前用户
~/.zshrc
```
### 配置
```shell
touch ~/.zshrc
```

prompt : 类似 bash 中的 PS1
    如在.zshrc 中输入并保存：
```
PROMPT='%n in %~ ->'
```
    重新打开终端（shell为zsh）或source ~/.zshrc 后如图
![prompt](prompt.png)
    显示了当前用户（%n表示），当前工作目录（%～表示）
 
%F：foreground color 前景色
```
PROMPT='%F{#fa7c04}%n%f in %F{#ffff00}%~%f ->'
```
![prompt-color](prompt-color.png)

13.2.1 Simple Prompt Escapes
```
%%
    一个 ' % ' 字符
%)
    一个 ' ) ' 字符
```

13.2.2 Login infomation
```
%l
    登陆的 tty 路径，不带 ' /dev/ ' 前缀。若以 ' /dev/tty ' 开头，该前缀将被删除（如登陆tty1 将显示 1)
%y
    登陆的 tty 路径，不带 ' /dev/ ' 前缀，不会特殊对待 ' /dev/tty '（如登陆tty1 将显示 tty1）
%M 
    这台机器的 hostname
%m
    hostname 一部分，以 ' . ' 分隔，后面接整数以显示主机名的多个组成部分，负数则显示尾部部分
%n
    $USERNAME
```

13.2.3 Shell state
```shell
%#
# 等价于
%(!.#.%%)
# root 用户为 ‘#’
# 普通用户为 ‘%’ 
# 或改成 %(!.#.$) 则普通用户为 '$'
%?
    上一次命令执行返回的状态（0表示成功）
%_
%^

%d
%/
    当前工作目录，' % ' 后加 正整数 表示 仅从尾部开始显示几层目录，否则显示完整路径
%~
    与%d和%/相似，当目录从 $HOME 开始时，将会用 ' ~ ' 替代或作为 前缀(仅当短于完整路径)，
```

13.2.4 Date and time
```
%D
    日期：年-月-日 格式
%W
    日期：月/日/年 格式
%w
    星期 日
%T
    当前时间 24小时制
%t
%@
    当前时间 12小时制 am/pm
%*
    当前时间 显示秒数 24小时制
%D{string}
    如%D{%H:%M:%S} 显示当前时间

13.2.5 Visual effects
%B(%b)
    开始（结束）粗体模式
%E
    清除到行尾
%U(%u)
    开始（结束）下划线模式
%S(%s)
    开始（结束）标准输出模式
%F(%f)
    开始（结束）使用前景色：%F{#color}text with foreground color%f
%K(%k)
    开始（结束）使用背景色：%K{#color}text with background color%f
```