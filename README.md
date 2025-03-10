# 微星 B360M 迫击炮 + AMD 独显黑苹果 EFI

## 我的配置

|          硬件 | 型号                                    |
| ------------: | :-------------------------------------- |
|          主板 | 微星 B360M 迫击炮                       |
|           CPU | Intel Core i7-8700                      |
|          显卡 | 蓝宝石 RX580 8G 2304SP 白金版 1366MHz   |
|         硬盘1 | 三星 970 Pro 1T M2 NVMe（Windows 系统） |
|         硬盘2 | 三星 SM961 512G M2 NVMe（MacOS 系统）   |
|         硬盘3 | 东芝 TR200 960G SSD SATA（数据盘）      |
|          内存 | 英睿达镁光 DDR4 2666Mhz 16G*4 (共 64G)  |
|   无线 + 蓝牙 | BCM943602CS 双频 BT4.1 无线网卡 PCI-E   |
|   机箱 + 电源 | 酷冷至尊Q300L机箱，海韵FOCUS GX-850电源 |
|       显示器1 | 43寸 4K 飞利浦显示器 BDM4350UC          |
|    显示器2、3 | 28寸 4K 泰坦军团显示器 P28H2V           |
| USB3.1 Type-C | Type-E 转为 Type-C 的 USB 3.1 的挡板线  |

## 兼容本 EFI 的设备

|            硬件 | 型号                                                        |
| --------------: | :---------------------------------------------------------- |
|            主板 | 微星 B360M 迫击炮（钛金版）                                 |
|             CPU | Intel 8代、9代酷睿处理器，最好有核显                        |
|            显卡 | RX560、RX570、RX580、RX590、Vega56、Vega64、Radeon VII      |
|            硬盘 | 除了几个特别，比如 PM981、970 Evo Plus 等，其它的应该都可以 |
|            内存 | 其它的没试过，反正镁光的没问题                              |
|     无线 + 蓝牙 | 淘宝上很多苹果免驱的无线 + 蓝牙的 PCI-E 卡都可以            |
|     机箱 + 电源 | 根据你的爱好和CPU、显卡的功率来决定                         |
|          显示器 | 根据个人爱好任意选择                                        |
|          读卡器 | 只要是苹果上免驱的都可以                                    |
|     键盘 + 鼠标 | 根据个人爱好任意选择                                        |
| 摄像头 + 麦克风 | 只要是苹果上免驱的都可以                                    |
|        其它外设 | 根据个人爱好随意选配                                        |

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

## 更新日志

### 2025年2月4日

* 增加了对其他系统的启动图标支持

### 2025年1月29日（大年初一）

* 更新 OC 到 1.0.3。
* 删除 Clover。
* 驱动更新为最新版本。
* 支持 MacOS 升级到 Sequoia 15.3。

### 2021年6月22日

* 删除 OC。
* 更新 Clover 到 5137 版本。
* 驱动更新为最新版本。
* 支持 Big Sur 升级到 11.4。

### 2021年1月10日

* 更新 OC 到 0.6.5 版本。
* 更新 Clover 到 5128 版本。
* 驱动更新为最新版本。
* Clover 已经可以启动 Big Sur（需要从 Preboot 分区启动），为了让多系统引导时，其它系统保持原汁原味，默认启动改为 Clover。

### 2020年12月13日

* 更新 OC 到 0.6.4 版本。
* 驱动更新为最新版本。
* 更新了一下 OC 的配置文件，方便关闭 SIP。

### 2020年11月4日

* 更新 OC 到 0.6.3 版本。
* 驱动更新为最新版本。

### 2020年7月4日

* 更新 Clover 版本到 5119。
* 默认改为 OC 0.6.0 启动（修改自：[MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI](https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI)）。
* OC 下 Lilu 更新到 1.4.5。
* OC 下 WhateverGreen 更新到 1.4.0。
* AppleALC 更新到 1.5.0。
* IntelMausi 更新到 1.0.3。
* VirtualSMC 更新到 1.1.4。
* 增加了 USBPorts.kext 和 USBPower.kext。
* 默认机型改为 iMac19,2（因为我的 i7-8700 跟这个机型最匹配）。

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

## EFI 使用

关于三码修改和 BIOS 设置部分请参考：https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI#%E4%BD%BF%E7%94%A8-efi

## 感谢

* [SuperNG6](https://sleele.com/)
* [GeQ1an](https://github.com/GeQ1an/MSI-B360M-MORTAR-HACKINTOSH-OPENCORE-EFI)
* [黑果小兵](https://blog.daliansky.net/)
* [xin](https://blog.xjn819.com/)
* [Bat.bat](https://github.com/williambj1/OpenCore-Factory)
* [GoldenGateExt](https://github.com/HJebbour/GoldenGateExt-OpenCore-Theme)

## 小技巧

### 跟 Windows 和 BIOS 中的时间同步

```
sudo sh -c "$(curl -fsSL https://raw.githubusercontent.com/xiaoMGithub/LocalTime-Toggle/master/fix_time_osx.sh)"
```

### 更新卡住

电脑更新重启后，可能会出现更新安装到一定进度后，界面卡死不动，也没有读盘的情况，这种情况下，关机重启就可以继续更新了。

### 无线网卡

无线网卡如果跟我一样是 BCM943602CS 的话，需要用 OpenCore Legacy Patcher 安装一下 Root Patch。
![截图加载失败](ScreenShot/RootPatch@2x.png)

### 其他系统启动图标设置

就是在各个系统的 EFI 启动目录下面，添加 .contentFlavour 和 .contentDetails 这两个文件，其中 .contentFlavour 内容对应的是图标，
.contentDetails 对应的是显示的文字。例如：

#### Windows 11 

在 EFI\Microsoft\Boot 下面添加 .contentFlavour 文件，内容为：
`Windows11:Windows`, 就是先找 `Windows11` 的图标，没有的话就找 `Windows` 的图标。添加 .contentDetails 文件，内容为：`Windows 11`。

#### Linux

在 EFI 下面的对应系统的目录下，例如 Debian 就是 EFI\debian，在其中添加 .contentFlavour 文件，内容为：`Debian:Linux`, 添加 .contentDetails 文件，内容为：`Debian`。

## Geekbench 6.3.0 跑分

* CPU (单核：1535，多核：6794)：https://browser.geekbench.com/v6/cpu/10175452
* Metal (62654)：https://browser.geekbench.com/v6/compute/3564445
* OpenCL (48600): https://browser.geekbench.com/v6/compute/3564419

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
