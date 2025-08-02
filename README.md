# Asus P8B75-V Hackintosh Desktop
Asus P8B75-V Hackintosh-Desktop-macOS Monterey-OpenCore

# Configuration

## 硬件配置 / Specifications:

Processor：Intel Xeon E3-1230v2 Processor（Ivy Bridge，None IGPU）

Memory：24GB DDR3 1600MHz

Hard Disk：Intel S3510 120G SATA SSD，Samsung 860 EVO 250G SATA SSD，WDC HDD 500G x2

Integrated Graphics：Nvidia Quadro 410，Nvidia GeForce 750ti

Sound Card：Realtek ALC887 (layout-id:12)

Network Card：Broadcom BCM943602CDP Wireless LAN 802.11ac，Realtek RTL8111 PCI Express Gigabit Ethernet

## 无法工作 / Non-working:

-CPU Frequency Conversion,frequency locked at 3.7 GHz (Maybe it can be solved by unlocking CFG lock)

-Nvidia GeForce 750ti (Can install NVIDIA Webdriver on macOS High Sierra to Working)

## 注意事项 / matters needing attention:

-It is necessary to load AppleLPC by modifying InfoPersonality.kext, otherwise the system may run unstable.(maybe...)

需要通过修改InfoPersonality.kext的方式加载AppleLPC，否则可能造成系统运行不稳定（或许...）

SkyLake以前有两个重要组件FWH和LPC (Firmware Hub/Low Pin Count)，在SkyLake后Intel使用了新的规范，两个组件集成到了PMC（Power Management Controller），或多或少跟PMCR/PPMC的功能实现相关，因此我认为它具备加载必要性。

SkyLake used to have two important components, FWH and LPC (Firmware Hub/Low Pin Count). After SkyLake, Intel used a new specification. The two components were integrated into PMC (Power Management Controller), more or less with PMCR/PPMC. The function implementation is related, so I think it is necessary to load.


方法：将S/L/E目录中的AppleLPC导出，将AppleLPC.kext/Contents/info.plist的IOKitPersonalities信息复制到InfoPersonality.kext/Contents/info.plist。然后查看LPCB设备的IOReg IO名称，添加到InfoPersonality.kext/Contents/info.plist中的IOKitPersonalities-AppleLPC-IONameMatch


Method: Export the AppleLPC in the S/L/E directory, and copy the IOKitPersonalities information in AppleLPC.kext/Contents/info.plist to InfoPersonality.kext/Contents/info.plist. Then look at the IOReg IO name of the LPCB device, add to IOKitPersonalities-AppleLPC-IONameMatch in InfoPersonality.kext/Contents/info.plist

-Thanks[@PMheart](https://github.com/PMheart)

注意：加载AppleLPC会导致Recovery HD载入超时，且导致在Recovery HD内磁盘载入失败无法读取，原因不明。

Note: Loading AppleLPC will cause Recovery HD load timeout and cause disk load failure in Recovery HD to be unreadable for unknown reasons.

## 未经测试 / Untested availability:

-None

## 维护者 / Maintainer

© [Miracle櫻乃.](https://github.com/Miracle-Sakuno), Released under the [MIT License](./LICENSE) .<br>
Authored and maintained by Miracle櫻乃. with help from contributors ([list](https://github.com/Miracle-Sakuno/Asus-VivoBook-X509FB-Hackintosh/graphs/contributors)).

> GitHub [@Miracle櫻乃.](https://github.com/Miracle-Sakuno) · Twitter [@Miracle櫻乃.](https://twitter.com/Miracle_Sakuno) · Telegram Channel [@Rabbit House](https://t.me/RabbitHouse_i)

# 停止更新
# Stop updating
