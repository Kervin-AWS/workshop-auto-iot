---
title: "7. 在 Alexa Developer 控制台中配置 Account Linking"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 80
---

1.	打开 [Alexa Console](https://developer.amazon.com/alexa/console/ask)

2.	在 **Skills** 列表中，选择之前创建的 Skill

3.	在左侧导航栏中，选择 **Account Linking**

4.	在 **Security Provider Information** 下，选择 **Auth Code Grant**

5.	在 **Authorization URI** 中输入 `https://alexa-workshop-dev-cn01.auth.us-east-1.amazoncognito.com/oauth2/authorize`

6.	在 **Access Token URI** 中输入 `https://alexa-workshop-dev-cn01.auth.us-east-1.amazoncognito.com/oauth2/token`

7.	在 **Client ID** 中输入`4od0k6ioo94e29naua62fhk0tt`

8.	在 **Client Secret** 中输入`mteph8cegr5v645tn4ua1ommobpcd26k9ner80c2fbudkguqgm8`
 ![Image](/images/png/019.png)

9.	点击 **Add scope** 并且输入 `openid`. 对于 Smart Home Skill, 至少需要选择一个 scope

10.	其余保持默认不变，在右上角点击 **Save** 按钮
 ![Image](/images/png/020.png)
 
{{% notice warning %}}
注意，为了简化实验，我们已经配置好了Cognito。请把Account Link最下方的三个链接给到我们，我们会在Cognito中进行设置，这样才能Link成功。
{{% /notice %}}
 ![Image](/images/png/021.png)

 请进入共享文档[https://shimo.im/sheets/KxxDpXx3XdD3DKkQ/MODOC](https://shimo.im/sheets/KxxDpXx3XdD3DKkQ/MODOC)，将您的三个URL输入其中，如下图所示，并通知现场工作人员

 ![Image](/images/png/404.png)
