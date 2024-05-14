![Flysky-i6x Blueprint](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky.png)
# FlySky i6X Radio Datasheet 🕹️
> **Unofficial Flysky-i6x Documentation**

## Basic Specifications 
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

## MCU (Microcontroller Unit)
The Fkysky-i6x transmitters utilize a 32-bit ARM microcontroller for functionallity. Depending on when you purchased your radio it will use either:
- The [STM32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) Series MCU
- The [APM32](https://global.geehy.com/product/fourth/M0+) Series MCU

> [!NOTE]  
> Newer versions of the radio use the APM32 as a replacement for the STM32.
> Although, they may return to using the STM32 it's possible that they continue to use the APM32.
> Except different DFU drivers, they function practically identical, and both can have their firmware flashed using binary programmers.

[How to identify which microcontroller your Flysky-i6x has?](https://github.com/SpawnCampGames/flysky-i6x/blob/main/MCU.md)

## Storage Specifications
| RAM Type          | Space     | 
|-------------------|-----------|
| System RAM        | 16,384 B  |
| Flash Memory      | 131,072 B |

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

> VCC to all Terminals when Radio is **Off**

## Trainer Port / USB Connection 🎮
- **PS2** / **[S-Video](https://en.wikipedia.org/wiki/S-Video)** style connector

![TrainerPort](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6XTrainerPort.png)
### Flysky-i6X Trainer-Port Pinout

| Pin Number | Function | 
|------------|----------|
| 1          | PPM_OUT  | 
| 2          | PPM_IN   | 
| 3          | D-       | 
| 4          | D+       | 

### 3 pins / wires are used for the Trainer/USB cable:
- **D+** (Data) RX
- **D-** (Data) TX
- **Ground** (GND) Outer ring

![USBCable](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6XUsbSide.png)

| ==== | === | === | ====  |
|--------|----|----|---------|
| Ground | D+ | D- | Unused  |

## Hidden Factory / System Menu
This menu is useful for calibrating the gimbal sticks on the Factory Firmware, testing inputs, or checking out the firmware.
- Sticks adjust (Adjust gimbal sticks / reset center position) 
- Def sticks mode (Set default gimbal stick configuration / Mode1, Mode2 for example)
- Key test (Screen for testing buttons on the radio)
- LCD test (Sets screen solid black for a moment / Test for identifying bad pixels)
- LCD brightness (Allows you to change LCD brightness / Technically the contrast)
- Bind (Binds to available receivers / RXs)
- RF frequency (Radio frequency settings / Allows selecting left or right antenna)
- Voltage adjust (Adjust supply voltage readings)
- Firmware ver. (Displays firmware version)
- Firmware update (Enters firmware update mode)
- Restart 

To access the Flysky-i6x System Menu: 
1. Move both gimbals to the **lower left-hand corners.**
2. While holding gimbals in position flip the *Power* switch to the **On** position.

![SystemMenu](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky_SystemMenu.png)

## Firmware Update Mode
To access the Flysky-i6x Firmware Update Mode:
1. Push the two **left-hand** trim buttons towards the LCD screen.
2. While holding both trim buttons in position flip the *Power* switch to the **On** position.

![FirmwareUpdateMode](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky_FirmwareUp.png)

## Custom Firmware 💻
### OpenI6X (*OpenTX* for Flysky FS-i6X)
Turn Flysky-i6x into a fully programmable radio, Unlocking its full potential & Adding support for additional protocols.
- [OpenI6X](https://github.com/OpenI6X/opentx) (Official Github Page)
- [OpenTX for Flysky-I6X](https://www.rcgroups.com/forums/showthread.php?3916435-FlySky-I6X-port-of-OpenTX) (Official RCGroups Forum Post)

> [!WARNING]  
> Always create a backup of your factory firmware before flashing custom firmware!
> Use caution when modifying your radio's firmware!
> Done improperly can cause the device to become bricked!

## Storage Specifications (OpenI6X / OpenTX Firmware)
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
