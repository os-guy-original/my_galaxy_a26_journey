# How To ROOT This Device
## Extracting the AP
- Firstly, you need to unlock your Bootloader using [this guide](HOW_TO_BOOTLOADER.md).
- Then, grab your Android 15 firmware files with [this guide](HOW_TO_BOOTLOADER.md), top part shows you which one you need.
- Extract the firmware and take the `AP` file.
## Installing Magisk
- Grab the magisk manager APK file from [this page](https://github.com/topjohnwu/Magisk/releases/tag/v30.6).
- After that, install it.
- Grab the Android 15 `AP` file that you extracted before and copy it over to your phone.
- Open up magisk manager and select **Install**.
- Select **Patch Method**.
- Select the `AP` file that you copied over from you computer.
- Once the patching finishes, go to you Downloads folder from your phone and grab the `magisk_patchedxxxx.img.tar` file, and copy it to your computer.
- Enter the [download mode](HOW_TO_BOOTLOADER.md#how-to-enter-download-mode) and flash the magisk patched `AP` file with Odin. Learn how to install Odin on your system, [Linux](HOW_TO_BOOTLOADER.md#flashing-android-15-with-linux---newbies) `(first 3 steps)` & [Windows](HOW_TO_BOOTLOADER.md#flashing-android-15-with-windows---newbies) `(First step)`.
  - Windows:
    Choose AP and select the patched `AP` file.
  - Linux:
    Enter `odin4 -a /path/to/magisk_patchedxxxx.img.tar` from terminal.
- When it's done, set-up your phone and you should now a Magisk app on your home screen which'll download the magisk manager.
- Once it's downloaded and installed, it'll ask you to do some required stuff to actually set up root. Just accept it.

# FAQ
### Will The Root Be Deleted When I Install A GSI?
No, it'll not. Now it's a part of your phone ;).

### Will I Be Able To Upgrade To OneUI 8 With This?
OneUI 8 will probably overwrite these but PLEASE don't try that.
