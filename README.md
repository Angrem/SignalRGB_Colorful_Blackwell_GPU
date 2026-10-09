# SignalRGB Colorful Blackwell GPU Plugin

SMBus plugin adding SignalRGB support for Colorful iGame RTX 50-series (Blackwell) graphics cards.

## Test Environment & Compatibility
* **Tested On:** Windows 11
* **Tested App Version:** SignalRGB `2.5.74`
* **Verified Working GPU:** Colorful iGame GeForce RTX 5080 Ultra OC V2-V (`SubDevice 0x1511`)

> **Note:** This plugin should work across other listed Colorful RTX 50-series GPUs using the same SMBus frame protocol, but it remains **untested** on those specific models.

## Known Limitations
* **Single Zone Only (1 LED):** The hardware SMBus microcontroller on these GPUs accepts a fixed 11-byte command payload at register `0x0B`. Extending packet length to address multiple LED segments causes buffer clipping errors. The entire lighting strip is controlled as a single unified color zone.

## Supported Devices

| GPU Model | Vendor ID | Device ID | SubDevice ID | SubVendor ID |
| Colorful 5060Ti iGame Ultra White DUO OC 16G | `0x10DE` | `0x2D04` | `0x1500` | `0x7377` |
| Colorful 5060Ti iGame Ultra White OC 16G | `0x10DE` | `0x2D04` | `0x1501` | `0x7377` |
| Colorful 5070 iGame Ultra White OC 12G | `0x10DE` | `0x2F04` | `0x1500` | `0x7377` |
| Colorful 5070 iGame Ultra White OC | `0x10DE` | `0x2F04` | `0x1501` | `0x7377` |
| Colorful 5070 iGame Vulcan | `0x10DE` | `0x2F04` | `0x1201` | `0x7377` |
| Colorful 5070Ti iGame Ultra White OC | `0x10DE` | `0x2c05` | `0x1500` | `0x7377` |
| Colorful 5070Ti iGame Ultra White OC | `0x10DE` | `0x2c05` | `0x1501` | `0x7377` |
| Colorful 5080 iGame Ultra White OC | `0x10DE` | `0x2c02` | `0x1500` | `0x7377` |
| Colorful 5080 iGame Ultra OC | `0x10DE` | `0x2c02` | `0x1511` | `0x7377` |
| Colorful 5080 iGame Ultra White OC | `0x10DE` | `0x2c02` | `0x1501` | `0x7377` |
| Colorful 5080 Advanced OC | `0x10DE` | `0x2c02` | `0x1401` | `0x7377` |

## Installation

1. Download `Colorful_Blackwell_GPU.js` from this repository.
2. Place the file into your local plugins directory:
   `C:\Users\<YourUsername>\Documents\WhirlwindFX\Plugins\Colorful`
3. Restart SignalRGB completely (exit from tray).
