---
title: " VMware获取该虚拟机的所有权失败\t\t"
tags:
  - vmware
url: 1128.html
id: 1128
categories:
  - 其他
date: 2018-04-16 10:59:10
---

介绍
--

没有关虚拟机，直接关闭的主机，导致出现“VMware获取该虚拟机的所有权失败”错误，提示配置文件XXX\\XXX\\XXX.vmx

解决
--

虚拟磁盘(.vmdk)本身有一个磁盘保护机制，为了防止多台虚拟机同时访问同一个虚拟磁盘(.vmdk)带来的数据丢失和性能削减方面的隐患，每次启动虚拟机的时候虚拟机会使用扩展名为**.lck****（磁盘锁）文件对虚拟磁盘****(.vmdk)****进行锁定保护**。当虚拟机关闭时.lck（磁盘锁）文件自动删除。 直接将“虚拟机名.vmx.lck”文件夹删除即可