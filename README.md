<h1 align="center">Hackintosh for ASUS M413IA</h1>
<p align="center">
  <img src="Img/vivobook.png"
       width="300" 
       height="320"/>
</p>

> [!NOTE]
> - This model contains a CNVi only key lock or something like a whitelist, so it will never support **BCM94360NG**. If you still want to have some continuity features, then try the DW series from Dell, like DW1560 or DW1820A.
# Specification

| Hardware | Name |  
|    :---:     |    :---:   |
| Model  | Asus VivoBook M413IA EK480T |  
| Processor | AMD Ryzen® 5 4500U | 
| Ram | 8GB Onboard |
| Graphics | AMD Radeon® Vega 6 |
| Storage | Intel® SSDPEKNW512G8 |
| Wi-Fi Card | Intel® Wi-Fi 6 AX200 |
| Audio | Realtek ALC256 |
| Display | 14.0-inch FHD (1920 x 1080) IPS Non-Touch Screen |
| Touchpad | ELAN I2C Touchpad (ELAN WBF included) |
| Keyboard | PS2 Keyboard (ASUS ATKD) with no keyboard backlight |
| Card Reader | microSD Card Reader |
| Camera | VGA Web Camera 720p HD |
| Battery | 42WHrs, 3S1P, 3-cell Li-ion |

## Extra Hardware
> [!NOTE]
> This hardware is not included in the default spec of M413IA.

| Hardware | Name |  Note |
|    :---:     |    :---:   |  :---:   |
| Storage | WDC PC SN730 SDBQNTY-512G-1001 | M413IA has 2 NVMe M.2 slots, so I filled the last M.2 slot with this. |
| Wi-Fi Card | Dell DW1820A ( BCM94350ZAE ) | Replacement for Intel® Wi-Fi 6 AX200 (not recommended to use). |
# Features
## Working
| Name | Note |  
|    :---:     |    :---:   |
| SMBios | MacBookPro16,3 |
| iGPU/APU | ✅ Works with NootedRed |
| Audio | ✅ Both internal speaker and microphone work, but HDMI is not working (NRed) |
| Wifi and BlueTooth | ✅ Works with AirportItlwm and IntelBluetoothFirmware |
| USB | ✅ |
| Function keys | ✅ F1/F2/F3/F4/F5/F6/F7/F8/F10/F12 and Fn+Esc work |
| TouchPad | ✅ Works with AMD support Voodool I2C kext from ChefKiss |
| Card reader, Type-C port | ✅ |
| Sleep | ✅ with some modifications to BIOS |
| Battery | ✅ Battery Health and Charging Limit feature |
| Extra | Battery lasts for 2 hours, temperature often is between 45ºC to 65ºC |

## Not working
| Name | Note |  
|    :---:     |    :---:  |
| Apple DRM | ❌ Apple TV, anything that related to DRM |
| Continuity feature | ❌ Only HandOff and some features only work with Intel WiFi card |
| VCN 2 | ❌ VCN 2 (Video Core Next 2) is not working, but VCN 1 is |

## Function keys

> [!NOTE]
> Like when using Windows, you can use Function keys without Fn+Fx since I've mapped them all.
> - Fn+Esc is also working.
> - F1: Mute
> - F2: Decrease volume
> - F3: Increase volume
> - F4: Decrease brightness
> - F5: Increase brightness
> - F6: On/Off Touchpad
> - F7: Limit Battery Charging 80%/100%
> - F8: Show Desktop
> - F9: N/A
> - F10: On/Off Display
> - F11: N/A
> - F12: Play/Pause

# Preview
<img src="Img/info.png" alt="About This Mac" title="About This Mac">
