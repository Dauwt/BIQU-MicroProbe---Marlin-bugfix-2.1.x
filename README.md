# BIQU-MicroProbe - Marlin-bugfix-2.1.x
Config files for Marlin bugfix 2.1.x Firmware that uses the BIQU MicroProbe V1 and V2 for an Ender-3!

## Step-by-Step
### Connecting the BIQU MicroProbe to your MotherBoard
* Start by connecting your MicroProbe to your board, **you can see how to do it [here](https://github.com/bigtreetech/MicroProbe/blob/master/MicroProbe%20V2%20User%20Manual_20240330.pdf)**, but instead of connecting the **Probe and GND Pins** to the default pins, connect them **to the Z_EndStop pins in your MotherBoard!**
* The connections stays the same for both tthe BIQU MicroProbe V1 and V2!

### Building and Compiling the Firmware
* **First clone/download [this repository](https://github.com/MarlinFirmware/Marlin/tree/bugfix-2.1.x)**(Marlin bugfix 2.1.x), then clone/download the corresponding files for your MicroProbe from **[here](config)!**
* Then go to the **Marlin folder** inside of the Repository you cloned/downloaded and **copy and paste the files you have just downloaded(replace the old files with the new files)!**
#### Changing the firmware for your needs
* You can **adapt the firmware for your needs**, but the main thing you need to do is **change the chip type inside the platformio.ini file** so it can compile in the right way for your Motherboard!
* For that change this:
    ```
    [platformio]
    src_dir      = Marlin
    boards_dir   = buildroot/share/PlatformIO/boards
    default_envs = STM32G0B1RE_btt  // Change this for your own Motherboard chip type!
    include_dir  = Marlin
    extra_configs =
        Marlin/config.ini
        ini/avr.ini
        ini/due.ini
        ini/esp32.ini
        ini/features.ini
        ini/hc32.ini
        ini/lpc176x.ini
        ini/native.ini
        ini/samd21.ini
        ini/samd51.ini
        ini/stm32-common.ini
        ini/stm32f0.ini
        ini/stm32f1-maple.ini
        ini/stm32f1.ini
        ini/stm32f4.ini
        ini/stm32f7.ini
        ini/stm32h7.ini
        ini/stm32g0.ini
        ini/teensy.ini
        ini/renamed.ini
        
* After this you can **compile the firmware** using, **for example**, **PlatformIO** in VS Code!

### Loading the Firmware to your printer
* First take your **SD Card** and **copy and paste the firmware.bin file outputed from the compilation!**
* Then **plug your SD Card** into your printer and **turn the Printer on!**
* **No more steps your done!**

## Using the Precompiled firmware
* Keep in mind that the **precompiled firmware provided** in this repository **only works with BTT SKR Mini E3 V3.0!**
* If you're **using this Motherboard** then all you have to do is **download the right .bin file from [here](bin)(one uses the BIQU MicroProbe V1 and the other the V2)!**
* And then **copy and paste** it to your SD Card with this name, **'firmware.bin'**, then plug and turn on your printer! 
* **No more steps your done!**

## 
**Firmware modified by dauwt**🥸
