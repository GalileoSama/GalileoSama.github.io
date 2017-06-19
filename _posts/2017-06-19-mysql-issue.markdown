---
layout:     post
title:      "MySQL 问题 —— MySQL issue"
subtitle:   "Mac OX 升级造成的 MySQL 服务无法启动的问题"
date:       2017-06-19 15:00:00
author:     "Galileo"
header-img: "img/post-bg-nextgen-web-pwa.jpg"
header-mask: 0.3
catalog:    true
tags:
    - MySQL
    - Mac
---



> 忙活了一早上。

## MySQL 服务无法启动了

Mac OX的升级可能导致的MySQL无法启动，在ＭySQL操作面板上会提示："Warning:The /usr/local/MySQL/data directory is not owned by the ‘mysql‘ or '-mysql'"
这应该是某种情况下导致/usr/local/mysql/data的宿主发生了改变

![](/img/in-post/post-mysql-issue/mysql-before.png)
*宿主变化了 [图片来源: Galileo]*

解决方法：

```
sudo chown -R  _mysql:wheel  /usr/local/mysql/data
```

![](/img/in-post/post-mysql-issue/mysql-after.png)
*宿主变化了 [图片来源: Galileo]*


## 问题补充

之后遇到的问题可能都会记录到这里。


**慢慢积累，慢慢提高**



---


