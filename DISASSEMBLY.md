## To Disassemble the Flysky-i6X
> May void the warranty.

![Flysky-i6X Disassembly](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_Disassembly.png)

1. Remove the (4) Phillips-head screws on the back of the radio.
2. Carefully pry the housing apart by starting at the bottom.
3. Angle the bottom of the back cover outwards to help release the (4) plastic tabs within the handle.
4. (Optional) Disconnect the wiring (**Power** [P2] & **Trainer Port** [P1]) between the two parts to completely seperate the two halves.*

> [!WARNING]
> The back cover is connected by (2) wired connections.  
> Avoid forcefully prying apart the housing as it may damage the wiring and / or circuit board.

> [!CAUTION]
> Remove the **AA** batteries or the **Power** [P2] connector to help prevent accidental short-circuits and / or other issues to the exposed circuitry.

## Microcontroller (MCU) Identification
Which microcontoller does my Flysky-i6X have?
> Gain access to the radio's mother-board and inspect chipset at the location marked on diagram.

![Flysky-i6X MCU Location](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_MCU_Location.png)

- If labelled STM32 with markings of the **ST MicroElectronics** and **ARM** logos:  
Your radio is equipped with the [STM32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) Series MCU

- If labelled APM32 with markings of the **Gheey** and **arm** logos:  
Your radio is equipped with the [APM32](https://global.geehy.com/product/fourth/M0+) Series MCU

![Possible Flysky-i6X MCUs](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_MCU.png)
