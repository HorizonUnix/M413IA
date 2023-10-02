<h1 align="center">Welcome to Installation Guide</h1>

# Preparation 
- A USB drive with sufficient storage (Minimum 8GB)
- A Plist editor (OCAT, ProperTree)
- Make sure Python is installed
  
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

- [`Lilu`](https://github.com/acidanthera/Lilu)
- [`VirtualSMC`](https://github.com/acidanthera/VirtualSMC)

You cannot boot at all without these

### VirtualSMC plug-ins (some are same repo with VirtualSMC)

- `SMCBatteryManager`
- `SMCLightSensor`
- `SMCSuperIO`
- [`SMCRadeonSensor`](https://github.com/NootInc/RadeonSensor)
- [`SMCProcessorAMD`](https://github.com/Lorys89/SMCProcessorAMD)
- [`AsusSMC`](https://github.com/hieplpvip/AsusSMC)

### Graphics

- [`NootedRed`](https://github.com/NootInc/NootedRed)

### Audio

- [`qhuyduong's AppleALC fork`](https://github.com/qhuyduong/AppleALC/)

### Wi-Fi/Bluetooth

- [`AirportItlwm`](https://github.com/OpenIntelWireless/itlwm)

### USB

- [`USBToolBox`](https://github.com/USBToolBox/kext)

### Input

- [`VoodooPS2`](https://github.com/acidanthera/VoodooPS2)
- [`VoodooI2C for AMD by ChefKiss Inc`](https://chefkissinc.github.io/Extras/Kexts/VoodooI2C.zip)

In this case M413IA touchpad is HID (aka `VoodooI2CHID` Satellites)

### Storage

- [`NVmeFix`](https://github.com/acidanthera/NVMeFix)
- [`EmeraldSDHC`](https://github.com/acidanthera/EmeraldSDHC)

### Extra

- [`AppleMCEReporterDisabler`](https://chefkissinc.github.io/Extras/Kexts/AppleMCEReporterDisabler.zip)
- [`AmdTscSync`](https://github.com/naveenkrdy/AmdTscSync)
- [`RestrictEvents`](https://github.com/acidanthera/RestrictEvents)
- [`ECEnabler`](https://github.com/1Revenger1/ECEnabler)
- [`BrightnessKeys`](https://github.com/acidanthera/BrightnessKeys)

After download all kext, please drag to `EFI/OC/Kexts` and do a clean snapshot using ProperTree.
## ACPI

Download [`SSDTTime`](https://github.com/corpnewt/SSDTTime)

1. Run .bat file
2. Press `P` to dump DSDT
3. Press `1` then `C`
4. Press `3`
5. Press `4` then `B`
6. Press `5`
7. Press `8`
8. Press `0` then pick the one that has `19`
9. Press `A` then `A` again

After that, run `PatchMerge.bat` and follow the intrusction, also only drag the .aml file not .dsl to `EFI/OC/ACPI` and never drag `DSDT.aml`.
## Configuration
Enable these:
- `Booter->Quirks->AvoidRuntimeDefrag`
- `Booter->Quirks->DevirtualiseMmio`
- `Booter->Quirks->DiscardHibernateMap`
- `Booter->Quirks->EnableSafeModeSlide`
- `Booter->Quirks->ProvideCustomSlide`
- `Booter->Quirks->SetupVirtualMap`
- `Booter->Quirks->RebuildAppleMemoryMap`
- `Booter->Quirks->SignalAppleOS`
- `Booter->Quirks->SyncTimePermissions`

- `Kernel->Quirks->DisableLinkeditJettison`
- `Kernel->Quirks->PanicNoKextDump`
- `Kernel->Quirks->PowerTimeoutKernelPanic`
- `Kernel->Quirks->ProvideCurrentCpuInfo`
- `Kernel->Emulate->DummyPowerManagement`
 
- `Misc->Boot->HideAuxillary` (press space will show extra option)
- `Misc->Boot->PollAppleHotKeys`
- `Misc->Boot->ShowPicker`
- `Misc->Boot->HibernateSkipsPicker`
- `Misc->Security->AuthRestart`
- `Misc->Security->AllowSetDefault`
- `Misc->Security->BlacklistAppleUpdate`
etc...
# Installer
## Online
We will use the `macrecovery.py` included in OpenCorePkg folder (`OpenCorePkg/Utilities/macrecovery`)

- macOS Catalina (10.15): `python3 macrecovery.py -b Mac-CFF7D910A743CAAF -m 00000000000PHCD00 download`
- macOS Big Sur (11): `python3 macrecovery.py -b Mac-2BD1B31983FE1663 -m 00000000000000000 download`
- macOS Monterey (12): `python3 macrecovery.py -b Mac-E43C1C25D4880AD6 -m 00000000000000000 download`
- macOS Ventura (13): `python3 macrecovery.py -b Mac-B4831CEBD52A0C4C -m 00000000000000000 download`
- macOS Sonoma (14): ...


### ETA: 2 weeks
### Version 0.5
### Credits
- ChefKissInc
- Dortania
