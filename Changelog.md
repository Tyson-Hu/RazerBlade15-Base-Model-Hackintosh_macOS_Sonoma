RazerBlade 15 Base Model(2018) Big Sur EFI Changelog
==================
### Support Version: macOS 10.15.1 ~ macOS 11 beta5 / public beta2  
#### v1.1.0
- Remove dependencies corecapture and IONetworkingFamily
- Fix issue on scanpolicy stuck on recovery (while it's not `0`)
- Add SecureBoot, default set to `j132` ➡️ `MacBookPro15,2 (July 2018)`
- Delete driver `AudioDxe`
- Add protocol `AppleImg4Verification` & `AppleSecureBoot`
- Add boot-arg: `igfxrpsc=1`
- DmgLoading Changed: `Any` to `Signed`
- ~~Issue: Can't boot to `Recovery`~~ (fixed)
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
