# How To Install ADB & Fastboot?
## Linux
### Official Distro Packages
- Search for terms like `android-tools`, `adb`, `fastboot` with your package manager.
- Find the appropriate ones, and install them.
### From Google
- Here's a quick command for you:
  ```bash
  curl -L https://dl.google.com/android/repository/platform-tools-latest-linux.zip -o pt.zip && unzip -j pt.zip "platform-tools/adb" "platform-tools/fastboot" && sudo mv adb fastboot /usr/bin/ && rm pt.zip
  ```
  It'll gonna download `platform-tools-latest-linux.zip` as `pt.zip`, extract it, put the `adb` and `fastboot` to `/bin` with sudo, and remove the `pt.zip` later.

## Windows
### Winget
- Open up powershell and paste this:
  ```PowerShell
  winget install --id=Google.PlatformTools -e
  ```
  > Didn't tested it because i don't have a Windows machine.
### From Google
- Open up Powershell and type:
  ```PowerShell
  $url = "https://dl.google.com/android/repository/platform-tools-latest-windows.zip"; $dest = "$env:USERPROFILE\platform-tools"; $zip = "$env:TEMP\pt.zip"; Invoke-WebRequest -Uri $url -OutFile $zip; Expand-Archive -Path $zip -DestinationPath $env:USERPROFILE -Force; $oldPath = [Environment]::GetEnvironmentVariable("Path", "User"); if ($oldPath -notlike "*$dest*") { [Environment]::SetEnvironmentVariable("Path", "$oldPath;$dest", "User") }; Remove-Item $zip; Write-Host "Success! Refresh your terminal to use adb." -ForegroundColor Green
  ```
  It'll download `platform-tools-latest-windows.zip` as `pt.zip`, extract it to your user folder, add the new `platform-tools` directory to your **User PATH** so you can run them from anywhere, and remove the ``pt.zip`` later.
---
Done! You've successfully installed ADB & Fastboot!
