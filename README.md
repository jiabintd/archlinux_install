# ArchLinux_install
只需一个简单的 bash 脚本向导，即可在官方 Arch Linux 安装介质上启动后安装 Arch Linux。
使用此脚本，您可以使用两个简单的终端命令安装 Arch Linux。
此向导用于安装最少的软件包（Base、引导加载程序和可选的 archdi）。
在此向导结束时，您可以安装或启动[archdi](https://github.com/MatMoul/archdi) (Arch Linux Desktop Install) 来安装和配置桌面软件包。

您可以观看我的视频，了解如何在此处使用它。
[here](https://www.youtube.com/playlist?list=PLytHgIKLV1caHlCrcTSkm5OF2WSVI1_Sq).

## 如何使用
首先, 使用具有可引导设备的 [Arch Linux 映像](https://www.archlinux.org/download/) 进行引导。[bootable device](https://wiki.archlinux.org/index.php/USB_flash_installation_media).

然后确保您在Arch iso上有互联网连接。如果你使用的是无线链接[`iwctl`](https://wiki.archlinux.org/index.php/Iwd#iwctl) 命令可能对您有用，您还可以从 Arch Linux 指南中阅读 [网络配置](https://wiki.archlinux.org/index.php/Network_configuration) 以获取更详细的说明。

然后从命令行下载脚本：
```bash
    curl -LO archfi.sf.net/archfi
```
如果 SourceForge 已关闭，请改用以下命令：
```bash
    curl -LO matmoul.github.io/archfi
```
最后，启动脚本：
```bash
    sh archfi
```
然后按照屏幕上的说明完成操作。
如果您需要额外的帮助，请访问提供的视频播放列表并按照我的示例进行操作。

## 更多自定义安装
```bash
    sh archfi -cpl {URL of your custom package list}
```
可以在示例文件夹中找到示例自定义包列表文件。

## 对于开发人员

您可以使用以下命令测试脚本：
```bash
    sh archfi -t {githubusername} {branchname}
```
例：
```bash
    sh archfi -t matmoul master
```
