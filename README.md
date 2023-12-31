# MSI_B660M_MASTER_MAX_12490F_RX6600
基于opencore的苹果引导文件

硬件说明：

| 类型 |               型号                |
| :--: | :-------------------------------: |
| 主板 |     MSI_B660M_MASTER_MAX_WIFI     |
| 内存 | 光威ddr4 3600MHZ  8G x 4（共32G） |
| CPU  |             I5-12490F             |
| GPU  |          技嘉 RX6600  8G          |
| 网卡  |        苹果拆机网卡 BCM94360CD CS2 加转接卡        |

驱动情况：

1、cpu正常睿频，gpu免驱加上参数优化仿冒W6600X 性能提升。由于使用的苹果网卡，随航、隔空投送，鼠标蓝牙共享等均可正常使用。

2、对显卡的固件进行了修改调整的风扇启动的规则，避免MAC环境下温度高的问题

3、由于技嘉显卡的问题，在黑苹果下移动鼠标会有轻微的电流声，可以通过降低显卡频率避免，但是会降低性能因此未做调整。调整方式参考（[解决/抑制黑苹果系统显卡电流声/滋滋声、啸叫噪音问题 - 知乎 (zhihu.com)](https://zhuanlan.zhihu.com/p/629023610)）

优化：
1、屏蔽系统更新，避免出现自动更新系统导致的无法启动问题，在host中添加以下内容
## Mac Software Update

127.0.0.1 swdist.apple.com

127.0.0.1 swscan.apple.com

127.0.0.1 swcdn.apple.com

127.0.0.1 gdmf.apple.com

127.0.0.1 xp.apple.com

127.0.0.1 mesu.apple.com

127.0.0.1 updates.cdn-apple.com

建议使用switch host([下载地址](https://github.com/oldj/SwitchHosts/releases))软件来实现host修改，方便下次启动更新
