# ROG 玩家国度 幻15 2020（GU502LV）黑苹果 EFI配置文件
# ROG Zephyrus M15 GU502LV-Hackintosh

## 一、硬件配置

|     |     |
| --- | --- |
| **配置** | **名称** |
| CPU | i7-10875h |
| 屏幕  | 4K  |
| 显卡  | Graphics UHD 630 + RTX 2060 |
| 硬盘  | WD sn730 1T+500G |
| 内存  | DDR4 16GB*2 |
| 声卡  | ALC294 |
| 有线网卡 | Realtek RTL8168 |
| 无线网卡&蓝牙 | AX201^①^ |
 
 <font size=1.5>① 意味着不能通过更换网卡来实现隔空投送等功能，但可将无线网卡接在m2口上，此法尚未测试可行性，无线网卡的驱动效果见下文</font >
## 二、EFI信息

|     |     |
| --- | --- |
| **环境** | **版本** |
| OpenCore | 0.8.1 |
| MacOS | Monterey 12.4 |
## 三、使用体验
### 已驱动
- 核显完美
- 网卡：有线完美
- 电池管理完美
- 触摸板完美
- CPU、温度传感器正常
- CPU变频正常
- USB 3.0正常
- 声音调节快捷键正常
### 未驱动
- 独显RTX2060未驱动，已屏蔽
- HDMI接口，接在独显上，目前无解，可采用USB转HDMI，已测试雷电接口转HDMI不行
- 隔空投送、通用控制不能用，接力正常
### 已发现的问题
- 耳机孔无声BUG，已找到[解决方案](https://www.jianshu.com/p/19e5c321a842)。具体实现过程：使用最新版AppleALC，节点设为99，下载(ALCPlugFix)[black-dragon74/ALCPlugFix-Swift],使用解决方案链接中最底下的配置文件即可。在此感谢果农大佬
- 连接手机热点有BUG，经常连不上
- 蓝牙连手机BUG，连上立马断开，已测试Big Sur不存在此BUG

EFI[下载](https://github.com/xiaoheiwu123/ROG-Zephyrus-M15-GU502LV-Hackintosh/releases/tag/EFI)，自己更换三码

最后附上[厚切大佬的教程](https://zhuanlan.zhihu.com/p/347899851)
