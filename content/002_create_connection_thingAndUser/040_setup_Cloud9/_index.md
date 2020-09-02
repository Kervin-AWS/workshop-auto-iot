---
title: "3. 启动Cloud9"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 40
---
{{% notice info %}}
本实验使用使用 Cloud9 开发环境，下面将引导你运用EC2创建Cloud9环境
{{% /notice %}}

1.	[<span style="color: red;">**启动EC2**</span> ](https://cn-northwest-1.console.amazonaws.cn/ec2/v2/home?region=cn-northwest-1#Home:)，新建实例：
 ![Image](/images/png/010.png)

2.	点击Marketplace，搜索`Cloud9`，点击选择
 ![Image](/images/png/011.png)

3.	选择实例类型，此处选择t3a.small:
 ![Image](/images/png/012.png)

4.	新建并下载密钥对，此处按照要求命名
 ![Image](/images/png/013.png)

然后点击启动实例，成功后，查看实例公有IP，

在浏览器中输入 `公有IP:8181` <span style="color: red;">**（请关闭所有代理）**</span>

输入用户名： `aws`，

密码： `实例ID`（如下图所示），进入Cloud9界面.

![Image](/images/png/014.png) 

![Image](/images/png/015.png)

