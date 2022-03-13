# 从零开始的UEFI裸机编程 中文版示例代码

同人志《从零开始的UEFI裸机编程》中文版示例代码

本体可以在可以在 [>这里<](https://kagurazakakotori.github.io/ubmp-cn) 在线阅读，请配合使用

如果您发现示例代码中存在问题，欢迎在 [Issues](https://github.com/kagurazakakotori/ubmp-cn-code/issues) 中提出


## 目录结构

* `baremetal`: 裸机编程的例子的目录
* `gnuefi`: 使用gnu-efi的例子的目录
* `drivers`: UEFI驱动程序目录
  * `UsbMouseDxe.efi`: USB鼠标驱动 (提取自 Clover EFI bootloader r5070)
* `linux`: Linux相关例子所用内容目录

## 环境要求

* amd64(x86_64)平台
* GNU make
* GCC
* MinGW-w64 GCC交叉编译器
* QEMU
* OVMF
* gnu-efi (版本 >= 3.0.14)
* dos2unix
* imagemagick

最新版的 gnu-efi 可以在 [https://gitlab.com/ncroxon/gnu-efi](https://gitlab.com/ncroxon/gnu-efi) 下载

在 Ubuntu 20.04 上安装上述工具的代码如下:

```shell
sudo apt install build-essential gcc-mingw-w64-x86-64 qemu-system-x86 ovmf gnu-efi dos2unix imagemagick
```

## Makefile 规则

* `make`: 编译.efi可执行文件
* `make run`: 编译、构建文件系统并运行
* `make clean`: 删除中间文件和可执行文件

## 关于 Linux 内核

请在编译完Linux内核后将 `arch/x86/boot/bzImage` 文件复制到 `linux/kernel` 目录下
