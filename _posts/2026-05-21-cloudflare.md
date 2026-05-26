---
layout: post
title: 腾讯云域名+cloudflare解析
date: 2026-05-21
featured: learn
featured_name: 学习记录
---

本篇文章讲述了用腾讯云购买域名，并使用cloudflare进行DNS解析。让国内访问博客页面变快。

# 腾讯云注册域名

腾讯云注册账号，实名后注册域名，很简单。价格大概一年50左右。

# 记录github项目地址

进入github仓库的如下页面，查看当前仓库网址首页。

本地使用ping xxxx.io，查看该域名对应的网址ip，记录下来

![gitiowangzi](/assets/images/2026-05-21-cloudflare/gitiowangzi.png)

把注册的域名填入custom domain，并开启强制https访问

![tengxunyun3](/assets/images/2026-05-21-cloudflare/tengxunyun3.png)

# cloudflare注册配置

[cloudflare主页](https://dash.cloudflare.com/login)

Cloudflrare页面注册账号，如果首次注册会让直接填写域名开始，然后选择一个方案。使用快速扫描dns记录，稍等cloudlare会把你的腾讯云的免费解析地址查出来。

![cloudflare1](/assets/images/2026-05-21-cloudflare/cloudflare1.png)

删除检测出来的全部地址。然后把第二步找到的ip填入内容部分，名称一个是域名，另一个是www，然后保存，如图。

![cloudflare2](/assets/images/2026-05-21-cloudflare/cloudflare2.png)

查看cloudflare中的ns地址

![cloudflare3](/assets/images/2026-05-21-cloudflare/cloudflare3.png)

# 腾讯云修改第三番解析

把第三部最后查到的ns填入腾讯云的第三方解析

![tengxunuyun](/assets/images/2026-05-21-cloudflare/tengxunuyun.png)

# 完成

稍等20分钟左右会收到cloudflare的邮件，告诉你已经代理好了，然后去网站看会有活动的标识。说明cloudflare已经负责解析你的域名了。

![tengxunyun2](/assets/images/2026-05-21-cloudflare/tengxunyun2.png)

回到github的setting，pages上能看到域名下有dns in process。

此时在国内尝试访问你的主页，速度应该会变快了。

查看访问网页的ip，ip归属是cloudflare，说明ip已经被隐藏了。

![ip](/assets/images/2026-05-21-cloudflare/ip.png)

![ipcl](/assets/images/2026-05-21-cloudflare/ipcl.png)





