---
title: "1. 创建智能灯泡模拟器"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 20
---

在本节中，我们会创建Iot事物、证书以及安全策略。

{{% notice warning %}}
注意：请选择宁夏Region
{{% /notice%}}

1. 登陆 AWS IoT Core 控制台，显示如下。

    ![Image](/images/png/002.png)

2. 在左侧导航栏中，选择 **Onboard** 菜单

3. 在 **Configuring a device** 中, 点击 **Getting Started** 按钮

4. 在 **How are you connecting to AWS IoT?** 页面, 选择 **Linux** 作为运行平台; 选择 **Node.js** for IoT Device SDK， 然后点击 **Next**

    ![Image](/images/png/003.png)

5. 在 **Name** 字段中输入 `ratchet`, 点击 **Next step**
    {{% notice warning %}}
    如果您与别人共享这个 AWS 账号，请输入一些前缀来区别您和别人创建的事物, e.g. cw_ratchet。
    {{% /notice%}}
    ![Image](/images/png/004.png)

6. 在 **Download connection kit** 页面中，点击 **Linux/OSX** 按钮来下载我们所需的文件。当下载完成后，点击 **Next** 按钮。
    ![Image](/images/png/005.png)

总结一下, 我们在之前的步骤中，创建了如下内容：
- 一个 安全策略 来控制事物访问 IoT Core
- 一个 Linux/OSX zip 文件，包含连接 IoT Core 所需的证书

![Image](/images/png/006.png)

{{% notice warning %}}
请不要丢失这个 ZIP 文件，它包含 private key（私有安全密钥）, 一旦遗失，无法再次获取。
{{% /notice%}}


在这个实验中，您将会创建如何资源:

- 一个虚拟的 Alexa-Enabled 智能家居灯泡
- 一个用于建立用户和设备绑定关系的系统，该服务基于 AppSync, Cognito User Pool, Lambda, DynamoDB 构建
- 一个 Alexa 的后端服务，该服务处理来自 Alexa 的指令，同时通过 IoT Core 操作灯泡的开关状态
