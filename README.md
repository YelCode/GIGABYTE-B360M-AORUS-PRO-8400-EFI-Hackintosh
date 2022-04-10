# B360M-AORUS-PRO-8400-EFI

## 最新进展
* 最新10.15.6 (10.15.7估计可以直接使用 )
* macOS Big Sur 暂不适配
* 解决4k屏息屏之后 无法唤醒的问题 目前很完美 没有大问题

## 黑苹果硬件配置
1. CPU i5 8400
2. 主板 技嘉 B360 M AORUS PRO 小雕
3. 内存 阿斯加特洛极系列 DDR4 2400 16G*2
4. 固态硬盘 760P M.2 Nvme 256G
5. 机箱 先马米立方
6. 无线网卡 BCM94360CD 蓝牙+无线 免驱

> 要对应版本选择 覆盖EFI磁盘的EFI文件夹 版本错误可能会导致无法启动系统

## 10.15
### 10.15.6
> 基本完美，未发现大问题

## 10.14
#### 10.14.5
##### 修复问题 （终于抽空改了一些，自己动手，丰衣足食）
1. USB3.0不识别

#### 10.14.4
##### 已知问题 
1. USB3.0不识别

#### 10.14.2
##### 已知问题 
1. 休眠后DP声音无效
2. HDMI视频无视频输出
3. USB3.0不识别

## 10.13
#### 10.13.6已知问题 
1. 休眠后DP声音无效
2. HDMI视频无视频输出

## 给作者一个赞赏

<img src="https://s1.ax1x.com/2022/04/10/LAbkPe.jpg" width="300" alt="微信二维码">

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

> EFI参考以下博文加上修改而来，经过本人电脑实践可行，配置不同，请小心使用并备份原版EFI

## EFI下载

[CSDN积分下载-10.14.2](https://download.csdn.net/download/q670051552/10888077)

[Github下载，可以star一下或者一起维护](https://github.com/StarYellow/GIGABYTE-B360M-AORUS-PRO-8400-EFI-Hackintosh)

## 参考博文和安装方法
[黑苹果B360M I3 8100 EFI](https://blog.csdn.net/flyhorstar/article/details/85242675)

[【黑果小兵】macOS Mojave 10.14.2 18C54 正式版 with Clover 4792原版镜像
](https://blog.daliansky.net/macOS-Mojave-10.14.2-18C54-official-version-with-Clover-4792-original-image.html)
