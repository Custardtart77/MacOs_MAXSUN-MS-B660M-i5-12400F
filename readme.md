# 铭瑄MAXSUN MS-挑战者B660M + Inter i5-12400f
[github链接](https://github.com/Custardtart77/MacOs_MAXSUN-MS-B660M-i5-12400F)

## 配置

| 配置 | 型号 |
| --- | --- |
| CPU | [Intel i5 12400F] |
| 主板 | [MAXSUN MS-挑战者B660M] |
| 显卡 | [盈通Rx580-8G 2304sp]|
| 内存 | 光威DDR4 3200 16Gx2 |
| 网卡 | BCM943602CS 3天线 |
| 硬盘 | [大华 SSD 500GB+1TB]|
| OC版本 | 0.8.6 |
| macOS | macOS Ventura 13.0.1|
| 机型 | MacPro7,1 |

## 更新
### 2022.11.20
更改三码，添加睿频开关


### 2022.11.19
上传制作版的初版的EFI

#### 优化过程遇到的问题：
* USB定制，[参考国光的教程](https://apple.sqlsec.com/6-%E5%AE%9E%E7%94%A8%E5%A7%BF%E5%8A%BF/6-1/)
注意：USB定制完后进入mac再使用Hackintool软件进行修正，特别是USB蓝牙，一定要将蓝牙对应的USB改成内建模式，否则无法正常睡眠，可以参考[B站视频](https://www.bilibili.com/video/BV1CQ4y1M7oZ/?spm_id_from=333.880.my_history.page.click&vd_source=2668bb09f63b9dd046418142c8a39582)

* OC启动windows出现异常。解决办法：在config.plist中重新定制windows的UEFI引导，参照[教程](https://www.bilibili.com/video/BV1gY411h7hH/?spm_id_from=333.880.my_history.page.click&vd_source=2668bb09f63b9dd046418142c8a39582)

* 解决字体显示小以及开启HIDPI的方法，直接上[github](https://github.com/xzhih/one-key-hidpi)

* mac系统下风扇不转，读取AMD显卡bios参数，实现在oc中实现显卡参数注入，参考[B站视频](https://www.bilibili.com/video/BV1ZT4y1v7Ac/?spm_id_from=333.880.my_history.page.click&vd_source=2668bb09f63b9dd046418142c8a39582)


## 主板设置(有些主板没有相关的设置也没关系)
### 开启 - Enable
| 选项 | 备注 |
| --- | --- |
| VT-x | [VT-x	也叫 Intel® Virtualization Technology是 CPU 硬件虚拟化技术] |
| Above 4G decoding | [4G 以上解码] |
| Hyper-Threading | 超线程技术|
| Execute Disable Bit | Intel 新一代处理器的功能，主要做病毒防护使用 |
| DVMT Pre-Allocated: 64MB | 分配给DVMT所需内存，4k 分辨率笔记本建议设置 128MB 及其以上 |
| EHCI/XHCI Hand-off | EHCI/XHCI 切换|
| OS type: Windows 8.1/10/11 UEFI Mode| 操作系统类型 |
| SATA Mode: AHCI | 硬盘启动模式|


### 关闭 - Disable 

| 选项 | 备注 |
| --- | ---|
| Fast Boot |	快速启动 |
| Secure Boot |	安全启动 |
| Serial/COM Port |	串行通讯端口 |
| Parallel Port |	并行端口|
| CSM	Compatibility Support Module | 兼容容性支持模块 |
| Thunderbolt |	雷电，安装的时候容易引发一些玄学问题，建议关掉省事儿 |
| Intel SGX |	也叫做 Software Guard Extensions，是一种基于 CPU 硬件的安全保障机制 |
| Intel Platform Trust |	英特尔平台可信技术，主要用于密钥管理和安全认证服务 |
| CFG Lock |	MSR 0xE2 写保护，建议关闭 |
| VT-d |	也叫 Intel® Virtualization Technology for Directed I/O (VT-d) |

## Links

- [OC Auxiliary Tools](https://github.com/ic005k/QtOpenCoreConfig)
- [ProperTree](https://github.com/corpnewt/ProperTree)
- [Hackintool](https://github.com/headkaze/Hackintool)
- [OpenCore](https://dortania.github.io/OpenCore-Install-Guide/prerequisites.html)
- [OpenCorePkg](https://github.com/acidanthera/OpenCorePkg)
- https://blog.daliansky.net/
- https://apple.sqlsec.com/
- https://space.bilibili.com/16323318/channel/collectiondetail?sid=296068
- https://bbs.pcbeta.com/forum.php?gid=86
- https://www.tonymacx86.com/
- https://github.com/daliansky/OC-little


## 镜像来源
[>>黑果小兵<<](https://github.com/daliansky/Hackintosh)