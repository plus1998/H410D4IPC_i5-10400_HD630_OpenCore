
# EFI
OpenCore: 0.6.4
macOS version: Big sur 11.1

## 硬件配置

| 配件   | 型号 | 说明 |
|------|----|----|
| 主板   |  昂达H410D4 IPC  |  USB3 * 1, USB2 * 2, Tpye-C * 1 |
| CPU  |  i5-10400  |  6c12t, L3 12M  |
| 内存   |  酷兽ddr4 2666（笔记本）  |  16G * 2  |
| 显卡   |  Intel UHD Graphics 630  |  DP * 1, HDMI * 1  |
| SSD  |  西数SN550 500G  |  NVME  |
| 声卡   |  ALC662  |  alcid=5  |
| 有线网卡 |  RTL8111  |  千兆网卡  |
| 无线网卡 |  AC3168  |  itlwm驱动  |
| 电源 |  DC电源  |  150w  |
| 机箱 |  酷鱼MG PLUS DC-ITX  |    |


## 说明

* 已做USB定制: TypeC, USB3正常
* 蓝牙正常工作，WIFI能满足个人日常使用

## 已知问题
* WIFI不满速
* AirDrop不可用

## 关于英特尔网卡问题

[AirportItlwm发行版](https://github.com/OpenIntelWireless/itlwm/releases)

*有需要的可以更换博通网卡（博通网卡驱动方法自己找）,移除以下内核*
* AirportItlwm.kext
* IntelBluetoothFirmware.kext
* IntelBluetoothInjector.kext

##### 2020-11-24

测试v1.2.0-alpha [AirportItlwm](https://github.com/OpenIntelWireless/itlwm/releases)，目测网速提升20%-50%。十分看好这个项目。建议长期关注


##### 2020-12-15

* 热心网友反馈，10.15.7可以正常使用新EFI，所以删除了原EFI。如遇到10.15.7英特尔网卡无法使用的情况。请自行替换AirportItlwm。
保持在OC 0.6.3
* 由于条件限制，如遇到蓝牙或者usb口无法使用的情况，请取消勾选 USBPorts.kext, USBPower.kext。 同时勾选 USBInjectAll.kext 开机后自行定制USB。

##### 2020-12-19

* 更新到OC 0.6.4
* 更新plist修复引导版本识别错误的问题