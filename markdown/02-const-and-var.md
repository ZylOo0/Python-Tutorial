# 变量与运算符

程序离不开数据和算法。因此，变量和运算符是你首先需要认识的两个概念。


## 常量与变量

简单理解，直接使用的数据，就是常量，最常见的常量有数字和字符串。

```python
50
```

```python
3.14
```

```python
"helloworld"
```

如果将这些数据存储起来，起个名字，我们就得到了变量，这类似于数学中的 `x`、`y`、`z`。
在 Python 中，我们可以通过 `=` 定义变量：

```python
x = 50
y = 3.14
z = "helloworld"
```

一旦定义了变量，我们就可以通过变量名去引用或者修改其中的数据：

打印：

```python
print(x)
```

```python
print(y)
```

```python
print(z)
```

修改：
```python
x = 500
y = "OneFlow Cloud"
```

```python
print(x)
```

```python
print(y)
```

在 Python 中，变量名的命名是有规定的：
- 字母或者下划线开头,之后跟若干个字母、数字、下划线（如 `1x` 是非法的变量名，`x1`、`_x1` 均可）
- 变量名不能与关键字重复，所谓的关键字，可以认为是 Python 程序内部的保留字

运行下面这段代码，会报出语法错误：

```python
if = 500
```


## 进位制

python中可以直接使用整数和小数，还支持10进制、16进制、2进制、8进制。
- 10 进制：默认情况
- 16 进制：`0x` 作为前缀
- 8 进制：`0o` 作为前缀
- 2 进制：`0b` 作为前缀

下面三个变量的值在10进制下均为16：

```python
number1 = 0x10
number2 = 0o20
number3 = 0b10000
```

```python
print(number1)
```

```python
print(number2)
```

```python
print(number3)
```


## 常见运算符

加、减、乘、除、整除、取余，他们分别对应的符号：

```text
+, -, *, /, //, %
```

掌握了数字之间的运算之后，可以把Python当作一个简易的计算器使用。

```python
100 + 555
```

```python
number1 = 3.1415
number2 = 2.73
```

```python
number1*number2
```

```python
number1/number2
```

```python
number1//number2
```

取余运算符的运算结果是：左边的数值除以右边的数值之后，所得的余数。

```python
10%3
```

```python
10%4
```

```python
10%5
```

取余运算符有很多的用处，比如可以将一个大数字，限定在一定范围内。再比如，可以通过对2取余来判断数字的奇偶性。在此后的学习中可以慢慢体会。


## 字符串

简而言之，字符串就是给人看的数据（而不是给机器进行运算的数据）。

```python
"I love this world"
```

在 Python 中，定义字符串数据的方法是使用引号，既可以使用双引号，也可以使用单引号，两者在绝大多数情况下是完全等价的：

```python
mystr1 = "hello"
mystr2 = 'world'
```

```python
print(mystr1)
```

```python
print(mystr2)
```

还可以使用三引号来表示字符串，其特点在于可以换行：

```python
mystr3 = '''
        *
      *****
    *********
      *****
        *
'''
```

```python
print(mystr3)
```


## 转义字符

如果字符串里本身就有引号，那么就会造成语法错误：

```python
print("Alice says, "Hello, Bob"")
```

这是因为 Python 只会将两个相邻的引号之间的内容识别为字符串，并不能够识别字符串中嵌套的引号。此时我们有两种做法解决这个问题。

- 字符串内外使用不同的引号：

```python
print('Alice says, "Hello, Bob"')
```

- 使用转义字符 `\"`：

```python
print("Alice says, \"Hello, Bob\"")
```

所谓的转义字符，就是用 `\` 加上特定字符，表达出特殊的显示效果。上面这个例子中，我们就将 `"` 表示的含义从“字符串的标识”转变为了“单纯的字符”。

这样的转义字符有很多，比如，`\n` 是换行符：

```python
print("hello\nworld")
```

再比如，`\t` 是水平制表符，也就是跳到下一个 TAB 位置：

```python
print("hello\tworld")
```

但是，假设我们要打印下面这个路径，由于转义字符的存在，就无法得到正确的输出：

```python
print("C:\notebook")
```

此时，我们可以在字符串前面加上一个`r`，表示原始字符串，不进行转义操作：

```python
print(r"C:\notebook")
```


## 字符串的格式化

当我们需要输出多个相似的字符串时，如果完整地创建每个字符串变量，就会显得非常冗余：

```python
mystr1 = "Wish you good luck, Alice"
print(mystr1)
mystr2 = "Wish you good luck, Bob"
print(mystr2)
```

这种情况下，最好的做法是格式化，就是在基本的字符串变量中“留空”，然后用其他数据“填空”：

```python
mystr3 = "Wish you good luck, {0}"
print(mystr3.format("Alice"))
print(mystr3.format("Bob"))
```

到这里，你已经掌握了如下内容：
- 学会了使用常量和变量，以及用 `print()` 函数来打印它们
- 学会了把 Python 当计算器用
- 学会了字符串的基本特性