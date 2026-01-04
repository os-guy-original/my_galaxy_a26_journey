# How To Install microG Services
As you all know, microG is a FOSS replacement for Google Mobile Services.
Some of the GSIs give it bundled, but some of them don't.

If you're using a vanilla GSI, this guide is for you.

## First Checks
# KernelSU and KernelSU-Next
- Firstly, you need to install your desired KernelSU solution with [this guide](HOW_TO_ROOT.md).
- You need [meta-overlayfs](https://github.com/KernelSU-Modules-Repo/meta-overlayfs) installed. Just flash it with your KernelSU/KernelSU-Next manager.

### Magisk
- Firstly, you need Magisk, which should've been installed on OneUI 7. Check the [guide here](HOW_TO_ROOT.md).
- Once you set it up on OneUI 7 and got the Magisk on the GSI, we can continue.

## Installation
- Grab the `noogle-microg` module from [this page](https://github.com/os-guy-original/noogle-magisk/releases/tag/v3.1).
- Open up your root manager and click on `Modules`.
- Click on `Install` (or `Install from storage` if Magisk) and select the `noogle-microg-vX.Y.zip`.
- It'll gonna ask you to download the **microG Services** and the **Companion App (FakeStore)**. Just click **Vol+** and it'll automatically set it up for you.
- Once it finishes, reboot your device.
- After device is booted up, go to **Modules** page again, and run the **Action** of the module so it'll gonna grant the necessary permssions for the **microG Services**.

# FAQ
### I Installed microG Services But Play Integrity Always Fails, How Can I Fix It?
Try [PIF (Play Integrity Fork)](https://github.com/osm0sis/PlayIntegrityFork) module, it may help you fix the problem.. There's nothing I can do for this issue for now.
> [!IMPORTANT]
> If your GSI already has an option for fixing the Play Integrity, don't install modules like this. They'll going to conflict and may cause more issues.
#### It Crashes When I Install A PIF Solution Via Root Manager, How Can I Fix It?
It's an expected behaviour. Just install some apps like [Droid-ify](https://f-droid.org/packages/com.looker.droidify/) or [F-Droid](https://f-droid.org/en/) itself, add the [microG Repository](https://repo.microg.org/fdroid/repo?fingerprint=9BD06727E62796C0130EB6DAB39B73157451582CBD138E86C468ACC395D14165), and re-install microG Services with the Companion (FakeStore) app without uninstalling them.

### Can I Use It To Replace GApps (Google Apps)?
It's pretty work-in-progress and not expected to success.
