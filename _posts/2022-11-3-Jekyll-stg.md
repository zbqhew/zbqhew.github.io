---
layout:       post
title:        "Jekyll 从入门到放弃"
author:       "JuPeiqi"
header-img:   "img/jekyll-stg/stgbg.jpg" #头部图片
header-mask:  0.2 #头部蒙上透明挡板，越小透明度越高，越大约暗
header-style: text
catalog:      true
tags:
    - 从入门到放弃
    - 计算机
---
### 引言

想自建个博客玩玩，这在非计算机专业的牛马当中应该是件相当酷 awesome 的事情了。

在网上看了好多攻略，感觉就在 github 上用 jekyll 建一个是最简单的事了。真的开搞后，觉得好难呀，以前玩过的唯一能跟博客搭点边的就是 QQ 空间了，但是在 github 上似乎比开通个 QQ 空间要难上许多许多。我觉得我有必要再把这流程再梳理一遍，做一个真·保姆级别的教程，来给同样零计算机基础的同学填填坑，也为了自己下次重新上手 Jekyll 时，同坑不踩二遍。

### 准备工作

首先的首先，要做一些准备工作，用 Jekyll 搭建一个博客，很多都是推荐在 Linux 系统上进行的，但我这门外汉只会用 WIndows 系统，又不是不能用🐶。在我第一次尝试时，遇到了诸多问题，导致我要么软件安装失败，要么各种包安装失败，要么服务器连接不上，有一部分原因是我的电脑被做过一些优化、很多服务要么被关要么被卸，注册表也被修改得一地鸡毛，所以在失败若干次后，我将自己的电脑初始化重新安装系统，系统是 **Windows11**。在新系统中，仅仅关闭了 **SysMain** 、 **Windows Search** 、 **Windows 推送通知系统服务** 三个服务，想把 **Windows Defender** 也关闭，但是关闭之后系统很多功能总是罢工，所以就一直留着了。系统准备好了，还需要准备梯子，因为 github 没梯子很不稳定，梯子就需要自备了，好像讲太多要被请去喝茶😒。 

初始化的 **Windows11** 、梯子准备完毕。

### 安装 Jekyll RubyGems

