# How To Unlock Bootloader On OneUI 8?
This is a bit risky if you don't know what's are the contents of BL and AP files.

> [!IMPORTANT]
> You need the firmwares that have the SAME EXACT bit value. It's the **last 5th** character of the build number, or Version if you're downloading from [SamFW](https://samfw.com/firmware/SM-A266B).
> For example, I used A266BXXS**4**AYG9 as the OneUI 7 build, and A266BXXU**4**BYI2 for OneUI 8. Noticed that the 4s are highlighted? That is the BIT value.
> 
> It'll gonna vanish your data, be careful if you have some personal data left on your device.

# Gathering The Files
- Get the OneUI 7 and OneUI 8 firmwares from a trusted website like SamFW.
- Extract the downloaded ZIPs.
- Put them into seperate folders to **NOT MIX THEM**.
- Install the [Magisk](https://github.com/topjohnwu/Magisk/releases) app on your device.

# How To Extract `.tar.md5` Files?
- You need to rename the file name to remove the `.md5` extension from it.
  - Example: `AP_xxx.tar.md5` -> `AP_xxx.tar.md5`
- Then use your favorite `.tar` extractor to extract the contents of your zipped file.

# Unlocking Bootloader On OneUI 7 First
- Follow (bootloader unlocking process)[/HOW_TO_BOOTLOADER.md] of OneUI 7 `line 13`.
- Reboot to your system and go back to your computer.

# Preparing The OneUI 8 Firmware
> [!WARNING]
> READ THE FOLLOWING CAREFULLY!

- Go to the contents of the extracted OneUI 7 folder.
- Extract the BL zip.
- Go to the contents of the extracted OneUI 8 folder.
- Do the same extraction for the `BL_xxxxx.tar.md5` and remove the `sboot.img.lz4` inside the contents.
- Grab the `sboot.img.lz4` FROM **OneUI 7** BL contents and put it into the **OneUI 8** BL contents. This'll basically swap the sboot of OneUI 8 with the OneUI 7.
- Now, extract the **OneUI 8** AP zip and delete the `vbmeta.img.lz4` inside of it.
- Grab the `vbmeta.img.lz4` from the **OneUI 8** BL, and **MOVE** it over to the **OneUI 8** AP folder.
- Now, select every content of the **OneUI 8** AP folder with CTRL + A, and TAR it with your favorite TAR archiver.
  - Don't forget that you MUST NOT see another folder tree when you directly opened the TAR archive. You know what I mean.
- Now, move this AP zip to your phone and patch it with Magisk. This is required to patch that `vbmeta.img` file.
- Once it patches, move the patched AP file over to you computer and extract it.
- Grab the `vbmeta.img` from the magisk patched AP folder and move it over to the **OneUI 8** BL folder.
- Now TAR your **tinkered OneUI 8** BL folder by selecting everything in it with CTRL + A.
- Now you can just delete the magisk patched AP completely.
- Now zip the **OneUI 8 tinkered** AP folder by selecting everything in it with CTRL + A.
- And lastly use your favorite Samsung flash tools to flash the tinkered AP, BL with the stock CP, CSC.

# FAQ
## The OEM Unlock Option Is Missing In Developer Options
This can mean 2 things:
- Either your bootloader is locked again, which can happen if you didn't follow the tutorial carefully.
- Or even the OneUI doesn't know what's happening, which is my case right now. Don't worry, the bootloader is actually unlocked.
  - If that's the case, a simple reboot can make it appear back.

## The OEM Unlock Is NOT Grayed Out, What's Happening?
On EVERY Android, grayed out OEM Unlock option means the Bootloader is already unlocked, so you can't even disable OEM Unlock.
But in our case, the option is NOT grayed out, but enabled.

What to do? Yeah, just don't touch it. Your bootloader is already unlocked if you see the orange state text on boot.
