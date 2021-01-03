# Switchroot-Magisk

This script is from the official [Magisk Github Repo](https://github.com/topjohnwu/Magisk).  I have adjusted the files for arm64 so that the script will work properly. What this does basically is patches your clean boot.img with Magisk. Thanks to **ByLaws** of Switchroot, Magisk has now been fixed in this version where there was a timing issue with sd cards in the past being to slow to probe thus causing hanging with a black screen. You may also flash the magisk zip in twrp.  this just gives you an alternative method if you want to be prerooted before flashing lineage.

# Requirments

Switchroot Android Q On the Nintendo Switch. Linux or Windows with (wsl) on your PC or Laptop.

# Dependencies 

```sudo apt install binfmt-support qemu qemu-user-static```

# Guide

- Git clone or extract the Magisk folder anywhere.
- Copy your clean boot.img into the folder.
- Open terminal in the folder and make the file executable ```chmod +x boot_patch.sh``` 
- Then type ```./boot_patch.sh boot.img```
- Once the script is done you will have a new file called new-boot.img
- Rename new-boot.img back to boot.img and place this in your `switchroot/install folder`
- **(Fresh Install Only)** Open the lineage.zip and place boot.img file at the root of the zip.  This will prevent lineage from overwriting Magisk.
- **(Non Fresh Install)**  Flash in Hekate and reboot. 
- **(Fresh Install Only)** Reboot to twrp and follow the normal installation method of flashing the lineage zip and the open gapps.
- Once you are booted in, open your app drawer and click the new icon.  It will prompt you to update and grant permissions.
- Open the Magisk Manager app and it will prompt you that it needs to reboot.
- Once booted back in you will have root access with no black screen on reboots.

# Alternative

- If you do not want to use this script you can simply flash the ``magisk-debug.zip`` in twrp.  Enjoy!!!!!!
