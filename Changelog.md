RazerBlade 15 Base Model(2018) Big Sur EFI Changelog
==================
### Support Version: macOS 10.15.1 ~ macOS 11 beta6 / public beta3  
#### v1.2.0
- Updated builtin firmware versions(Boot Rom Version: `1554.40.9.0.0` to `1554.40.13.0.0`)
- Added `ProcessorType` option to `Generic` (Default set to `0`, if you want to custom, go ahead.)
- Added IA32 binary variant to the release bundles
- For older version macOS (Not & not gonna test, if you want challenge youself, do it!):
  - Fixed improper handling of cacheless kexts without an Info.plist
  - Fixed improper calculation of kext startup address for blocking
  - Added mkext 32-bit kext injection (10.4-10.6)
  - Added cacheless 32-bit kext injection (10.4-10.7)
  - Added 32-bit kernel/kext patching/blocking support
#### v1.1.0
- Remove dependencies corecapture and IONetworkingFamily
- Fix issue on scanpolicy stuck on recovery (while it's not `0`)
- Add SecureBoot, default set to `j132` ➡️ `MacBookPro15,2 (July 2018)`
- Supoort medium secutiry level
- Delete driver `AudioDxe`
- Add protocol `AppleImg4Verification` & `AppleSecureBoot`
- Add boot-arg: `igfxrpsc=1`
- Add EnablePassword: False
- Add PasswordHash: <>
- Add PasswordSalt: <>
- Add ApECID: 3478613715
- DmgLoading Changed: `Any` to `Signed`
- Fix VMware compatibility with Apple Secure Boot
- Fix prelinked kext patches in KC mode
- Added `DisableLinkeditJettison` quirk (defalut enabled)
- Fix issues in 11.0 kext injection and patching
- Add `Force` for 10.8 or lower syetem's kext support(defalut empty, cz I don't use that)
- Add `Scheme` for 10.8 or lower syetem's kext support(defalut empty, cz I don't use that)
#### v1.0.8
- EFI Bump Version:     
  - AirportBrcmFixup 2.0.8 ➡️ 2.0.9     
  - AppleALC 1.5.1 ➡️ 1.5.2     
  - HibernationFixup 1.3.4 ➡️ 1.3.5     
  - Lilu 1.4.6 ➡️ 1.4.7      
  - VirtualSMC 1.1.5 ➡️ 1.1.6     
  - SMCBatteryManager 1.0 ➡️ 1.1.6     
  - SMCLightSensor 1.0 ➡️ 1.1.6     
  - SMCProcessor 1.1.5 ➡️ 1.1.6     
  - SMCSuperIO 1.1.5 ➡️ 1.1.6     
  - WhateverGreen 1.4.1 ➡️ 1.4.2     
#### v1.0.7
- Some correction on USBPorts
#### v1.0.6.1
- Defalut disabled `VerbStub`, if your headset microphone doesn't switch to audio input AUTOMATICALLY while you plug in headphone, enabled it
- Delete boot-arg: `-brcmfxbeta` , `-hbfxbeta`
#### v1.0.6
- Add `USBPower` / enhance the power support on apple devices(charging speed up for iPad / iPhone)
#### v1.0.5
- Update `USBPorts` / Fix some issues on USB Customize
Fix the Window Size Error after boot into system(Lock Screen)
#### v1.0.4
- SMBIOS Changed: `Macbook pro 15,3` to `Macbook pro 15,2`
- Try to fix the problem on `Thunderbolt 3`. Gratitude: `doanhmaple`
#### v1.0.3
- Add GUI Picker
- Simplify EFI
- Update `AirportBrcmFixup`
- Fix issue on `DW1560` (Now support beta4)
#### v1.0.2
- Update `OpenCore 0.6.1`
- Add DmgLoading: `Any`
- Faster Boot (about 10s)
- SMBIOS Changed: `MacBook Pro 16,4` to `MacBook Pro 15,3` (Fix the problem on booting stuck at `Thunderbolt3` PCIe)
#### v1.0.1
- Add `USBPorts` / USB customize
- Add `HiDPI`
#### v1.0.0
- Update `OpenCore 0.6.0`
- Update `AirPortBrcmFixup`
- Update `AppleALC`
- Update `CPUFirend`
- Update `HibernationFixup`
- Update `Lilu`
- Update `NVMeFix`
- Update `VirtualSMC`
- Update `VoodooI2C`
- Update `VoodooInput`
- Fix Hibernation
- Fix `CLT`
- Disabled `SIP`
- Disabled `Authenticated-root`
#### v0.9.0
- Fix issue on `Safari`
- Fix issue on `WiFi`
- Add boot-arg: `vsmcgen=1`
#### v0.8.0
- Replace `FakeSMC` with `VirtualSMC`
- Replace `ACPIBatterymanger` with `SMCBatterymanager`
#### v0.7.0
- Fix TouchPad
- Fix Battery
#### v0.6.0
- Update `OpenCore 0.6.0 beta` (Now support macOS 11)
- Update `Lilu beta`
- Replace `VirtualSMC` with `FakeSMC`
#### v0.5.0
- Update `OpenCore 0.5.9`
- Update `Lilu`
- Fix Multi Touch
#### v0.4.0
- Now using `OpenCore` to boot
- Add `OpenCore 0.5.8`
#### v0.3.0
- Update `CLOVER v5118`(Now support 10.15.5)
- Fix audio
#### v0.2.0
- Shield Nvdia graphic card
- Fix some display issue
#### v0.1.0
- Support macOS 10.15.4
- Add `CLOVER v5103`
