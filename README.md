![Flysky-i6x Blueprint](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky.png)
# FlySky i6X RC Radio Datasheet 🕹️
> 📝 **Unofficial Flysky-i6X Documentation**

## Factory Specifications 
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

---

## MCU (Microcontroller Unit)

The Fkysky-i6X RC Transmitter utilizes a 32-bit ARM microcontroller for functionallity. Depending on the date of purchase, it will use either:
- The [STM32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) Series MCU
- The [APM32](https://global.geehy.com/product/fourth/M0+) Series MCU

> [!IMPORTANT]  
> Some newer versions of the radio use the APM32 as a replacement for the STM32.  
> Although, they may return to using the STM32 it's possible that they continue to use the APM32.  
> Except for different DFU drivers they function the same and can, both, have their firmware flashed with binary programmers.
>
> [How to identify which microcontroller your Flysky-i6x has?](https://github.com/SpawnCampGames/flysky-i6x/blob/main/DISASSEMBLY.md#microcontroller-mcu-identification)

---

## Storage
| RAM Type          | Space     | 
|-------------------|-----------|
| System RAM        | 16,384 B  |
| Flash Memory      | 131,072 B |

## Auxillary Switches
The Flyksy-i6x RC Transmitter comes equipped with:
- **SWA:** 2-Position Switch
- **SWB:** 2-Position Switch
- **SWC:** 3-Position Switch
- **SWD:** 2-Position Switch
- **VRA:** Potentiometer (Variable Resistor)
- **VRB:** Potentiometer (Variable Resistor)

![Flysky-i6X Switch Front](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Flysky_Switch_Front.png)  
Radio Front

![Flysky-i6X Switch Back](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Flysky_Switch_Back.png)  
Radio Back

### Switch Voltages
| Switch Type | Position | White Wire | Green Wire  | Yellow Wire  |
|-------------|----------|------------|-------------|--------------|
| 3-Way       | Upper    | 2v         | 5v          | 5v           |
|             | Middle   | 2v         | 3.5v        | 5v           |
|             | Lower    | 2v         | 2v          | 5v           |
|-------------|----------|------------|-------------|--------------|
| 2-Way       | Upper    | 2v         | 5v          | 5v           |
|             | Lower    | 2v         | 2v          | 5v           |


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

---
## Hidden Menus
### Hidden Factory / System Menu

![SystemMenu](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky_SystemMenu.png)

To access the Flysky-i6X System Menu: 
1. Move both gimbals to the **lower left-hand corners.**
2. While holding gimbals in position flip the *Power* switch to the **On** position.

This menu is useful for calibrating the gimbals on the Factory Firmware, testing inputs, or checking out the firmware.
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

### Firmware Update Mode

![FirmwareUpdateMode](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/Blueprint_Flysky_FirmwareUp.png)

To access the Flysky-i6X Firmware Update Mode:
1. Push the two **left-hand** trim buttons towards the LCD screen.
2. While holding both trim buttons in position flip the *Power* switch to the **On** position.

---

## Custom Firmware 💻
### OpenI6X (*OpenTX* for Flysky FS-i6X)
Turn Flysky-i6x into a fully programmable radio - Unlocking its full potential & adding support for additional protocols. [^1]
- [OpenI6X](https://github.com/OpenI6X/opentx) (Official Github Page)
- [OpenTX for Flysky-I6X](https://www.rcgroups.com/forums/showthread.php?3916435-FlySky-I6X-port-of-OpenTX) (Official RCGroups Forum Post)

> [!WARNING]  
> Always create a backup of your factory firmware before flashing custom firmware!
> Use caution when modifying your radio's firmware!
> Done improperly can cause the device to become bricked!

### Storage (OpenI6X / OpenTX Firmware)
| RAM Type          | Used      | Max      | Remaining | Usage    |
|-------------------|-----------|----------|-----------|----------|
| System RAM        | 15,916 B  | 16,384 B | 468 B     | 97%      |
| Flash Memory      | 125,500 B | 131,072 B| 5,572 B   | 95%      |

<sub>*Source: Openi6X GitHub Issues circa v1.11.1*</sub>

### OpenI6X Features
Comparison with original firmware:
| Feature                | FlySky i6X        | OpenI6X                         |
|------------------------|-------------------|---------------------------------|
| Channels               | 6/10              | 16                              |
| Mixers                 | 3                 | 32                              |
| Models                 | 20                | 16 / Unlimited [^2]             |
| Protocols              | AFHDS, AFHDS2A, PPM | AFHDS2A, PPM, CRSF            |
| Trainer                | PPM               | SBUS, PPM                       |
| Logical switches       | ❌                | ✔️                               |
| Global variables       | ❌                | ✔️                               |
| Timers                 | ❌                | ✔️                               |
| Voice annoucements     | ❌                | ✔️ [^3]                          |

### APM32 Tools and Drivers (For Flashing)
- APM32 Main Site: https://global.geehy.com/
- Driver: https://global.geehy.com/uploads/tool/Dfu%20Driver.zip
- DFU Programmer: https://global.geehy.com/uploads/tool/DFUProgrammer_English.msi

** For the STM32 MCU, Links from the [OpenI6X Github Page](https://github.com/OpenI6X/opentx) work.
*** APM32 Links can/could be broken or invalid hence why I linked the sources above.

### Compatible Modules and Receivers for FlySky-i6X with (OpenTX) 📡
- [View List](https://github.com/SpawnCampGames/flysky-i6x/blob/main/COMPATIBILITY-LIST.md)

### Restore After Flash
- [Factory Flysky Firmware Update](https://www.flysky-cn.com/i6x-xiazai-1) (exe)
- [Stock Firmware Download](https://github.com/OpenI6X/opentx/files/9311451/flysky_i6x_stock.zip) (zipped .bin)
- [Restore Factory Firmware Flysky I6X](https://github.com/OpenI6X/opentx/discussions/385) (zipped package of .exe, .bin, and programmer)

---

> [!TIP]
> **Contributions:**  
> Either direct or indirect,
> I'd like to **Thank** all the great sources through-out the web on the Flysky-i6 and i6x.  
> You can find info and links to all of them here: 📌[Flysky I6X Help](https://github.com/SpawnCampGames/flysky-i6x/blob/main/HELP.md) page.

---

<p align="center"><img src="https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_Radio_ON.png"></p>
<p align="center">- SpawnCampGames Electronics Division 2024 -</p>

[^1]: Not officially supported by Flysky. Community run open-source firmware.
[^2]: Unlimited by using USB mass storage mode eeprom backup/restore.
[^3]: By adding [DFPlayer](https://github.com/OpenI6X/opentx/wiki/Modifications#dfplayer)
