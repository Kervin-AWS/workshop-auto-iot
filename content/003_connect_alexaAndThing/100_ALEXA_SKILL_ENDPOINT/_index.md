---
title: "9. 配置 ALEXA SKILL ENDPOINT"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 100
---
本小节，将刚才创建的 Lambda 函数与 Alexa Skill link在一起。

1.	拷贝 Lambda 方法的 **ARN**, 在 **Cloud 9** 中输入
    ```shell
    aws lambda list-functions
    ```
    将下图中的ARN拷贝下来
    
     ![Image](/images/png/203.png)

2.	打开 [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask), 选择创建的 Smart Home 技能

3.	在 **Default endpoint** 黏贴拷贝的 Lambda ARN
 ![Image](/images/png/026.png)
 
点击右上角的 **Save** 按钮