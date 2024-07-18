Infineon Customized OpenOCD
===============

### Overview

The Open On-Chip Debugger (OpenOCD) is free software that provides debugging, in-system programming, and boundary-scan testing.

To work with ModusToolbox and Infineon devices and probes, Infineon has modified OpenOCD to support:
- Devices from PSoC 61/62/63/64 product lines and the corresponding kits
- Devices from PSoC 4000S, PSoC4100S, PSoC 4100S Plus and PSoC 4500 product lines and the corresponding kits
- KitProg3 onboard programmer
- MiniProg4 standalone programmer

From the [release page](https://github.com/Infineon/openocd/releases), download and unpack the appropriate archive for your OS. Source for these executables are available on the [ModusToolbox FOSS page](https://www.infineon.com/cms/en/design-support/software/free-and-open-source-software-foss/modustoolbox-foss-packages/)

If you want to update ModusToolbox to use this release, replace the contents of the */ModusToolbox/tools_3.x/openocd* folder with the downloaded package from the release page. Otherwise just put the tool in any convenient location.

On the different versions of macOS, you may see a dialog that Apple cannot check this package for malicious software. If this happens, please follow [instructions](https://support.apple.com/guide/mac-help/open-an-app-by-overriding-security-settings-mh40617/14.0/mac/14.0) from Apple.

This software component is licensed under GNU General Public License v2

### FOSS usage

Infineon maintains a collection of [Free and Open Source Software](https://www.infineon.com/cms/en/design-support/software/free-and-open-source-software-foss/modustoolbox-foss-packages/) (FOSS) packages. It includes OpenOCD.

### More Information

[openOCD Release Notes](https://github.com/Infineon/openocd/blob/main/RELEASE.MD)

OpenOCD documentation in [HTML](http://openocd.org/doc/html/index.html) or [PDF](http://openocd.org/doc/pdf/openocd.pdf).

© Cypress Semiconductor Corporation (an Infineon company), 2020-2024.