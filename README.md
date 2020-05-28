# 微星 B360M 迫击炮 + AMD 独显黑苹果 EFI

## 我的配置

|               硬件 | 型号                                    |
|-------------------:|:----------------------------------------|
|               主板 | 微星 B360M 迫击炮                       |
|                CPU | Intel Core i7-8700                      |
|               显卡 | 蓝宝石 RX580 8G 2304SP 白金版 1366MHz   |
|              硬盘1 | 三星 970 Pro 1T M2 NVMe                 |
|              硬盘2 | 三星 SM961 512G M2 NVMe                 |
|              硬盘3 | 东芝 TR200 960G SSD SATA                |
|               内存 | 英睿达镁光 DDR4 2666Mhz 16G*2 (共 32G)  |
|        无线 + 蓝牙 | BCM943602CS 双频 BT4.1 无线网卡 PCI-E   |
|    摄像头 + 麦克风 | 蓝色妖姬 480p USB2 摄像头带内置麦克风   |
| 机箱 + 电源 + 风扇 | 酷冷至尊Q300L机箱，MWE500电源，风扇 * 3 |
|               键盘 | 罗技 K780                               |
|               鼠标 | 罗技 M590                               |
|      USB3.1 Type-C | Type-E 转为 Type-C 的 USB 3.1 的挡板线  |
|            显示器1 | 43寸 4K 飞利浦显示器 BDM4350UC          |
|            显示器2 | 23寸 1080p AOC 显示器 2367              |
|             读卡器 | 绿联 USB 3.0 四合一读卡器               |

## 兼容本 EFI 的设备

|               硬件 | 型号                                                        |
|-------------------:|:------------------------------------------------------------|
|               主板 | 微星 B360M 迫击炮（钛金版）                                 |
|                CPU | Intel 8代、9代酷睿处理器，有无核显都可以                    |
|               显卡 | RX560、RX570、RX580、RX590、Vega56、Vega64、Radeon VII      |
|               硬盘 | 除了几个特别，比如 PM981、970 Evo Plus 等，其它的应该都可以 |
|               内存 | 其它的没试过，反正镁光的没问题                              |
|        无线 + 蓝牙 | 淘宝上很多苹果免驱的无线 + 蓝牙的 PCI-E 卡都可以            |
|    摄像头 + 麦克风 | 只要是苹果上免驱的都可以                                    |
| 机箱 + 电源 + 风扇 | 根据你的爱好和CPU、显卡的功率来决定                         |
|        键盘 + 鼠标 | 根据个人爱好任意选择                                        |
|             显示器 | 根据个人爱好任意选择                                        |
|             读卡器 | 只要是苹果上免驱的都可以                                    |
|           其它外设 | 根据个人爱好随意选配                                        |

## 显卡选择注意事项

因为微星 B360M 迫击炮主板的第 4 个 PCI-E 插槽跟第 2 个 M2 槽冲突，所以如果像我一样选择双 M2 硬盘的话，那么在选择显卡的时候一定要注意不要选择超过两个 PCI-E 插槽厚度的显卡，否则第 3 个 PCI-E 插槽（PCI-E x1）会被显卡挡住不能用，这样就无法插苹果免驱的无线 + 蓝牙网卡了。

我测试过可以正常使用的显卡有：

* 蓝宝石 RX580 8G 2304SP 白金版 1366MHz (厚度为 42mm)
* 迪兰（Dataland）RX VEGA56 8G X-Serial 战神（厚度为 40mm）

厚度小于等于 42mm 的显卡应该都不妨碍第三个 PCI-E 插槽。

对于 44mm 的显卡，比如：

* 蓝宝石 RX580 8G 2304SP 超白金极光
* 蓝宝石 RX590 8G 超白金

跟无线网卡一起插入可能有一定的冲突，但如果无线网卡比较薄，或自己想办法打磨一下，机箱又采用横放的话，也许可以避免显卡风扇刮到无线网卡，但我个人不建议冒这个风险。

个人建议，如果有钱就上 Radeon VII，这个显卡厚度上是 40mm，是没有问题的。

## 更新注意事项

更新 EFI 之后，第一次进系统最好是带 -v 参数启动，否则可能会出现禁止符号，无法启动。如果出现这种情况下，再次启动时，加上 -v 参数就可以了。进入系统之后，最好使用 Hackintool 重建一下驱动缓存。

## 更新日志

### 2020年5月28日

