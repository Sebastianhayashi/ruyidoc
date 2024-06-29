# Hello Ruyi

欢迎来到 [RuyiSDK](https://github.com/ruyisdk) 相关介绍内容，以下是本文相关内容：

> 1. 什么是 RuyiSDK -> 介绍
> 2. 为什么会有 RuyiSDK -> 背景
> 3. RuyiSDK 有什么用 -> 功能
> 4. 我可以在什么设备上运行 -> 支持的设备
> 5. RuyiSDK 的原理是什么 -> RuyiSDK-架构示意图
> 6. 我该从何开始 -> 让我们开始吧！
## 介绍

RuyiSDK 是一个由中科院软件所（ISCAS）所启动的开源项目，该项目旨在为 RISC-V 开发者提供一个便捷、完善的开发环境。其提供了相关最新的硬件信息、软件支持，例如在支持的设备中有提供相关支持硬件情况；软件层面提供了镜像（如 [RevyOS](https://github.com/ruyisdk/revyos)）、工具链、包管理器等。

其最终目标是希望为 RISC-V 开发者提供一个完善、便捷的开发环境，使得 RISC-V 成为主流架构，以及建设并运营一个完善的社区以便开发者交流。最终希望 RuyiSDK 可以走向国际化，为全球的 RISC-V 开发者提供开发的便捷。

## 背景

RISC-V 是第五代精简指令集，由加州伯克利分校所发起的一个开源项目，相比 Cisc 而言更具精简性，指令执行效率更高。开源使其能够更加方便的运用在不同的领域，目前在 IoT、智能家居、芯片设计、操作系统、软件开发等领域都有应用。

而在过往针对 RISC-V 的开发面临的问题在于相关资讯没有统一的平台，使得开发者从最开始的学习、再到开发应用的效率大幅降低，而 RuyiSDK 的出现就是为了解决这些问题。

## 功能

RuyiSDK 分为以下三个部分：
### Ruyi 包管理器

该包管理器是一个在线的软件源，在该包管理器中，我们提供了如下内容：

```
1. 工具链
2. 调试工具
3. 模拟器
4. 运行环境
5. 文档
6. 源码
7. 工具、系统镜像
8. GUI（TODO）
```

### Ruyi IDE

该 IDE 是一个为 RISC-V 架构设计的开发工具箱，开发者可以轻松的通过 Ruyi 包管理器获取，可以对于实际的开发场景对于代码的编写以及调试。
使用包管理器开发者可以获取该工具箱中的编译工具链、调试工具和模拟器，开发者可以使用模拟器或者在 RISC-V 开发板上对自身的程序进行编写以及调试。

### Community

在我们的社区当中，提供了大量的相关技术文章、代码、教程视频，以及我们会举办一定的线下活动获得来自用户的反馈，在线上也会有相应的论坛提供给开发者进行技术交流。

----

RuyiSDK 对 RISC-V 设备的集成和支持主要包括以下几个方面：

1.  RISC-V 开发板镜像相关信息以及下载、安装教程，便于开发者获取相关镜像（换而言之提供一个镜像站），其中涵盖多种操作系统（如基于 Debian 的 RevyOS、openEuler riscv64等）提供给开发者使用。
2.  提供 RISC-V 开发板对应的演示程序、开发资料和相关工具（含适用的编译工具链、模拟器等）的信息维护和下载，方便 RISC-V 开发者快速上手。
3.  在集成开发环境中增加 RISC-V 设备专有向导页面、实现开发环境和运行环境的文件传输、支持在 RISC-V 设备上调试应用程序等。

## 支持的设备

目前 RuyiSDK 支持的设备如下：

| 链接                                                     |
|---------------------------------------------------------|
| [Allwinner Nezha D1](https://d1.docs.aw-ol.com/d1_dev/) |
| [Canaan Kendryte K230](https://www.canaan-creative.com/product/k230/) |
| [Milk-V Duo](https://milkv.io/zh/duo)                   |
| [Milk-V Duo S](https://milkv.io/zh/duo-s)               |
| [Milk-V Mars](https://milkv.io/zh/mars)                 |
| [Milk-V Mars CM](https://milkv.io/zh/mars-cm)           |
| [Milk-V Meles](https://milkv.io/zh/meles)               |
| [Milk-V Pioneer Box](https://milkv.io/zh/pioneer)       |
| [Milk-V Vega](https://milkv.io/zh/vega)                 |
| [SiFive HiFive Unmatched](https://www.sifive.com/boards/hifive-unmatched) |
| [Sipeed Lichee RV](https://wiki.sipeed.com/hardware/en/lichee/RV/RV.html) |
| [Sipeed LicheePi 4A](https://wiki.sipeed.com/hardware/en/lichee/th1520/lpi4a/1_intro.html) |
| [StarFive VisionFive](https://www.starfivetech.com/site/boards) |
| [StarFive VisionFive2](https://www.starfivetech.com/site/boards)          |
> 文档可能更新不及时，查看最新支持的设备请通过指令`ruyi device provision`查询。

## RuyiSDK-架构示意图

![Structure-RuyiSDK.png](./img/Structure-RuyiSDK.png)

## 让我们开始吧！

从 RuyiSDK 开始使用设备！
### 获取并安装OS

开始的第一步：

```bash
$ ruyi device provision
```

该指令会识别硬件信息，并且开始自动执行对应程序为用户自动部署 RISC-V 开发环境，按照引导信息一步步执行即可。
