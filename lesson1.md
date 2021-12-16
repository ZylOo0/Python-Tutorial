# Python介绍

## Python与人工智能
python语言在人工智能领域几乎是不可替代的存在。当今的主流深度学习框架全部提供了python库，例如pytorch和tensorflow等等。从科研到生产，python已经成为了业界的共识。可以说，想要从事人工智能的相关工作，python是必须学习的一项前置技能。

## Python能做什么
python是一门非常全能的语言，在人工智能以外的计算机相关领域也有广泛涉足，比如Web开发、爬虫、数据分析、科学计算等等。python能够引入非常多的外部库，这样它就能够以精炼的代码完成强大的功能。

我们可以使用pandas库来读取文件：
```
import pandas as pd
FILE_PATH = "./data/weather.csv"
df = pd.read_csv(FILE_PATH)
df
```
还可以使用matplotlib库来绘图：
```
import matplotlib.pyplot as plt
plt.plot(df["day"], df["temp-l"])
plt.plot(df["day"], df["temp-h"])
plt.show()
```

## 如何运行Python
python主要有交互式和脚本式两种运行方式，oneflow智能云平台可以完全兼容这两种方式。现在，我们正在一个Jupyter Notebook中以交互式的方式运行。你可以选中代码块，点击运行按钮，就可以看到代码的运行结果了。你也可以在代码块中进行修改。