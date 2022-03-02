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

-It is necessary to load AppleLPC by modifying InfoPersonality.kext, otherwise the system may run unstable.

需要通过修改InfoPersonality.kext的方式加载AppleLPC，否则可能造成系统运行不稳定

SkyLake以前有两个重要组件FWH和LPC (Firmware Hub/Low Pin Count)，在SkyLake后Intel使用了新的规范，两个组件集成到了PMC（Power Management Controller），或多或少跟PMCR/PPMC的功能实现相关，因为我认为它具备加载必要性。

方法：将S/L/E目录中的AppleLPC导出，将AppleLPC.kext/Contents/info.plist的IOKitPersonalities信息复制到InfoPersonality.kext/Contents/info.plist。然后查看LPCB设备的IOReg IO名称，添加到InfoPersonality.kext/Contents/info.plist中的IOKitPersonalities-AppleLPC-IONameMatch

感谢[@PMheart](https://github.com/PMheart)

## 未经测试 / Untested availability:

-None

## 维护者 / Maintainer

© [Miracle樱乃.](https://github.com/Miracle-Sakuno), Released under the [MIT License](./LICENSE) .<br>
Authored and maintained by Miracle樱乃. with help from contributors ([list](https://github.com/Miracle-Sakuno/Asus-VivoBook-X509FB-Hackintosh/graphs/contributors)).

> GitHub [@Miracle樱乃.](https://github.com/Miracle-Sakuno) · Twitter [@Miracle樱乃.](https://twitter.com/Miracle_Sakuno) · Telegram Channel [@Rabbit House](https://t.me/RabbitHouse_i)

此文档暂时归档，若有其他维护者请勿改动

### 注意：本人公开的社交账号仅为此Github，Twitter和Telegram频道，以及本人QQ账号为：2112074157。除以上四个本人专用账号之外，其他任何以我的名义来发布消息的都是骗子，注意核实
### 尤其注意此人QQ账号：1063995989，1248394877长时间故意盗用本人身份发布各类不实消息，请各位注意核实，并帮助我举报他
### 感谢各位支持

Note: my social account is only for GitHub, twitter and telegraph channels, and my QQ account is 2112074157. In addition to the above four personal accounts, any other person who publishes information in my name is a liar. Pay attention to verification

Pay special attention to this person's QQ account: 1063995989，1248394877. He deliberately embezzles his identity and publishes all kinds of false news for a long time. Please pay attention to verification and help me report him

Thank you for your support
