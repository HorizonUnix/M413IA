<h1 align="center">Hackintosh Guide for ASUS M413IA</h1>
<p align="center">
  <img src="Img\vivobook.png"
       width="400" 
       height="420"/>
</p>

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
| Touchpad | I2C Touchpad |
| Keyboard | PS2 Keyboard |
| Card Reader | microSD Card Reader |
| WebCam | VGA Web Camera |
| Battery | 42WHrs, 3S1P, 3-cell Li-ion |

# Feature
## Working
| Name | Note |  
|    :---:     |    :---   |
| iGPU/APU | ✅ Worked with [NootedRed](https://github.com/ChefKissInc/NootedRed) |
| Audio | ✅ Both speaker and microphone worked with [qhuyduong's Apple ALC fork](https://github.com/qhuyduong/AppleALC), but HDMI is not working (NRed)
| Wifi and BlueTooth | ✅ Worked with [AirportItlwm](https://github.com/OpenIntelWireless/itlwm) and [IntelBluetoothFireware](https://github.com/OpenIntelWireless/IntelBluetoothFirmware) |
| USB | ✅ |
| Function keys | ✅ Fn+F1/F2/F3/F4/F5/F6 |
| TouchPad | Worked with AMD support [Voodool I2C](https://github.com/VoodooI2C/VoodooI2C/commit/f9f703b760711e25bd094058ecb6f19dea52dc5f) kext from ChefKiss |
| Card reader, Type-C | ✅ |
| Sleep | ✅ with some modifications to BIOS and macOS |
| Extra | Battery last for 2 hours, temperature often be between 45ºC to 65ºC |
## Not working
| Name | Note |  
|    :---:     |    :---   |
| Continuity feature | ❌ HandOff, AirDrop not worked on Intel Wi-fi card |

# Preview

<p align="center"><img src="Img\info.png"/></p>

# Thanks to
- [ChefKissInc](https://chefkissinc.github.io)
- Dortania
