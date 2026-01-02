# How To Install microG Services
As you all know, microG is a FOSS replacement for Google Mobile Services.
Some of the GSIs give it bundled, but some of them don't.

If you're using a vanilla GSI, this guide is for you.
## First Checks
- Firstly, you need Magisk, which should've been installed on OneUI 7. Check the [guide here](HOW_TO_ROOT.md).
- Once you set it up on OneUI 7 and got the Magisk on the GSI, we can continue.

## Installation
- Grab the `noogle-microg` module from [this page](https://github.com/os-guy-original/noogle-magisk/releases/tag/v3.0).
- Open up Magisk manager and click on `Modules`.
- Click on `Install from storage` and select the `noogle-microg-vX.Y.zip`.
- It'll gonna ask you to download the **microG Services** and the **Companion App (FakeStore)**. Just click **Vol+** and it'll automatically set it up for you.
- Once it finishes, reboot your device.
- After device is booted up, go to **Magisk Modules** page again, and run the **Action** of the module so it'll gonna grant the necessary permssions for the **microG Services**.

# FAQ
### I Installed microG Services But Play Integrity Always Fails, How Can I Fix It?
Try [PIF (Play Integrity Fork)](https://github.com/osm0sis/PlayIntegrityFork) module, it may help you fix the problem.. There's nothing I can do for this issue for now.
> [!IMPORTANT]
> If your GSI already has an option for fixing the Play Integrity, don't install modules like this. They'll going to conflict and may cause more issues.

### Can I Use It To Replace GApps (Google Apps)?
It's pretty work-in-progress and not expected to success. It may even be removed.
Use at your own risk.
