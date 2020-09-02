---
title: "11. 将灯泡连接到树莓派的引脚上"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 110
---
按下图将灯泡通过母母的杜邦线连接到树莓派上：
 ![Image](/images/png/027.png)
 
灯泡的R极 -> 树莓派18引脚

灯泡的负极-> 树莓派GND引脚

## 将代码拉取到树莓派中

1.	通过ssh进入树莓派

用户名： pi 

密码： `awsworkshop`

```shell
ssh pi@192.xxx.xxx.xx
```


2.	首先拉取github树莓派端的代码

```shell
git clone https://github.com/Kervin-AWS/aws-alexa-workshop-raspi-cn.git
```

3.	在本地terminal内进入“创建智能灯泡模拟器”步骤中下载的证书文件夹，将生成的cert.pem 、 private.key 通过scp的方式传入树莓派的aws-alexa-workshop-raspi-cn文件夹中

    ```shell
    scp ./cert.pem pi@xxx.xxx.xxx.xxx:/home/pi/aws-alexa-workshop-raspi-cn

    scp ./private.key pi@xxx.xxx.xxx.xxx:/home/pi/aws-alexa-workshop-raspi-cn
    ```
    ![Image](/images/png/401.png)


4.	在树莓派内通过 vim 或者 nano 修改ledSwitch.py 中的awsiotHost为自己设置的IOT Endpoint
    ![Image](/images/png/402.png)
 
5.	修改ledSwitch.py 中的thingName为自己设置的item name
    ![Image](/images/png/403.png)

6.	修改完成后保存退出
 
7.	在树莓派命令行中输入python ledSwitch.py，启动IOT脚本

    ```shell
    python ledSwitch.py
    ```
