---
layout: post
title: githubdesktop使用
date: 2026-05-10
featured: learn
featured_name: 学习记录
---


## 什么是GitHub Desktop?

GitHub Desktop是一个有可视化页面用于推送合并代码到仓库的软件，对于不会用git的人友好。它使用github账号登入，通过账号对自己仓库操作无需密钥。

[GitHub Desktop下载](https://desktop.github.com/download/)

# github创建仓库

登入github，从左侧选择All repositories,然后选择new repositories。
如图，仓库名称自定义，可见必须选public，因为博客是公开的，所以内容需要公开，外部才能直接访问。其余默认即可。
![cangku](/assets/images/2026-05-20-vscode1/cangku.png)

打开仓库，尝试手动随便上传个文件到仓库

![shangchuantupian](/assets/images/2026-05-20-vscode1/shangchuantupian.png)

## 克隆仓库

打开GitHub Desktop软件，登入自己的账号

![login](/assets/images/2026-05-10-GitHubDesktop/login.png)

登入自己账号后能直接看到自己的仓库，选好文件夹点击克隆即可。

![cangku](/assets/images/2026-05-10-GitHubDesktop/cangku.png)

克隆成功后本地能看到仓库内的文件了

## 提交修改

在本地以任何方式修改仓库文件后，github desktop就能检测到修改，把修改的文件自动add到这里，比如这次我修改了三个文件，包括增加了一个图片。

![change](/assets/images/2026-05-10-GitHubDesktop/change.png)

在下面的“Summary（required）”输入此次合入的描述（必填）。然后点击commit，就能确认此次修改。

接下来是把修改推送到仓库，点击右上角的“fetch origin”，即可把代码push到仓库。
