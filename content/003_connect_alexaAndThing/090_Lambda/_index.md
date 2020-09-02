---
title: "8. 创建并部署 ALEXA 后端 LAMBDA"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 90
---

{{% notice info %}}
由于考虑到信息安全问题，具有admin权限的账号需要您手动输入两次账户密钥，感谢您的耐心与理解
{{% /notice %}}

1.	首先，进入您的 Cloud9 环境根目录, 打开一个`terminal`配置aws configure，赋予该环境您global账户的访问权限，为后面的global lambda远程部署做准备（此处使用Global账号）

    此步骤需要您通过输入
    ```shell
    aws configure
    ```
    来配置AKSK、Region等信息

    AWS Access Key ID: `现场提供的Global AK`

    AWS Secret Access Key ID: `现场提供的Global SK`

    region: `us-east-1`
    

    ![Image](/images/png/202.png)

2.	在 terminal 中输入 

```shell
git clone https://github.com/Kervin-AWS/aws-alexa-workshop-smarthome-cn.git 

cd aws-alexa-workshop-smarthome-cn 
```

3.	编辑 `config.json` 文件, 
    
    您需要修改 `alexaSmartHomeAppId` 为您的Alexa Skills Id，
    
    您需要修改 `iotEndpoint` 为您的中国区的IOT endpoint，

    其余参数保持默认不变。

4.	编辑index.js 中的AWS.IotData 初始化代码，**输入现场提供的中国区账号AKSK**，从而可以实现对国内IOT设备的控制。注意本实验仅为实现功能，生产环境将会采用非明文的认证方式。

    AWS Access Key ID: `现场提供的China AK`

    AWS Secret Access Key ID: `现场提供的China SK`

    region: `cn-northwest-1`

    ![Image](/images/png/022.png)
 
5.	为了简化实验，请您编辑index.js 中的 AWS.DynamoDB.DocumentClient 初始化代码，请复制下方的**DynamoDB只读AKSK**到`index.js`中的28行，注意本实验仅为实现功能，生产环境将会采用非明文的认证方式。
    
    AWS Access Key ID: `现场提供的DynamoDB AK`

    AWS Secret Access Key ID: `现场提供的DynamoDB SK`

    ![Image](/images/png/023.png)
 
6.	修改serverless.yml 里面的function名称，注意每一个IOT要用不同的名称
     ![Image](/images/png/025.png)
 
7.	运行 `npm install` 来安装依赖， 包括开发环境的依赖

8.	运行 `npm config set registry https://registry.npm.taobao.org` 换源

9.	运行 `npm install -g serverless` 来安装serverless。

10.	运行 `sls deploy`

 ![Image](/images/png/201.png)

部署成功后，您可以通过命令行查看部署好的一个类似于 `alexa-smarthome-{stage}-backend` 的 Lambda 方法，并且查看到RAN

```shell
aws lambda list-functions
```
 ![Image](/images/png/203.png)

