DFU-Bootloader-for-gcc-compiler
===============================
This project contains code examples of a the DFU bootloader modified to be built by gcc. 
gcc_nrf51_bootloader_xxaa.ld is added
PSTORAGE_MIN_BLOCK_SIZE was changed to 0x000c to match with gcc build.

Note that the bootloader address was set to 0x35000 to make enough room for the build with debug option. If you build with release (or all) (that has optimization) you can move the bootloader up to have more room for your application.

Requirements

nRF51 SDK version 6.0.0
nRF51822 Development Kit version 2.1.0 or later
The project may need modifications to work with other versions or other boards.



About this project

This application is one of several applications that has been built by the support team at Nordic Semiconductor, as a demo of some particular feature or use case. It has not necessarily been thoroughly tested, so there might be unknown issues. It is hence provided as-is, without any warranty.

However, in the hope that it still may be useful also for others than the ones we initially wrote it for, we've chosen to distribute it here on GitHub.

The application is built to be used with the official nRF51 SDK, that can be downloaded from https://www.nordicsemi.no, provided you have a product key for one of our kits.

Please post any questions about this project on https://devzone.nordicsemi.com.
