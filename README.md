# nslu2_wheezy
Debian Wheezy on NSLU2 with 4GB USB flash drive (cleaned some big packages like Exim, Apache2, etc).

Download and extract files to computer.

From other Linux system:
Write NSLU2 firmware image by network to NSLU2 internal 8MB flash:
 1. Start recovery mode on NSLU2 (power on NSLU2 with hold reset button ~10sec )
 2. Flash firmware: upslug2 -i nslu2.wheezy_flash.image  (or with Upgrade_207_XP from Windows XP)
    
On other Linux system attach 4GB or bigger USB flash drive and write filesystem to it:

dd if=./nslu2.wheezy_fs.image of=/dev/sdb

Current settings:

Network: dhcp

User: root; password: root

User: pi; password: raspberry

recomended to change fstab from /dev/sda to disk UUID:

edit /etc/fstab
and 
update-initramfs -u


NSLU2_V23R63.zip - original Linksys firmare if you want restore to build it. (Dont use EraseAll tool !!! Flash firmware with upslug2 or Upgrade_207_XP)

![alt text](https://rdzdx.github.io/nslu2_wheezy/picture.jpg)
