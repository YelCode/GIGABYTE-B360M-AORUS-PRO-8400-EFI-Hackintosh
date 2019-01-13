# B360M-AORUS-PRO-8400-EFI

## 黑苹果硬件配置
1. CPU i5 8400
2. 主板 B360 M AORUS PRO 小雕
3. 内存 阿斯加特洛极系列 DDR4 2400 16G
4. 固态硬盘 760P M.2 Nvme 256G

## EFI只适用于10.14.2 其他版本未做尝试
### 已知实现功能
1. 声卡
2. 网卡
3. CPU变频
4. 休眠
5. DP输出口（可4K）

### 已知问题
> 由于本人需求稳定，转战10.13.6 故没有精细测试


## BIOS设置
1. 硬盘模式调整为 AHCI
2. 开启支持 UEFI 启动，一般默认是开启的
3. 关闭VT-d，安完完系统后，再开启
4. 关闭CFG-Lock（我的BIOS没有此选项）
5. 关闭Secure Boot Mode
6. OS Type选项，设置为 Other OS
7. 关闭IO SerialPort
8. 设置 XHCI Handoff 为 开启

## 安装方法
[黑苹果B360M I3 8100 EFI](https://blog.csdn.net/flyhorstar/article/details/85242675)

[【黑果小兵】macOS Mojave 10.14.2 18C54 正式版 with Clover 4792原版镜像
](https://blog.daliansky.net/macOS-Mojave-10.14.2-18C54-official-version-with-Clover-4792-original-image.html)

## 参考
[黑苹果B360M I3 8100 EFI](https://blog.csdn.net/flyhorstar/article/details/85242675)

[【黑果小兵】macOS Mojave 10.14.2 18C54 正式版 with Clover 4792原版镜像
](https://blog.daliansky.net/macOS-Mojave-10.14.2-18C54-official-version-with-Clover-4792-original-image.html)