* 更新 Clover 版本到 5118。
* 更新 Lilu 到 1.4.4。
* 更新 WhateverGreen 到 1.3.9（[ayun2001 魔改版](http://bbs.pcbeta.com/viewthread-1847847-1-1.html)）。
* 添加了 NVMeFix 1.0.2。
* 可以正常升级到 macOS Catalina 10.15.5。

### 2020年3月25日

* 更新 Clover 版本到 5107。
* 更新 Lilu 到 1.4.3。
* 更新 AppleALC 到 1.4.8。
* 更新 VirtualSMC 到 1.1.1。
* 更新 WhateverGreen 到 1.3.7（[ayun2001 魔改版](http://bbs.pcbeta.com/viewthread-1847847-1-1.html)）。
* 可以正常升级到 macOS Catalina 10.15.4。
* 自己又增加了 2 条 16G 内存，现在有 64G 内存了。

### 2020年1月23日

* 重新启用 USB 定制（如果主板不一样，请自行重新定制）。
* 开启节能五项之断电后自动启动。（感谢 PCBeta 的 bb1045 提供的方案）
* 开启原生NVRAM。（感谢 PCBeta 的 bb1045 提供的方案）

### 2020年1月9日

* 更新 Clover 版本到 5103。
* 更新了一些驱动。

### 2019年12月14日

* 加入 NightShiftUnlocker.kext。
* 更新 WhateverGreen.kext 到 1.3.6。

### 2019年12月6日

* 更新 Clover 版本到 5100。
* 加入 slide 启动项，修正有时无法启动的问题。
* 自动开启 TRIM 支持。

### 2019年12月6日

* 更新驱动到最新版本。
* 更新 Clover 版本到 5099。

### 2019年11月1日

* 更新驱动到最新版本。
* 可以正常升级到 macOS Catalina 10.15.1。

### 2019年10月9日

* 更新 Clover 版本到 5070。
* 可以正常升级到 macOS Catalina。

### 2019年8月27日

* 更新 Clover 版本到 5058。

### 2019年8月22日

* 更新 Clover 版本到 5051。

### 2019年8月21日

* 经过一个多月的使用测试后，首次发布。

## EFI 简介

这个 EFI 的特点是使用的是 `iMacPro1,1` 机型，用独显硬解，因此 CPU 有无核显都可以正常工作，且比使用核显硬解更正常。已做了 USB 定制，所有 USB 接口都可用，睡眠正常，唤醒正常。

Clover 版本为：5100。

Clover 驱动包含：

* ApfsDriverLoader.efi
* AptioMemoryFix.efi
* EmuVariableUefi.efi
* FSInject.efi
* HFSPlus.efi
* VirtualSmc.efi

系统驱动包含：

* AppleALC.kext - 1.4.5
* IntelMausi.kext - 1.0.2
* Lilu.kext - 1.4.1
* USBInjectAll.kext - 0.7.4
* VirtualSMC.kext - 1.0.9
* WhateverGreen.kext - 1.3.6
* NightShiftUnlocker.kext - 2.2.1

下面这 2 个是 VirtualSMC 的插件

* SMCProcessor.kext
* SMCSuperIO.kext

## EFI 使用

如果你的配置跟我上面配置相同或兼容，那么你可以直接使用该 EFI 进行安装。安装前请注意，一定要用 Clover Configurator 重新生成并替换 SMBIOS 部分的内容，否则会因为机器有同一个硬件 ID 而被苹果封锁。生成时，请选择 `iMacPro1,1` 机型，不要更改机型，如果你的 CPU 有核显，并且核显已经再 BIOS 中打开，也可以选择 `iMac19,2` 机型，这种情况下，核显可以和独显一起工作。

![截图加载失败](ScreenShot/SMBIOS@2x.png)

如果你的显卡跟我一样是 RX 580 8G 2304sp 的话，建议把显卡设置页面设置为下图这样：

![截图加载失败](ScreenShot/GPUConfig@2x.png)

你会发现显卡功耗会降低 20w 左右。

## 小技巧

### 开启原生电源管理

如果你在 BIOS 里面把 `CFG Lock` 选项设置为 `Disable`，那么你还可以用 Clover Configurator 修改配置文件，将 `AppleIntelCPUPM` 和 `内核电源` 两个选项的对勾去掉，这样就可以开启原生电源管理了，据说性能会有微小的一点提升。

### 跟 Windows 和 BIOS 中的时间同步

```
sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/xiaoMGithub/LocalTime-Toggle/master/fix_time_osx.sh)"
```

## Geekbench 跑分

* CPU (单核：6079，多核：28401)：https://browser.geekbench.com/v4/cpu/14377865
* Metal (131638)：https://browser.geekbench.com/v4/compute/4463241
* OpenCL (133320): https://browser.geekbench.com/v4/compute/4463244

![截图加载失败](ScreenShot/CINEBENCH20@2x.png)

## 系统截图

![截图加载失败](ScreenShot/neofetch@2x.png)
![截图加载失败](ScreenShot/AboutMyMac@2x.png)
![截图加载失败](ScreenShot/Audio@2x.png)
![截图加载失败](ScreenShot/Microphone@2x.png)
![截图加载失败](ScreenShot/Monitor@2x.png)
![截图加载失败](ScreenShot/Monitor2@2x.png)
![截图加载失败](ScreenShot/VideoProc@2x.png)
![截图加载失败](ScreenShot/USB@2x.png)
![截图加载失败](ScreenShot/LAN@2x.png)
![截图加载失败](ScreenShot/Wifi@2x.png)
![截图加载失败](ScreenShot/BT@2x.png)
![截图加载失败](ScreenShot/GPU_Monitor@2x.png)
![截图加载失败](ScreenShot/GraphicsDriver@2x.png)
![截图加载失败](ScreenShot/HWMonitorSMC2@2x.png)