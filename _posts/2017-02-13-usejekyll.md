---
layout:     post
title:      "30分钟在Github上建立属于你的免费blog"
subtitle:   "没看错,就是30分钟"
date:       2016-12-06 12:00:00
author:     "YingJie"
header-img: "img/blog-2-wrongthink.jpg"
catalog:	true
tags:
    - 教程
---

### 基本准备

1. 去注册一个Github账号，点[这里](https://www.github.com)
2. 下载git并安装，点[这里](http://git-scm.com/)
3. 本地任一目录新建一个文件夹myblog(尽量不要用中文命名)

### 配置Git和Github

1. 桌面,鼠标右键，Git Bash Here，这样就进入了git
2. 输入 `ssh-keygen –t rsa –C "邮箱地址"`(这里的邮箱地址是Github邮箱地址,**双引号用半角符号**，你可以直接复制这段内容，然后在git窗口，右键Paste)
3. 连续按大概3-4次回车键，直到界面出现RSA 2048字符
4. 进入 "C:\Users\用户名\.ssh" 文件夹，用编辑器打开"id_rsa.pub"文件,全选,复制。(这里编辑器推荐[notepad++](https://notepad-plus-plus.org/)，或[visual studio code](https://code.visualstudio.com/))(如果你没有发现.ssh文件夹，请[点这](http://www.baidu-x.com/?q=%E9%9A%90%E8%97%8F%E6%96%87%E4%BB%B6%E5%A4%B9))
5. 进入Github,点击头像,点击"settings",点击"SSH and GPG keys"点击New SSH key,给sshkey起个名字填写在title框中,然后把"id_rsa.pub"文件中的内容复制到key框中,点击Add SSH key,应该会有一次密码验证,填写,确定,OK.
6. 配置用户名和邮箱:
`git config –global user.name "Github用户名"`

`git config –global user.email "Github邮箱"`
(再次强调，**双引号用半角符号**)
7. 可以把这个git窗口关闭了

### 创建仓库

![按如图操作](http://ww1.sinaimg.cn/large/88b1b9f5ly1fcoo8so23cj20nk0h6dhw)

### 同步代码

`1. 进入你的本地代码目录,右键"Git bash here"`

`2. git init (初始化本地文件夹为git仓库)`

`3. git remote add origin git@github.com:github用户名/github用户名.github.io.git`

`4. git pull git@github.com:github用户名/github用户名.github.io.git`

### copy jekyll 模板

这里用的是黄玄的博客模板，[博客地址](https://huangxuan.me),如果你觉得这个模板漂亮就继续。

还是刚才的git窗口，继续：
`git clone git@github.com:Huxpro/huxpro.github.io.git`
等待clone完成，会发现myblog文件夹内多出一个名为huxpro.github.io的文件夹，进入该文件夹，删除README.md和隐藏文件夹.git。然后把其余文件全选，剪切，粘贴到myblog文件夹，再删除huxpro.github.io文件夹

### 修改

修改myblog文件夹下的_config.yml文件，右键，notepad++打开,怎么修改请看[这里](https://github.com/Huxpro/huxpro.github.io/blob/master/README.zh.md)

修改完成后，在刚才的git终端继续：

` git add .`

` git commit -m "本次提交描述"`

` git push origin master`

完成后浏览器进入：github用户名.github.io网站，这就是你的博客了，当然现在大部分信息是别人的，你需要自己一步步修改。

### 写新文章

[这里](https://github.com/Huxpro/huxpro.github.io/blob/master/README.zh.md)已经描述的很清楚了，简单说一下，就是新建一个xxxx-xx-xx-文章标题.md的文件，头部是这样的格式：

![头部格式](http://ww1.sinaimg.cn/large/88b1b9f5ly1fcopv7l41vj20ix0703yw)

有需要注意的几点：
**1. 文件格式编码一定要是UTF-8无BOM格式**

**2. 头部信息要求特别严格，一定要按照作者说的那样写**

**3. 请自学markdown格式，大概5分钟时间**

这里有几个jekyll主题地址，你可以选择其它模板

[jekyll主题网站0](http://jekyllthemes.org/)

[jekyll主题网站1](https://jekyllthemes.io/)

[jekyll主题网站2](http://themes.jekyllrc.org/)

[jekyll主题网站3](http://yongyuan.name/blog/collect-jekyll-theme.html)