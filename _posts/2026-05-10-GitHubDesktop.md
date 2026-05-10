---
layout: post
title: githubdesktop使用
date: 2026-05-10
featured: learn
---


## 什么是GitHub Desktop?

GitHub Desktop是一个有可视化页面用于推送合并代码到仓库的软件，对于不会用git的人友好。它使用github账号登入，通过账号对自己仓库操作无需密钥。

[GitHub Desktop下载](https://desktop.github.com/download/)

## 克隆仓库

首先登入自己的账号

![login](/assets/images/2026-05-10-GitHubDesktop/login.png)

登入自己账号后能直接看到自己的仓库，选好文件夹点击克隆即可。

![cangku](/assets/images/2026-05-10-GitHubDesktop/cangku.png)

克隆成功后就在本地能看到自己的文件

## 提交修改

在本地以任何方式修改仓库文件后，github desktop就能检测到修改，把修改的文件自动add到这里，比如这次我修改了三个文件，包括增加了一个图片。

![change](/assets/images/2026-05-10-GitHubDesktop/change.png)

在下面的“Summary（required）”输入此次合入的描述（必填）。然后点击commit，就能确认此次修改。

接下来是把修改推送到仓库，点击右上角的“fetch origin”，即可把代码push到仓库。
