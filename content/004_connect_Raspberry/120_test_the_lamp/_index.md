---
title: "12. 测试 SMART HOME SKILL"
date: 2018-10-03T10:17:52-07:00
draft: false
weight: 110
---
至此，我们已经完成了所有Alexa Smart Home Skill的配置。现在，您可以通过语音来进行智能灯泡开关控制的测试了。 在本节中，我们还将有两个进阶挑战，可以使得您通过简单而明确的指令控制多个灯泡。

您可以通过Alexa APP， Alexa Developer Console 或者 Echo 来进行测试。

1.	打开 [Alexa Developer Console](https://developer.amazon.com/alexa/console/ask), 选择您创建的技能

2.	点击 **Test** tab, 尝试输入 `turn on the <device-friendly-name> ` 
  ![Image](/images/png/030.png)

3.	检查树莓派的灯泡状态变化
<video src="/images/png/test_pi.mp4" width="800px" height="600px" controls="controls"></video>

4. 如果您没有树莓派，您可以在IOT 控制台通过设备的影子查看虚拟设备的状态切换
  ![Image](/images/png/400.png)

