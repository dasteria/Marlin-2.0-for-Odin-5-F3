# Mks-Robin-Nano-Marlin2.0-Firmware for FoKoos Odin 5-F3 3D Printer

## Features
The firmware of MKS Robin Nano, based on [Marlin2.0.x](https://github.com/MarlinFirmware/Marlin), adds the [LittlevGL](https://github.com/littlevgl/lvgl) which adds a colourful GUI and touch screen suport.  

![](https://github.com/makerbase-mks/Mks-Robin-Nano-Marlin2.0-Firmware/blob/master/Images/MKS_Robin_Nano_printing.png)

## Build
As the firmware is based on Marlin2.0.x which is built on the core of PlatformIO, the buid compiling steps are the same as Marlin2.0.x. You can directly using [PlatformIO Shell Commands](https://docs.platformio.org/en/latest/core/installation.html#piocore-install-shell-commands), or using IDEs contain built-in PlatformIO Core(CLI), for example, [VSCode](https://docs.platformio.org/en/latest/integration/ide/vscode.html#ide-vscode) and [Atom](https://docs.platformio.org/en/latest/integration/ide/atom.html). VSCode is recommended.

## About the gcode file preview
The images should be added to gcode file when slicing, and MKS has developed the [plugin for Cura](https://github.com/makerbase-mks/mks-wifi-plugin) to make it.

## About the image conversion
- Open [LVGL online image converter tool](https://lvgl.io/tools/imageconverter). 
- Open bmp images.
- Enter the saved file name.
- Choose color format:True color.
- Choose file output format:Binary RGB565.
- Start convertion.
- Save bin file.
- Copy the converted bin file to the assets folder.
- Copy the assets folder to the SD card.
- SD card is connected to the motherboard, and you can see the update interface after powering on.

## Firmware Can be run on Robin Nano V1.x / V2.x boards and V3.x boards
## MKS Robin Nano V1.x build and update firmware

1. Build config:
     
- platformio.ini: 
     
     default_envs = mks_robin_nano35    
- Configuation.h:  
     #define SERIAL_PORT 3  
     #define MKS_ROBIN_TFT35  
     #define MOTHERBOARD BOARD_MKS_ROBIN_NANO  
     #define TFT_LVGL_UI  
     #define TOUCH_SCREEN  

2. Update firmware:
   
- Enter the `.pio\build\mks_robin_nano35` directory, copy the `assets` folder and `Robin_nano35.bin` to the sd card
- Insert SD card to the motherboard, and you can see the update interface after power on.   

## For more information and configuration options, please refer to Robin nano series Wiki
- [MKS Robin Nano V1.x Wiki](https://github.com/makerbase-mks/MKS-Robin-Nano-V1.X/wiki). 
- [MKS Robin Nano V2.x Wiki](https://github.com/makerbase-mks/MKS-Robin-Nano-V2.X/wiki). 
- [MKS Robin Nano V3.x Wiki](https://github.com/makerbase-mks/MKS-Robin-Nano-V3.X/wiki).

## More information about the Robin Nano V1.X
Please refer to [MKS Robin Nano github](https://github.com/makerbase-mks/MKS-Robin-Nano-V1.X).
