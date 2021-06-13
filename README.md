# Asus P8B75-V Hackintosh Desktop
Asus P8B75-V Hackintosh-Desktop-macOS Big Sur-OpenCore

# Configuration

## 硬件配置 / Specifications:

Processor：Intel Xeon E3-1230v2 Processor（Ivy Bridge，None IGPU）

Memory：24GB DDR3 1600MHz

Hard Disk：Intel S3510 120G SATA SSD，Samsung 860 EVO 250G SATA SSD，WDC HDD 500G x2

Integrated Graphics：Nvidia Quadro 410，Nvidia GeForce 750ti

Sound Card：Realtek ALC887 (layout-id:13)

Network Card：Broadcom BCM94360CD Wireless LAN 802.11ac，Realtek RTL8111 PCI Express Gigabit Ethernet

## 无法工作 / Non-working:

-CPU Frequency Conversion (Maybe it can be solved by unlocking CFG lock)

-Sleep S3 (Maybe it can be solved by unlocking CFG lock)

-Nvidia GeForce 750ti (Can install NVIDIA Webdriver on macOS High Sierra to Working)

## 注意事项 / matters needing attention:

-It is necessary to load AppleLPC by modifying VirtualSMC, otherwise the system may run unstable.
需要通过修改VirtualSMC的方式加载AppleLPC，否则可能造成系统运行不稳定

[course/教程](https://www.bilibili.com/read/cv6353697/)

## 未经测试 / Untested availability:

-None

## 维护者 / Maintainer

© [Miracle樱乃.](https://github.com/Miracle-Sakuno), Released under the [MIT License](./LICENSE) .<br>
Authored and maintained by Miracle樱乃. with help from contributors ([list](https://github.com/Miracle-Sakuno/Asus-VivoBook-X509FB-Hackintosh/graphs/contributors)).

> GitHub [@Miracle樱乃.](https://github.com/Miracle-Sakuno) · Twitter [@Miracle樱乃.](https://twitter.com/Miracle_Sakuno) · Telegram Channel [@Rabbit House](https://t.me/RabbitHouse_i)

此文档暂时归档，若有其他维护者请勿改动
