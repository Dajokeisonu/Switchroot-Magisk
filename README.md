# Magisk-Switchroot-Solution 

This script is from the official Magisk Github Repo https://github.com/topjohnwu/Magisk.  I have adjusted the files for arm64 so that the script will work properly. What this does basically is patches your clean boot.img with Magisk and enables recovery.  The point of this is a work around to the black screen issue on reboot for Nintendo Switch Users flashing Magisk in twrp. The version of Magisk that will be included will be the beta version as it has been found to be the most stable and compatible.

# Requirments

Switchroot Android Q On the Nintendo Switch. Linux on your PC or Laptop.

# Guide

- Git clone or extract the Magisk folder anywhere.
- Copy your clean boot.img into the folder.
- Open terminal in the folder and make the file executable ```chmod +x boot_patch.sh``` 
- Then type ```./boot_patch.sh boot.img```
- Once the script is done you will have a new file called new-boot.img
- If you are getting an error enter ```sudo apt install binfmt-support qemu qemu-user-static``` That should resolve the error you receive.
- Rename new-boot.img back to boot.img and place this in your `switchroot/install folder`
- **(Fresh Install Only)** Open the lineage.zip and place boot.img file at the root of the zip.  This will prevent lineage from overwriting Magisk.
- **(Non Fresh Install)**  Flash in Hekate and reboot. 
- **(Fresh Install Only)** Reboot to twrp and follow the normal installation method of flashing the lineage zip and the open gapps.
- Once you are booted in, open your app drawer and click the new icon.  It will prompt you to update and grant permissions.
- Open the Magisk Manager app and it will prompt you that it needs to reboot.
- Once booted back in you will have root access with no black screen on reboots ENJOY!!!
