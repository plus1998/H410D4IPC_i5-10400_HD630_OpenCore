
## EFI
OpenCore: 0.6.2
macOS version: 10.15.7

## 硬件配置

| 配件   | 型号 | 说明 |
|------|----|----|
| 主板   |  昂达H410D4 IPC  |  DP * 1, HDMI * 1  |
| CPU  |  i5-10400  |    |
| 内存   |  酷兽ddr4 2666（笔记本）  |  16G * 2  |
| 显卡   |  Intel UHD Graphics 630  |  未测试4k以及双显示器  |
| SSD  |  西数SN550 500G  |  NVME  |
| 声卡   |  ALC662  |  注入alcid=5  |
| 有线网卡 |  RTL8111  |    |
| 无线网卡 |  AC3168  |  itlwm驱动  |
| 电源 |  DC电源  |  150w  |
| 机箱 |  酷鱼MG PLUS DC-ITX  |    |

## 说明
* 已做主板定制化，不建议不同型号主板使用
* 蓝牙正常工作，WIFI能满足个人日常使用，点击查看[英特尔网卡支持列表](https://docs.oiw.workers.dev/itlwm/Compat.html#gen-1)
* 目测休眠正常

## 已知问题
* 100兆电信带宽环境下无线网卡带宽测试30Mbps左右
* AirDrop不可用


 