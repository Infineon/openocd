Infineon Customized OpenOCD
===============

### Overview

The Open On-Chip Debugger (OpenOCD) is free software that provides debugging, in-system programming, and boundary-scan testing.

To work with ModusToolbox and Infineon devices and probes, Infineon has modified OpenOCD.
Supported devices with kits based on them:
- AIROC™ CYW20809 Bluetooth® LE system on chip
- PSOC™ 6 and PSOC™ 64
- PSOC™ 4, PSoC™ 4 HVPA, PSOC™ 4 HVMS
- PMG1, CCGx
- CYW4390x
- XMC7xxx, XMC5xxx
- TRAVEO™ T2G Body High
- TRAVEO™ T2G Body Entry
- TRAVEO™ T2G Cluster 6M/4M MCU
- TRAVEO™ T2G Cluster Entry 4M (CYT2CL)
- FX3G2 and FX3G3
- PAG2S
- PSOC™ Control C3
- PSOC™ 4100T Plus
- PSOC™ Edge E84
Supported probes:
-  SEGGER J-Link (with libusbK driver)
-  Infineon KitProg3 on-board programmer
-  Infineon MiniProg4 standalone programmer
-  FTDI-based adapter on CYW954907AEVAL1F / CYW943907AEVAL1F kits
From the [release page](https://github.com/Infineon/openocd/releases), download and unpack the appropriate archive for your OS. Source for these executables are available on the [ModusToolbox FOSS page](https://www.infineon.com/cms/en/design-support/software/free-and-open-source-software-foss/modustoolbox-foss-packages/)

If you want to update ModusToolbox to use this release, replace the contents of the */ModusToolbox/tools_3.x/openocd* folder with the downloaded package from the release page. Otherwise just put the tool in any convenient location.

On the different versions of macOS, you may see a dialog that Apple cannot check this package for malicious software. If this happens, please follow [instructions](https://support.apple.com/guide/mac-help/open-an-app-by-overriding-security-settings-mh40617/14.0/mac/14.0) from Apple.

This software component is licensed under GNU General Public License v2

### FOSS usage

Infineon maintains a collection of [Free and Open Source Software](https://www.infineon.com/cms/en/design-support/software/free-and-open-source-software-foss/modustoolbox-foss-packages/) (FOSS) packages. It includes OpenOCD.

### More Information

[openOCD Release Notes](https://github.com/Infineon/openocd/blob/main/RELEASE.MD)

OpenOCD documentation in [HTML](http://openocd.org/doc/html/index.html) or [PDF](http://openocd.org/doc/pdf/openocd.pdf).

© Infineon Technologies AG, 2020-2026. This document is the property of Infineon Technologies AG and its affiliates ("Infineon").