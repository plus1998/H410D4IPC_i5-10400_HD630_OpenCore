
# EFI
OpenCore版本: 0.7.5
支持macOS版本: Catalina, Big Sur, Monterey

更新EFI前请做EFI备份，升级系统有风险，请知悉

![系统信息](https://github.com/plusl894860970/H410D4IPC_i5-10400_HD630_OC_BigSur/blob/3140e25e6ab1c1ff71dcf829a3bee53145d1c00c/images/info.png)

## 硬件配置

| 配件   | 型号 | 说明 |
|------|----|----|
| 主板   |  昂达H410D4 IPC  |  USB3 * 1, USB2 * 2, Tpye-C * 1 |
| CPU  |  i5-10400  |  6核12线程  |
| 内存   |  酷兽ddr4 2666（笔记本）  |  16G * 2  |
| 显卡   |  Intel UHD Graphics 630  |  DP * 1, HDMI * 1  |
| SSD  |  西数SN550 500G  |  NVME  |
| 声卡   |  ALC662  |  alcid=5  |
| 有线网卡 |  RTL8111  |  千兆网卡  |
| 无线网卡 |  BCM94360CS2  |  免驱  |
| 电源 |  DC电源  |  150w  |
| 机箱 |  酷鱼MG PLUS DC-ITX  |    |


## 说明

* 已做USB定制: TypeC, USB3正常

## 关于英特尔网卡问题 (2020-12-21已移除英特尔网卡驱动)

~~AirportItlwm.kext~~

~~IntelBluetoothFirmware.kext~~

~~IntelBluetoothInjector.kext~~


##### 2020-11-24

~~测试v1.2.0-alpha，目测网速提升20%-50%。十分看好这个项目。建议长期关注~~


##### 2020-12-15

* 热心网友反馈，10.15.7可以正常使用新EFI，所以删除了原EFI。如遇到10.15.7英特尔网卡无法使用的情况。请自行替换AirportItlwm。
* 由于条件限制，如遇到蓝牙或者usb口无法使用的情况，请取消勾选 USBPorts.kext。 同时勾选 USBInjectAll.kext 开机后自行定制USB。

##### 2020-12-19

* 更新到OC 0.6.4
* 更新plist修复引导版本识别错误的问题

##### 2020-12-21

* 终于选择弃暗投明，放弃了英特尔网卡。换了 BCM94360CS2 ，重新定制了USB。
* 继续使用英特尔网卡的前往 [AirportItlwm发行版](https://github.com/OpenIntelWireless/itlwm/releases) 下载驱动


##### 2021-11-09

* 受前人恩惠，当知恩图报，敢为人先。
* 因为没有人反馈升级到Monterey的情况，所以先直接更新OC版本到0.7.5，目前测试BigSur 11.6正常，可以直接在线升级到Monterey。
* 因为我换了白苹果网卡完成了闭环！所以我没有再去关注[OpenIntelWireless](https://github.com/OpenIntelWireless/itlwm/releases)项目，也不再在此项目更新相关内容，请知悉
