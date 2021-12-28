# 使用 input 获取用户输入

## 什么是内置函数

在 Python 中，从运行开始，就有一些可以现成使用的函数，我们称为“内置函数”。
我们之前使用的 `print`，就是一个内置函数，它的作用是将内容输出到控制台。
我们可以通过 `dir` 内置函数，查看 Python 中的所有内置函数：

```python
dir(__builtins__)
```

## 内置函数 input

`print` 和 `input` 是我们学习的头两个内置函数。
- `print`：输出函数，将数据输出到控制台
- `input`：输入函数，可以将键盘的输入，给保存到变量中

使用 `input` 函数读取键盘的输入，保存到变量 `myname` 中：

```python
myname = input("Please enter your name: ")
```

然后使用 `print` 函数将它打印出来：

```python
print(myname)
```

有了输入和输出后，我们可以更灵活的处理我们的程序。

```python
name1 = input("Please enter your name: ")
name2 = input("Please enter your name: ")
mystr = "Wish you good luck, {0}"
print(mystr.format(name1))
print(mystr.format(name2))
```

## input 的返回内容不能直接进行数字计算

我们使用 `input` 函数来读取数字：

```python
num1 = input("Please enter a number: ")
```

就会发现，使用这个变量进行计算时会报错：

```python
num1 + 1
```

这是因为，`input` 获取的输入内容是字符串类型的，`num1` 变量其实是一个字符串，而不是数字。数字运算只能在数字类型的数据之间进行，

## 内置函数 int、float 和 str

既然 `input` 函数只能获取字符串，那怎么来得到数字呢？

我们不需要从输入中直接获取数字，我们可以通过另外一个内置函数 `int` 来将字符串转换为数字：

```python
num1 = int(num1)
print(num1)
```

这里将 `num1` 传入 `int` 函数中，函数返回一个整数型数字，并重新将变量 `num1` 的值修改为该数字。

再次对 `num1` 进行数字运算，就不会报错了：

```python
num1 + 1
```

`int` 返回的是整型的数字，也就是整数，另一个内置函数 `float` 则会返回浮点型的数字，也就是小数：

```python
num2 = '3.14159'
num2 = float(num2)
print(num2)
```

反过来，将字符串转换为数字也是可以的，我们需要用到内置函数 `str`：

```python
num2 = str(num2)
print(num2)
```

本课中你学会了：
- 使用 `input` 函数获取用户输入的字符串
- 使用 `int`、`float` 和 `str` 函数将字符串和数字互相转换

Python 的内置函数还有很多，在接下来的课程中你会慢慢遇到。