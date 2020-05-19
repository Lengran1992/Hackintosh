# Hackintosh（2020.5.19更新）
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

# 驱动版本（2020.5.19最新）

AppleALC.kext
1.4.9
定制万能声卡驱动

Lilu.kext
1.4.4
SDK & Library

Innie.kext
1.2.0
磁盘外置修复驱动

NoTouchID.kext
1.0.3
禁用 Touch ID 检测, 修复输密码时卡顿

SMCAMDProcessor.kext
1.0
AMD CPU 检测驱动

AMDRyzenCPUPowerManagement.kext
0.6.3
AMD CPU 检测驱动

SmallTreeIntel82576.kext
1.0.6
I211-AT 有线网卡驱动

VirtualSMC.kext
1.1.3
SMC 和传感器驱动

VoodooPS2Controller.kext
2.1.2
PS2 键盘/触摸板 驱动

WhateverGreen.kext
1.3.9
显卡补丁驱动

---------------------------------------------------------
# 更新日志

2020年5月19日 

OC内核更新至0.5.8；

---------------------------------------------------------
2020年4月7日 

1.优化 config.plist，去除多余语句

2.进 recovery，需要 vboxhfs.efi 或 hfsplus.efi，如用 vboxhfs.efi 依旧无法进入，就换用 hfsplus.efi。（此 EFI 用的是 hfsplus.efi）

3.SMCAMDProcessor.kext 更新至1.0，添加 AMDRyzenCPUPowerManagement.kext，不再需要依赖VirtualSMC.kext，项目地址：https://github.com/trulyspinach/SMCAMDProcessor/releases

4.推荐个神器 Kext Updater，下载地址：https://bitbucket.org/profdrluigi/kextupdater/downloads/ 

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
