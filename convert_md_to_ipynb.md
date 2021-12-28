# 如何将md文件转换为ipynb文件

docs.oneflow.org 中的基础专题，同时也被放到了 oneflow.cloud 中作为 Jupyter 项目。docs.oneflow.org 中的内容是 markdown 写的，因此有将 markdown 转为 Jupyter Notebook 的需求。

首先，我们需要为 Jupyter Notebook 安装一个插件 Jupytext。打开命令行，输入以下命令来安装：

```
pip install jupytext --upgrade
```

然后打开 Jupyter Notebook，将需要转换的 markdown 文件上传到工作目录中去：

![image.png](https://oneflow-public.oss-cn-beijing.aliyuncs.com/convert_md_to_ipynb/img1.png)

进入该文件，此时它已经可以像一个 ipynb 文件一样运行了。

接下来，点击左上角 File，选择 Download as -> Notebook (.ipynb)：

![image.png](https://oneflow-public.oss-cn-beijing.aliyuncs.com/convert_md_to_ipynb/img2.png)

此时 ipynb 文件就下载完成了。