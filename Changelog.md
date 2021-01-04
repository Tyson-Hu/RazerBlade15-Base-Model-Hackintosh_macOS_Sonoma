RazerBlade 15 Base Model(2018) Big Sur EFI Changelog
==================
### Support Version: macOS 10.15.1 ~ macOS 11.2 beta
#### v1.5.0
- Fixed installing OpenDuet on protected volumes
- Updated underlying EDK II package to edk2-stable202011
- Updated builtin firmware versions for SMBIOS and the rest
- Fixed macrecovery server protocol compatibility
- Added basic audio assistant support in OpenCanopy
- Added compiled ACPI samples to the package
- Fixed timer resolution restoration at boot time
- Fixed memory capacity when using custom SMBIOS memory config
- Removed no longer required `DeduplicateBootOrder` quirk
- Fixed macserial crashes when processing invalid serials
- Fixed macserial issues when processing 2021 year serials
- Added advanced error checking in ocvalidate utility
- Added `SetupDelay` to configure audio setup delay
- Reworked LogoutHook.command to support older macOS
- Implemented MP3 audio decoding for audio assistant support
- Added support for `PickerVariant` for more theme variants
- Added `OC_ATTR_HIDE_THEMED_ICONS` `PickerAttribute` for Time Machine
- Fixed OpenUsbKb compatibility with certain keyboards
- EFI Bump Version:     
  - AppleALC 1.5.5 ➡️ 1.5.6
  - HibernationFixup 1.3.8 ➡️ 1.3.9
  - WhateverGreen 1.4.5 ➡️ 1.4.6
#### v1.4.0
- AirportBrcmFixup: set of available drivers depends on the system version(`brcmfx-alldrv`)
- Added `AllowRelocationBlock` quirk for older macOS and safe mode
- Ignore verbs without `alc-verbs` HDEF property or `alcverbs=1` boot-arg
- Enabled loading in safe mode (mainly for AGDP fixes)
- Added boot-arg: `nvram-log=1` (enables AppleEFINVRAM logs)
- Added `BlacklistAppleUpdate` to fix 11.0 broken update optout
- Dropped HII services from OpenDuet improving size and performance
- Fixed patching of injected kexts in mkext
- Added support for launching from relative paths
- Added direct path passing for tools via `RealPath`
- Allowed launching tools and entries in text mode via `TextMode`
- Updated builtin firmware versions for SMBIOS and the rest
- Fixed ACPI patches not applying if tables are in locked memory
- Fixed `DisableSingleUser` quirk when Apple Secure Boot is enabled
- Added `BootstrapShort` to workaround buggy Insyde firmwares
- Changed `Bootstrap(Short)` to choose dynamic entry (requires NVRAM reset)
- Avoided `Boot` prefix in `RequestBootVarRouting` to workaround AMI issues
- Added bootloader patch support in `Booter` `Patch` section
- Fixed startup hang on firmwares allowong reentrance for timer functions
- Made pointer control optional for OpenCanopy via `PickerAttributes`
- Added support for `StartupMute` variable in `PlayChime`
- Added support for per-volume icons for APFS on Preboot
- Removed HII dependency from OpenUsbKbDxe driver
- Fixed undefined behavior in OpenDuet causing random crashes and hangs
- EFI Bump Version:     
  - AirportBrcmFixup 2.1.1 ➡️ 2.1.2
  - AppleALC 1.5.4 ➡️ 1.5.5
  - HibernationFixup 1.3.7 ➡️ 1.3.8
  - Lilu 1.4.9 ➡️ 1.5.0
  - VirtualSMC 1.1.8 ➡️ 1.1.9
  - SMCBatteryManager 1.1.8 ➡️ 1.1.9
  - SMCLightSensor 1.1.8 ➡️ 1.1.9
  - SMCProcessor 1.1.8 ➡️ 1.1.9
  - SMCSuperIO 1.1.8 ➡️ 1.1.9
  - WhateverGreen 1.4.4 ➡️ 1.4.5
