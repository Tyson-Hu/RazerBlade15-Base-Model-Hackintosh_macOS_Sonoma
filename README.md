<img align="right" src="https://github.com/acidanthera/OpenCorePkg/blob/master/Docs/Logos/OpenCore_with_text_Small.png" alt="OpenCore 0.6.1" width="225">

# Razer Blade 15 Base Hackintosh
![GitHub issues](https://img.shields.io/github/issues/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur)
![GitHub](https://img.shields.io/github/license/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur)
![GitHub last commit](https://img.shields.io/github/last-commit/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur)

<img align="right" src="https://www.tonymacx86.com/data/attachments/438/438790-8ae35cbb5010a132a8dc82015df0eb32.jpg" alt="Critter" width="245">

特别鸣谢：   
- [Dortania](https://dortania.github.io) - 黑苹果安装向导（OpenCore）
- [Acidanthera](https://github.com/acidanthera) - OpenCore以及核心kext全家桶
- [RehabMan](https://github.com/RehabMan) - ACPI的关键修补
- [doanhmaple](https://github.com/doanhmaple) - ACPI电池修补🔋 & 雷电三修补⚡️
- [EmeryWan](https://github.com/EmeryWan) - BIOS修改 & 系统设置

**支持macOS：10.15.1 ～ 11.0 beta6 ｜ [变更目录](https://github.com/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur/blob/master/Changelog.md)**     
**暂无bug，期待你们的反馈<3**    

<img align="left" src="https://github.com/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur/blob/master/image/daliansky.png" alt="名言" width="220">

⚠️：本人不会为你操作过程中所出现的任何错误负责！   
 
![OpenCore Version](https://img.shields.io/badge/OpenCore-0.6.2-ff69b4)
![GitHub release (latest by date)](https://img.shields.io/github/v/release/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur)
![GitHub release (latest by date including pre-releases)](https://img.shields.io/github/v/release/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur?include_prereleases)
![GitHub All Releases](https://img.shields.io/github/downloads/Mother-FKR/RazerBlade15-Base-Model-Hackintosh_macOS_Big_Sur/total)

EFI支持以下这些安装：1.OTA 2.完整安装包 3.U盘安装 4.虚拟机     
**建议从左往右尝试**         
**最后再尝试我后面写的关于虚拟机安装教程！**   

稳定版采用 `OpenCore 0.6.1`，测试版EFI采用 `OpenCore 0.6.2`。

<img align="right" src="https://static.dribbble.com/users/3460/screenshots/14117702/media/7c3c5728cec212f97ece1b0c5bf3f08c.png" alt="Peel1 by Ryan Putnam" width="245">

#### 关于这篇文章 & 交流
由于我需要同时兼顾我的大学课程和博客，在后续的时间我将降低我的更新频率，学业为重希望大家理解，不过我也向大伙们保证不会停更的（日更我肯定是肝不动了，毕竟👴每周都要做Lab Report，因此我尽量保持周更。） 

如果你安装的时候遇到一些困难或者有什么不懂的地方，可以尝试找个QQ群进行交流？我在这个群里➡️ "[OpenCore技术交流群](https://shang.qq.com/wpa/qunwpa?idkey=665ed002721454d2e811535020261a04b0aae2fa3b6a2ffde5778a852f892178)"，大神众多非OC适配者慎入.

## 文件说明 / File Description  
- **CLOVER**
  - `CLOVER`引导`EFI`，版本`5103`，对应系统 `macOS 10.15.4`。由于我已经转入 `OC` 引导，因此不会再进行更新，放在这里只是为了给那些需要使用 `5120` 的人作为参考
  - EFI with `CLOVER`，`v5103`, for `macOS 10.15.4`. I won't update it anymore,because of I move to `OC`. Just a reference for guys who want to use `CLOVER v5120`.
  - 问题：无问题  / Issue: None

- **EFI beta**  (使用时记得改名为 `EFI`)
  - `OpenCore` 版本的EFI，版本 `0.6.1`，对应系统 `macOS 11`。该版本的EFI更新频率较高（更新比较激进，基本对应最新自编译 `Kext` 和 `OpenCore`）因此很容易出现一些BUG。喜欢尝鲜的可以使用。
  - EFI with `OpenCore` , `v0.6.1`, for `macOS 11`. Update with High Freq (**Lastest `Kext`[Self Compile] & `OpenCore`[From `OpenCore-Factory`]**)which could cause some **ISSUE** that don't expect.
  - **问题：**
    - **包含`EFI`里所有的BUG**
    - **可能会有其他未知BUG**
  - **Issue:**
    - **Contain all BUG in `EFI`**
    - **Might have other unknow BUG**

- **EFI** 
  - `OpenCore` 版本的EFI，版本 `0.6.1`，对应系统 `macOS 11` & `macOS 10.15.6`。较为稳定的EFI，只有在确认稳定后才会进行更新，因此更新频率不是很高。
  - EFI with `OpenCore` , `v0.6.1`, for `macOS 11` & `macOS 10.15.6`. `Stable Version` of EFI, Only update while it's stable to use. Thus not too high freq.
  - **问题：**
    - **睡眠唤醒后时间仍定格在睡眠前（需手动更新时间）** 
    - **无法自动切换音频输出，开机默认耳机输出，变更输出需要手动切换。(无法解决)**
  - **Issue:**
    - **Time Freeze while laptop sleep, That means you have to MANUALLY update the time after sleep.**
    - **Can't switch audio output automatically. You have to MANUALLY switch it(Can't solve)**

- **Tools**
  - 里面包含该教程需要的基本工具（软件）。
  - Include some necessary / basic `tools` for this tutorial

- **Wallpaper**
  - 我备份的壁纸。。。
  - Just `Wallpaper`

- **image**
  - 本教程所包含的图片的缓存，对于你们来说并没有什么用
  - `image caches` for this tutorial, `useless` to your guys.

- **Changelog**
  - 关于Releases上的变更目录。
  - Changelog for releases.


## 写在最前
- 本文的内容主要参考了[EmeryWan](https://github.com/EmeryWan)的文章[“雷蛇灵刃15黑苹果”](https://github.com/EmeryWan/Razer-Blade-15-2018-Base-Hackintosh)作为入门黑苹果的教程（该文章采用了Clover的引导），[Razer Blade 15 Base Model Hackintosh](https://github.com/blade15basehackintosh)的文章["razerbladehackintosh"](https://github.com/blade15basehackintosh/razerbladehackintosh)作为OC（OpenCore）引导转换的参考文档，以及[doanhmaple](https://github.com/doanhmaple)的文章[“Razer-Blade-15-Advanced-2018-Hackintosh”](https://github.com/doanhmaple/Razer-Blade-15-Advanced-2018-Hackintosh)对ACPI的电池修补工作的patch帮助。这里再次感谢他们对安装黑苹果的分享和付出（Big thanks for [EmeryWan](https://github.com/EmeryWan), [Razer Blade 15 Base Model Hackintosh](https://github.com/blade15basehackintosh) and [doanhmaple](https://github.com/doanhmaple)!!!)。如果你还需要更多关于黑苹果安装以及优化的教程，可以前往[黑果小兵的部落阁](https://blog.daliansky.net/)和[Hackintosh黑苹果长期维护机型EFI及安装教程整理](https://github.com/daliansky/Hackintosh)查看，里面有很多杂七杂八的机型配置和安装教程以及一些实用的黑苹果优化。
- 跟很多人一样，我开始接触黑苹果这个领域是因为macOS的流畅与稳定性，对码农更友好的unix内核和好看的系统UI。再者由于新冠疫情的影响，我被迫长时间拘留在家中实在无聊🥱，并且找到了很多相同机型的教程，这大大减少了入门黑苹果的难度。
- 如果你只想寻求稳定的macOS，建议你前往文章开头的那些文章查看（macOS 10.15），**⚠️这里我只会讲解关于macOS 11 的安装⚠️** ，当然如果你希望充分利用你的显卡（例如GTX1060，GTX1070，GTX960，GTX980等20系之前的英伟达显卡[**RTX系列：RTX2060，RTX2060 SUPER，RTX2070，RTX2070Ti，等类似显卡均不可用 🚫** ]），你可以尝试安装macOS 10.13（High Sierra是支持英伟达显卡的最新的版本，在此之后只能运行你的IGPU，也就是英特尔的集成显卡），请自行爬贴查找教程。
- **本文并不会讲解关于OC配置的问题，我相信既然你想升级 macOS Big Sur ，那么你应该具有一定的OC基础知识，再者由于机型的不同大家的OC也都不大一样，这里很难进行细说。如果你真的是新手并且想尝试新系统，那我也不建议你进行操作，首先新系统的bug有很多，它并不是理想的macOS，其次各种驱动和插件对于 macOS Big Sur 都还在测试阶段并不稳定，如果哪里出了问题，一个新手很难去解决。**
- 看到这里如果你真的打算继续安装macOS 11。那么建议你最好更换为博通的网卡进行使用，USB网卡和英特尔网卡驱动在11里仍然存在众多问题，~~现无法在11里运行~~ (USB网卡现在可以使用，但需要关闭SIP)。
- **同机型或者相似机型的同学们可以参考我的efi，当然在你使用我的efi的时候记得更改里面的三码（我忘改了😭），以免造成设备冲突！**

## 基础配置 & 知识
由于许多核心Kext都对CLOVER引导停止了维护，OpenCore作为新力军建议提前 研究 / 制作 引导，以适应未来的场景。

- CLOVER
  - [Razer Blade 15 Base Model (2018) [Clover] [10.15.3 / Catalina]](https://github.com/EmeryWan/Razer-Blade-15-2018-Base-Hackintosh)
  - [Razer Blade 15 Advanced Model (early-2019) [Clover] [10.14 / 10.15]](https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh) [英文 / English]
  - [Razer Blade 15 Avdanced Model (2018) [Clover] [10.13 / High Sierra]](https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh) [英文 / English]
- OpenCore
  - [Razer Blade 15 Base Model (2018) [OpenCore] [10.15.4 / Catalina]](https://github.com/blade15basehackintosh/razerbladehackintosh) [英文 / English]
  - [Razer Blade 15 Advanced Model (2018) [OpenCore] [10.15.5 / Catalina]](https://github.com/doanhmaple/Razer-Blade-15-Advanced-2018-Hackintosh) [英文 / English]
- OpenCore向导
  - [vanilla-laptop-guide](https://dortania.github.io/vanilla-laptop-guide/) [英文 / English]
  - [使用OpenCore引导黑苹果](https://blog.xjn819.com/?p=543)
  - [精解OpenCore](https://blog.daliansky.net/OpenCore-BootLoader.html)
  - [从Clover到OpenCore](https://blog.daliansky.net/From-Clover-To-OpenCore.html)
  - [【持续更新】OpenCore引导-v各种卡及OC引导常见问题解决方案速查表合集](http://imacos.top/2020/03/28/0154/) 
- **其他机型的EFI（不会配的或者想要现成的看这里！）**
  - [Hackintosh黑苹果长期维护机型EFI及安装教程整理](https://github.com/daliansky/Hackintosh)
  
*以上所有的文章均为 搬运 / 转载 如果觉得有用，可以打赏原作者 **（我不是原作者！！！）***

## 目录
- 更新
  - [ macOS Big Sur Beta6 （9/3 更新）](#93-更新)
  - [ macOS Big Sur Beta5 & Public Beta2 （8/19 更新）](#819-更新)
  - [ macOS Big Sur Public Beta (8/13更新)](#813-更新)
  - [ macOS Big Sur Beta4 （8/4 更新）](#84-更新)
  - [ macOS Big Sur Beta3 （7/22 更新）](#722-更新)
  - [ Clover v5120 （7/16 更新）](#716-更新-clover-v5120)
  - [ macOS 10.15.6 （7/15 更新）](#715-更新-非-big-sur--catalina)
  - [ 【黑果小兵】macOS Big Sur Beta 2 Installer for OpenCore and PE双EFI分区原版镜像 （7/11 更新）](#711-更新)
  - [macOS Big Sur Beta2 （7/7 更新）](#77-更新)
- [一些问题](#一些问题)
- [硬件介绍](#1硬件介绍)
- [最终效果](#2最终效果)
- [解锁BIOS](#3解锁bios)
- [安装前的准备](#4安装前的准备)
- [系统安装](#5系统安装)
- [一些优化](#6一些优化)
- [附加：U盘直装](#7附加u盘直装)
- [参考](#8参考)
- [变更目录](#9变更目录)

## 9/3 更新  
时隔数周苹果终于释出了 `macOS Big Sur Beta6`，版本号 `20A5364e`, 正常 `OTA` 更新即可。增量包大小 `4GB` 左右，全量包大小 `12GB` 左右。 从版本号也可以看出 `macOS 11` 已经趋于正式版的路上。   

![11 beta6](image/beta6.png)

注意⚠️： 使用gibmacos下载时请选择 `customer`，`developer` ~~无此版本。~~ 也🉑️。   

如果你在 `OpenCore`开启了 `SecureBoot` 并设置了 `apECID`（不知道怎么设置？同机型直接套用我的EFI即可，非同机型的也可以参考我的config），开机后你会发现 `beta6` 将不会从快照启动。 前提是你拥有完整的安全性，至于如何拥有完整的安全性，你需要下载完整安装包（12GB那个.app文件），并进入recovery进行覆盖安装，后续我会抽出时间来制作教程。。    

![11 beta6 snapshot](image/beta6-snapshot.png)

已知问题：   
`beta3` 修复的bug在 `beta6` 它又回来啦！  
 
![11 beta6 issue](image/beta6-issue.jpg)

可能劝退：第三方kext在重启后将失去作用，官方给出的方法是再次安装（简直丧心病狂。。。）   

![11 beta6 issue](image/beta6-issue2.png)

smb出现问题，介意的请待在 `beta5`  

## 8/19 更新
这次官方推迟了一天发布 `beta5`，版本号 `20a5354i`，正常 `OTA` 更新即可。增量包大小 `7.15GB`，全量包大小 `12.13GB`。目前版本已无什么大的BUG，更多的为UI BUG，可以日常使用。 `Public Beta2` 内容与 `beta5` 一致(版本号也均为 `20A5354i`)，用哪个看你自己了。 

![11 beta5](image/beta5.jpg)

![11 beta5](image/beta5-1.jpeg)

## 8/13 更新
对 `AirportBrcmFixup` 进行了修补， 现在 `DW1560 / Brcm94352z` 在 `Beta4` 和 `Public Beta` 均可正常运行，不会再卡开机boot。    

`Beta4` 与 `Public Beta` 内容一致，只是变更了版本号而已，这里我选择使用 `Public Beta`。   

版本说明：  
`20A5343j` ➡️ `Public Beta`   
`20A5343i` ➡️ `Beta4`

附上截图：   
![11 publicbeta](image/publicbeta1.png)

## 8/4 更新 
苹果官方推出了 macOS Big Sur Beta4，更新过程与之前一致。由于我在 `beta4` 中有许多软件都出现了问题，因此我决定回到 `beta3` 版本继续使用，所以这里并没有放出截图。公测版(Public Beta)与 `beta4` 内容一致，只是更改了版本号。**EFI 现已修复，可以进行 `ota` 升级至 `beta4`**

## 7/22 更新 
苹果官方推出了 macOS Big Sur Beta3，图如下，大小为4.96GB，全量包为12GB多，正常OTA更新即可。

![11 beta3](image/beta3.jpg)

![11 beta3](image/beta3-2.png)

更新完成，附上截图：

![11 beta3](image/beta3-3.png)

这次更新也修复了一些bug，例如菜单栏的时钟得到汉化+修复：

![11 beta3](image/beta3-4.png)

被人疯狂吐槽的电池图标得到更换：

![11 beta3](image/beta3-5.png)

已知问题：   
由于苹果在beta3中更新了SDK，现被识别成 `macOS 11.0` 而非  `macOS 10.16`，因此一些bash无法识别并安装，这里需要注意⚠️ 。

![11 beta3](image/beta3-6.png)

可以看到提示需升级 `CLT`，但我检查过没有新的更新了，因此问题出在SDK中，这需要官方进行适配。

![11 beta3](image/beta3-7.png)

图中可以看到并无检查到更新：

![11 beta3](image/beta3-8.png)

### 关于`CLT`的修复
前往 https://developer.apple.com/download/more/ 登陆苹果账号并下载 `Xcode 12 beta` 和 `Command Line Tools for Xcode 12 beta3`,下载完成后双击安装 `CLT` 即可，`Xcode 12` 需要解压xip文件后拖入应用程序完成安装，**同时删除老版本 `Xcode`**   

![CLT](image/CLT.png)

## 7/16 更新 (`CLOVER v5120`)
`CloverBootloader` 发布了最新版`CLOVER`引导 `v5.0 r5120` ，此次更新从 `OpenCore` 那边搬来了 `OcQuirks.efi` 和 `OpenRuntime.efi` 以实现引导 `Big Sur`。原文如下

>    “This release includes OcQuirks.efi and OpenRuntime.efi copied from OpenCore project.”
>                                                
>  “OcQuirks.plist embedded into config.plist and present in Clover GUI as separate menu to tune settings on the fly.”
> 
> “Kernel patching includes pattern for Big Sur.”

这里附上原文章地址供大家下载 [点击跳跃至 `CloverBootloader`](https://github.com/CloverHackyColor/CloverBootloader/releases/tag/5120)

考虑到还是有不少人不会配置 `OC`，我把自己当时使用的CLOVER放入本文，希望可以对你有所帮助。（`CLOVER` 版本为 `v5103`，对应系统版本为 `10.15.4`）

## 7/15 更新 （"**非 `Big Sur`**" / `Catalina`）
1. 苹果官方推送 `macOS 10.15.6` 正式版（版本号 `19G73` ，日常OTA升级即可，无其他问题。
2. 苹果官方推送 `Safari 14.0` 测试版 [适用于 `macOS 10.15 及更低版本`]，内容与 Big Sur 版本里的 `Safari` 同步。     
   
更新推送图：[10.15.6 beta4 ➡️  10.15.6]

![10.15.6正式版](image/15.6.jpg)

更新完毕： 

![10.15.6正式版](image/15.6-2.jpg)

## 7/11 更新
黑苹果大佬更新了他自己制作的恢复镜像，对于新手来说应该是福音！！！

[【黑果小兵】【微信首发】macOS Big Sur Beta 2 Installer for OpenCore and PE双EFI分区原版镜像](https://blog.daliansky.net/WeChat-First-macOS-Big-Sur-Beta-2-Installer-for-OpenCore-and-PE-dual-EFI-partition-original-image.html)   

这里简略的搬运一些描述 ⬇️    

特点：
- 两个独立的`EFI`引导分区，同时支持 `OpenCore` / `PE` 引导
- 支持 `z300` / `b300` 等部分台式机直接安装
- `PE` 可连接网络，可远程协助，集成 `向日葵` 和 `AnyDesk`

*©️ 搬运自[黑果小兵的部落阁](https://blog.daliansky.net/)，版权为Daliansky所有，侵权立删！©️*

## 7/7 更新
苹果刚发布了macOS BigSur的beta2版本，同样为全量包，大小将近10GB，使用普通的OTA更新即可。（下载可能略慢，如果进度条不动请耐心等待，这并不是卡了）

![beta2](./image/beta2.jpg)

下面为更新完成的样子（感觉就变了个版本号.....）

![info2](./image/info2.png)

从macOS Catalina升级后直接为**beta2**版本，因此并不影响后面的操作。

**7/7 之前：**  
**macOS Catalina ➡️ macOS Big Sur beta1 ➡️ macOS Big Sur beta2**   
**7/7 之后：**   
**macOS Catalina ➡️ macOS Big Sur beta2**   

不确定的可以自己查看自己的**版本号**：
- `20A4299v`  ---beta1
- `20A4300b`  ---beta2

踩过的坑：   
- **安装卡引导的请将你的OC更新到7/6以后的OC版本，~~并把kext里的`VisualSMC`更换为`FakeSMC`~~ (新版 `VirtualSMC` 已解决该问题，v1.1.5+)**
- ~~安装后无电池图标🔋或者电量一直为0%（触摸板可用但是设置里识别不出来的，**别问我为啥这跟触摸板也有关系，我也不知道，反正我是这样做就好了😯**），请将kext里的`SMCBatteryManager`更换为`ACPIBatteryManager`~~ **(新版 `VirtualSMC` 已解决该问题，v1.1.5+)**
- 无需在OC里注入显卡信息，如果显示出现问题可尝试删除`Device`里的显卡注入信息 **（仅限 UHD630，其他型号无视本信息）**

## 一些问题
我也是刚接触黑苹果不久，到我写这篇文章才一个多月？ 还有很多问题是我无法解决的，当然我后面也会努力爬贴查找解决方案，毕竟 `macOS 11` 我不就是这么过来的嘛。如果有哪位大佬知道如何解决可以联系我，感激不尽！

- ~~与10.15的问题一样，睡眠后无法唤醒，开盖就只有黑屏，其他都正常运作~~  (已解决，现在可以直接关盖睡眠💤 )
- ~~无法进入Recovery  （直升无此问题，但这里并不会讲解直升，也许以后会？）~~  (具体解决方案请移步[[6-10修复Recovery无法进入](#6-10修复recovery无法进入)])
- ~~Wi-Fi老断~~  (更新AirportBrcmFixup)
- ~~直升系统导致Safari无法正常运行（过一会就闪退）~~
- ~~开机画屏~~  （显卡注入问题，UHD630 无需再注入显卡id）
- ~~电池无显示 & 电量始终为 0%  （具体解决方案请移步 [[6-3]电池修复](#[6-3]电池不显示) ）~~ [新版 `VirtualSMC` 已修复此问题，v1.1.5+]
- ~~触摸板可用但是设置偏好里找不到触摸板  （具体解决方案请移步 [[6-3]电池修复](#[6-3]电池不显示) ）~~ [新版 `VirtualSMC` 已修复此问题，v1.1.5+]
- ~~`sip` 无法关闭  （需要进入Recovery方可更改，据说直升无此问题）~~ (具体解决方案请移步 [[6-6]关闭 `SIP`](#6-6关闭-sip)
- ~~时间无法更改自定义设置~~ (`beta3` 已修复该错误)
- ~~蓝牙不可用~~ （已通过更换网卡解决）
- ~~USB网卡不可用~~ (`chris1111`现已更新USB网卡对macOS11的支持，**使用时需关闭 `SIP`!!!**)
- ~~状态栏卡顿~~   (具体解决方案请移步 [[6-4]状态栏卡顿](#[6-4]状态栏的卡顿) ）
- **新增：睡眠时，时间会定格在睡眠前的时候，唤醒后需手动同步时间。**
- **目前无解：无限实现自动切换音频输出，需手动进行切换**

    
## [1]硬件介绍
|        部件      |        型号         |                   最终情况                   |
| :----------: | :-----------------: | :------------------------------------------: |
|     CPU      |      Intel Core i7-8750H processor, 6 Cores / 12 Threads, 2.2GHz / 4.1GHz, 9MB Cache       |                     无问题（系统将采用UHD630作为显卡）                   |
|     IGPU     |        Intel UHD 630       |   无问题   |
|     GPU      |  Nvdia 1060 Max-Q   | 除 10.13 High Sierra 安装 WebDriver 外，10.13以上版本皆不可用（建议直接屏蔽掉） |
|      内存    |   16GB dual-channel DDR4-2667MHz, up to 64GB    |       无问题      |
|     硬盘     | 更换为 Sabrent Rocket NVMe 1TB          |                     无问题                     |
|     网卡     |       9560NGW （现已更换为DW1560 / BCM94352Z）             |           无问题（Windows驱动需要自己下载）            |
|    显示器    |        15.6" Full HD 60Hz, 1920 x 1080 IPS      |                无问题（可以在60Hz和48Hz之间切换）                     |
|    摄像头    |       HD webcam (1MP / 720P)              |                     无问题                     |
|    扬声器    |       Realtek ALC256              |                     无问题                     |
|    耳机    |           爱插啥就是啥                          |                     无问题                     |
|    麦克风    |                 鬼晓得啥型号                |                     无问题                     |
|    触控板    |            全玻璃                |             无问题                             |
|  HDMI 接口   |                     |    直通显卡，除安装 High Sierra 外不可用     |
| Mini DP 接口 |                     |    直通显卡，除安装 High Sierra 外不可用     |
|    雷电3     |                     |   被识别成 USB3.1 ？？？（eGPU目前不确定，应该无法使用）  |
|    大小      |       17.8mm x 235mm x 355mm  |    这tm还能变？？？ | 
|    重量       |         2.21 Kg        |    还想变的更轻？别做梦了老铁     | 
|    电池      |    80Wh （好像是，我忘了，反正不耐用...)   |无问题（还能有问题 ？？？）    |
|    电源适配器  |       180W          | 没PD快充，当然你可以自己试试诱骗器    | 

### [1-1]硬件更换 / 硬件升级
**网卡 & 蓝牙** 

| 网卡型号 | 描述 |
| ---: | :--- | 
| ``BCM94352Z (DW-1560)`` | 适配macOS 11，双天线，即装即用（用我EFI的话）。**Windows 10需要安装驱动才可使用！** | 
| ``BCM94360cs2`` | 双天线 + 免驱，但是需要自己另购买转接卡，据说2.4GHz WiFi 与 蓝牙有干扰 | 
| ``BCM94350ZAE(DW-1820a)`` | 黑果小兵推荐的网卡，在macOS 11中已不是免驱卡，需要自己打驱动补丁，并且需要屏蔽针脚，爱折腾的可以上 |
   

**固态硬盘**

| NVMe硬盘  | 4k 支持 | 描述  |
| ---: | :--- |  :--- | 
|  ``Samsung EVO 970 NVMe``  |   否  |  一个性能非常优秀的SSD，当然价格也非常的扎心，我知道买不起是我的问题，但是不支持4k使我劝退 |
|  ``Sabrent Rocket NVMe``  |   是  |   由`stonevil`大佬确认，外网许多评测都对该SSD的性价比表示认可，我也入手了该SSD，顺序读取3500MB/s  |
|  ``WD Black SN750 NVMe``  |   未知  |   没人测试过该SSD对4k的支持，不过性价比不错，性能略逊970  |
|  ``WD Black SN550 NVMe`` |  未知  |  750的低配，蓝盘温度相比黑盘温柔很多，当然性能也略低，性价比不错|
| ``Samsung PM981`` / ``Samsung PM981a``  |  否  |  皆为970系列的OEM版，无保不建议，据说安装系统也有一些问题，唯一的优点也就是便宜了  |

**内存条**[搬运自`stonevil`的帖子]

| 内存条型号 | 内存大小 | 内存频率 | 时序 | 亚马逊链接 | 消息来源 |
| ---: | :--- | :--- | :--- | :--- | :--- |
| ``Ballistix Sport LT 32GB`` | 2x16Gb | 2666 | CL16 | [Amazon](https://www.amazon.com/gp/product/B06XRBS4Y5/ref=ppx_yo_dt_b_asin_title_o03_s00?ie=UTF8&psc=1) | [stonevil](https://www.tonymacx86.com/members/stonevil.254235/) |
| ``Kingston Technology HyperX Impact 32GB`` | 2x16Gb | 2666 | CL15 | [Amazon](https://www.amazon.com/dp/B01NAL3TYY/?coliid=I3Q9P4ZU9V435H&colid=1ZGSQH2G88154&psc=1&ref_=lv_ov_lig_dp_it) | [Razer Blade 15 Advanced RAM upgrade](https://www.reddit.com/r/razer/comments/c1c9wl/razer_blade_15_advanced_ram_upgrade/) |
| ``Samsung 16GB DDR4 PC4-21300``  |  16Gb (需自己买两片) | 2666  |  CL19  | [Amazon](https://www.amazon.com/Samsung-PC4-21300-2666MHZ-SODIMM-laptop/dp/B07F6N8L3S/ref=sr_1_8?crid=1ZAJ4EFZ2FBQY&dchild=1&keywords=samsung+ram+32gb+ddr4&qid=1596330429&sprefix=samsung+ram+32%2Caps%2C158&sr=8-8)  | 自己找的 |

**工具套件**

| 工具 | 链接 |
| ---: | :--- |
| ``iFixIt Pro Tech Toolkit`` | [iFixIt](https://www.ifixit.com/Store/Tools/Pro-Tech-Toolkit/IF145-307?o=4) |

## [2]最终效果
![info](./image/info.png)

## [3]解锁BIOS
### [3-1]Base版 `BIOS` 解锁

| | BIOS版本 |
| ---: | :--- |
| ``System BIOS`` | 1.02 |

 解锁BIOS可以参考EmeryWan的[教程](https://github.com/EmeryWan/Razer-Blade-15-2018-Base-Hackintosh#3-%E8%A7%A3%E9%94%81bios), 这里就不多描述了。macOS BigSur 对BIOS的大致设定与Catalina一致，有条件的可以尝试解锁CFG。（后面有时间的时候我会尝试一步步教你怎么解锁。）    
 ~~**更新：我已上传改好的bios（1.0.2），只可供同机型同版本bios使用！！！**~~
 **此操作具有不可逆的危险，有可能刷坏bios导致无法点亮，请谨慎操作！！！**   
 
### [3-1-1]提取机器现使用的 `BIOS`   
将 `Tools` 里的 `AFUWINGUI` 打开，在信息页面点击底部的 `储存` / `Save` 进行BIOS提取。↓    

![bios](./image/bios-1.png)   

文件名和存放位置按自己喜好，记得住就行。↓
  
![bios](./image/bios-2.png)   

接着打开 `Tools` 里的 `AMIBCP`，左上角菜单栏点击 `File` → `Open` 打开刚刚提取的BIOS文件。↓   

![bios](./image/bios-3.png)   

打开后在左侧导航栏里找到 `  ` → `Setup` → `Chipset`，并将右侧的 `System Agent Configuration` 的 `Acces/Use` 由 `Default` 改为 `USER`。

![bios](./image/bios-4.png)   

![bios](./image/bios-5.png)   

改完显示如下：↓   

![bios](./image/bios-6.png)   

接着进入：
- `Setup`
  - `Advanced`
    - `Power & Performance`

将以下项目权限从 `Default` 修改为 `USER`：
- `Power & Performance`
- `CPU - Power Management Control`
- `Intel(R) Speed Shift Technology`

![bios](./image/bios-7.png)  

最后进入：
- `Setup`
  - `Advanced`
    - `Power & Performance`
      - `View/Configure CPU Lock Configuration`

将以下项目权限从 `Default` 修改为 `USER`：
- `CFG Lock`
- `Overclocking Lock`

![bios](./image/bios-8.png)   

打开左上角菜单栏 `File` → `Save As...`，将修改好的BIOS文件保存到你记得住的地方，名字也是一样。保存完毕后即可关闭 `AMIBCP`。

![bios](./image/bios-9.png) 

回到 `AFUWINGUI`，点击底部的按钮 `开启` / `Open` 来读取刚才修改保存好的BIOS文件。  

![bios](./image/bios-10.png) 

**刷入前请尽可能关闭所有程序(包括杀毒软件)，以防止刷入BIOS过程被中断！！！**  
读取完毕后点击底部按钮 `刷新` / `Flash` 即可开始刷入修改好的BIOS。

![bios](./image/bios-11.png) 

刷入中途可能出现卡顿，假死等状况(反正我是没遇到)请不要关闭软件或关闭电脑以免造成不可逆的损失！

### [3-2]Advanced版 BIOS解锁
由于我使用的并不是Advanced版本，所以我无法提供具体的图文教程，你们可以参考stonevil大佬的帖子[Razer_Blade_Advanced_early_2019_Hackintosh](https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh) 我Base版修改也是基于他的文章，这里再次感谢stonevil！！！
   
**此操作具有不可逆的危险，有可能刷坏bios导致无法点亮，请谨慎操作！！！**

## [4]安装前的准备
### [4-1]BIOS设置

- `Advanced`
  - `Power & Performance`
    - `CPU - Power Management Control`
      - `CPU Lock Configuration`
        - `CFG Lock` 设置成 `Disabled`
        - `Overclocking Lock` 设置成 `Disabled`
  - `Thunderbolt(TM) Configuration`
    - `Security Level` 设置成 `No Security`

- `Chipset`
  - `System Agent (SA) Configuration`
    - `Graphics Configuration`
      - `DVMT Pre-Allocated`  设置成 `64`
      - `DVMT Total Gfx Mem`  设置成 `MAX`

- `Security`
  -  `Secure Boot` 设置成 `Disabled`

- `Boot`
  - `Fast Boot` 设置成 `Disabled`

  - `CSM Configuration`
    - `CSM Support` 设置成 `Disabled`

### [4-2]软件下载
- **macOS下**
  - 下载好的macOS Big Sur 安装app
  - 一个可以正常工作的 macOS
  - [VMWare Fusion](https://www.vmware.com/products/fusion.html) （虚拟机软件,普通版或pro版都可以）
  - [Paragon VMDK Mounter](http://dl.paragon-software.com/free/VMDK_MOUNTER_2014.dmg) （挂载虚拟机的软件）
  - OpenCore 0.6.0 自编译 （可以直接去下载 Williambj1 每天更新编译好的OC[（点击前往Opencore-Factory）](https://github.com/williambj1/OpenCore-Factory/releases), 也可以自行编译官方的源码[（点击前往OpenCorePkg）](https://github.com/acidanthera/OpenCorePkg)。
- **Windows下**
  - 一个可以正常工作的 Windows （我相信在坐的各位都有吧🤔）
  - 一个可以编辑代码的软件
    - Sublime Text，Visual Studio Code 等等
  - VMWare WorkStation Pro （注意这里必须是pro版本⚠️）
  - Unlocker 302

## [5]系统安装
*安装过程基于远景论坛的大佬Bat.bat的帖子[「教程」简单扯扯用 VMWare 在实体机上装 Big Sur](http://bbs.pcbeta.com/forum.php?mod=viewthread&tid=1862049&highlight=big%2Bsur)，侵权立删*

### 以下步骤均在macOS上执行
首先在 macOS 中先分一个新的 APFS 容器。**⚠️注意，这里指的一个独立的新容器，建议分60G 以上，越大越好**。这个新的容器就是你要安装系统的磁盘，分完请记住该容量的大小，后面会用到

![disk1](./image/disk1.jpg)

打开VMWare Fusion  
用 VMWare Fusion 新建一个自定义虚拟机

![vm1](./image/creatCostom.png)

系统随便选一个苹果系统就行，我这里选的`10.15`。

![vm2](./image/creatCostom2.png)

点击`继续`

![vm3](./image/creatCostom3.png)

点击`自定设置`

![vm4](./image/creatCostom4.png)

点击`继续`，**这里请记住虚拟机存放的位置，后面会用到。**

![vm5](./image/creatCostom5.png)

点击`处理器与内存`

![vm6](./image/creatCostom6.png)

拖动小标到8G大小，这里调整内存的主要原因是怕安装的时候卡住。。。

![vm7](./image/creatCostom7.png)

设置完左上角点击关闭即可。

接着用 Paragon VMDK Mounter 打开新建的虚拟机，挂载刚创建的分区。**（我相信你们安装VMDk的时候都会卡在激活页面，这里给你们提供了一些有用的帮助：VMDK-MOUNTER-2014-434979472，51537-43450-1B2D9-8213A，怎么填就不用我说了吧，傻子都会😊）**

![vmdk1](./image/vmdk1.png)

点击`Attach Selected`。这里由于我是在macOS 11 上截的图，因此出现了“⚠️”，10.15不会出现这个问题

![vmdk2](./image/vmdk2.png)

如果你出现了此问题，并显示以下窗口：

![vdm1](./image/vdm1.jpg)

请前往`系统偏好设置` ➡️ `安全性与隐私` ➡️ `通用`，解除左下角的锁定然后允许操作即可

![vdm2](./image/vdm2.jpg)

打开`磁盘工具`，将挂载上的 VMDK （显示为外置磁盘）格式化成 HFS（macOS扩展（日志式）），名字就叫 `Big Sur Installer`。

![disk2](./image/disk2.jpg)

**备注：抹盘应选择红框下方的子磁盘，这里标错了很抱歉**

完成格式化后关闭磁盘工具，用如下命令将 Big Sur 安装程序写入 VMDK磁盘。   
```
sudo /Applications/Install\ macOS\ Big\ Sur\ Beta.app/Contents/Resources/createinstallmedia --volume /Volumes/Big\ Sur\ Installer  
```
备注：这段口令只适用与跟我文件存放相同位置的人，你可以自己拖动安装包和磁盘进入终端（拖进）以对齐文件位置。输入正确后终端询问你是否继续，打 `y` 即可。

![code](./image/code.jpg)

进入磁盘工具卸载VMDK分区，然后打开虚拟机，如果能进安装界面，直接点关机。   

~~打开 OC 的 `config.plist`，使用`OCC`，`Xcode`或者`PaperTree`都行，在`NVRAM`里的 `7C436110-AB2A-4BBB-A880-FE41995C9F82` 下 `Add` 添加 `booter-fileset-basesystem` 和 `booter-fileset-kernel`，类型为 `Data`，值为 `<00>` (OCC里填`00`即可)，`Block` 加不加无所谓，毕竟我们不需要刷新这个变量。~~ 

~~这里我以`OCC`为例，其他工具同理。~~

**(新版 `OpenCore` 已不需要此步骤，请略过！)**

![config](./image/config.png)

将你制作好的安装盘虚拟机拷贝到`nas`或者`exfat`格式的磁盘中作为中介，至此在macOS上的操作就结束了🔚。

### 以下步骤均在Window下执行
首先把刚才创建的虚拟机转进 Windows，在上面👆操作的最后一步里你用什么存的就从那里转移出来（我咋这么多废话😯）

解锁下载好的 `VMWare Workstation Pro` （作为一个🇨🇳人，你还不会这种最基础的东西？百度一堆好吧👌）

导入刚才转移过来的虚拟机（双击vmx文件就行。。。）

用 `Sublime Text`，`Visual Studio Code` 或其他杂七杂八能用的工具打开虚拟机的 `vmx` 文件，该改的该，该加的加

![vmp1](./image/vmp1.png)

**下面的是我自己随便生成的，不要拿来登陆⚠️**

```
board-id.reflectHost = "TRUE" 
board-id = "Mac-937A206F2EE63C01"
hw.model.reflectHost = "FALSE"
hw.model = "MacBookPro15,1"
serialNumber.reflectHost = "FALSE"
serialNumber = "D25XVQYDKGYG"
smbios.reflectHost = "FALSE"
```
备注：第一行的参数应该文件里已经包含了，可以不用再添加一遍。参数顺序无所谓，放哪里都行。(看图⬇️)

![vmp2](./image/vmp2.png)

**进入 `任务管理器` ，关掉所有关于 `VM` 的进程！**
  
接着运行你下载好的 `Unblocker 302`，(右键管理员运行 `win-install`，注意必须是以管理员运行⚠️）**如果不运行的话你会发现后面打开虚拟机的时候一直重启（没错，无限重启，贼恶心🤮）**

![unlocker302](./image/unlocker.png)

接着进入`VMWare Workstation Pro` ➡️ 点击 `编辑虚拟机设置`

![vmp3](./image/vmp3.png)

点击 `添加`

![vmp4](./image/vmp4.png)

点击 `硬盘` ➡️ 点击 `下一步`

![vmp5](./image/vmp5.png)

点击 `SATA` ➡️ 点击 `下一步`

![vmp6](./image/vmp6.png)

点击 `使用物理磁盘` ➡️ 点击 `下一步`

![vmp7](./image/vmp7.png)

点击 `设备` 角标 选择 你自己要安装的磁盘分区（**开头叫你分的那个APFS容器**）所对应的磁盘，然后选择 `使用单个分区` ➡️ 点击 `下一步` **(忘了是哪个盘？我来帮你想想，找到了！是这一步分的盘！[点我传送](#以下步骤均在macos上执行))**

![vmp8](./image/vmp8.png)

点击在文章开头创建的 `APFS` 容器 (**请根据分区大小判断⚠️**)  ➡️ 点击 `下一步`

![vmp9](./image/vmp9.png)

点击 `完成`

![vmp10](./image/vmp10.png)

到这应该已经成功添加物理安装磁盘，我们现在可以在设备列表里看到这个刚刚添加的磁盘，确认无误后点击 `确定` 即可

![vmp11](./image/vmp11.png)

虚拟机开机，直接进安装程序安装，无需再抹盘，然后各种点，装机总会吧.....   装完到选择语言的时候就可以关掉虚拟机了

到此，虚拟机安装就正式结束了。现在你可以重启电脑💻，然后用 OC 开机，继续刚才的激活向导，设置完就可以吃螃蟹了🦀️

**恭喜你，现在已经完成了macOS Big Sur 的系统安装🎉**

## [6]一些优化
### [6-1] 打开TRIM
如果你将系统装在了固态硬盘上，应开启TRIM。这样可以防止系统对硬盘进行多次擦写从而确保硬盘寿命。（什么？你问我机械硬盘要开吗？反正我是开了）

进入终端，填入以下指令：

```
sudo trimforce enable
```

完成后系统会要求你重启

### [6-2]洗白序列号 / 三码
自行进入OCC打开 `config.plist` ,在 `PlatformInfo` 里的 `Generic` 生成三码即可

![occ](./image/occ.jpg)

**注意，如果你打算用 OpenCore 引导 Windows，请将 `System UUID` 一栏修改成你BIOS对应的UUID，否则导致Windows的所有软件激活失效！⚠️**

### [6-3]电池不显示 **(最新版的 `VirtualSMC` 已修复该问题！)**
~~将kext里的 `SMCBatteryManager` 换成 `ACPIBatteryManager` 即可解决问题（前提是你的dsdt是补好的！）~~

### [6-4]状态栏的卡顿
#### [6-4-1]删除 WiFiAgent 解锁卡顿问题
big sur的卡顿是因为找不到wifi设备造成的！那么使用usb网卡、无网卡的用户就需要删掉 `WiFiAgent` 这个启动项，这里只是移动了下位置。

```
$mount -o rw /

$cd /System/Library/LaunchAgents

$sudo mv com.apple.wifi.WiFiAgent.plist ../LaunchAgentsIgnored
```
运行完毕重启即可

~~提示：USB网卡现在还无法在macOS Big Sur 上使用！当然说不定以后可以（说的都是什么废话...）~~ `chris1111`已经更新支持黑苹果的USB网卡驱动，这里附上链接🔗供大🔥🚪查看 [点击跳转至`Wireless-USB-Big-Sur-Adapter`](https://github.com/chris1111/Wireless-USB-Big-Sur-Adapter)   
**使用时需要关闭 `SIP` !!! [点击跳转至[6-6]关闭 `SIP` & `Authenticated-root`](#6-6关闭-sip--authenticated-root) 

![usb](./image/usb.png)

#### [6-4-2]直接更换博通网卡
删除`WiFiAgent`只是缓兵之计，除了插网线否则你还是连不上网，因此给电脑更换博通网卡才是最好的解决方法。（而且雷蛇拆机并不会影响保修，不像某些厂商....）

整个机身共有 10 颗螺丝分一种规格，你需要一把 `T5` 的螺丝刀来打开它，卸下所有螺丝即可拆下背板。

![laptop](./image/laptop1.jpg)

网卡位于机器的右下角，插槽处被一张防静电胶布覆盖，需要揭开它。

![laptop](./image/laptop2.jpg)

记得断开天线，不会吧，不会吧，不会有人不知道吧。

换好装上背板即可

### [6-5]开启HiDPI
**开启教程选择下面 `[6-5-1]将旧系统的 HiDPI 转移到 macOS 11` 或 `[6-5-2]通过 one-key-hidpi 开启` 其中一个即可。**  

由于macOS11对于安全性更强的要求，macOS Catalina中解锁sle的命令已经失效了。尽管如此，HiDPI的开启不受影响，传统开启的方法是把显示器文件写入进系统目录 `/System/Library/Displays/Contents/Resources/Overrides`，这样做有风险而且升级后失效。  

把显示器文件写入目录 `/Library/Displays/Contents/Resources/Overrides` 能取得相同效果，而且这样做的好处有：
- 支持 Big Sur
- 升级系统后不需要重新开启
- 保持系统目录纯净
- 容易恢复，删除`/Library/Displays/` 文件夹即可

### [6-5-1]将旧系统的 HiDPI 转移到 macOS 11 **(需要你旧系统已开启HiDPI)**
开启方法：

![hidpi](./image/hidpi1.png)

![hidpi](./image/hidpi2.png)

结果展示：

![hidpi](./image/hidpi3.png)

*备注：因为我并没有开启HiDPI因此这些图片都取自hxd的[博客](https://wanan.run/2020/07/01/%E9%BB%91%E8%8B%B9%E6%9E%9C%E5%AE%89%E8%A3%85Big%20Sur%E8%BF%87%E7%A8%8B%E4%B8%AD%E9%81%87%E5%88%B0%E7%9A%84%E9%97%AE%E9%A2%98%E6%80%BB%E7%BB%93/#more)里, 灵感来自远景大佬郑世祺，[来源](http://bbs.pcbeta.com/viewthread-1862148-1-1.html)。* *版权归郑世祺所有，侵权立删©️*

### [6-5-2]通过 `one-key-hidpi` 开启
操作原理与开头说的一致，这里只是将目标位置进行更改，你需要做的就是打开 `终端`，  
并输入以下代码：  
```bash
bash -c "$(curl -fsSL https://raw.githubusercontent.com/mlch911/one-key-hidpi/master/hidpi.sh)"
```
*`one-key-hidpi`由 `xzhih` 大佬开发，并由 `mlch911` 进行fork并对目标位置进行更改。在这里再次感谢！[点击进入issue查看详情🔎](https://github.com/xzhih/one-key-hidpi/issues/136)*   

接着按照你自己的机型设置对应的设备和分辨率，设置完成后重启即可生效。  

### [6-6]关闭 `SIP` & Authenticated-root
由于在 macOS Big Sur 中，苹果更新了安全机制，新增了 `authenticated root` 这也使得开机从只读快照启动而非直接系统文件启动，因此老方法 `E7030000` 已失效，但是根据 dortania 向导的提示，现在需使用 `FF0F0000` 关闭 `SIP`。

![sip](./image/sip-1.png)

具体操作：   
打开 `config.plist`  
- NVRAM
  - add / 添加
    - 7C436110-AB2A-4BBB-A880-FE41995C9F82
      - `csr-active-config`
        - `FF0F0000` ｜ 数据类型：`DATA`
  - block / 删除
    - 7C436110-AB2A-4BBB-A880-FE41995C9F82
      - `csr-active-config`

图例：

![sip](./image/sip-2.png)

![sip](./image/sip-3.png)

修改完成后保存关闭即可，重启查看效果。   

### ~~[6-7]修改系统快照 [**这里并不推荐修改，因为会失去OTA的机会！**]~~[在b6开启`SecureBoot`达到中等安全时将不会从快照启动]
~~*感谢macrumors论坛的ASentientBot会员，是他提供的方法*~~   
~~1. 关闭SIP和authenticated-root（这是Big Sur新增的安全功能），关闭方法请查阅上面的章节[[6-6]关闭 `SIP` & Authenticated-root](#6-6关闭-sip--authenticated-root)。~~   
   
~~2. 重启后打开终端执行 `sudo -s` 切换到root。~~
~~3. 输入 `diskutil list` 找到 Big Sur 的只读快照。快照名会叫`disk#s#s#`，如下图所示，我这里的快照叫 `disk3s5s1`。~~
![snapshot](./image/snapshot-1.png)
~~4. 输入 `diskutil mount disk#s#` 挂载真正的系统分区（对于我而言就是`diskutil mount disk3s5`）系统分区一般来说为快照分区上面的磁盘区（看上面那个图），例如你的快照为 `disk1s2s1`，那么你的系统分区为 `disk1s2`。~~
~~5. 运行命令 `/S*/L*/F*/apfs.fs/C*/R*/apfs_systemsnapshot -v "/Volumes/你挂载的分区名" -r ""`，这个命令会允许你从真的系统盘启动。**注意！你挂载的分区名为你的系统盘名称 + 1，比如快照盘叫 `Macintosh HD`，那么挂载后的系统盘就叫 `Macintosh HD 1`。当然你也可以在磁盘工具中的装载点看到**~~
![snapshot](./image/snapshot-3.png)
~~6. 如果你想删除掉以前的只读快照，终端运行 `sudo diskutil apfs deletesnapshot`即可。~~


### ~~[6-8]启用修改系统文件~~ [OTA时会提示broken，现不推荐这么做]
~~在操作完上述的[[6-6]关闭`SIP` & Authenticated-root](#6-6关闭-sip--authenticated-root) 和 [[6-7]修改系统快照](#6-7修改系统快照)后，重启在终端输入 `mount -uw /`即可启用修改系统文件。~~

### [6-9]USB定制驱动
通过定制USB接口驱动可以让你电脑的USB接口正常工作，同时也能间接解决睡眠问题（当然我这个睡眠不是通过这个解决的。。。）定制的方法也很简单，全程花费十分钟左右。   

准备工具：
- macOS Big Sur
- Hackintool
- 一个有线鼠标或者其他 `USB2.0` 接口的硬件用作后续的测试
- 一个 `USB 3.0` 的U盘或其他同接口的硬件用作后续的测试（ `USB3.1`，`3.2` 都可，这里只是用于测试接口）
- USBInjectAll.kext (这里我就不提供了，网上搜索一堆)
  
如何分辨 `USB2.0` 和 `USB3.0` ？   

![usb_customize](./image/usb_customize.png)   
*图片转载自网页 [使用 Hackintool 定制黑苹果 USB 端口，适用于 Clover & OpenCore](https://heipg.cn/tutorial/custom-usbports-for-hackintosh.html),侵权立删©️*

挂载 `EFI` 分区，用 `终端` 或者 `OCC` 都行   
将 `USBInjectAll.kext` 放入 `/EFI/OC/Kexts`。

![usb_customize](./image/usb_customize-1.png)

将 `USBInjectAll.kext` 添加到 `config.plist` 中，并将底部 `Quirks` 窗口中的 `XhciPortLimit` 勾上以解除USB接口限制。   

![usb_customize](./image/usb_customize-2.png)

设置完成后保存并重启macOS  

解压 `Tools`里的 `Hackintool` 并安装它，然后打开该软件。  

进入 `Hackintool` 后跳转到 `USB` 窗口（顶部），你会看到一堆USB接口。（**由于我已经定制过USB，因此图里的接口比较少**）   

![usb_customize](./image/usb_customize-3.png)

接着将你准备好的 `USB2.0` 设备把电脑上所有的接口都插一遍并记录下来。(直接修改 `连接器种类`就行） 
如图所示，当我插入我的 `USB2.0` （我的鼠标）设备时，我的 `HS01` 接口检测到了设备插入，那么对应的就是 `HS01` ➡️ `USB2.0`。
![usb_customize](./image/usb_customize-4.png)

记录下来后将你的 `USB2.0` 设备插入另外一个接口，这时可以看到 `HS02` 检测到了设备的插入，那么对应的就是 `HS02` ➡️ `USB2.0`
![usb_customize](./image/usb_customize-5.png)

接着将你的USB3.0，Type-C都轮流测试一遍并记录下来（直接修改 `连接器种类`就行）  
![usb_customize](./image/usb_customize-6.png)

**测试Type-C时，记得两面都要测试。如果只有一面有检测到，那么就是 `TypeC+Sw`。如果两面都有检测到，那么就是 `TypeC`**  

**同时需要注意系统最多支持占用 `15` 条 `USB线路`，`USB2.0` 或着叫 `HSxx` 的端口占用 `1` 条 `线路`， `USB3.0`， `TypeC`， `TypeC+Sw` 或者叫 `SSxx` 的端口占用 `2` 条 `线路`！因此如果它们加起来超过 `15` 条 `线路`，那么你就需要做出取舍！如果你的 `USB线路` 加起来没有 `15` 条或者 刚好 `15` 条(比如我），那没事了当我没说**    

最后，定制完成后，你需要删除多余无用的接口。（确保你所有的接口都测试过了！，测试完成后剩下这些灰色的接口就是无用的接口，选中点击下方的 `➖` 即可删除）  

![usb_customize](./image/usb_customize-7.png)  

删除完成后，点击右侧的到处按钮，到处定制好的USB驱动。  

![usb_customize](./image/usb_customize-8.png)  

导出的驱动位于桌面，你会看到生成的这三个文件，在 `OpenCore` 中，我们只需要这个 `USBPorts.kext`。将 `USBPorts.kext`拖入 `/EFI/OC/Kexts` 并将其添加到 `config.plist` 中。  

![usb_customize](./image/usb_customize-9.png)

将 `USBInjectAll.kext` 从 `config.plist` 中删除，并取消勾选下方 `Quirks` 窗口中的 `XhciPortLimit`

![usb_customize](./image/usb_customize-10.png)

设置完成后保存重启即可完成USB定制。

### [6-10]修复Recovery无法进入
用 `OCC` 打开 `config.plist`,   
找到 `UEFI` -> `APFS` -> `JumpstartHotPlug` 勾选即可

### [6-11]解决App Store无法登录的问题
重置 `NVRAM` 即可解决该问题   
打开终端，输入命令：

```bash
sudo nvram -c
```

接着输入用户密码后回车，不必理会提示信息，重启即可

### [6-12]修改显存大小 **(心理优化)**
首先声明这里的显存只是一个数字，并无任何实际作用！你要想装逼可以直接改个RTX3080(只不过也是Intel的显卡就是了xd)。   

打开 `config.plist`,进入 `DeviceProperties`:  
首先添加你显卡所需要的参数，比如 `AAPL,ig-platform-id`,  
然后这是添加显存参数 `framebuffer-unifiedmem`,值根据你想要显示的显存修改。    

显存值例子：  
000000FF ➡️ 4080MB  
00000080 ➡️ 2048MB  

![VRAM](./image/4080-config.png)

备注：`UHD630` 经测试最高只能修改到4080MB，再往上会变成0MB。

保存重启即可。  
![VRAM](./image/4080.png)  

### [6-13]解决 `macOS` 与 `Windows` 时间不同步
造成两系统时间不同步的原因为两者对时间计算的方式不同，  
`Windows` 将 `BIOS` 时间作为系统时间，  
而 `macOS` 将 `BIOS` 时间作为 `UTC` 时间，再根据你所在的时区进行计算得出系统时间。   

使用 `Hackintool` 解决问题：  
打开 `Hackintool`,顶栏选择 `工具` / `Tool`，点击底部第五个图标以生成 `Windows 注册表`。  
![time](./image/time-1.png) 

`Hackintool` 会将生成的这两个文件放到 `桌面`，将这两个文件转入你的 `Windows`。  
![time](./image/time-2.png) 

进入 `Windows` 后，打开文件 `WinUTCOn.reg`将其注入进系统重启即可。  
备注：  
WinUTCOn.reg ➡️ 开启UTC时间计算  
WinUTCOff.reg ➡️ 关闭UTC时间计算  
当你不需要该时间结算方法后，双击运行 `WinUTCOff.reg` 即可。  

## [7]附加：U盘直装
*搬运自 Bochi‘s Blog [OpenCore U盘全新直装Big Sur](https://wanan.run/2020/07/07/OpenCoreU%E7%9B%98%E5%85%A8%E6%96%B0%E7%9B%B4%E8%A3%85BigSur/)*

### 准备：

- U盘 16GB以上
- 安装文件
- 7/6或更新的 `OC`，`Lilu`，`WhateverGreen`

~~`Lilu` 和 `WhateverGreen` 我已放入`Tools`里,可以自行下载（同样由Bochi提供，在这里再次感谢🙏）。~~  
**请从`release`里下载最新版本驱动，里面包含你们需要的 `Lilu` ， `WhateverGreen` 和 `OC`。**  
什么？你说U盘也需要提供？你怕是再想peach！！！ 💢
### Config 修改 （OpenCore 0.6.0）：

- `NVRAM`
  - `7C436110-AB2A-4BBB-A880-FE41995C9F82`
    - 删除 `csr-active-config` 
- ~~`Kernel`~~ (VirtualSMC 1.1.5+ 已修复该问题)
   - ~~`添加 / Add`~~
     - ~~添加 `FakeSMC`~~
     - ~~禁用 `VirtualSMC`~~

保存退出

### 将安装文件写入U盘

终端输入指令：
```
sudo /Volumes/Install\ macOS\ Beta/Install\ macOS\ Beta.app/Contents/Resources/createinstallmedia --volume /Volumes/UNTITLED /Volumes/Install\ macOS\ Beta/Install\ macOS\ Beta.app --nointeraction
```
其中，`createinstallmedia`、`Install macOS Beta.app` 这两个文件、还有中间`/Volumes/UNTITLED`的**U盘名字**可以直接**拖拽**到终端。

### 安装

重启以U盘启动即可进入系统安装界面，接着一直点，重启几次便可完成系统安装

### 启动项问题

如果安装成功后在OC中找不到新系统的启动项，就进入已经装好的Mac系统 ➡️ `系统偏好设置` ➡️ `启动磁盘` ➡️ 选择 `macOS 11` 的启动盘然后重新启动即可。



## [8]参考
- https://github.com/EmeryWan/Razer-Blade-15-2018-Base-Hackintosh
- https://github.com/blade15basehackintosh/razerbladehackintosh
- https://github.com/doanhmaple/Razer-Blade-15-Advanced-2018-Hackintosh
- https://github.com/stonevil/Razer_Blade_Advanced_early_2019_Hackintosh
- https://blog.daliansky.net/
- http://bbs.pcbeta.com/viewthread-1862049-1-1.html
- http://bbs.pcbeta.com/viewthread-1862835-1-1.html
- http://bbs.pcbeta.com/viewthread-1862148-1-1.html
- https://wanan.run/2020/07/07/OpenCoreU%E7%9B%98%E5%85%A8%E6%96%B0%E7%9B%B4%E8%A3%85BigSur/
- https://wanan.run/2020/07/01/%E9%BB%91%E8%8B%B9%E6%9E%9C%E5%AE%89%E8%A3%85Big%20Sur%E8%BF%87%E7%A8%8B%E4%B8%AD%E9%81%87%E5%88%B0%E7%9A%84%E9%97%AE%E9%A2%98%E6%80%BB%E7%BB%93/
  
## [9]变更目录
- 9/3
  - 更新 beta6
- 9/1
  - 开学降低更新频率
- 8/19
  - 更新 beta5
  - 删除启动参数 `-brcmfxbeta` ，`-hbfxbeta`
  - 默认禁用 `VerbStub`，需要使用请手动开启。
- 8/17
  - 添加 Windows & macOS 时间同步教程
- 8/15
  - 象征性添加3.8GB / 4080MB显存 （使用 `config_4080.plist`）
  - 添加显存修改教程
- 8/14
  - 添加 `SecureBoot`，默认设置为 `j132` 对应 `MacBookPro15,2 (July 2018)`
  - 更新 `USBPorts.kext`，修复开机画幅大小的问题。
  - 更新 `OpenCore Configurator 2.10.0.0` 
- 8/13
  - 修复 `DW1560` 在 `Beta4` 和 `Public Beta` 的问题
  - **更新8/13号自编译 `VirtualSMC` (VirtualSMC 1.1.6)**
    - Fix audio lags in Safari caused by reading SMM in SMCDellSensors plugin([#36](https://github.com/acidanthera/VirtualSMC/pull/36))  
    - Sync changelog
    - Add experimental support for supplement information ([#34](https://github.com/acidanthera/VirtualSMC/pull/34))
    - Drop extra semicolon
  - **更新8/13号自编译 `Lilu`  （Lilu 1.4.7）**
    - Sync changelog
    - Do not remove osfmk folder from SDK's libraries (will be used by SMCDellSensors and probably SMCProcessor)
  - **更新8/13号自编译 `AppleALC`  （AppleALC 1.5.2）**
    - Added missing layout7.xml ([#586](https://github.com/acidanthera/AppleALC/pull/586))
    - Update Changelog.md
    - Update README_CN.md
  - **更新8/13号自编译 `AirportBrcmFixup`（AirportBrcmFixup 2.0.9）**
    - boot-arg and property `brcmfx-aspm` supports special value `255` in order to skip logic disabling APSM for 0x14e4:0x43a3 (DW1820A).
    - Update Changelog.md
- 8/12
  - 更新正式版 `EFI` 
  - 更新 `OpenCore Configurator 2.9.1.0` 
  - 更改机型为 `MacBook Pro 15,2`
  - 添加图像化引导
- 8/7
  - 更新HIDPi教程
- 8/4
  - 更新USB定制教程
  - 更新 macOS Big Sur Beta 4
- 8/3
  - 更新EFI驱动到最新稳定版本
  - 更新官方Kext全家桶（搬运自@acidanthera）
  - 更新OpenCore 0.6.0 （搬运自@acidanthera）
  - 更新macOS系统优化：USB驱动定制教程
  - **更新8/3号自编译 `VirtualSMC` (VirtualSMC 1.1.4)** 
    - Improve SMC generation debugging
    - Force x86_64
    - Resolve booting issue on macOS 11 due to provider race condition
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Fixed crashes when trying to read CLKT key
    - Update README.md
  - **更新8/3号自编译 `Lilu`  （Lilu 1.4.6）**
    - Fixed another race condition in kext patcher loading code in 11.0
    - Resolve init issues on 11.0 with multiple PCI root devices
    - Force x86_64
    - Process already loaded kexts early in 11.0
    - Make function routing atomic in several places
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Initialise kernel patches in parallel to PCI
    - Add RTC register indices
    - Abort on PCI register read failure
    - Implement Lilu loading at console init in 11.0
    - Fix typo in debug logging
    - Update README.md
  - **更新8/3号自编译 `WhateverGreen`  （WhateverGreen 1.4.1）**
    - Force x86_64
    - fix typo and spaces ([#59](https://github.com/acidanthera/WhateverGreen/pull/59))
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Update FAQ.IntelHD.cn.md ([#58](https://github.com/acidanthera/WhateverGreen/pull/58))
    - Update README.md
    - Update FAQ.IntelHD.en.md
  - **新增8/3号自编译 `NVMeFix`   (NVMeFix 1.0.3)**
    - Added constants for 11.0 support.
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Leave a note regarding 11.0
    - Force x86_64
  - **新增8/3号自编译 `CPUFriend`   (CPUFriend 1.2.1)**
    - Added constants for 11.0 support
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Force x86_64
  - **更新8/3号自编译 `AppleALC`  （AppleALC 1.5.1）**
    - Force x86_64
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Update README.md
  - **更新8/3号自编译 `AirportBrcmFixup`（AirportBrcmFixup 2.0.8）**
    - Force x86_64
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Fix ordering of build stages ([#8](https://github.com/acidanthera/AirportBrcmFixup/pull/8))
    - Update README.md
  - **更新8/3号自编译 `HibernationFixup`   (HibernationFixup 1.3.4)**
    - Force x86_64
    - Get things compile in Xcode 12 (is not guaranteed to work)
    - Added constants for 11.0 support
  - **更新8/2号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - Update SSDT-EC-USBX.dsl
    - OcCpuLib: Fix display name for i9 CPUs like 7920X

- 8/2
  - **睡眠修复，现在可以直接合盖睡眠或手动点击睡眠💤 ！！！**
  - **更新8/1号编译版本 `OpenCore` (OpenCore 0.6.0)**（**I disable nvmefix, if you are using nvme drive you should enable it!!! / 我在efi中未启用nvmefix的kext，如果你使用nvme硬盘使用系统，请手动启用！！！**)
    - Patches: Add AtaAtapiPassThru IDE timeout patch
    - OcAppleSecureBootLib: Fix invalid assertion
    - OcAppleIm4Lib: Fix memcpy undefined reference
    - Include: Add BlockIoVendor header
    - EfiLdr: Revert removal of memmap shifts
    - Include: Update AppleCsrConfig with 11.0 definitions
    - BootSector: Drop unused and non-functional GENPAGE mode
    - EfiLdr: Fixed 32-bit booting on machines with over 4 GBs of RAM
    - Docs: Document the DeviceProperty limitations for some drivers
    - Update SSDT-EC-USBX.dsl (#92)
    - OcXmlLib: Free original buffer on failure
    - OcXmlLib: Correct/clarify XmlDocumentExport
    - OcXmlLib: Fix previous commit
    - OcXmlLib: Add plist doctype export option
    - DataBase: Fixed BIOSReleaseDates
    - PlatformInfo Automatic for all models
    - Build: Fix warnings
    - OcFileLib: Implement AllocateCopyFileData
    - OcXmlLib: Implement XmlNodeChangeContent
    - Utilities: Drop OpenDuetPkg binary and rebuild it with OC
    - OcDevicePathLib: Added a workaround for PCI0 with 0x1 _UID
    - OpenCoreMisc: Perform serial init separately via SerialInit option
    - Docs: Fix the hint regarding RebuildAppleMemoryMap
    - OcAfterBootCompatLib: Fix 32-bit dead loop
    - Docs: Provide errata entry on OSXSAVE issue
    - OcAppleKernelLib: Fixed OSXSAVE reporting when emulating CPUID on newer CPUs
    - Docs: Improve the documentation
    - OcConsoleLib: Update UGA comments
    - OcFileLib: Consolidate to use GetFileInfo
    - DataBase: Update builtin firmware versions for 11.0
    - Update SampleLegacy.plist

- 8/1
  - 更新 `USB-Adapter` 驱动 by `chris1111`
- 7/30
  - 更新BIOS教程 (Base版 Only)
- 7/26
  - 修复CLT问题
- 7/25
  - 修复SIP问题
  - 修复Authenticated-root问题
  - 修复系统写入权限&nbsp;&nbsp;&nbsp;&nbsp;&nbsp;/[Beta3]貌似已失效，后续会进行测试/
- 7/22
  - 更新 macOS Big Sur beta3
- 7/20 
  - **更新7/20号自编译 `WhateverGreen`  （WhateverGreen 1.4.1）**
    - Update FAQ.IntelHD.en.md
  - **更新7/20号自编译 `AirportBrcmFixup`（AirportBrcmFixup 2.0.8）**
    - Support brcmfx-aspm for all chipsets
    - Support boot-arg & property `brcmfx-aspm` to override value used for pci-aspm-default, support ioreg property brcmfx-wowl
  - **更新7/20号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - Includes: Fix MKext header comments
    - OcCompressionLib: Expose Adler32 function
    - OcDevicePathLib: Fix potential deadloop
    - Patches: Add AtaAtapiPassThru patches for G33
    - Includes: Add missing Mach prefixes
    - Includes: Fix additional typos
    - OcFileLib: Fix typo
    - Patches: Add SataControllerDxe patch for G33 in RAID mode
    - OcAppleKernelLib: Fix memory corruption with many kexts in 11.0
- 7/18 
  - **新增自编译驱动 `VoodooInput` (VoodooInput 1.0.6)**
  - **更新7/18号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - Docs: Fix debugging patches
    - Docs: generated pdf
    - OcMemoryLib: Fix typo
    - Utilities/KextInject: Determine Info/EXE reserve sizes
- 7/16 
  - **更新7/16号自编译 `AirportBrcmFixup`（AirportBrcmFixup 2.0.8）**
    - Fix critical issue introduced in previous 2 commits (getting of brcmfx-driver index)
    - Check and fix incorrect value brcmfx-driver (if specified value is unsupported in current osx system)
  - **更新7/16号自编译 `VirtualSMC` (VirtualSMC ?.?.?)** 
    - Include SMCDellSensors in package ([#33](https://github.com/acidanthera/VirtualSMC/pull/33))
    - Sync changelog
    - Compatibility fixes in SMCBatteryManager for 10.16 ([#32](https://github.com/acidanthera/VirtualSMC/pull/32))
    - Update Changelog.md
    - **Added a new plugin SMCDellSensors (adapted SMI Monitor from HWSensors):**
      - monitor and control temperature and fans in Dell computers by using SMM technology ([#31](https://github.com/acidanthera/VirtualSMC/pull/31))
        - Port SMIMonitor for VirtualSMC
        - Use mp_rendezvous instead of mp_rendezvous_no_intrs and disable/enable interrupts in assembler code
        - Add keys for fan control, configurable multiplier and names
        - Fix issue with non-sorted keys, add target speed support.
        - Update Changelog.md
        - Fix project & file name in sources, add copyrights and links to the original sources
        - Fix issues in fan control, remove unsupported on real Macs key F0As.
        - Use _Atomic instead of stateLock
        - Do not disable interrupts while reading SMM, rename variables according to review remarks.
        - Increase SMM reading interval
        - Increase maximum amount of temp sensors 8
        - Revert max amount of temp sensors to 6 (we do not have so many smc keys to keep them all), rename variable for FS! again (with comments)
        - Fix attributes for F0Mn & F0Mx, add logging if someone wants to update these keys
        - Disable update timer during sleep/shutdown phase, otherwise reading of SMM prevents sleeping with closed lid.
        - Use DBGLOG for logging
        - Fix module version and remove unused variable.
        - **Co-authored-by: lvs1974 
          <lvs1974@users.noreply.github.com>**
  - **更新7/16号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - OcBootManagementLib: Load icons for custom boot entries ([#91](https://github.com/acidanthera/OpenCorePkg/pull/91))
    - Update Changelog.md
    - DataBase: Update builtin firmware versions
    - Update AutoGenerated.c
    - DataBase: Update SmcRevision
    - OcFileLib: Provide workaround for buggy drivers
    - DataBase: Fixed typos
    - Includes: AppleKeyMapAggregator revision is UINT64
    - OcMemoryLib: Fix typo

- 7/15
  - 更新 `macOS 10.15.6` 正式版 & `Safari 14.0` 测试版 **（非 `Big Sur` 更新）**
  
- 7/14 
  - **更新7/14号自编译 `VirtualSMC` (VirtualSMC ?.?.?)** 
    - Fixed running smcread on 11.0 without IOKit framework
  - **更新7/14号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - Docs: Fixed typo
    - DataBase: Updeted MBP164

- 7/13
  - **更新7/13号自编译 `VirtualSMC` (VirtualSMC ?.?.?)** 
    - Update README.md  **(只是更新说明文档，无驱动变化)**
  - **更新7/13号自编译 `WhateverGreen`  （WhateverGreen 1.4.1）**
    - Update README.md  **(只是更新说明文档，无驱动变化)**
  - **更新7/13号自编译 `AppleALC`  （AppleALC 1.5.1）**
    - Update README.md  **(只是更新说明文档，无驱动变化)**
  - **更新7/13号自编译版本 `Lilu` (Lilu 1.4.6)**
    - Update README.md  **(只是更新说明文档，无驱动变化)**
  - **更新7/13号编译版本 `OpenCore` (OpenCore 0.6.0)**
    - Delete OpenCore_with_text_Right.png
    - Docs: Fixed previous
    - Docs: Added links to customised icons.
    - Docs: Update SampleLegacy
    - Docs: Fixed Samples
- 7/12
  - **新增7/12号编译版本 `OpenCore` (OpenCore 0.6.0) [转载自`OpenCore-Factory`]**
    - Docs: Drop Generic key as it is unused from Legacy
    - Docs: Rename SampleFull to SampleLegacy and fix typos
  - **更新7/12号自编译 `VirtualSMC` (VirtualSMC ?.?.?)** 
    - Fix sign issues in legacy smc tool
- 7/11
  - 更新一些我自己用的壁纸....（算是给自己的壁纸做备份？？？)
  - **更新7/11号自编译 `AirportBrcmFixup`（AirportBrcmFixup 2.0.8）**
    - Merge remote-tracking branch `refs/remotes/origin/master`
    - Fix wrong base class IOService for FakeBrcm, now it works in older osx
    - Update README.md
    - Commit required files for previous commit
    - Remove injectors for AirPortBrcm4360 and AirPortBrcmNIC from main Info.plist and move them into separate plugins AirPortBrcm4360_Injector and AirPortBrcmNIC_Injector (kexts with plist only)
- 7/10
  - Release打包 📦  改为分包模式：
    - `x/x-DEBUG.zip`
    - `x/x-RELEASE.zip`  (一般使用`RELEASE`版即可)
  - 修复Wi-Fi不定时自动断开的毛病
  - 更新release分支，一般会在8 ~ 24小时左右更新驱动
    - **⚠️ 注意：我发布的自编译驱动未经原作者同意，因此有问题请不要在原作者的issue里发表！⚠️**
  - **更新7/10号自编译 `Lilu`  （Lilu 1.4.6）**
    - Silence stupid clang analyzer
  - **更新7/10号自编译 WhateverGreen  （WhateverGreen 1.4.1）**
    - Revert workaround for ATIController::start on 11.0
- 7/9
  - **更新7/9号自编译 `OpenCore` （OC 0.6.0）** (已添加进Tools里)
    - DxeIpl: Fix ACPI reset register detection
  - **更新7/8号自编译 `Lilu`  （Lilu 1.4.6）**
    - Added device publishing API to monitor device startup
  - **更新7/9号自编译 `WhateverGreen`  （WhateverGreen 1.4.1）**
    - Add first generation Intel HD Graphics support
  - **更新7/8号自编译 `AppleALC`  （AppleALC 1.5.1）**
    - Use new device publishing API for 11.0 syncing 
  - **更新7/5号自编译 `AirportBrcmFixup`  （AirportBrcmFixup 2.0.8）**
    - Fix warning 'Value stored to 'subSystemDeviceID' during its initializ…
- 7/7
  - **更新 macOS Big Sur beta2**
  - **更换 `VisualSMC` 为 `FakeSMC`**
- 7/5
  - 更换 `Broadcom BCM94352Z` / `DW1560` 网卡 
    - 蓝牙得到解决
    - Wi-Fi得到解决
    - 状态栏卡顿得到解决
  - **修复状态栏卡顿**
- 7/4
  - **修复开机画屏**
  - **修复电池显示**
  - **修复触摸板**
- 6/30
  - **更新 macOS Big Sur beta1**  
  - **更新 OC 0.6.0**  
  
~~后续内容还在施工中👷，请耐心等待⌛️~~   
~~作者不会鸽的放心吧，咕咕咕咕～～～~~

> 文章大致已经完成  ✅ ，后续将为各种小修小补...

## 未来计划 / Plans ：
- ~~增加BIOS修改的图文教程 / Add detail for BIOS's tutorial  [七月底 / Late July]~~ [已完成 / Finished] ✅
- ~~独立变更目录 / Separate `changelog` to a individual file [七月底 / Late July]~~ [已完成 / Finished] ✅
- ~~增加英语版本教程 / Add `English` version [八月底 / Late August]~~ ❌
  - **Reason for cancellation** : `OC` now support `OTA`, no more need for this tutorial.  
