# nslu2_wheezy
Debian Wheezy on NSLU2 with 4GB USB flash

Download and extract files.

From other Linux system:
Write NSLU2 "bios" by network to NSLU internal 8MB flash:
 1. Start recovery mode on NSLU2 (with reset button)
 2. Flash "bios": upslug2 nslu2.wheezy_flash.image
    
Write filesystem to USB flash:

dd if=./nslu2.wheezy_fs.image of=/dev/sdb

Current settings:

Network: dhcp

User: root; password: root

User: pi; password: raspberry

recomended to use disk UUID:

 edit /etc/fstab
 
 update-initramfs -u

 ![alt text](https://rdzdx.github.io/nslu2_wheezy/picture.jpg)
