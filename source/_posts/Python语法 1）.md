---
title: python语法 1）
top: false
comments: true
tags: python
top_img: https://w.wallhaven.cc/full/x8/wallhaven-x8e89o.jpg      #点进文章的
cover: https://gimg2.baidu.com/image_search/src=http%3A%2F%2Fwww.linuxprobe.com%2Fwp-content%2Fuploads%2F2019%2F12%2F4-4.png&refer=http%3A%2F%2Fwww.linuxprobe.com&app=2002&size=f9999,10000&q=a80&n=0&g=0n&fmt=jpeg?sec=1621728499&t=a273dccc8bbb05a97309829bfed72369    #界面外的
---

**缩进**：python中的缩进是用来只是代码块
如果省略缩进则会报错，空格数取决于自己（在一个代码块中必须使用数目一样的空格）
**注释**：# 开头（单行注释）
"""   """ 三引号开始三引号结尾(多行注释)
**创建变量**：python中创建变量没有声明变量的命令，首次赋值时，即是创建变量
对于字符串串变量而言，则需要使用单引号或双引号声明
**变量名称**：变量可以使用短名称（如 x 和 y）或更具描述性的名称（age、carname、total_volume）。
**Python 变量命名规则**：
变量名必须以字母或下划线字符开头
变量名称不能以数字开头
变量名只能包含字母数字字符和下划线（A-z、0-9 和 _）
变量名称区分大小写（age、Age 和 AGE 是三个不同的变量）
**向多个变量赋值：**可以在一行中为多个变量赋值

```python
x, y, z = "silu", "azhi", "shen"
```

    也可以为多个变量赋予相同的值
```python
x = y = z = "silu"
```

**输出变量：print语句

 - 文字 + 变量（需将文字放置引号内）


```python
x = "xiaozhi"          #仅为x为字符串时成立
print("azhi" + x)
```

 - 对于数字而言 + 起运算符作用

**格式化输出：**
格式化符号

 - 整形


```python
x = 6
print("今天学了%d个语法" %x)
print("今天学了%03d个语法" %x) # %03d 不足三位补零，超过三位原值。
```

 - 浮点型

```python
x = 5.50
print("小阿志%f元一斤" %x)   #默认是六位小数
print("小阿志%0.2f元一斤" %x) 
```

 - 字符串型

```python
x = 'azhi'
print("室友%s胖胖的" %x)
```

 - 多个格式化输出

```python
name = 'azhi'
age = 18
print("胖胖的室友叫%s，今年%d岁了" %(name,age))
print(""胖胖的室友叫%s，明年%d岁了" %(name,age+1)")   #多个格式化输出
```

 - f'{}' 格式化表达式

```python
age = 18
name = azhi
print(f'室友的名字时{name}，今年{age}岁了') #相对于%格式化 f格式化语法更简便更快捷。
```

**全局变量：**

 - 在函数外部创建变量

```python
x = "azhui"
def myfunc():
  print(x)
myfunc()
```

 - 在函数内部创建全局变量，使用global关键字

```python
def myfunc():
  global x
  x = "silu"
myfunc()
print(x)
```

 - 如果在函数内部创建与全局变量相同的名称的变量，该变量为局部变量，并且只能在函数内部使用，相同名称变量的全局变量将保留原样，并且拥有原始值

```python
x = "silu"
def myfunc():
  x = "azhi"
  print(x)
myfunc()
print(x)
```

 - 在函数内部更改全局变量的值，使用 global  关键字

```python
x = "silu"
def myfunc():
  global x
  x = "azhi"
myfunc()
print(x)
```

**内置数据类型**
在编程中，数据类型是一个重要的概念。
变量可以存储不同类型的数据，并且不同类型可以执行不同的操作。
在这些类别中，Python 默认拥有以下内置数据类型：

| 文本类型： | str |
|--|--|
| 数值类型： |int, float, complex  |
| 序列类型： | list, tuple, range |
|映射类型：| dict|
|集合类型：  | set, frozenset |
|布尔类型： |bool|
|二进制类型|bytes, bytearray, memoryview|


**获取数据类型**
您可以使用 type() 函数获取任何对象的数据类型：

```python
x = "silu"
print(type(x))
```

**类型转换**
您可以使用 int()、float() 和 complex() 方法从一种类型转换为另一种类型：




**复数**
复数用 "j" 作为虚部编写
**多行字符串:**
用三个双（单）引号将多行字符串赋值给变量

```python
a = """Python is a widely used general-purpose, high level programming language. 
It was initially designed by Guido van Rossum in 1991 
and developed by Python Software Foundation. 
It was mainly developed for emphasis on code readability, 
and its syntax allows programmers to express concepts in fewer lines of code."""
print(a)
```

**字符串是数组**
像许多其他流行的编程语言一样，Python 中的字符串是表示 unicode 字符的字节数组。
但是，Python 没有字符数据类型，单个字符就是长度为 1 的字符串。
方括号可用于访问字符串的元素。

获取位置 1 处的字符（第一个字符的位置为 0）：

```python
a = "Hello, World!"
print(a[0])
```

**转义字符：#待补充**
\t （一个tab键四个空格）
**裁切：（含左不含右）**
指定开始索引和结束索引，以冒号分隔，以返回字符串的一部分。

```python
b = "Hello, World!"
print(b[2:5])  #打印出 llo  注意：是从位置2打印到位置5（不含5）
```

**负的索引：（-1是最后一个索引）**
获取从字符串末尾开始切片

```python
b = "Hello, World!"
print(b[-5:-2])  #打印出 orl 从位置5到位置1的字符，从字符串末尾开始计数
```