首先来安装 **Jekyll RubyGems** ，打开 [Jekyll RubyGems](https://jekyllrb.com/docs/installation/)  的下载页面 （https://jekyllrb.com/docs/installation/）

点击 [Windows](https://jekyllrb.com/docs/installation/windows/)
![](/img/in-post/jekyll-stg/install-1.jpg)

点击 [RubyInstaller Downloads](https://rubyinstaller.org/downloads/)
![](/img/in-post/jekyll-stg/install-2.jpg)

点击 [Ruby+Devkit 3.1.2-1 (x64)](https://github.com/oneclick/rubyinstaller2/releases/download/RubyInstaller-3.1.2-1/rubyinstaller-devkit-3.1.2-1-x64.exe)就开始下载啦
![](/img/in-post/jekyll-stg/install-3.jpg)

点击 **另存为**，存到自己想存的地方，然后打开 **rubyinstaller-devkit-3.1.2-1-x64.exe** ；或者直接**打开**也可以。
![](/img/in-post/jekyll-stg/install-4.jpg)

进入到安装 ruby 和 devkit 的安装环节，依次点击 **I accept the Licence**、**Next** 
![](/img/in-post/jekyll-stg/install-5.jpg)

路径用默认的不改， **Add Ruby executables to your PATH** 和 **Associate .rb and .rbw files with this Ruby installation** 保持✔，点 **Install** 
![](/img/in-post/jekyll-stg/install-6.jpg)

**Ruby Ri and HTML documentation** 和 **MSYS2 development toolchain 2002-04-19** 都打上✔，然后点 **Next**
![](/img/in-post/jekyll-stg/install-7.jpg)

然后就要经历一小会儿的安装读条时间
![](/img/in-post/jekyll-stg/install-8.jpg)

读条完毕， **Run 'ridk install' to set up MSYS2 and development toolchain** 保持打勾，点击 **Finish** 
![](/img/in-post/jekyll-stg/install-9.jpg)

安装完成啦，而且自动打开了 Ruby 的命令行窗口
![](/img/in-post/jekyll-stg/install-10.jpg)

在打开的的 **Ruby命令行**窗口里直接按 **Enter** ，等待片刻，出现下图Jekyll RubyGems就算是安装成功啦
![](/img/in-post/jekyll-stg/install-11.jpg)

### 折腾 Jelyll

下面就进入到 Jekyll 的折腾环节了，关闭之前命令行窗口，在开始菜单里找到 **Start Command Prompt with Ruby** 并打开
![](/img/in-post/jekyll-stg/jekyll-1.jpg)

输入 ```gem install bundler``` 按下 **Enter** ，等待片刻出现下图
![](/img/in-post/jekyll-stg/jekyll-2.jpg)

输入 ```bundle init``` 按下 **Enter** ，等待片刻出现下图
![](/img/in-post/jekyll-stg/jekyll-3.jpg)

输入 ```bundle install``` 按下 **Enter** ，等待片刻出现下图
![](/img/in-post/jekyll-stg/jekyll-4.jpg)

输入 ```gem install jekyll bundle``` 按下 **Enter** ，等待很久很久出现下图
![](/img/in-post/jekyll-stg/jekyll-5.jpg)

至此，跟 Jekyll 所有的工作就算完成啦。

### 快速生成 Jekyll 模板

下面我们就来使用下 Jekyll 自带的模板吧
输入 ```jekyll new blog``` 按下 **Enter** ，生成一个示例博客模板
![](/img/in-post/jekyll-stg/example-1.jpg)

输入 ```cd blog``` 按下 **Enter** ，进入新生成的 blog 目录
![](/img/in-post/jekyll-stg/example-2.jpg)

再次输入 ```bundle install``` ，按下 **Enter** ，等待许久后出现下图
![](/img/in-post/jekyll-stg/example-3.jpg)

输入 ```bundle exec jekyll serve``` ，按下 **Enter** ，生成本地服务器来预览自己的blog，当出现下图时，一个本地服务器版的Jekyll模板就算完成啦
![](/img/in-post/jekyll-stg/example-4.jpg)

下面我们打开浏览器，输入网址 http://127.0.0.1:4000/ 看看效果
![](/img/in-post/jekyll-stg/example-5.jpg)

一个非常简洁的本地版个人博客就算搭建完成了。

### 使用 github 上别人的模板

网上可以搜到很多漂亮的Jekyll模板网站， [Jekyll Themes](http://jekyllthemes.org/)收录的更多，可以慢慢挑。我也尝试了好些个，但是不同的Jekyll 模板经常让我遇到不同的、难以解决的问题，所以我就挑了一个比较成熟，几乎没有什么困难就跑起来的模板： [Hux Blog](https://huxpro.github.io)。

首先将他的博客模板下载下来，打开他的博客对应的仓库 https://github.com/Huxpro/huxpro.github.io ，依次点击 **Code**、**[Download ZIP](https://codeload.github.com/Huxpro/huxpro.github.io/zip/refs/heads/master)** 下载完整的博客模板
![](/img/in-post/jekyll-stg/hux-1.jpg)

打开下载下来的压缩文件  **huxpro.github.io-master.zip** ，将  **huxpro.github.io-master**  复制到想要的位置，这里我复制到 **C:\Users\WDAGUtilityAccount** ，和之前生成的 **blog** 模板在同一个文件夹中。打开 **C:\Users\WDAGUtilityAccount\huxpro.github.io-master** 文件夹，我们可以看到如下所示目录文件
![](/img/in-post/jekyll-stg/hux-2.jpg)

关闭之前Ruby命令行窗口，重新打开 **Start Command Prompt with Ruby** ，输入 ```cd huxpro.github.io-master``` ，按下 **Enter**
![](/img/in-post/jekyll-stg/hux-3.jpg)

输入 ```bundle install``` ，按下 **Enter** ，等待许久出现下图
![](/img/in-post/jekyll-stg/hux-4.jpg)

输入 ```bundle exec jekyll serve``` ，按下 **Enter** ，生成本地服务器来预览下载的Jekyll博客模板
![](/img/in-post/jekyll-stg/hux-5.jpg)

下面我们打开浏览器，输入网址 http://127.0.0.1:4000/ 就可以看到这个精美的博客啦
![](/img/in-post/jekyll-stg/hux-6.jpg)

下一步就是把别人模板上的信息替换成自己的，把它打造成自己的博客，用记事本或者自己习惯使用的文本编辑器打开  **C:\Users\WDAGUtilityAccount\huxpro.github.io-master**  文件夹下的配置文件 **_config.yml** ，将信息修改为自己的，比如将 ```title: Hux Blog``` 改为 ```title: 隔壁老王``` ，将 ```header-img: img/home-bg.jpg``` 修改为自己喜欢的图片。
![](/img/in-post/jekyll-stg/hux-7.jpg)

打开 **C:\Users\WDAGUtilityAccount\huxpro.github.io-master** 文件夹中 **_posts** 文件夹，可以删除其中所有文件，然后自己编写博文在此文件夹中保存为 **日期-XX.md** 格式。
![](/img/in-post/jekyll-stg/hux-8.jpg)

更改完毕后，返回 **Ruby命令行窗口** ，按下 **Ctrl+C** ，输入 ```y``` 按 **Enter** 关闭本地服务器，再输入 ```bundle exec jekyll serve``` ，按下 **Enter** 重新开启本地博客服务器
![](/img/in-post/jekyll-stg/hux-9.jpg)

打开 http://127.0.0.1:4000/ 网页并刷新，若右下角弹出 **REFRESH** 按钮，直接点击以下
![](/img/in-post/jekyll-stg/hux-10.jpg)

网页差不多变成自己想要的样子，还有诸多细节微调，自己慢慢尝试吧。
![](/img/in-post/jekyll-stg/hux-11.jpg)

点开刚写进去的博客，感觉还不错🐶
![](/img/in-post/jekyll-stg/hux-12.jpg)

进行下一步之前，先把  **Ruby命令行窗口** 关闭

### 部署到 Github

首先得有个 Github 账号，注册就不说了，直接登录 https://github.com/，然后得下载一个 [Github 桌面版](https://desktop.github.com/) ,浏览器中打开 (https://desktop.github.com/) ，点击 [Download for Windows(64bid)](https://desktop.githubusercontent.com/github-desktop/releases/3.1.2-7cd66717/GitHubDesktopSetup-x64.exe)
![](/img/in-post/jekyll-stg/github-3.jpg)

打开 **GitHubDesktopSetup-x64.exe** ,在安装界面点击 **Sign in to GitHub.com** 
![](/img/in-post/jekyll-stg/github-4.jpg)

在浏览器上弹出得窗口点击**打开**
![](/img/in-post/jekyll-stg/github-5.jpg)

在界面中点击 **Finish**
![](/img/in-post/jekyll-stg/github-6.jpg)

打开 路径 **C:\Users\WDAGUtilityAccount** ，修改 **huxpro.github.io-master** 文件夹名称为 **zbqhew.github.io** , **zbqhew** 为 github 自己账号的用户名。

返回 **GitHub Desktop** 界面，点击 **Add an Existing Repository from your hard drive...**
![](/img/in-post/jekyll-stg/github-7.jpg)

点击 **Choose...** 选择 **zbqhew.github.io** 文件夹，点击 **create a repository**
![](/img/in-post/jekyll-stg/github-8.jpg)

点击 **Create repository**
![](/img/in-post/jekyll-stg/github-9.jpg)

点击 **Publish repository**
![](/img/in-post/jekyll-stg/github-10.jpg)

**Keep this code private**取消打✔，点击 **Publish repository**
![](/img/in-post/jekyll-stg/github-11.jpg)

等待上传成功后，我们打开浏览器，打开 [Github官网](https://github.com/) ，选择刚上传的 **zbqhew/zbqhew.github.io** 仓库
![](/img/in-post/jekyll-stg/github-12.jpg)

点击 **Settings** ,再点击 **Pages** ，在下面得界面中，我们应该就可以看到 **https://zbqhew.github.io/** 网址，若没有出现这个网址，点击 **None** 按钮，选择 **main** ,然后点 **Save** ，等待5分钟后，刷新网页，就可以看到 **https://zbqhew.github.io/** 了
![](/img/in-post/jekyll-stg/github-13.jpg)

点击 **https://zbqhew.github.io/** 看看博客
![](/img/in-post/jekyll-stg/github-14.jpg)

这就成了。



Tips：
1. 要翻墙，不然有很多步骤可能就卡住了
2. 每次使用一个新的模板时，都要进入模板目录，运行一次```bundle install```
3. 有部分命令，官方文档中写的 ```bundler``` ，实际操作时，打错写成 ```bundle``` 也不影响
4. 网上有些模板比较老，在模板目录中运行 ```bunble install``` 会失败

### Jekyll 常用命令
- jekyll --version 查看版本号
- gem list jekyll 查看详细版本号
- gem outdated 查看有新版本的包
- gem update jekyll 更新Jekyll
- gem install jekyll-docs 安装离线Jekyll文档
