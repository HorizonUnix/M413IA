<h1 align="center">Welcome to Installation Guide</h1>

# Preparation 
- A USB drive with sufficient storage (Minimum 8GB)
- A Plist editor (OCAT, ProperTree)

# Building EFI
## OpenCore
OpenCore is essentially a bootloader that is run by the firmware (the BIOS/UEFI) to start macOS.

1. [Download OC](https://github.com/acidanthera/OpenCorePkg/releases)

2. Extract the zip file

3. Copy the EFI folder from `OpenCorePkg/X64/EFI` to a suitable location

4. Remove some unnecessary driver from `EFI/OC/Driver`, and keep '
