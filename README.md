# rpi-bootstrap

Minimal configuration utility for Raspberry Pi first time setup, by overlaying files into the rootfs of a raw OS image.

Does not require building a new Raspbian image, which can 20-30 minutes depending on the hardware and network (using [pi-gen](https://github.com/Rpi-Distro/pi-gen)).

Currently tested running `rpi-bootstrap` on a Fedora 30 host, to modify a Raspbian lite image.

Connect an SD card to flash the modified image to, and execute the following from this repository's top level directory:

`${sd_device}` is where the SD card is mounted, e.g. `/dev/sda` on my laptop. You can find this out by running `lsblk`.

```
sd_device= # Set to the device shown by lsblk with the SD card plugged in
./rpi-bootstrap ${sd_device}
```

Based on commands given at http://kmdouglass.github.io/posts/create-a-custom-raspbian-image-with-pi-gen-part-1/.
