# Python 介绍

## Python 与人工智能

既然你来到了这里，我相信你一定对人工智能十分感兴趣。而 Python 正是人工智能领域的主要编程语言，当今的主流深度学习框架全部提供了 Python 库，例如 PyTorch 和 TensorFlow 等等。从科研界到生产界，Python 已经成为了共识。可以说，想要从事人工智能的相关工作，Python 是必须学习的一项前置技能。

## Python 能做什么

Python 的应用领域十分广泛，主要有如下方面：

+ 人工智能：PyTorch 和 Tensorflow 等深度学习框架提供完善的 Python API。
+ 网络爬虫：使用 Scrapy 等框架，从 Web 网页爬取数据并提取结构性数据。
+ 数据分析和可视化：使用 Pandas 和 Matplotlib 等第三方库，解决数据处理的一切需求。
+ Web应用开发：使用 Django 和 Flask 等 Web 开发框架，高效灵活地开发网站。

Python 的更多应用，在 GitHub 的高 Star 仓库 [awesome-python](https://github.com/vinta/awesome-python]) 中都有归纳。总而言之，Python 是一门无所不能的编程语言。

下面是一些简单的样例，选中代码块并点击运行按钮，你就可以看到运行结果了。

我们可以将函数绘制成曲线图：
```python
import numpy as np
import matplotlib.pyplot as plt

def f(t):
    return np.exp(-t) * np.cos(2*np.pi*t)

t1 = np.arange(0.0, 5.0, 0.1)
t2 = np.arange(0.0, 5.0, 0.02)

plt.figure()
plt.subplot(211)
plt.plot(t1, f(t1), 'bo', t2, f(t2), 'k')

plt.subplot(212)
plt.plot(t2, np.cos(2*np.pi*t2), 'r--')
plt.show()
```

我们还可以给程序设置进度条，方便我们观察运行的进度：
```python
import time
import random
from tqdm import tqdm

a = [0] * 20
for i in tqdm(a):
    time.sleep(random.random())
```

以上的代码依赖了第三方库，你暂时不必理解。一旦你掌握了 Python 这门语言，第三方库的学习就会非常轻松了。而相比其他语言，Python 又是简单易学的。

## 怎么学 Python

答案是自己动手。不仅是 Python，学习任何一项编程技术都需要勤于动手，自己把代码敲一遍、运行一遍，胜过你看十遍。

Python 的运行方式有两种，交互式和脚本式，OneFlow 智能云平台都支持。你现在打开的是一个 Jupyter Notebook 文件，也正在进行 “Python 交互式编程”。本系列从 Notebook 交互式编程开始介绍 Python，后续也会介绍 Python 脚本式编程。

## 本项目的文件组织形式

我们设计了一套针对初学者的动手学 Python 教程，每个“动手学 Python”的项目中都有若干个 Notebook 文件（`xxx.ipynb`），每个 `ipynb` 文件对应一个必备的 Python 知识点，点开即可边学边练。你只需要按照顺序学习，就能够顺利地掌握 Python 这门语言，而不必苦于记忆繁琐的细节和暂时用不到的知识。

还等什么，赶紧打开下一个文件，正式开始学习吧！