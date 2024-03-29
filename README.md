# DELL-7472
## 电脑配置

| 规格   | 详细信息                                              |
|------|---------------------------------------------------|
| 电脑型号 | DELL-7472                                         |
| 处理器  | Intel i5-8250U                                    |
| 内存   | DDR4 16GB                                         |
| 硬盘   | 256GB SSD（Replace 三星PM961）                        |
| 集成显卡 | Intel HD620                                       |
| 独立显卡 | GeForce MX150 2G（Disable）                         |
| 声卡   | Realtek ALC256                                    |
| 网卡   | Realtek RTL8111 + DW1820（Replace DW1820A or BCM94360CS2） |


## 正常功能：
1：显卡 （核显正常，独显禁用）  
2：声卡(耳机、蓝牙耳机均正常使用)  
3：hdmi输出  
4：网卡（有线网卡正常，无线网卡无解，换为DW1820A免驱。）  
5：触摸板正常，手势完美，打字和触控无间歇问题。  
6：usb全部正常。  
7：电池电量显示正常。  
8：摄像头正常使用  
9：睡眠正常。  
10：变频正常。  
11：支持原生亮度快捷键。


## 镜像下载
- [MacOS Catalina 10.15.6](https://blog.daliansky.net/macOS-Catalina-10.15.6-19G73-Release-version-with-Clover-5119-original-image-Double-EFI-Version-UEFI-and-MBR.html) |
[MacOS BigSur 11.6.6](https://blog.daliansky.net/macOS-BigSur-11.6.6-20G624-Release-version-with-OC-0.8.0-and-Clover-5142-and-PE-original-image.html) |
  [MacOS Monterey 12.5](https://osx.cx/macos-monterey-12-5-21f79.html)
- 感谢 @黑果小兵 @黑苹果社区


## 说明
- 网卡DW1820A在***MacOS Monterey***无法使用，如果需要强制使用可以在BIOS中禁用WIFI使用，不禁用WIFI有大几率卡LOGO。
- `hackintool`目录下有所需要的工具以及ACPI、BIOS等。

## BIOS设置
* General -> Boot Sequence：勾选所有Boot Sequence选项
* General -> Advanced Boot Options：取消Enable Legacy Option ROMs
* System Configuration -> SATA Operation：勾选AHCI
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
- 2022.09.02 替换网卡为BCM94360CS2，支持Monterey 12.5安装。
- 2022.08.08 优化触摸板体验，使用**VoodooI2C.kext**和**VoodooPS2Controller.kext**解决打字和触控有间歇的问题。删除多余驱动。
- 2022.08.05 升级OC0.8.2，支持MacOS BigSur安装。
- 2022.08.04 更新传感器驱动；使用ssdt屏蔽独显，解决风扇狂转和CPU温度高问题。
- 2022.04.23 升级OC0.6.6，更新驱动文件。
- 2021.04.20 全新EFI
