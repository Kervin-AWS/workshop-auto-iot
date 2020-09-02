---
title: "4. 连接 IoT Core"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 50
---
{{% notice info %}}
请确认当前网络环境是否屏蔽了 8883 端口。 如果被屏蔽，可以考虑使用一个 guest network 或者 个人热点。
{{% /notice %}}

1.	Git clone 如下代码仓库, 在 Cloud9 的 terminal 中输入

```shell
git clone https://github.com/Kervin-AWS/aws-alexa-workshop-smarthome-lamp-cn.git 

cd aws-alexa-workshop-smarthome-lamp-cn
```

2.	解压之前下载的 ZIP 文件. 您将获得如下文件:

    - 一个 private key, `\<thing-name\>.private.key`

    - 一个 device certificate, `\<thing-name\>.cert.pem`

3.	把 private key 重命名为 **private.key** 并且拖拽上传到 **credentials** 文件夹(选择替换).

4.	将 device certificate 重命名为 **cert.pem** 并且拖拽上传到 **credentials** 文件夹(选择替换).

5.	修改 `index.js` 中的配置并保存

    - `iotEndpoint`. 在 **IoT Core** 控制台左侧 **Settings** 菜单中可以找到
    ![Image](/images/png/016.png)

    
    - `thingName`. 之前创建的事物名称

    - `deviceBindingUrl`. 这个请不要修改它，本实验已经帮您配置好Amplify

6.	安装依赖. 在 Cloud9 的 terminal 中运行 
```shell
npm install
```

7.	运行 
```shell
node index.js 
```
启动应用程序。运行成功后， terminal 将会输出一个二维码。 在下一步中，我们将使用这个二维码完成用户和设备之间的绑定关系。
 ![Image](/images/png/017.png)