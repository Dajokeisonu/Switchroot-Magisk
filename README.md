# Magisk-Switchroot-Solution

This script is from the offical magisk github.  I have adjusted the files for arm 64 so that the script will work properly. What this does basically is patches your clean boot.img with magisk and enables recovery.  The point of this is a work around to the black screen issue on reboot for Nintendo Switch Users flashing magisk in twrp. 

# Guide

- git clone or extract the magisk folder anywhere.
- copy your clean boot.img into the folder
- open terminal in the folder and make the file executable chmod +x boot_patch.sh 
- then type ./boot_patch.sh boot.img
- Once the script is done you will have a new file called new-boot.img
- rename new-boot.img back to boot.img and place this in your switchroot/install folder
- (Fresh Install Only) open the lineage zip that was created and place the boot.img file at the root of the zip as well.  This will prevent lineage from overwriting magisk
- flash in hekate and reboot (Non Fresh Install)
- (Fresh Install) reboot to twrp and follow the normal installation method of flashing the lineage zip and the gapps.
- once you are booted in, open your app drawer and click the new icon.  It will prompt you to update and grant permissions.
- open the magisk manager app and it will prompt you that it needs to reboot.
- once booted back in you will have root access with no black screen on reboots ENJOY
