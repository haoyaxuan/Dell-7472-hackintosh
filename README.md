# DELL-7472
## 电脑配置

| 规格     | 详细信息                                 |
| -------- |--------------------------------------|
| 电脑型号 | DELL-7472                            |
| 处理器   | 英特尔 酷睿 i5-8250U                   |
| 内存     | DDR4 16GB                            |
| 硬盘     | 256GB SSD                            |
| 集成显卡 | 英特尔图形卡 UHD620（无独显）                   |
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
* 修改BIOS - 关闭『安全引导』
* 修改BIOS - 开启『AHCI』
* 修改BIOS - 关闭『Enable Legacy Option ROMs』


## BIOS设置 For 隐项
* 将EFI-shell文件夹复制到U盘，改名为EFI，然后从U盘启动
* 设置 Pre-Allocated DVMT 为 64M:
  ***setup_var 0x795 0x02***
* 禁用 CFG lock:
  ***setup_var 0x4ed 0x00***


## 耳麦驱动
1：系统安装好后，解压『ALC256.zip』得到驱动文件。  
2：执行『 sudo mount -uw / 』命令将系统根目录改为读写，如果不改，重建缓存会失效。
3：将文件中的『CodecCommander.kext』放入到『/Library/Extensions/』目录，并重建缓存。  
4：将文件中的 SSDT-ALC256.aml 放到EFI的ACPI目录中，并修改config.plist文件使其生效。  
注：切记不要插着耳机安装，插着耳机安装会导致无法开机，需要断电5分钟后才可以开机。


## 更新日志
- 2022.04.23 升级OC0.6.6，更新驱动文件。
- 2021.04.20 全新EFI

## 联系方式
QQ：3129598

## 觉得资源还不错的可以打赏一下
| 微信                                                         | 支付宝                                                       |
| ------------------------------------------------------------ | ------------------------------------------------------------ |
| ![wechatpay](https://github.com/haoyaxuan/dell7472/blob/master/images/wechatpay.png) | ![alipay](https://github.com/haoyaxuan/dell7472/blob/master/images/alipay.png) |

