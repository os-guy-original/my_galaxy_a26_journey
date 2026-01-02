# How To FLash TWRP?
- Grab Odin for your desired system, [Linux](HOW_TO_BOOTLOADER.md#flashing-android-15-with-linux---newbies) `(first 3 steps)` & [Windows](HOW_TO_BOOTLOADER.md#flashing-android-15-with-windows---newbies) `(First step)`.
- You need to have your Bootloader Unlocked. Check how to do it [here](HOW_TO_BOOTLOADER.md).
- Grab latest TWRP for this device from [this page](https://eu.dl.twrp.me/a26x/). `.img.tar` is recommended.
- Enter [download mode](HOW_TO_BOOTLOADER.md#how-to-enter-download-mode) on your phone and press **Vol+** to skip the warnings.
- Plug your phone into your computer.
- Flash the downloaded TWRP file with Odim.
  - Windows:
    Choose AP and select the TWRP file.
  - Linux:
    Enter `odin4 -a /path/to/twrp.img.tar` from terminal.
- Once it finishes, you need to **IMMEDIATELY** enter TWRP with **Power + Vol+** once the `Download Mode` closes. Otherwise the Stock OS will overwrite it with the Stock Recovery.

Congrats! You now have TWRP installed on your device.
You can now reboot to your system.

# FAQ
### It Replaced TWRP with the Stock Recovery Even Though I Entered TWRP Immediately. How Can I Fix it?
Just re-flash TWRP. It's not your fault.

### There Are A Lot Of Mount Errors. How To Fix them?
Samsung made most of the part of the filesystem read-only. You can try re-flashing TWRP again.

### Is There Any OrangeFox Builds For This Device?
I couldn't find any official or unofficial build of OrangeFox for this device. No luck there.
