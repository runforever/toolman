# 在 VSCode 中使用 Jupyter Notebook

*作者：奔跑的青椒*<br />
*出处：知识星球【涛哥聊 Python】*

> Jupyter Notebook 是一个开源的Web应用程序，允许用户创建和共享包含代码、方程式、可视化和文本的文档，它是数据科学和机器学习领域最常用的工具之一。

> VSCode 全称 Visual Studio Code，是微软出的一款轻量级代码编辑器，免费、开源而且功能强大。

### 背景
由于平时会做一些做数据科学项目，经常会使用 Jupyter Notebook 做数据探索，正常使用 Jupyter Notebook 是在浏览器中使用，过程中经常在代码编辑器和浏览器之间来回切换，浏览器中编辑代码的体验也非常不好，于是乎就有了在代码编辑器中使用 Jupyter Notebook 的想法，Google 一番后，原来 VScode 在 2019 年 10 月 9 日已经原生支持使用 Jupyter Notebook 了。

在浏览器中使用 Jupyter Notebook 的效果：

![图1-1](http://cdn.defcoding.com/067C1802-C6DA-4194-AF52-BA0DCCE28150.png)

### VSCode 中使用 Jupyter Notebook
效果如下：

![图2-1](http://cdn.defcoding.com/239D34F6-975F-4920-A676-B254D639E28B.png)

**1. 创建 Notebook**<br />
Mac 环境下使用快捷键 `Cmd + Shift + P`，输入 `Create New Blank Jupyter Notebook`。<br />

![图2-2](http://cdn.defcoding.com/641F5FB8-8E14-4D97-8ED6-EA87A147F664.png)

Mac 环境下使用 `Shift + Enter` 快捷键运行代码，也可以使用 `Alt + Enter` 和 `Ctrl + Enter`，读者可以亲自测试并了解三者的区别。

**2. 更快的自动补全**<br />

![图2-3](http://cdn.defcoding.com/41DD6B46-75BB-48CE-BB96-3D2224A33A52.png)

**3. VSCode IntelliSense（智能提示）**<br />
![图2-4](http://cdn.defcoding.com/9780A400-84A2-408C-8469-45E13F096A50.png)

**4. 图片显示效果**<br />
![图2-5](http://cdn.defcoding.com/AFBC48B0-BBB7-4571-A67B-28A45AF656CE.png)

**5. 连接远程 Jupyter Notebook服务**<br />
由于 Mac 不适合用作机器学习项目研究，所以我专门购买了一台有 RTX2060 显卡的 PC 用作训练机器学习模型的服务器，服务器上启动 Jupyter Notebook Server，VSCode 通过设置远程 Jupyter Notebook Server 地址连接远程服务。

1. Mac 环境下使用快捷键 `Cmd + Shift + p`，输入 `Specify local or remote Jupyter server for connections`。
2. 选择 Existing 后，输入远程服务器 URI。

![图2-6](http://cdn.defcoding.com/6F0AC31E-36F1-4DC2-9DD5-E480BD48561F.png)

连接远程服务的效果图：

![图2-6](http://cdn.defcoding.com/14DA5C29-FCBB-4053-9D82-84CBD40C0FBC.png)

请查看：[https://code.visualstudio.com/docs/python/jupyter-support](https://code.visualstudio.com/docs/python/jupyter-support) 官方文档解锁更多玩法。

### 题外话
这里无意挑起代码编辑器战争，其他的代码编辑器估计有类似的功能或者插件，也许只有想不到，没有做不到。
