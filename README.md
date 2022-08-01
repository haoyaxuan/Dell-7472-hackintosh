# DELL-7472
## 电脑配置

| 规格     | 详细信息                                 |
| -------- |--------------------------------------|
| 电脑型号 | DELL-7472                            |
| 处理器   | 英特尔 酷睿 i5-8250U                      |
| 内存     | DDR4 16GB                            |
| 硬盘     | 256GB SSD                            |
| 集成显卡 | 英特尔图形卡 UHD620（无独显 or 禁用独显）           |
| 声卡     | 瑞昱 ALC256                            |
| 网卡     | RealtekRTL8111 + DW1820（已更换 DW1820A） |


## 正常功能：
1：显卡 （核显正常，独显无解）
2：声卡(耳机、蓝牙耳机均正常使用)  
3：hdmi输出  
4：网卡（有线网卡正常，无线网卡无解，换为DW1820A免驱。）  
5：触摸板正常，部分手势可用。  
6：usb全部正常。  
7：电池电量显示正常。  
8：摄像头正常使用  
9：睡眠正常。  
10：变频正常。  
11：支持原生亮度快捷键。


## 镜像下载
- 黑果小兵部落阁 [MacOS Catalina 10.15.6](https://blog.daliansky.net/macOS-Catalina-10.15.6-19G73-Release-version-with-Clover-5119-original-image-Double-EFI-Version-UEFI-and-MBR.html)，感谢 @黑果小兵


## BIOS设置
* General -> Boot Sequence：勾选所有Boot Sequence选项
* General -> Advanced Boot Options：取消Enable Legacy Option ROMs
* System Configuration -> Serial Port：勾选Disabled
* System Configuration -> SSATA Operation：勾选AHCI
* System Configuration -> USB Configuration：勾选全部
* System Configuration -> Audio：勾选全部
* Secure Boot -> Secure Boot Enable：勾选Disable
* Intel Software Guard Extensions -> Intel SGX Enable：勾选Disable


## BIOS设置 For 隐项
* 将EFI-shell文件夹复制到U盘，改名为EFI，然后从U盘启动
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0x795 0x02***
* 禁用 CFG lock:
  ***setup_var 0x4ed 0x00***


## 更新日志
- 2022.04.23 升级OC0.6.6，更新驱动文件。
- 2021.04.20 全新EFI

## 联系方式
QQ：3129598

## 觉得资源还不错的可以打赏一下
| 微信                                                         | 支付宝                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![wechatpay](https://github.com/haoyaxuan/dell7472/blob/master/images/wechatpay.png) | ![alipay](https://github.com/haoyaxuan/dell7472/blob/master/images/alipay.png) |

