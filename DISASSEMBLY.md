## To Disassemble the Flysky-i6X 🛠️
> Disassembly of your radio *may* void the warranty. ⚠️

![Flysky-i6X Disassembly](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_Disassembly.png)

**Instructions:**
1. Remove the (4) Phillips-head screws on the back of the radio.
2. Carefully pry the radio's housing apart starting at the bottom.
3. Angle the bottom of the back cover outwards to help release the (4) plastic tabs within the handle.
4. (Optional) Disconnect the wiring (**Power** [P2] & **Trainer Port** [P1]) to completely seperate the two halves.*

**For reassembly follow in reverse.**

> [!WARNING]
> The back cover is connected by (2) wired connections.  
> Avoid forcefully prying apart the housing as it may damage the wiring and / or circuit board.

> [!CAUTION]
> Remove the **AA** batteries or the **Power** [P2] connector to prevent accidental short-circuits and / or other issues to the exposed circuitry.

## Microcontroller (MCU) Identification
How to know which microcontoller your Flysky-i6X has?
> Gain access to the radio's mother-board and inspect the chipset at the location marked on the diagram below.

![Flysky-i6X MCU Location](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_MCU_Location.png)

![Possible Flysky-i6X MCUs](https://github.com/SpawnCampGames/flysky-i6x/blob/main/doc/FlyskyI6X_MCU.png)

#### APM32 *(Left)*
- If labelled APM32 with markings of the **Gheey** and **arm** logos:  
▶️ Your radio is equipped with the [APM32](https://global.geehy.com/product/fourth/M0+) Series MCU

#### STM32 *(Right)*
- If labelled STM32 with markings of the **ST MicroElectronics** and **ARM** logos:  
▶️ Your radio is equipped with the [STM32](https://www.st.com/en/microcontrollers-microprocessors/stm32-32-bit-arm-cortex-mcus.html) Series MCU



> [!Note]
> Both MCUs provide identical functionallity for the Flysky-i6X.  
> Both MCUs can be flashed with custom firmware.
