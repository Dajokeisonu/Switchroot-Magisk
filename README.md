# Magisk-Switchroot-Solution

This script is from the official Magisk Github Repo https://github.com/topjohnwu/Magisk.  I have adjusted the files for arm64 so that the script will work properly. What this does basically is patches your clean boot.img with Magisk and enables recovery.  The point of this is a work around to the black screen issue on reboot for Nintendo Switch Users flashing Magisk in twrp. The version of Magisk that will be included will be the beta version as it has been found to be the most stable.

# Guide

- Git clone or extract the Magisk folder anywhere.
- Copy your clean boot.img into the folder.
- Open terminal in the folder and make the file executable ```chmod +x boot_patch.sh``` 
- Then type ```./boot_patch.sh boot.img```
- Once the script is done you will have a new file called new-boot.img
- If you are getting an error it is possible you are missing dependencies ```sudo apt install binfmt-support qemu qemu-user-static``` This should resolve the `` cannot execute binary file: Exec format error``
- Rename new-boot.img back to boot.img and place this in your switchroot/install folder
- (Fresh Install Only) Open the lineage zip that was created and place the boot.img file at the root of the zip as well.  This will prevent lineage from       overwriting Magisk.
- Flash in Hekate and reboot (Non Fresh Install)
- (Fresh Install) reboot to twrp and follow the normal installation method of flashing the lineage zip and the open gapps.
- Once you are booted in, open your app drawer and click the new icon.  It will prompt you to update and grant permissions.
- Open the Magisk Manager app and it will prompt you that it needs to reboot.
- Once booted back in you will have root access with no black screen on reboots ENJOY!!!
