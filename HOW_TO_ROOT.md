# How To ROOT This Device
You got 2 options here.
- KernelSU - Runs inside kernel, less detectable - **RECOMMENDED**
- Magisk - User Space

## KernelSU
> [!IMPORTANT]
> The method used below is to install a GKI (Generic Kernel Image).
>
> They'll be only used for testing purposes, starting from version 3.0.0 and KernelSU team states that there'll be no future release for GKIs.
>
> The method shown below worked fine on this device, and it's the recommended way for fixing Play Integrity.

- You need a GSI installed on your system. This method does and will not work on OneUI. [See how](HOW_TO_GSI.md).
- You need to grab the `Anykernel3` version that matches your current kernel. Here are the [releases](https://github.com/tiann/KernelSU/releases/tag/v2.1.2).
  - For example, the kernel version that my device uses is `5.15.153-android13-8-gb57bf46f2a43`, so I need to download this specific release: `AnyKernel3-android13-5.15.153_2024-09.zip`.
  - Basically, run `adb shell uname -a` on your computer while your device is plugged in, you should see something like this:
    ```bash
    # It's usually like this:
    Linux localhost 5.15.153-android13-8-gb57bf46f2a43 #1 SMP PREEMPT Fri Nov 14 09:12:15 UTC 2025 aarch64 Toybox
  
    # Kernel version is: 5.15.153-android13-8-gb57bf46f2a43
    ```
  - `5.15.153` is the actual Linux kernel version and `android13` is the Android version, don't worry, it's not your OS version.
  - So we need to get `AnyKernel3-android13-5.15.153_2024-09.zip`, the `2024-09` part is the security patch date. You can simply ignore that.
- Once the `.zip` downloaded, head over to the **TWRP**. Follow [this guide](HOW_TO_TWRP.md) if you didn't flashed TWRP yet, or OneUI vanished the previous one.
- Enter **ADB Sideloading** from **Advanced** section.
- Flash `Anykernel3` with this command:
  ```bash
  adb sideload /path/to/Anykernel3-xxxxxxxx.zip`
  ```
- Once it's done, reboot to System.
- Download and install KernelSU manager app, and you shoud be able to use KernelSU now!

## Magisk
### Extracting the AP
- Firstly, you need to unlock your Bootloader using [this guide](HOW_TO_BOOTLOADER.md).
- Then, grab your Android 15 firmware files with [this guide](HOW_TO_BOOTLOADER.md), top part shows you which one you need.
- Extract the firmware and take the `AP` file.
### Installing Magisk
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
### Will The Magisk Get Deleted When I Install A GSI?
No, it'll not. Now it's a part of your phone ;).

### Will I Be Able To Upgrade To OneUI 8 With This?
OneUI 8 will probably overwrite Magisk but PLEASE don't try that.
