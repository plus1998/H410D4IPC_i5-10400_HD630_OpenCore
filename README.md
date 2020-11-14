
# EFI
OpenCore: ~~0.6.2~~ 升级到0.6.3  
macOS version: Catalina 10.15.7 / Big sur 11.0.1

## 硬件配置

| 配件   | 型号 | 说明 |
|------|----|----|
| 主板   |  昂达H410D4 IPC  |  USB3 * 1, USB2 * 2, Tpye-C * 1 |
| CPU  |  i5-10400  |  6c12t, L3 12M  |
| 内存   |  酷兽ddr4 2666（笔记本）  |  16G * 2  |
| 显卡   |  Intel UHD Graphics 630  |  DP * 1, HDMI * 1  |
| SSD  |  西数SN550 500G  |  NVME  |
| 声卡   |  ALC662  |  注入alcid=5  |
| 有线网卡 |  RTL8111  |  千兆网卡  |
| 无线网卡 |  AC3168  |  itlwm驱动  |
| 电源 |  DC电源  |  150w  |
| 机箱 |  酷鱼MG PLUS DC-ITX  |    |


## Catalina 说明
* 已做主板定制化，不建议不同型号主板使用
* 蓝牙正常工作，WIFI能满足个人日常使用，点击查看[英特尔网卡支持列表](https://docs.oiw.workers.dev/itlwm/Compat.html#gen-1)
* 目测休眠正常

# 关于Big Sur

*11.0.1已经发布了，原来的EFI可以升级，升级之后可以开机，但是画面没有显示。*

` 我创建了一个新的EFI用于支持Big Sur引导( EFI在BigSur文件夹中 ) `

**由于测试条件有限，我不保证Big Sur的EFI可以在Catalina上正常引导, 也不保证Big Sur的EFI可以顺利升级**
**建议<font color="#dd0000">使用原EFI在线升级后</font>到windows, linux或者PE下替换 EFI。也欢迎测试成功的在issue中反馈（失败就不用反馈了）**

## Big sur 说明

*基本上与Catalina使用一致*

* 已做USB定制: TypeC, USB3正常
* 蓝牙正常工作，WIFI能满足个人日常使用



## 已知问题
* ~~100兆电信带宽环境下无线网卡带宽测试30Mbps左右, 50兆也可以跑到26Mbps~~ WIFI不满速
* AirDrop不可用

## 关于英特尔网卡问题

*有需要的可以更换博通网卡（博通网卡驱动方法自己找）,移除以下内核*
* AirportItlwm.kext
* IntelBluetoothFirmware.kext
* IntelBluetoothInjector.kext
