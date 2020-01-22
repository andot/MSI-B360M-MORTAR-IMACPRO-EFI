# 微星 B360M 迫击炮 + AMD 独显黑苹果 - Clover 引导 EFI 

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



### 2020年01月22日

从源库更新了 Clover 和一些驱动。
更新了一些主题，删除了一些主题。
为 300 系主板启用了原生 NVRAM。

### 2019年12月19日

在 BIOS 中关闭了 `CFG Lock`，因此将 `AppleIntelCPUPM` 和 `内核电源` 两个选项的取消勾选。

### 2019年12月18日

*forked from andot*

- 更改 机型为 `iMac19,2`。
- 根据微星 B360M 迫击炮主板和追风者 MG NEO 410 机箱定制 USB 驱动——
  - 禁用 USB 端口限制补丁
  - 删除 原 EFI 中的 `USBInjectAll.kext`
  - 加入 `EFI/CLOVER/ACPI/patched/SSDT-EC.aml` 和 `EFI/CLOVER/kexts/Other/USBPorts.kext`
