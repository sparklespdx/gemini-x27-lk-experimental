# Gemini PDA Bootloader

This is a fork of the [official LK bootloader from Planet Computers.](https://github.com/dguidipc/gemini-lk). I'm going to use it to do some experiments, perhaps with booting from the SD card.

Master branch is for my version, the x27 with the new LCM. I make no promises about other hardware revisions.

### Build instructions

There are multiple ways to build this, I cross compile on x86 using the prebuilt Android NDK Standalone toolchain from Google:

https://dl.google.com/android/repository/android-ndk-r10e-linux-x86_64.zip

SHA Hash is: f692681b007071103277f6edc6f91cb5c5494a32

I add the libraries to my PATH, then I run:

`cd lk && make aeon6797_6m_n`

### Changing the boot image

The files for the splash images are `lk/dev/logo/fhd/fhd_uboot.bmp` and `lk/dev/logo/fhd/fhd_kernel.bmp`. GIMP seems to export to BMPs just fine, but remember to check the "Do not write color space information" box under "Compatibility Options" when you export (it cuts down on the size). The images are 2160x1080.
