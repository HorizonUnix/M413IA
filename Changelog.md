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
