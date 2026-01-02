# How To Unlock Bootloader?
Firstly, we all know that Samsung removed Bootloader Unlocking from OneUI 8.
But, this phone came with OneUI 7 (Android 15), so, if you updated to OneUI 8, just go back to OneUI 7.
You need to be careful, the OneUI 7 Firmware that you'll download MUST have the same `Bit Value` as your current OneUI 8 one.

To check your current `Bit Value`:
- Go to: Settings > Phone information > Software information > Build number
- Check the **LAST 5TH** character. In our case, it might be **4**. If it's 5, you can not go back to Android 15 **with this method**.
- If it's 4, you're good to go, just download the latest [Android 15 update for Galaxy A26 5G from SamFw](https://samfw.com/firmware/SM-A266B) which has the **same Bit Value with your device**.
- Once it's downloaded, extract it.
- Finally, Flash it with your desired software, Odin is recommended.

Set-up your Android 15, enable `Developer Mode` and toggle on `OEM Unlcoking` from there.
Once it's toggled, enter [download mode](#how-to-enter-download-mode) BUT don't press **Vol+** once the warning appears.
You need to **HOLD Vol+** instead of pressing. It'll ask you to unlock the bootloader, just press **Vol+** to accept it.
> [!IMPORTANT]
> It'll gonna vanish your data, be careful if you have some personal data left on your device.
It'll gonna reboot and you'll need to Set-up your device.

## How To Enter Download Mode
- Power off your device.
- Get a working cable.
- Plug one side of it to your computer.
- Hold **Vol+** and **Vol-** on your phone at the same time.
- Plug in the cable to phone and you should see the Download mode warning screen appear. You can now release the keys.
- Click **Vol+** again to enter Download mode.

## Flashing Android 15 with Linux - Newbies
- Grab [OdinV4](https://github.com/Adrilaw/OdinV4/releases/tag/v1.0).
- Extract it, give it execution permissions and copy it to one of the executable folders from `PATH`.
  ```bash
  chmod +x /path/to/extracted/binary/odin4
  # Then
  sudo cp /path/to/extracted/binary/odin4 /bin
  ```
- Test with `odin4 -h`.
- If it shows the help text, that means the installation was successful.
- You need to install `android-udev` package from your distribution packages.
  > For example, on arch linux: `sudo pacman -S android-udev`
- Enter [download mode](#how-to-enter-download-mode) on your phone.
- Plug in your cable and flash everything with odin4.
  ```bash
  odin4 -a /Path/To/AP -b /Path/To/BL -c /Path/To/CP -s /Path/To/CSC # !! NOT HOME_CSC !!
  ```
- Wait for the tool to finish flashing.
- After the flash is complete, wait for your device to Boot up, it might take several minutes.
- Set-up your device and make sure that you enabled **USB Debugging** and **OEM Unlcoking** from `Developer Options`.

## Flashing Android 15 with Windows - Newbies
- Grab the OdinV3 from [this website](https://www.odinflash.com/).
- Enter [download mode](#how-to-enter-download-mode) on your phone.
- Plug in your cable and flash everything with Odin:
  > AP - AP_xxxxxx.md5.tar
  > 
  > BL - BL_xxxxxx.md5.tar
  > 
  > CP - CP_xxxxxx.md5.tar
  > 
  > CSC - CSC_xxxxxxx.md5.tar
- Wait for the tool to finish flashing.
- After the flash is complete, wait for your device to Boot up, it might take several minutes.
- Set-up your device and make sure that you enabled **USB Debugging** and **OEM Unlcoking** from `Developer Options`.
