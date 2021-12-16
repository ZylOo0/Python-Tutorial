# 变量和基本数据类型

## 变量
一个变量被赋值后才会创建成功，赋值时不需要声明类型。

用等号=来给变量赋值，左边是变量名，右边是值。

下面的代码创建变量a并赋值为0，然后使用print函数将变量的值打印出来：
```
a = 0
print(a)
```

<br>

## 基本数据类型

<br>

### **数字（Number）**
python中最常用的数字类型就是整数型int和浮点数型float。

我们创建变量b和c，其中b的值类型为int，c的值类型为float：
```
b = 10
c = 10.0
print(b)
print(c)
```

两种类型的数据混合运算，结果为浮点数：
```
d = b * c
print(d)
```

除法运算返回浮点数：
```
e = b / 2
print(e)
```

除了int和float，python还支持布尔型bool和复数型complex。

<br>

### **字符串（String）**
字符串用于表示文本，用单引号''或者双引号""括起来。

下面创建变量并分配一个字符串：
```
s1 = "hello wolrd"
print(s1)
```

使用反斜杠\来转义特殊字符，比如"\n"表示换行：
```
s2 = "hello\nworld"
print(s2)
```

字符串支持索引和切片操作。

通过[]来索引获得字符串中的字符：
```
s3 = s1[0]
print(s3)
```

通过[:]来截取字符串中的子字符串：
```
s4 = s1[0:5]
print(s4)
```

字符串支持加法+和乘法*运算。

使用+来拼接字符串
```
s5 = s1 + s2
print(s5)
```

使用*来重复字符串
```
s6 = s1 * 3
print(s6)
```

注意，字符串是不可变对象，因此不可以对字符串中的字符进行修改。

<br>

### **列表（List）**
列表是一种复合数据类型，可以将不同类型的值组合在一起，用方括号[]标注，用逗号分隔。

下面创建一个列表：
```
list1 = [5, 'abc', 7.5]
print(list1)
```

与字符串类似，列表也支持索引和切片操作：
```
sub1 = list1[0]
sub2 = list1[1:3]
print(sub1)
print(sub2)
```
可以发现，列表索引返回的是单个值，切片返回的仍然是一个列表。而字符串的索引和切片都会返回一个字符串。

列表也支持加法+和乘法*运算：
```
list2 = list1 + sub2
list3 = list1 * 3
print(list2)
print(list3)
```

与字符串不同的是，列表是可变对象，列表中的元素是可以改变的：
```
list1[2] = 10
print(list1)
```

<br>

### **元组（Tuple）**
元组与列表非常相似，最主要的不同之处在于元组是不可变对象，它的元素不能修改。元组用圆括号()标注，用逗号分隔。
下面创建一个元组：
```
tuple1 = (15, 20, 'hello', 17.5)
print(tuple1)
```

元组的索引和切片操作都是和列表一样的：
```
sub3 = tuple1[0]
sub4 = tuple1[1:4]
print(sub3)
print(sub4)
```

元组也可以进行加法+和乘法*运算：
```
tuple2 = tuple1 + sub4
tuple3 = tuple1 * 3
print(tuple2)
print(tuple3)
```

<br>

### **集合（Set）**
集合是由不重复元素组成的无序容器。集合一般用于检测元素是否存在，以及消除重复元素。集合还支持交集、并集等数学运算。

下面创建一个集合：
```
best = {'Beijing', 'Shanghai', 'Shenzhen'}
print(best)
```

使用|符号进行并集运算，使用&符号进行交集运算：
```
north = {'Beijing', 'Harbin', 'Xi\'an'}
south = {'Shanghai', 'Shenzhen', 'Hangzhou'}
print(north | south)
print(north & best)
print(south & best)
```

<br>

### **字典（Dictionary）**
字典是一种映射类型，用花括号{}标注，它是一个键值对的集合。其中，键必须使用不可变类型，且在该字典中唯一。
下面创建一个字典：
```
dict1 = {'name': 'orange', 'num': 12, 6: 'price'}
print(dict1)
```

我们可以使用中括号来获取键对应的值：
```
print(dict1['name'])
```

我们也可以修改和添加字典中的元素：
```
dict1['num'] = 20
dict1['size'] = 'big'
print(dict1)
```