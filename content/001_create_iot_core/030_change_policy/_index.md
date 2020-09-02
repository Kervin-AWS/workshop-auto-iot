---
title: "2. 修改默认的安全策略"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 30
---

默认的安全策略会限制这个设备能发布的消息 topic。在这个实验中，我们将会创建一个更加开放的安全策略，以便我们能够通过APP进行连接。因此，需要先找到 之前创建的策略。

1.	在 AWS IoT Core 控制台点击 **Manage**，它会默认选中 **Things**
 
2.	找到之前步骤中创建的事物, 例如本实验中叫做 **ratchet**

3.	选择这个事物

4.	在左侧菜单栏，点击 **Security**

5.	点击已经附加的策略，如下
    ![Image](/images/png/007.png)
6.	点击 **Policies**
    ![Image](/images/png/008.png)
7.	选择 Policy, 这个实验中，应该叫 ratchet-Policy

8.	点击 **Edit Policy Document**

9.	Enter the following for your document

```shell
{
  "Version": "2012-10-17",
  "Statement": [
    {
      "Effect": "Allow",
      "Action": [
        "iot:Publish",
        "iot:Subscribe",
        "iot:Connect",
        "iot:Receive"
      ],
      "Resource": [
        "*"
      ]
    }
  ]
}
```
10.	点击 **Save as new version**
    ![Image](/images/png/009.png)

现在，你的设备可以发布和订阅任何消息。至今，我们已经完成了三个 IoT 组件的创建:
- 设备证书
- 一个安全策略
- 安全策略与设备证书与事物的关联
