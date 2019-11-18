# Z6-KP7S1

Update 2019.4.4

## 1、电脑配置

| 规格     | 详细信息                                                     |
| -------- | ------------------------------------------------------------ |
| 操作系统 |                                                              |
| 处理器   | Intel® Core™ i7-7700HQ CPU @2.80GHz Kaby Lake                |
| 主板     | Intel 100 Series/C230 Series                                 |
| 内存     | 1、芝士DDR4-2400 8G；2、光威DDR4-2133 16G                    |
| 硬盘     |                                                              |
| 显卡     | 1、集成显卡：英特尔 HD 630；2、独立显卡：影驰Nvidia Geforce GTX 1050 2G |
| 显示器   | 奇美 CMN15CB 1920x1080                                       |
| 声卡     | 1、Realtek ALC269；2、Intel Kaby Lake HDMI                   |
| 网卡     | 1、有线：Realtek RTL8168/8111；2、无线：Broadcom BCM4352     |
| 蓝牙     | DW1560 蓝牙4.0                                               |
| 读卡器   | Realtek RTS5287                                              |

## 2、完善驱动

### 驱动版本

| 名称          | 版本  | 名称         | 版本  |
| ------------- | ----- | ------------ | ----- |
| FakeSMC       | 1758  | Lilu         | 1.3.5 |
| WhateverGreen | 1.2.7 | AppleALC     | 1.3.6 |
| RTL8111       | 2.2.2 | USBinjectAll | 0.7.1 |
|               |       |              |       |







### 0）Lilu





### 1）显卡

WhateverGreen

版本1.2.7

型号：

###  2）声卡

AppleALC

版本1.3.6

### 3）网卡

有线：型号：Realtek RTL8168/8111，直接使用

无线：型号：Dell Wireless 1510，免驱动

### 4）蓝牙

型号：CSR8510 A10，免驱动

### 5）电池



### 6）触摸板



### 7）显示器



### 8） USB



## 问题解决

### 关于睡眠

在EFI\Clover\kexts下放入HibernationFixup.kext，重启即可。

### 关于 HiDPI

使用"一键开启macOS HiDPI"脚本即可打开HiDPI。

### 关于亮度调节



### 关闭SIP

设置config文件中的CsrActiveConfig 为0x17，然后重启进入recovery模式，通过终端关闭SIP。

### 关于睿频

设置好机型，CPU已经睿频，可用cpu-s软件检测。

### 支持Trim

在命令行输入命令：sudo trimforce enable

## 未解决问题

1、屏幕亮度不能调节。

2、插上电源，也显示在使用电池。