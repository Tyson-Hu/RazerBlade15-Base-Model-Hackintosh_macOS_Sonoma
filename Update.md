# 更新时间线 / Update Time Line
## 目录 / Catalog
- [ macOS Big Sur 12.0 beta （6/7 更新）](#67-更新)
- [ macOS Big Sur 11.2 beta （1/4 更新）](#14-更新)
- [ macOS Big Sur 11.0.1 （11/12 更新）](#1112-更新)
- [ macOS Big Sur 11.0.1 RC2 （11/10 更新）](#1110-更新)
- [ macOS Big Sur 11.0.1 RC1 （11/5 更新）](#115-更新)
- [ macOS Big Sur 11.0.1 beta （10/28 更新）](#1028-更新)
- [ macOS Big Sur Beta10 （10/14 更新）](#1014-更新)
- [ macOS Big Sur Beta9 （9/29 更新）](#929-更新)
- [ macOS Big Sur Beta8 （9/22 更新）](#922-更新)
- [ macOS Big Sur Beta7 （9/17 更新）](#917-更新)
- [ macOS Big Sur Beta6 （9/3 更新）](#93-更新)
- [ macOS Big Sur Beta5 & Public Beta2 （8/19 更新）](#819-更新)
- [ macOS Big Sur Public Beta (8/13更新)](#813-更新)
- [ macOS Big Sur Beta4 （8/4 更新）](#84-更新)
- [ macOS Big Sur Beta3 （7/22 更新）](#722-更新)
- [ Clover v5120 （7/16 更新）](#716-更新-clover-v5120)
- [ macOS 10.15.6 （7/15 更新）](#715-更新-非-big-sur--catalina)
- [ 【黑果小兵】macOS Big Sur Beta 2 Installer for OpenCore and PE双EFI分区原版镜像 （7/11 更新）](#711-更新)
- [macOS Big Sur Beta2 （7/7 更新）](#77-更新)

## 6/7 更新
适配 macOS 12，目前还不确定为何显卡没有显示出来，但显卡是正常工作的。。。     

![12.0](/image/12.0.png)

## 11/12 更新
正式版，版本号`20B29`，没有什么想说的，冲就完事了。。。          

![11.0.1](/image/11.0.1.png)

## 11/10 更新
今日放出了 RC2，版本号`20B28`，可以看成是GM版，如果介意的话建议重新安装系统。 OTA后可能会出现激活的界面，（如果你OTA完卡在登陆转圈圈了，那应该就是这个没错了！等就完事了）

![11.0.1 beta](/image/11.0.1-RC2-1.png)

![11.0.1 beta](/image/11.0.1-RC2-2.png)

![11.0.1 beta](/image/11.0.1-RC2-3.png)

## 11/5 更新
终于释出 RC1，版本号`20B5022a`，基本可以确定正式版在三个版本之内:)

![11.0.1 beta](/image/11.0.1-beta2-1.png)

![11.0.1 beta](/image/11.0.1-beta2-2.png)

![11.0.1 beta](/image/11.0.1-beta2-3.png)

## 10/28 更新
果然不出意外我又被打脸了，不过在释出正式版之前就放出下一个测试版也是苹果的日常操作了，所以其实都在我的意料之中（手动滑稽）     
如果你检测不到更新，进入终端输入以下代码，然后关闭设置重新打开就可以检测到了。     

```
sudo /System/Library/PrivateFrameworks/Seeding.framework/Versions/A/Resources/seedutil unenroll         
```

```
sudo /System/Library/PrivateFrameworks/Seeding.framework/Versions/A/Resources/seedutil enroll DeveloperSeed
```

![11.0.1 beta](/image/11.0.1-beta-1.png)

![11.0.1 beta](/image/11.0.1-beta-2.png)

![11.0.1 beta](/image/11.0.1-beta-3.png)

## 10/14 更新
苹果今日放出了 `macOS Big Sur Beta10`， 版本号`20A5395g`，正常 `OTA` 更新即可。~~不出意外的话，下一次更新就是GM版本了~~（不敢bb了）

![11 beta10](/image/beta10-1.png)

![11 beta10](/image/beta10-2.png)

## 9/29 更新
苹果今日放出了 `macOS Big Sur Beta9`， 版本号`20A5384c`，正常 `OTA` 更新即可。~~不出意外的话，下一次更新就是GM版本了~~(疯狂打脸)

![11 beta9](/image/beta9-1.png)

![11 beta9](/image/beta9-2.png)

![11 beta9](/image/beta9-3.png)

![11 beta9](/image/beta9-4.png)

## 9/22 更新
这次就挺突然的，一周内连发两个版本？？？没错，苹果今日放出了 `macOS Big Sur Beta8`， 版本号`20A5374i`，正常 `OTA` 更新即可。增量包只有 `2GB`。算是一个小补。          

![11 beta8](/image/beta8-1.png)

![11 beta8](/image/beta8-2.png)

![11 beta8](/image/beta8-3.png)

![11 beta8](/image/beta8-4.png)


## 9/17 更新
又是一次漫长的等待。。。苹果终于释出了 `macOS Big Sur Beta7`，版本号`20A5374g`，正常 `OTA` 更新即可。增量包不到 `4GB`，全量包大小 `12GB` 左右。这次已g结尾的版本号让人想起gm版，不过这只是我瞎说的哈哈哈哈。

![11 beta7](/image/beta7-1.png)

![11 beta7](/image/beta7-2.png)

![11 beta7](/image/beta7-3.png)

![11 beta7](/image/beta7-4.png)


## 9/3 更新  
时隔数周苹果终于释出了 `macOS Big Sur Beta6`，版本号 `20A5364e`, 正常 `OTA` 更新即可。增量包大小 `4GB` 左右，全量包大小 `12GB` 左右。 从版本号也可以看出 `macOS 11` 已经趋于正式版的路上。   

![11 beta6](/image/beta6.png)

注意⚠️： 使用gibmacos下载时请选择 `customer`，`developer` ~~无此版本。~~ 也🉑️。   

如果你在 `OpenCore`开启了 `SecureBoot` 并设置了 `apECID`（不知道怎么设置？同机型直接套用我的EFI即可，非同机型的也可以参考我的config），开机后你会发现 `beta6` 将不会从快照启动。 前提是你拥有完整的安全性，至于如何拥有完整的安全性，你需要下载完整安装包（12GB那个.app文件），并进入recovery进行覆盖安装，后续我会抽出时间来制作教程。。    

![11 beta6 snapshot](/image/beta6-snapshot.png)

已知问题：   
`beta3` 修复的bug在 `beta6` 它又回来啦！  
 
![11 beta6 issue](/image/beta6-issue.jpg)

可能劝退：第三方kext在重启后将失去作用，官方给出的方法是再次安装（简直丧心病狂。。。）   

![11 beta6 issue](/image/beta6-issue2.png)

smb出现问题，介意的请待在 `beta5`  

## 8/19 更新
这次官方推迟了一天发布 `beta5`，版本号 `20a5354i`，正常 `OTA` 更新即可。增量包大小 `7.15GB`，全量包大小 `12.13GB`。目前版本已无什么大的BUG，更多的为UI BUG，可以日常使用。 `Public Beta2` 内容与 `beta5` 一致(版本号也均为 `20A5354i`)，用哪个看你自己了。 

![11 beta5](/image/beta5.jpg)

![11 beta5](/image/beta5-1.jpeg)

## 8/13 更新
对 `AirportBrcmFixup` 进行了修补， 现在 `DW1560 / Brcm94352z` 在 `Beta4` 和 `Public Beta` 均可正常运行，不会再卡开机boot。    

`Beta4` 与 `Public Beta` 内容一致，只是变更了版本号而已，这里我选择使用 `Public Beta`。   

版本说明：  
`20A5343j` ➡️ `Public Beta`   
`20A5343i` ➡️ `Beta4`

附上截图：   
![11 publicbeta](/image/publicbeta1.png)

## 8/4 更新 
苹果官方推出了 macOS Big Sur Beta4，更新过程与之前一致。由于我在 `beta4` 中有许多软件都出现了问题，因此我决定回到 `beta3` 版本继续使用，所以这里并没有放出截图。公测版(Public Beta)与 `beta4` 内容一致，只是更改了版本号。**EFI 现已修复，可以进行 `ota` 升级至 `beta4`**

## 7/22 更新 
苹果官方推出了 macOS Big Sur Beta3，图如下，大小为4.96GB，全量包为12GB多，正常OTA更新即可。

![11 beta3](/image/beta3.jpg)

![11 beta3](/image/beta3-2.png)

更新完成，附上截图：

![11 beta3](/image/beta3-3.png)

这次更新也修复了一些bug，例如菜单栏的时钟得到汉化+修复：

![11 beta3](/image/beta3-4.png)

被人疯狂吐槽的电池图标得到更换：

![11 beta3](/image/beta3-5.png)

已知问题：   
由于苹果在beta3中更新了SDK，现被识别成 `macOS 11.0` 而非  `macOS 10.16`，因此一些bash无法识别并安装，这里需要注意⚠️ 。

![11 beta3](/image/beta3-6.png)

可以看到提示需升级 `CLT`，但我检查过没有新的更新了，因此问题出在SDK中，这需要官方进行适配。

![11 beta3](/image/beta3-7.png)

图中可以看到并无检查到更新：

![11 beta3](/image/beta3-8.png)

### 关于`CLT`的修复
前往 https://developer.apple.com/download/more/ 登陆苹果账号并下载 `Xcode 12 beta` 和 `Command Line Tools for Xcode 12 beta3`,下载完成后双击安装 `CLT` 即可，`Xcode 12` 需要解压xip文件后拖入应用程序完成安装，**同时删除老版本 `Xcode`**   

![CLT](/image/CLT.png)

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

![10.15.6正式版](/image/15.6.jpg)

更新完毕： 

![10.15.6正式版](/image/15.6-2.jpg)

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

![beta2](/image/beta2.jpg)

下面为更新完成的样子（感觉就变了个版本号.....）

![info2](/image/info2.png)

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
