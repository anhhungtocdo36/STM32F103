# STM32F103C8T6
Included is a demo project that flashes a led connected to PC13 (ready to run on an STM32 Mini Dev Board STM32F103C8T6). 

## Installing & using ST-Link v2 to flash STM32 targets on Linux

In order to install the ST-Link utilities on Linux (Ubuntu) we have to make sure to have the libusb-dev library installed. On Ubuntu systems you can install the necessary library by executing:
```
sudo apt-get install libusb-1.0-0-dev
```
We will now download, build and install the latest ST-Link utilities from scratch
```
git clone https://github.com/texane/stlink stlink.git
cd stlink
make
#install binaries:
sudo cp build/Release/st-* /usr/local/bin
#install udev rules
sudo cp etc/udev/rules.d/49-stlinkv* /etc/udev/rules.d/
#and restart udev
sudo restart udev
```

## Flashing target

Install gcc cross compiler
````
sudo apt install gcc-arm-none-eabi
````
Run command to build and flash the device
````
make flash
````

## Hardware
![alt tag](https://raw.githubusercontent.com/ubogdan/STM32F103C8T6/master/jtag/STM32F103C8T6-1.jpg)

![alt tag](https://raw.githubusercontent.com/ubogdan/STM32F103C8T6/master/jtag/STM32F103C8T6-2.jpg)

