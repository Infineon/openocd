# Infineon OpenOCD v5.20.0 Release Notes

Please refer to the README.md for a complete description of the Infineon customized version of OpenOCD. This version of OpenOCD is released with [ModusToolbox Programming Tools v2.0.0](https://softwaretools.infineon.com/tools/com.ifx.tb.tool.modustoolboxprogtools).

## New Features

- Updated default adapter speed to 16 or 12 MHz for SWD and to 8 MHz for JTAG for all targets. (PROGTOOLS-8301)
- Switched to libusb 1.30. (PROGTOOLS-6673)
- Added support for Ubuntu 26.04.

## Supported Devices/Probes Added

- Added CYT2B6/CYT2B7 target configuration. (PROGTOOLS-8112)
- Added PSC3M3/P5 targets support. (PROGTOOLS-8294)
- Added PSoC 4100SL series support. (PROGTOOLS-8528)

## Known Issues

| ID | Known Issue | Workaround |
|----|-------------|------------|
| PROGTOOLS-1425 | A "JTAG-DP STICKY ERROR" message may appear in the IDE when connected via the JTAG interface of a MiniProg4 probe in CMSIS-DAP HID mode. | You can safely ignore this error, or switch the MiniProg4 to CMSIS-DAP bulk mode. |
| PROGTOOLS-1429 | JTAG performance on MiniProg4 may be significantly slower than SWD. | Use the SWD interface if JTAG performance is not acceptable. |
| PROGTOOLS-1869 | In Linux OS, with KitProg3 in CMSIS-DAP HID mode, a debug session in ModusToolbox can be destroyed if you use the Firmware Loader `--device-list` command while debugging. This is a limitation of the hidapi library used on Linux. macOS and Windows are not impacted. | If you have a debug session running, do not use the Firmware Loader tool. |
| PROGTOOLS-2388 | PSoC 64 Secure MCUs do not support programming and debugging via the JTAG interface. This is due to the specifics of PSoC 64 MCUs — JTAG pins are configured after an unpredictable amount of time, which causes warnings during programming via JTAG. | Use the SWD interface with PSoC 64 Secure MCUs. |
| PROGTOOLS-2238 | Unable to acquire PSoC 4 target with a J-Link probe if the target is in PROTECTED state. The J-Link probe does not support device acquisition in Test Mode. This prevents invocation of SROM API, making it impossible to re-program or erase the chip in PROTECTED state. | Unprotect/erase the chip using a MiniProg4 or KitProg3 probe. |
| PROGTOOLS-2099 | A "Failed to read memory at \<address\>" message may appear in the "Memory View" of the IDE when connected via the MiniProg4 probe and attempting to read memory from an invalid address. | You can safely ignore this error. |
| PROGTOOLS-3495 | When programming or debugging, the following error message may appear:<br>`Error connecting DP: cannot read IDR`<br>This occurs if the debug port is disabled in the BSP for the specific project. | Enable the debug port for the specific project, or safely ignore this message if the debug port is intentionally disabled. |

## More Information

- [OpenOCD README.md](https://github.com/Infineon/openocd/blob/main/README.MD)
- [ModusToolbox Software Environment, Quick Start Guide, Documentation, and Videos](https://www.infineon.com/cms/en/design-support/tools/sdk/modustoolbox-software/)
- [ModusToolbox Device Configurator Tool Guide](https://www.infineon.com/ModusToolboxDeviceConfig)
- [Infineon Technologies AG](https://www.infineon.com/)

© Infineon Technologies AG, 2020-2026. This document is the property of Infineon Technologies AG and its affiliates ("Infineon").
