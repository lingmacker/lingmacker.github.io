---
title: "Pve Nas添加额外硬盘"
date: 2023-04-01T16:53:24+08:00
draft: true
---

### pve 安装 nas 后添加额外硬盘
1. 通过 ssh 连接到 pve虚拟机，运行 `ls -l /dev/disk/by-id/` 查看所有硬盘

2. 找到要添加的硬盘 id，运行 `qm set 101 -sata2 /dev/disk/by-id/disk-id` 

   > 其中 101 需要改成 pve 中 nas 的虚拟机编号，-sata2 后面的数字改成 nas 添加的第几块磁盘，后面的 disk-id 就是第一步查到的硬盘 id