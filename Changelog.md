## [2.9.0]
- Support macOS Sequoia
  
## [2.8.0]

### Extend support patch to `v3.0.0`
## [2.7.0]

- Fix USB kext issue
- Remove HPET patches
- Update kexts
- Remove cosmetic SSDT
- Update kernel patches
## [2.6.0]

- Change Apple ALC layout-id to `56`
- Fix USB mapping
- Remove some useless kext
- Use `itlwm.kext` instead of `AirportItlwm.kext` (AirportItlwm.kext` sucks)
- Fix OC files
## [2.5.0]

- Update Kexts
- Use TSC Sync kext from ChefKiss
### For the L2T dream!
## [2.4.0]

- Update OC to `1.0.0`
- Update NootedRed
- Remove BRCM card support
## [2.3.0]

- Add base Intel card kext
- Auto Apple Safe Sleep instead of normal sleep
- Add work-around for Win/Mac dual booting
## [2.2.0]

- Provide proper support for Apple's Safe Boot (Hibernate mode 3)
- Update `ChefKiss`'s kext
- Support [GenericNVMeName](https://github.com/AppleOSX/GenericNVMeName)
- Force ASPM to disable with DW 1820A (similar to Apple's native Airport card) to fix issues with Bluetooth, WiFi, and random freezing
## [2.1.0]

### 2.1.0
- Update Kexts
- Completely remove DP injections for DW 1820A
- Fix Kernel Panic on DW 1820A
### 2.0.1
- Remove unused kext
- Add some cosmetic SSDTs
- Remove unused Kernel patches
- Fix BlueTooth issue
- Support [PatchSonomaWiFiOnTheFly](https://github.com/AppleOSX/PatchSonomaWiFiOnTheFly)
- Proper USB mapping
- Use another layout-id for ALC
## [2.0.1]

- Remove unused kext
- Add some cosmetic SSDTs
- Use USBToolBox instead of USBMap due to lacks of XHCI controllers
- Remove unused Kernel patches
## [2.0.0]

- Remove built-in UMAF tools
- Remove ELAN Fingerprint for power saving and prevent some random wake up
- Rework themes
- Remap ATKD keyboard
- Fix ACPI patch
- Add TRIM patch
- Add BT delay
### This update brings a native Mac experience 
## [1.9.0]

- Fix USB issues
- Fix Sleep issues
- Remove legacy patch about USB and Sleep
- Remove legacy patch for NootedRed
- Proper USB mapping
- Fix PCI injection 
- Update NootedRed kext
## [1.8.0]

- Optimize EFI
## [1.7.0]

- Native Sleep
- Fix ACPI
- Fix Patch
- Proper DP inject
- Fix Kexts
## [1.6.0]

- Fix Kernel Panic on DW 1820A by set a delay for native BCM kext
- Update NootedRed
- Remove CPUName patch on RE due to some issues with AMD (again)
- Set UpdateSMBios to Custom for OEM software on Windows
## [1.5.0]

- Fix Airdrop issue, WiFi on DW 1820A
- Proper support for SDCard
- Fix USBMap
- Support WiFi on Sonoma (please turn off IO kexts if using it below Sonoma)
- Fix Kexts
- Update NootedRed

## [1.4.0]

- Fix Airdrop issue on DW 1820A now fully functional
- Update NootedRed
- Use custom AMDRyzenPP kext for disable CPB only on macOS
- Fix an issue related to PCI
- Update Patches
- Update ACPI

## [1.3.0]

- Rewrite whole EFI
- Dropped support for macOS BS, Catalina
- Removed `AMDRyzenCPUPowerManagement.kext` and `SMCAMDProcessor.kext` both now replace with [UXTU4Mac](https://github.com/gorouflex/RielUXTU4Mac)
- Use another way to map USB
- Fix ACPI
- Fix Patches
- Fix black screen when system is wake by external keyboard
- Now user have to manually add their Intel WiFi card kext

## [1.2.0]

## Changes
### v.1.2.0 bring to you a big update and support more hardware for hackintosh
### Disable by default:
### Some unsupported BCM cards
- `BrcmPatchRam3.kext`
- `BrcmFirmwareData.kext`
- `AirPortBrcmFixup.kext` and related bundle
### BCM Sonoma Wifi Bundle fixup:
- `AirPortBrcmFixup.kext` and related bundle
- `IO80211Family.kext`
- `IO80211FamilyLegacy.kext` and related bundle
- `AMFIPass.kext`
- Block kext section
### Kexts
- Add custom `AMDRyzenCPUPowerManagement.kext` and `SMCAMDProcessor.kext` ( Still need more testing, recommend to disable both of it )
### Other changes
- Optimized EFI by some small changes


## [1.1.1]

### Changes
- Remove RE due some issues with AMD
- Change UpdateBiosMode to `Create` since `Custom` can be broke in the future

## [1.1.0]
### Changes
- Fixed random AppleUSB kernel panic after wake from sleep
- Fixed Fn keys do not work after wake from sleep
- Removed some useless SSDTs and ACPI Patches
- Changed F7 keys from `Increase/Decrease keyboard backlight` to `Limit battery charging 80%/100%`
