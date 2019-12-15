---
title: Windows系统下申请苹果证书
categories:
- app开发
tags:
- 命令
---



苹果描述文件分为开发版和发布版两种类型，开发版和需要我们添加用户设备才能在真机上进行调试。

### 具体步骤

1. 创建bundle ID

点击Certificates, Identifiers & Profiles，如下图所示：

![Certificates, Identifiers & Profiles](Windows系统下创建苹果描述文件/16.png)

先来创建Bundle ID（bundle ID可以翻译成包ID,也可以叫APP ID 或应用ID,它是每一个ios应用的`全球唯一标识），点击左侧菜单的Identifiers再点击加号添加按钮进行添加，如下

![Bundle ID](Windows系统下创建苹果描述文件/14.png)

选中第一个App IDs，再填写描述及bundle ID（按自己的需求来命名，尽量用英文），如下

![App IDs](Windows系统下创建苹果描述文件/15.png)

![名称](Windows系统下创建苹果描述文件/17.png)

2. 添加设备（发布版跳过步骤2）

   点击“Devices”进入注册设备界面。点击右上角“+”新建注册设备信息，如下

   ![设备](Windows系统下创建苹果描述文件/19.png)

   ![设备信息](Windows系统下创建苹果描述文件/13.png)

   可以通过苹果手机助手获取UDID

   如爱思助手，电脑下载爱思助手，连上苹果手机，设备信息里面那个设备标识就是udid。

   ![手机助手](Windows系统下创建苹果描述文件/18.png)

   3. 点击“Profiles”进入描述文件界面。点击右上角“+”新建描述文件，勾选描述文件类型，如下

      ![描述文件](Windows系统下创建苹果描述文件/20.png)

      ![描述文件类型](Windows系统下创建苹果描述文件/12.png)

      ![勾选证书](Windows系统下创建苹果描述文件/21.png)

      ![勾选设备](Windows系统下创建苹果描述文件/22.png)

      ![描述文件名称](Windows系统下创建苹果描述文件/23.png)

      ![下载描述文件](Windows系统下创建苹果描述文件/24.png)



