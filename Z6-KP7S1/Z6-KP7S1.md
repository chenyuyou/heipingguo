# Z6-KP7S1

Update 2019.11.18

## 1、电脑配置

| 规格     | 详细信息                                                     |
| -------- | ------------------------------------------------------------ |
| 操作系统 | macOS Mojave 10.14.6                                         |
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

| 名称               | 版本  | 名称                | 版本  |
| ------------------ | ----- | ------------------- | ----- |
| FakeSMC            | 1800  | Lilu                | 1.4.0 |
| WhateverGreen      | 1.3.5 | AppleALC            | 1.4.4 |
| RTL8111            | 2.2.2 | USBinjectAll        | 0.7.4 |
| AirportBrcmFixup   | 2.0.4 | CPUFriend           | 1.1.9 |
| HibernationFixup   | 1.3.1 | NoTouchID           | 1.0.3 |
| RTCMemoryFixup     | 1.0.4 | VoodooPS2Controller | 2.1.0 |
| ACPIBatteryManager |       |                     |       |

### 1）显卡

WhateverGreen，但并没有解决显卡硬解的问题。

###  2）声卡

AppleALC+Lilu

Layout ID为6。

### 3）网卡

有线：型号：Realtek RTL8168/8111，需要RTL8111。

无线：型号：Dell Wireless 1510，需要驱动AirportBrcmFixup

### 4）蓝牙

DW1560，安装BrcmPatchRAM

### 5）电池

ACPIBatteryManager可能有用。

### 6）触摸板

VoodooPS2Controller。

### 7）显示器

参考黑果小兵

### 8） USB

USBInjectAll，参考黑果小兵。 

### 关于睡眠

HibernationFixup.kext

### 关于 HiDPI

使用"一键开启macOS HiDPI"脚本即可打开HiDPI。

### 关闭SIP

设置config文件中的CsrActiveConfig 为0x17，然后重启进入recovery模式，通过终端关闭SIP。

### 关于睿频

设置好机型，CPU已经睿频，可用cpu-s软件检测。

### 支持Trim

在命令行输入命令：sudo trimforce enable

### 双系统时间问题

RTCMenoryFixup.kext

### 关闭TouchID

NoTouchID.kext