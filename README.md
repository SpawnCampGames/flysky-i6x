![Flysky-i6x Blueprint](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky.png)
# FlySky i6X Radio Data Sheet 🕹️
**Unofficial Flysky-i6x Documentation**

## MCU (Microcontroller Unit)
The radio will either use **STM32** or **APM32** for newer versions.


---
## Basic Specifications 🔧
- **Product Model:** FS- i6X  
- **Channels:** 6-10 (default 6)  
- **Wireless frequency:** 2.408 - 2.475GHz (2.4GHz)
- **Transmission power:** <20 dBm  
- **Wireless protocol:** AFHDS 2A
- **Modulation type:** GFSK
- **Range:** 500 ～ 1500m
- **Bands:** 135
- **Bandwidth:** 500KHz
- **Channel resolution:** 4096  
- **Battery:** 1.5AA * 4  (Rated to 6v)
- **Low voltage alarm:** ＜ 4.2V  
- **Antenna type:** Dual antenna  
- **Display:** STN transflective display, LCD 128x64 dot matrix  
- **Data port:** PS / 2 (PPM)  
- **Temperature range:** -10℃ 60℃
- **Humidity range:** 20% -95%  
- **Dimensions:** 174x89x190mm  
- **Body weight:** 392g

## Switches 💡
The Flyksy-i6x RC Transmitter comes equipped with:

- **SWA:** 2-Position Switch
- **SWB:** 2-Position Switch
- **SWC:** 3-Position Switch
- **SWD:** 2-Position Switch
- **VRA:** Potentiometer (Variable Resistor)
- **VRB:** Potentiometer (Variable Resistor)

### Switch Voltages
| Switch Type | Position | White Wire | Green Wire  | Yellow Wire  |
|-------------|----------|-----------------|-----------------|------------------|
| 3-Way       | Upper    | 2v              | 5v              | 5v               |
| 3-Way       | Middle   | 2v              | 3.5v            | 5v               |
| 3-Way       | Lower    | 2v              | 2v              | 5v               |
|-------------|----------|-----------------|-----------------|------------------|
| 2-Way       | Upper    | 2v             | 5v             | 5v              |
| 2-Way       | Lower    | 2v             | 2v             | 5v              |

## Trainer Port 🎮
- **PS2** / **[S-Video](https://en.wikipedia.org/wiki/S-Video)** style connector

![TrainerPort](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6XTrainerPort.png)
### 3 Pins are used for the Trainer/USB cable:
- **D+** (Data) RX
- **D-** (Data) TX
- **Ground** (GND) Outer ring.

### 4 Connections
![USBCable](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6XTrainerCable.png)
- PIN **1** PPM_OUT
- PIN **2** PPM_IN
- PIN **3** D-
- PIN **4** D+

![USBCable](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6XUsbSide.png)

| ==== | === | === | ====  |
|------|---|----|-----|
| Ground | D+ | D- | Unused  |

---

## Hidden / System Menu
To access the Flysky-i6x System Menu: 
1. Move both gimbals to the **lower left-hand corners.**
2. While holding gimbals in position flip the *Power* switch to **On**

![SystemMenu](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky_SystemMenu.png)

## [OpenI6X](https://github.com/OpenI6X/opentx) *OpenTX* for Flysky FS-i6X 
- turn Flysky-i6x into a programable radio, unlocking its full potential and adding support for additional protocols.
- ❓ [RC-Groups Forum OpenTX for Flysky](https://www.rcgroups.com/forums/showthread.php?3916435-FlySky-I6X-port-of-OpenTX)

## Storage Specifications
| RAM Type          | Used      | Max      | Remaining | Usage    |
|-------------------|-----------|----------|-----------|----------|
| System RAM        | 15,916 B  | 16,384 B | 468 B     | 97%      |
| Flash Memory      | 125,500 B | 131,072 B| 5,572 B   | 95%      |


<sub>*Source: Openi6X GitHub Issues circa v1.11.1*</sub>

## OpenI6X Features
### Comparison with original firmware:
| Feature                | FlySky i6X        | OpenI6X                         |
|------------------------|-------------------|---------------------------------|
| Channels               | 6/10              | 16                              |
| Mixers                 | 3                 | 32                              |
| Models                 | 20                | 16 / unlimited[^1]               |
| Protocols              | AFHDS, AFHDS2A, PPM | AFHDS2A, PPM, CRSF            |
| Trainer                | PPM               | SBUS, PPM                       |
| Logical switches       | x                 | ✓                               |
| Global variables       | x                 | ✓                               |
| Timers                 | x                 | ✓                               |
| Voice annoucements     | x                 | [✓][^2]

[^1]: Unlimited by using USB mass storage mode eeprom backup/restore.
[^2]:  By adding [DFPlayer](https://github.com/OpenI6X/opentx/wiki/Modifications#dfplayer)

### APM32 Tools (For Flashing)
- APM32 Main Site: https://global.geehy.com/
- Driver: https://global.geehy.com/uploads/tool/Dfu%20Driver.zip
- DFU Programmer: https://global.geehy.com/uploads/tool/DFUProgrammer_English.msi

## Restore After Flash
- [Factory Flysky Firmware Update](https://www.flysky-cn.com/i6x-xiazai-1) (exe)
- [Stock Firmware Download](https://github.com/OpenI6X/opentx/files/9311451/flysky_i6x_stock.zip) (zipped .bin)
- [Restore Factory Firmware Flysky I6X](https://github.com/OpenI6X/opentx/discussions/385) (zipped package of .exe, .bin, and programmer)
