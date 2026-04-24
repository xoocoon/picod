# picod

This is a fork of [picod](https://github.com/joan2937/picod), fixing bugs in the picod daemon.

While the daemon can be built and used independently of [gpiosvr](https://github.com/xoocoon/gpiosvr), it was developed and tested in the scope of that project.

# Installation

Original build instructions can be found on the picod page [Download & Install](https://abyz.me.uk/picod/download.html).

The first step is to install the Pico SDK as described on the Raspberry page [The C/C++ SDK](https://www.raspberrypi.com/documentation/microcontrollers/c_sdk.html). As an ARM architecture is required, it is recommended to install the SDK on a Raspberry Pi.

In April 2026, the [SDK installation script](https://raw.githubusercontent.com/raspberrypi/pico-setup/master/pico_setup.sh) has proven functional on a Raspberry Pi 5.

Building the daemon is simple:

```
git clone https://github.com/xoocoon/picod
cd picod/DAEMON
cmake .
make
```

The `picod.uf2` file should have been generated directly in the `DAEMON` directory.

To transfer it to the target Pico device, hold down its “BOOT/SEL” button, while connecting it to the Raspberry Pi via USB. In a file browser of your choice, copy the file to the `RPI-RP2` volume. After the automatic reboot, the Pico will run the daemon.
