## 西电线下A测2025年最新版（语音识别控制机械臂）
原创代码，已通过验收，附带完整教程和注意事项

官方教程：

1.***A级达标测试线下测试资料***: https://pan.baidu.com/s/1piDHYK3ogQ3HfwB3Ntq3Sw?pwd=ptbi 提取码: ptbi

2.***开源6路舵机控制器资料***（机械臂完整学习资料）： https://pan.baidu.com/s/1ySgArxOVMTYCaYL4E4oDvw   提取码：f8kf

![A测领取清单和注意事项](https://github.com/user-attachments/assets/bb9fca35-01ba-49cb-9c49-5d83e1e4185b)
![A测现场验收流程](https://github.com/user-attachments/assets/5c68876b-7730-431a-a8c7-2afefe339925)
**注意**:  
1.带电情况下，不能断开或连接杜邦线  
2.验收时，需要先重新编译机械臂的stm32源代码并烧录，这会擦除FLASH（机械臂自带的stm32在烧录时，需要先将烧录跳线帽拔下来，然后再烧录）  

3.上位机软件只能在调试时使用，正式测试时不能使用。此外，虽然上位机软件可以便捷地编辑动作组并保存到机械臂的stm32的FLASH中，但是正式验收时的重新烧录会擦除FLASH导致之前保存的动作组失效。  
4.每次重新给机械臂和Arduino上电后，需要将两者依次复位  

一、机械臂烧录教程

1.Micro-USB连接电脑和机械臂上的stm32

2.用keil打开stm32的源代码  
（keil安装教程："开源6路舵机控制器\2.软件工具\Keil安装包及mcuisp下载工具\Keil软件激活教程.pdf"）  
（stm32源代码："A级达标测试线下测试资料\LeArm\5.案例代码学习\stm32单片机\源码\STM32  2.2\STM32  2.2\STM32\OpenArmSTM32.uvprojx"）
<img width="1106" height="627" alt="image" src="https://github.com/user-attachments/assets/4820d5a4-4664-443f-a7e8-a9b97ef41722" />

**注**：stm32源代码以.uvproj或.uvprojx结尾

3.编译代码生成可烧录的hex文件
<img width="1331" height="652" alt="编译生成HEX" src="https://github.com/user-attachments/assets/9fad6070-e96a-4ab4-9f46-87d3cc8b37ae" />

