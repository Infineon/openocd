### Infineon OpenOCD v5.1.0 Release Notes

lease refer to the README.md for a complete description of the Infineon customized version of OpenOCD. This version of openOCD is released with [ModusToolbox™ Programming tools v1.1.0 ](https://softwaretools.infineon.com/tools/com.ifx.tb.tool.modustoolboxprogtools)

### New Features

- Adds support of PMG1, CCGx, PSoC™ 4 HV, TRAVEO™ T2G Body High, TRAVEO™ T2G Body Entry, FX3G2 and PAG2S product lines and the corresponding kits
- Delivers fixes for various defects
- Syncs with openOCD main branch  

### Known Issues

| ID                                | Known Issue                       | Workaround                          | 
|-----------------------------------|-----------------------------------|-----------------------------------|
|  PROGTOOLS-1425 | A "JTAG-DP STICKY ERROR" message may appear in the IDE when connected via the JTAG interface of a MiniProg4 probe in CMSIS-DAP HID mode.  |  You can safely ignore this error, or switch the MiniProg4 to CMSIS-DAP bulk mode. | 
|  PROGTOOLS-1429 | JTAG performance on MiniProg4 may be significantly slower than SWD.  |  Use the SWD interface if JTAG performance is not acceptable. |
|  PROGTOOLS-1869 | In Linux OS, with KitProg3 in CMSIS-DAP HID mode, a debug session in ModusToolbox can be destroyed if you use the Firmware Loader --device-list command while debugging. This is limitation of hidapi library used on Linux. MacOS and Windows OSs are not impacted. | If you have a debug session running, don't use the firmware loader tool.  |
|  PROGTOOLS-2388 | PSoC 64 Secure MCUs do not support the programming and debugging via JTAG interface.  It is because of the specifics of PSoC 64 MCUs - JTAG pins are configured after unpredictable amount of time after what causes a lot of warnings during programming via JTAG. | Use SWD interface with PSoC 64 Secure MCUs.  |
|  PROGTOOLS-2238 | Unable to acquire PSoC4 target with J-Link probe if target is in PROTECTED state. J-Link probe does not support device acquisition in Test Mode. This prevents invocation of SROM API making it impossible to re-program or erase the chip in PROTECTED state. | The workaround is to unprotect/erase the chip using MiniProg4 or KitProg3 probe.  |
|  PROGTOOLS-2099 | A "Failed to read memory at <address>" message may appear in "Memory View" of IDE when connected via the MiniProg4 probe and try to read memory from invalid address. | You can safely ignore this error.  |
|  PROGTOOLS-3495 | When programming or debugging, you see the following error message:
Error connecting DP: cannot read IDR. This occurs if the debug port is disabled in the BSP for the specific project. | You can enable the debug port for the specific project, or safely ignore this message if the debug port is still disabled. |

### More information

-   [openOCD
    README.md](https://github.com/Infineon/openocd/blob/main/README.MD)    

-   [ModusToolbox Software Environment, Quick Start Guide, Documentation, and
    Videos](https://www.infineon.com/cms/en/design-support/tools/sdk/modustoolbox-software/)

-   [ModusToolbox Device Configurator Tool
    Guide](https://www.infineon.com/ModusToolboxDeviceConfig)

-   [Cypress Semiconductor, an Infineon Technologies Company](https://www.infineon.com/)

© Cypress Semiconductor Corporation (an Infineon company), 2020-2024.

