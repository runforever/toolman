# 从提高 Python 第三方模块安装速度说起...

*作者：奔跑的青椒*<br />
*出处：知识星球【涛哥聊 Python】*<br />
*原文链接：【编程五分钟】系列文章 https://www.defcoding.com/tool#/fast_network*

> 成熟的编程语言通常通过包管理器从远端安装第三方模块，Linux 各大发行版通过各自的包管理器从远端安装软件，Docker 从远端拉去镜像，Git 从远端（GitHub）拉去代码，这些工具背后的远端有个共同特点：他们都在国外。

### 安装失败
经常有小盆友使用 Python 安装第三方模块提示网络问题安装失败，如下图：

![](http://cdn.defcoding.com/1587458883.PNG)

*图片来源：知识星球【涛哥聊 Python】小朋友日常遇到的问题*

由于**某种神秘的原因**导致国内连接国外远端经常掉线，每当你看到安装错误提示信息显示 `time out` 之类的错误基本可以确定是**神秘原因**的问题，至于**神秘原因**是什么不在本文的讨论范围，况且，我也不知道，我也不敢问。

### 如何应对
既然连接国外远端经常掉线，把远端换成国内的基本就可以解决大部分问题了，这里推荐大家使用 [阿里云官方镜像站](https://developer.aliyun.com/mirror/)，毕竟是阿里云，不用担心稳定性问题。

#### 更换 Python PyPI 镜像
来源：[阿里云更换 PyPI 镜像为阿里云镜像的方法](https://developer.aliyun.com/mirror/pypi)<br>
环境：*nix <br>
1. 编辑下列文件

```
~/.pip/pip.conf
```

2. 在上述文件中添加或修改:

```
[global]
index-url = https://mirrors.aliyun.com/pypi/simple/

[install]
trusted-host=mirrors.aliyun.com
```

其他编程语言和软件包管理器的修改方法可以查看 [阿里云官方镜像站](https://developer.aliyun.com/mirror/) 里相应的教程。

### 完美解决问题了吗？
前面说了，这种办法可以解决大部分问题，而我最近在搭建深度学习环境的时候遇到过国内镜像源提示包找不到，使用国外源就可以安装成功的情况，但这是少数，如果你不幸遇到这样的情况，首先，你得想办法能让自己的网络访问 Google，然后在 Terminal 下设置一下代理就可以愉快的使用国外源了，我的开发环境是 Mac，在 iTerm 下用这条命令解决问题。

```
export http_proxy=http://127.0.0.1:1087;export https_proxy=http://127.0.0.1:1087;
```

### 能访问 Google 之后
1. 新技术一般都是起源于国外，畅通无阻的使用 Google 能帮助你更快更好的找到问题的答案。
2. Youtube 上有很多技术教程，如果国内的视频教程无法解答你的问题，去 Youtube 上试试也许有不错的效果。
3. Stackoverflow 基本有你遇到的大多数编程问题，高效使用 Stackoverflow 能提升不少工作效率。
4. 国外很多静态资源存储是使用 AWS 的 S3，一定有同学遇到过 curl Github 上的几 Kb 脚本失败的情况，然后影响工作进展。

要说明的是：我并不关心国外网站上莫名奇妙黑中国的资讯和言论，我只关心合理使用工具解决我工作和学习的问题，作为程序员我相信科学和理性，做到独立思考，能用批判性思维看问题，最后，问我怎么能让自己的网络访问 Google，我只能这样回答你：

![](http://cdn.defcoding.com/下载.jpeg)