#### v1.3.0
- Added missing Secure Boot NVRAM variables required by 11.0
- Added support for `x86legacy` secure boot model
- Fixed Ps2MouseDxe not properly loading under OpenDuetPkg
- Added workaround for read-only errors on some X299 boards
- Added `ForceSecureBootScheme` quirk for virtual machines [Kernel->Quirks->ForceSecureBootScheme]
- Add `ForceResolution` option for enabling non-default resolutions [UEFI->Output->ForceResolution]
- Fixed plist-only kext injection in Big Sur
- Reduce audio lags in SMCDellSensors
- Added the PCI GMCH Graphics Control register definition. (by 0xFireWolf)
- Added a new API to solve multiple symbols in one shot conveniently. (by 0xFireWolf)
- Added a new `RouteRequest` constructor to work with function pointers without additional type castings. (by 0xFireWolf)
- Updated builtin firmware versions (Boot Rom Version: `1554.40.18.0.0` to `1554.40.33.0.0`)
- Increased slide allocation reserve to 200 MB for Big Sur beta 10
- Fixed assert when trying to enable direct renderer on blit-only GOP
- Added support for custom memory properties
- Fixed intermittent 32-bit prelinking failures caused by improper Mach-O expansion 
- Fixed failures in cacheless injection dependency resolution
- Added support for xml comments in plist files
- Fixed `BOOTx64.efi` and `BOOTIA32.efi` convention
- Fixed SMBIOS handling with multiple memory arrays
- Fixed memory array handle assignment on empty slots
- Refactoring, setup next RTC wake manually if IOPMrootDomain::setMaintenanceWakeCalendar was not called before sleep
- Fix an issue with posponed matching (method IOTimerEventSource::timer EventSource could fail)
- EFI Bump Version:     
  - AirportBrcmFixup 2.1.0 ➡️ 2.1.1
  - AppleALC 1.5.3 ➡️ 1.5.4
  - CPUFriend 1.2.2 ➡️ 1.2.3
  - HibernationFixup 1.3.6 ➡️ 1.3.7
  - Lilu 1.4.8 ➡️ 1.4.9
  - VirtualSMC 1.1.7 ➡️ 1.1.8
  - NVMeFix 1.0.4 ➡️ 1.0.5
  - SMCBatteryManager 1.1.7 ➡️ 1.1.8
  - SMCLightSensor 1.1.7 ➡️ 1.1.8
  - SMCProcessor 1.1.7 ➡️ 1.1.8
  - SMCSuperIO 1.1.7 ➡️ 1.1.8
  - WhateverGreen 1.4.3 ➡️ 1.4.4
  - VoodooInput 1.0.8 ➡️ 1.0.9
#### v1.2.1
- Delete `NoTouchID.kext`, no need for this anymore
#### v1.2.0
- Added `LegacyCommpage` quirk to improve pre-SSSE3 userspace compatibility
- Fixed legacy SATA HDDs displaying as external drives in the picker
- Added `ExtendBTFeatureFlags` to properly set `FeatureFlags` for Bluetooth (which substitutes `BT4LEContinuityFixup.kext`) 
- New GUI Picker Theme! Thanks: [blackosx](https://github.com/blackosx) 
- Fixed rare kernel panic in SMCSuperIO
- Workaround displaying `Preboot` due to macOS 11 bug (Display as `Macintosh HD`)
- Add `pci14e4,4331`, `pci14e4,4353` and `pci14e4,4357` into `AirPortBrcmNIC_Injector.kext`
- Do not alloc memory descriptors on systems without `vtd`
- Avoid CPU topology kernel panic
- Fixed plugin debug log not working with Lilu disabled
- Kexts get support on `Xcode 12`
- Updated builtin firmware versions(Boot Rom Version: `1554.40.9.0.0` to `1554.40.18.0.0`)
- Added `ProcessorType` option to `Generic` (Default set to `0`, if you want to custom, go ahead.)
- Add `SystemMemoryStatus` option to `Generic` (Default set to `Auto`, if you don't have memory tab in "about my mac", try this!)
- Fixed `UnblockFsConnect` option not working with APFS JumpStart
- Added IA32 binary variant to the release bundles
- Add `config` with `Secure Boot` & `ECID`
  - full support with `sucure boot`, boot without `snapshot`, (**but you can't directly OTA you system**, cz you `snapshot` **lost!**)
- **set default `config` without `ECID`** 
- EFI Bump Version:     
  - AirportBrcmFixup 2.0.9 ➡️ 2.1.0
  - AppleALC 1.5.2 ➡️ 1.5.3
  - CPUFriend 1.2.1 ➡️ 1.2.2
  - HibernationFixup 1.3.5 ➡️ 1.3.6
  - Lilu 1.4.7 ➡️ 1.4.8
  - VirtualSMC 1.1.6 ➡️ 1.1.7
  - NVMeFix 1.0.3 ➡️ 1.0.4
  - SMCBatteryManager 1.1.6 ➡️ 1.1.7
  - SMCLightSensor 1.1.6 ➡️ 1.1.7
  - SMCProcessor 1.1.6 ➡️ 1.1.7
  - SMCSuperIO 1.1.6 ➡️ 1.1.7
  - WhateverGreen 1.4.2 ➡️ 1.4.3
  - VoodooInput 1.0.7 ➡️ 1.0.8
  - VoodooI2C 2.4.4 ➡️ 2.5.1
- For older version macOS (Not & not gonna test, if you want challenge youself, do it!): 
  - Supports 64-bit macOS `10.6` and newer (`10.9` and newer is recommended)
  - Fixed improper handling of cacheless kexts without an Info.plist
  - Fixed improper calculation of kext startup address for blocking
  - Added 32-bit prelinking support
  - Added mkext 32-bit kext injection (10.4-10.6)
  - Added cacheless 32-bit kext injection (10.4-10.7)
  - Added 32-bit kernel/kext patching/blocking support
  - Fixed issues loading 10.7 EfiBoot
  - Transliterate unicode into ascii
#### v1.1.1
- `USBPower` Fix: Replace `AppleBusPowerController` with `AppleUSBHostResources`
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
