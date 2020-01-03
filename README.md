# B360M-AORUS-PRO-8400-EFI

## 提示
> 目前macOS 截止10.15.2 都不稳定 仍有蛮多问题的，所以暂不跟进。并且xcode对系统的要求是10.14.4或更高版本，追求稳定才是我的目标。

## 黑苹果硬件配置
1. CPU i5 8400
2. 主板 B360 M AORUS PRO 小雕
3. 内存 阿斯加特洛极系列 DDR4 2400 16G*2
4. 固态硬盘 760P M.2 Nvme 256G
5. 机箱 先马米立方（10.14.5修复usb，包括机箱三个前置）

> 要对应版本选择 覆盖EFI磁盘的EFI文件夹 版本错误可能会导致无法启动系统

### 实现功能
1. 声卡
2. 网卡
3. CPU变频
4. 休眠
5. DP输出口（可4K）

### 10.13
#### 10.13.6已知问题 
1. 休眠后DP声音无效
2. HDMI视频无视频输出

### 10.14
#### 10.14.2
##### 已知问题 
1. 休眠后DP声音无效
2. HDMI视频无视频输出
3. USB3.0不识别

#### 10.14.4
##### 已知问题 
1. USB3.0不识别

#### 10.14.5
##### 修复问题 （终于抽空改了一些，自己动手，丰衣足食）
1. USB3.0不识别

##### 已知问题
无

## BIOS设置篇(F1，F3皆可)
> 题外话，我刷的F3 突然有一天不能启动黑苹果了 自动退回F1了 后面重新设置BIOS

##### BIOS
- BIOS->Storage boot BIOS->other PCI devices->UEFI（开启支持 UEFI 启动，一般默认是开启的 ）
-  BIOS->CSM Support disable
-  BIOS->Secure Boot->Secure Boot Enable-> disabled（上一步设置后才有这个选项）
-  BIOS->Windoews 8/10 Features ->Other OS（设置启动系统类型）


##### Chipset
- Chipset->VT-d（关闭VT-d，安完完系统后，再开启）
-  关闭 Chipset->IOAPIC 24-119

##### Peripherals
- Peripherals->SATA AND RST->SATA Mode selection-> AHCI
-  Peripherals->Super IO Configuration-> Serial Port（关闭IO SerialPort ）
-  Peripherals->USB Configuration->XHCI Hand-off（设置 XHCI Handoff 为 开启 ）
-  关闭CFG-Lock（我的BIOS没有此选项）

> 部分EFI为以下博文下载收集而来，经过本人电脑实践可行

## EFI下载

[CSDN积分下载-10.14.2](https://download.csdn.net/download/q670051552/10888077)

[Github下载，可以star一下或者一起维护](https://github.com/StarYellow/GIGABYTE-B360M-AORUS-PRO-8400-EFI-Hackintosh)

## 参考博文和安装方法
[黑苹果B360M I3 8100 EFI](https://blog.csdn.net/flyhorstar/article/details/85242675)

[【黑果小兵】macOS Mojave 10.14.2 18C54 正式版 with Clover 4792原版镜像
](https://blog.daliansky.net/macOS-Mojave-10.14.2-18C54-official-version-with-Clover-4792-original-image.html)
