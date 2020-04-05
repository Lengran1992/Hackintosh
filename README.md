# Hackintosh
欢迎提出意见建议，不定期更新。

---------------------------------------------------------

# 我的电脑配置

处理器：AMD Ryzen 5 3600X 6-Core 六核

主板：华硕 ROG STRIX B450-F GAMING

内存：海盗船 DDR4 3200MHz 8GB*2

主硬盘：Intel 660P 1T

副硬盘：紫光存储 P100 512G

显卡：华硕 AMD Radeon RX 5700 XT 8 GB

有线网卡：Intel I211 Gigabit Network Connection

无线网卡：Fenvi FV-T919（BCM94360CD芯片）

---------------------------------------------------------

# 更新日志

2020年4月5日 

1.config.plist按照官方文档的格式重新进行排列

2.SMCAMDProcessor.kext 更新至1.0，添加 AMDRyzenCPUPowerManagement.kext，不再需要依赖VirtualSMC.kext，项目地址：https://github.com/trulyspinach/SMCAMDProcessor/releases

3.推荐个神器 Kext Updater，下载地址：https://bitbucket.org/profdrluigi/kextupdater/downloads/ 

驱动均已全部更新至最新

AppleALC.kext 1.4.7

Lilu.kext 1.4.2

Innie.kext 1.2.0

NoTouchID.kext 1.0.3

SMCAMDProcessor.kext 1.0

AMDRyzenCPUPowerManagement.kext 0.6

SmallTreeIntel82576.kext 1.0.6

VirtualSMC.kext 1.1.1

VoodooPS2Controller.kext 2.1.2

WhateverGreen.kext 1.3.7

---------------------------------------------------------

2020年3月26日 

更新支持10.15.4，自动开启HDR，如果屏幕发白，可以前往设置-显示器，关闭高动态范围

---------------------------------------------------------

2020年3月11日

OC内核更新至0.5.7；

---------------------------------------------------------

2020年1月13日 

1.OC内核更新至0.5.4；

2.机型及SMBIOS自定义，目前 AMD 的 CPU 显示无果，可自定义修改 /System/Library/PrivateFrameworks/AppleSystemInfo.framework/Versions/A/Resources/zh_CN.lproj/Processors.strings 当下显示的处理器显示，如当下 Mac 显示为”六核Intel Core i5“，只需在 Processors.strings 中修改为自己想要的型号即可。

修改步骤：

①挂载读写命令：

sudo -s

sudo mount -o rw /

②定位文件夹命令：

cd /System/Library/PrivateFrameworks/AppleSystemInfo.framework/Versions/A/Resources/zh_CN.lproj/

③替换文件命令：

cp 修改好的Processors.strings /System/Library/PrivateFrameworks/AppleSystemInfo.framework/Versions/A/Resources/zh_CN.lproj/

---------------------------------------------------------

2020年1月9日

首次发布，欢迎大家提出意见建议！

---------------------------------------------------------
