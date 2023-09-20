### 调用解释器
```shell
# 输入python进入交互模式
python3
```
传入参数 argv
```python
import sys
```
sys.argv[0] 脚本名称
sys.argv[1] 参数1
...
- - -
### 运行环境
1. 字符编码
    默认 utf-8
声明所使用的编码
```python
# _*_ coding: encoding _*_
```
encoding是python支持的编码名称
```python
#!/usr/bin/env python3
# _*_ coding: encoding _*_
```
- - -
### 基本介绍
1. 注释
python使用 '#' 作为注释
```python
# This is the first comment
avr1 = 1 # This is the second comment

avr2 = "# This is not a commet because it's inside quotes"
```
2. 算术运算
+, -, *, / 加减乘除
```python
>>> 3 + 5
8
>>> 9 - 1
8
>> 3 * 3
9
>> 9 / 2
4.5
```
%, //, ** 取余, 整除, 求幂
```python
>>> 9 % 4
1
>> 9 // 4
2
>> 2 ** 3
8
```
= 赋值
```python
>>> val = 3
>>> print(val)
3
```
使用未定义变量错误
```python
>>> n  # try to access undefined variable
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
NameError: name 'n' is not defined
```
交互模式下 _ 储存最后打印的表达式
```python
>>> width = 3
>>> height = 4
>>> width * height
12
>>> width + _
15
# _ 变量应视为只读，不应给其赋值
```
3. 文本
字符串 类型 str，用 ' ' 或 " " 括起来
```python
>>> 'some text'
'some text'
>>> "other text"
'other text'
```
字符串中使用引用需转义
```python
>>> 'This is \"some text\"'
```
r取消转义
```python
>>> print("C:\some\name")  # here \n means newline
C:\some
ame
>>> print(r"C:\some\name")  # note the r before the quote
C:\some\name
```
多行字符串可用 """ """ 或 ''' ''' 表示
```python
>>> print("""some
...  text""")
some
 text
>>>
```
在行尾添加 \ 阻止换行
```python
>>> print("""some\
...  text""")
some text
>>>
```
使用 * 重复字符串 或 使用 + 组合字符串
```python
>>> "This is " + 3 * "some " + "text"
'This is some some some text'
```
相邻字符串会自动合并
```python
>>> "Some" " text"
'some text'
>>> text = ('Put several strings within parentheses '
... 'to have them joined together')
>>> print(text)
Put several strings within parentheses to have them joined together
```
字符串可通过下标索引
```python
>>> word = "Python"
>>> word[0]
'P'
>>> word[1]
'y'
>>> 
```
当下标为负数时，从右开始索引
```python
>>> word = "Python"
>>> word[-1]
'n'
>>> word[-2]
'o'
>>>
```
索引允许通过切片获取子字符串
```python
# start is included and the end is excluded, s[:i] + s[i:] = s
>>> word = "Python"
>>> word[0:4]
'Pyth'
>>> word[4:6]
'on'
>>> word[:4]
'Pyth'
>>> word[4:]
'on'
>>> word[:3] + word [3:]
'Python'
```
```code
 +---+---+---+---+---+---+
 | P | y | t | h | o | n |
 +---+---+---+---+---+---+
 0   1   2   3   4   5   6
-6  -5  -4  -3  -2  -1
```
使用超过范围的索引会导致错误
```python
>>> word = 'Python'
>>> word[10]
Traceback (most recent call last):
  File "<stdin>", line 1, in <module>
IndexError: string index out of range
```
切片索引可以超出范围
```python
>>> word = 'Python'
>>> word [5:10]
'n'
>>> word [10:]
''
```
内建函数 len() 返回字符串的长度
```python
>>> s = '123456789'
>>> len(s)
9
```
4. 列表
```python
>>> color = ["red", "green", "blue"]
>>> color
["red", "green", "blue"]
>>> print(color[0])
red
>>> color[-1]
'blue'
>>> color[:2]
['red', 'green']
>>> color[:]
['red', 'green', 'blue']
```
列表的内容可更改
```python
>>> num = [1, 3, 5, 8, 9]
>>> num
[1, 3, 5, 8, 9]
>>> num[3] = num[3] - num[0]
>>> num
[1, 3, 5, 7, 9]
```
切片也可以赋值
```python
>>> letters = ['a', 'b', 'c', 'd', 'e', 'f']
>>> letters[2:5] = ['C', 'D', 'E']
['a', 'b', 'C', 'D', 'E', 'f']
>>> letters[2:5] = []
['a', 'b', 'f']
>>> letters[:] = []
[]
```
列表可以嵌套
```python
>>> forground = ["red", "green", "blue"]
>>> background = ["#ffff00", "#00ffff"]
>>> ground = [forground, background]
>>> ground
[['red', 'green', 'blue'], ['#ffff00', '#00ffff']]
>>> ground[0]
['red', 'green', 'blue']
>>> ground[1][0]
'#ffff00'
