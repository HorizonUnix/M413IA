<h1 align="center">Welcome to Installation Guide</h1>

# Preparation 
- A USB drive with sufficient storage (Minimum 8GB)
- A Plist editor (OCAT, ProperTree)

# Building EFI
## OpenCore
OpenCore is a bootloader that is run by the firmware (BIOS/UEFI) to start macOS

1. [Download OC](https://github.com/acidanthera/OpenCorePkg/releases)
2. Extract the zip file
3. Copy the EFI folder from `OpenCore-x.x.x-RELEASE/X64/EFI` to a suitable location
4. Remove some unnecessary driver from `EFI/OC/Drivers`, and keep only `HfsPlus.efi`, `OpenCanopy.efi`,`OpenRuntime.efi`, `ResetNvramEntry.efi`, `ToggleSipEntry.efi`
5. Copy `OpenCore-x.x.x-RELEASE/Docs/Sample.plist` to `EFI/OC/` and rename to `config.plist`

## Kexts
- Kext stands for Kernel Extension in macOS
- Kexts are bundles (folders) that end with the .kext extension. In macOS is a file but in Windows it's just a folder so if that folder does not end with .kext mean it's not a kext

### Necessary

- [Lilu](https://github.com/acidanthera/Lilu)
- [VirtualSMC](https://github.com/acidanthera/VirtualSMC)

You cannot boot at all without these

### VirtualSMC plug-ins (some are same repo with VirtualSMC)

- `SMCBatteryManager`
- `SMCLightSensor`
- `SMCSuperIO`
- [SMCRadeonSensor](https://github.com/NootInc/RadeonSensor)
- [AsusSMC](https://github.com/hieplpvip/AsusSMC)

### Graphics

- [NootedRed](https://github.com/NootInc/NootedRed)

### Audio

- [qhuyduong's AppleALC fork](https://github.com/qhuyduong/AppleALC/)

### Wi-Fi/Bluetooth

- [AirportItlwm](https://github.com/OpenIntelWireless/itlwm)

### USB

- [USBToolBox](https://github.com/USBToolBox/kext)

### Input

- [VoodooPS2](https://github.com/acidanthera/VoodooPS2)
- [VoodooI2C for AMD by ChefKiss Inc](https://chefkissinc.github.io/Extras/Kexts/VoodooI2C.zip)

In this case M413IA touchpad is HID (aka VoodooI2CHID Satellites)

### Storage

- [NVmeFix](https://github.com/acidanthera/NVMeFix)
- [EmeraldSDHC](https://github.com/acidanthera/EmeraldSDHC)

### Extra

- [AppleMCEReporterDisabler](https://chefkissinc.github.io/Extras/Kexts/AppleMCEReporterDisabler.zip)
- [AmdTscSync](https://github.com/naveenkrdy/AmdTscSync)
- [RestrictEvents](https://github.com/acidanthera/RestrictEvents)
- [ECEnabler](https://github.com/1Revenger1/ECEnabler)
- [BrightnessKeys](https://github.com/acidanthera/BrightnessKeys)

## ACPI

Download (SSDTTime)[https://github.com/corpnewt/SSDTTime]

### Version 0.4
