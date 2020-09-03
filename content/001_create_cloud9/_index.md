---
title: "创建 Cloud9 Lab环境"
weight: 11
chapter: false
draft: false
---

{{% notice info %}}
我们运用创建一个EC2 的Cloud9 实例来统一编程环境，简化实验的流程。
{{% /notice %}}

1. [登录EC2控制台](https://898111891143.signin.amazonaws.cn/console), 输入现场工作人员提供的用户名与密码
    
    本实验的用户名为：`demouser-xx`, 
    
    密码为现场工作人员提供的密码

    ![Image](/images/png/1.png)

    [<span style="color: red;">**启动EC2**</span> ](https://cn-northwest-1.console.amazonaws.cn/ec2/v2/home?region=cn-northwest-1#Home:)，新建实例：
    ![Image](/images/png/2.png)

2.	点击Marketplace，搜索`Cloud9`，点击选择
 ![Image](/images/png/3.png)

3.	选择实例类型，此处选择t3a.small:
 ![Image](/images/png/4.png)

4.  选择下一步，配置实例详细信息，然后连续点击三次下一步。来到步骤6: 配置安全组，修改安全组的名称为 `demo-(现场树莓派纸盒上的数字)` 或者可以和现场其他用户区别开的唯一编码，这一步将让您可以在后续找到您启动的EC2。
 ![Image](/images/png/5.png)

5.	点击审核和启动，在弹出的密钥对选择界面，选择在没有密钥对的情况下继续，然后勾选我确认，然后启动实例。
    ![Image](/images/png/6.png)

6. 然后点击启动实例，成功后，由于是共用账号，所以有较多实例，请在上方搜索栏根据安全组名称找到您启动的实例(请不要和现场的其他用户弄混)
    ![Image](/images/png/7.png)

7. 选中您创建的实例，我们为其赋予实验相关的IAM权限

    点击上方的操作，然后选择实例设置，Attach/Replace IAM Role

    ![Image](/images/png/8.png)

    选择ec2-s3-iot-access，并点击Apply

    ![Image](/images/png/9.png)

8. 登录基于EC2搭建的Cloud9 编程环境

    在浏览器中输入 `公有IP:8181` <span style="color: red;">**（请关闭所有代理）**</span>

    输入用户名： `aws`，

    密码： `实例ID`（如下图所示），进入Cloud9界面.

    ![Image](/images/png/10.png) 

    ![Image](/images/png/11.png)

9. 从github 下载代码
    在terminal中输入： 
    ```shell
    git clone https://github.com/Kervin-AWS/auto-iot-lab.git
    ```
    ![Image](/images/png/12.png)
