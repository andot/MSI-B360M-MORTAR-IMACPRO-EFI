# 微星 B360M 迫击炮 + AMD 独显黑苹果 EFI

## 我的配置

|               硬件 | 型号                                                        |
| -----------------: | :---------------------------------------------------------- |
|               主板 | MSI® B360M MORTAR                                           |
|                CPU | 英特尔® 酷睿™ i5-9400 处理器 2.9GHz                         |
|               显卡 | 蓝宝石® RX590 8G D5 超白金 极光特别版                       |
|              硬盘1 | 英特尔® 固态盘 760p 系列 512GB                              |
|              硬盘2 | 西部数据® 蓝盘 1TB                                          |
|               内存 | 海盗船 复仇者® LPX 2666MHz 8GB x 2                          |
|        无线 + 蓝牙 | 博通® BCM94360CD                                            |
| 机箱 + 电源 + 风扇 | 追风者® MG NEO Micro 410，振华® 冰山金蝶550战斗版，风扇 * 3 |
|               键盘 | IKBC® C87                                                   |
|               鼠标 | 罗技® MX Master 2S                                          |
|             显示器 | 宏碁® XV272U P 27英寸 2K 144Hz HDR400 IPS                   |


## 更新日志

### 2019年12月19日

在 BIOS 中关闭了 `CFG Lock`，因此将 `AppleIntelCPUPM` 和 `内核电源` 两个选项的取消勾选。



### 2019年12月18日

*forked from andot*

- 更改 机型为 `iMac19,2`。
- 根据微星 B360M 迫击炮主板和追风者 MG NEO 410 机箱定制 USB 驱动——
  - 禁用 USB 端口限制补丁
  - 删除 原 EFI 中的 `USBInjectAll.kext`
  - 加入 `EFI/CLOVER/ACPI/patched/SSDT-EC.aml` 和 `EFI/CLOVER/kexts/Other/USBPorts.kext`

### 2019年12月14日

加入 NightShiftUnlocker.kext。
更新 WhateverGreen.kext 到 1.3.6。

### 2019年12月6日

更新 Clover 版本到 5100。
加入 slide 启动项，修正有时无法启动的问题。
自动开启 TRIM 支持。

### 2019年12月6日

更新驱动到最新版本。更新 Clover 版本到 5099。

### 2019年11月1日

更新驱动到最新版本。可以正常升级到 macOS Catalina 10.15.1。

### 2019年10月9日

更新 Clover 版本到 5070。可以正常升级到 macOS Catalina。

### 2019年8月27日

更新 Clover 版本到 5058。

### 2019年8月22日

更新 Clover 版本到 5051。

### 2019年8月21日

经过一个多月的使用测试后，首次发布。

## Geekbench 4 跑分

* CPU (单核：5259，多核：21292)：https://browser.geekbench.com/v4/cpu/15048380
* OpenCL (150951): https://browser.geekbench.com/v4/compute/4671536