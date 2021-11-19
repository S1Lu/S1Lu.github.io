---
title: Linux 操作系统
top: true
img: https://s1lu.github.io/img/Linux%E6%93%8D%E4%BD%9C%E7%B3%BB%E7%BB%9F.jpeg
tags: Linux 操作系统
---


# Linux 操作系统

## Linux概述（8月31日/2021）

### 1）Linux操作系统的简介

```bash
linux是一套免费的、开放源代码的，并可以自由传播的类Unix操作系统软件。
```

### 2）Linux操作系统的特点

```bash
①多用户、多任务
②良好的兼容性
③强大的可移植性
④高度的稳定性
⑤良好的用户界面：
⑥提供了丰富的网络功能
⑦支持多种文件系统
①开放性
①设备独立性
```

### 3）Linux操作系统的主要应用领域

```bash
①桌面
②服务器
③嵌入式系统
④集群计算机
```

### 4）Linux系统结构

#### ①内核

```bash
整个操作的系统的核心，管理整个计算机系统的软硬件资源
内核采用模块化的结构主要包含CPU进程管理、内存管理、文件管理、磁盘管理等
```



#### ②Shell

```bash
不仅是一种交互式命令解释程序，而且还是一种程序设计语言。常见的有B Shell、C Shell、K Shell和Bash。
```



#### ③X Window

```bash
是UNIX和Linux等的图形化用户界面标准。
```



#### ④应用程序

```bash
种类繁多、数量丰富。
```

## 利用VMWare Workstation搭建虚拟机（9月1日/2021）

### 利用VMWare Workstation搭建虚拟机
#### ①虚拟机

```bash
虚拟机是指通过软件模拟的，具有完整硬件系统功能的，运行在一个完全隔离环境中的完整计算机系统。
```


#### ②虚拟机的作用

```ba
一方面可以方便的搭建各种网络环境，为实验奠定基础;另一方面可以保护真机，尤其是在做一些诸如硬盘分区、安装操作系统时，对真机没有任何影响。
```

③虚拟机的安装注意事项

```ba
虚拟机内存大小至少为1GB内存
网络类型选择桥接模式
磁盘容量至少20GB
```

#### ④Linux磁盘分区与目录结构简介

```bash
MBR：全称Master boot record，及硬盘的主引导记录。由三个部分组成，主引导程序（4446B）、硬盘分区表DPT（Disk Partition Table）（64B）、硬盘有效标志（2B）。
硬盘分区类型：硬盘分区包括主分区，扩展分区，逻辑分区三种类型。
主分区的数目最都有4个，在linux系统中，第一个逻辑分区编号始终为5
```

#### ⑤不同类型的磁盘和分区的设备文件命名有统一的规则。
```bash
IDE接口的硬盘设备表示为"hdX"形式的文件名。SATA或SCSI接口的硬盘设备表示为"sdX"形式文件名。其中“X”可以为a，b,c,d等字母序号。
硬盘分区：安装linux是必须至少有两个分区：交换分区，（又称swap分区，1GB）和根分区（又称/分区,4GB）。

一个较合理的分区方案
（1）/boot分区：系统引导，200MB，ext4文件系统
（2）swap分区：交换分区，1GB，swap文件系统
（3）/home分区：保存用户信息，512MB，ext4文件系统
（4）/分区：保存其他所有数据；4GB，ext4文件系统。
```

### VMware安装 Centos7

[VMware安装 Centos7]([https://s1lu.github.io/post/VMware%E5%AE%89%E8%A3%85%20Centos7/2021/](https://s1lu.github.io/post/VMware安装 Centos7/2021/))




#### 关机和重启命令
```bash
1.关机：init 0   
2.	shutdown -h now或shutdown -h 20:30
3.	Poweroff
4.	Halt
重启：1.init 6
2.	Reboot
3.	Shutdown -r now
注销命令：
1.	Exit
2.	[ctrl+D]组合键
在虚拟控制台和图形用户界面之间的转换
通过Ctrl-Alt-F[1-6](有Fn键加上Fn键）组合键在虚拟控制台之间切换
通过Ctrl-Alt-F7组合键访问图形控制台
root用户：特殊的管理账户，又称为超级用户，root几乎可以完全控制系统，而且几乎可以无限制地损坏系统。
```