# grub2_vhd
grub2.02 with vhd support (read only)


This is GRUB 2, the second version of the GRand Unified Bootloader.
GRUB 2 is rewritten from scratch to make GNU GRUB cleaner, safer, more
robust, more powerful, and more portable.

See the file NEWS for a description of recent changes to GRUB 2.

See the file INSTALL for instructions on how to build and install the
GRUB 2 data and program files.

See the file MAINTAINERS for information about the GRUB maintainers, etc.

If you found a security vulnerability in the GRUB please check the SECURITY
file to get more information how to properly report this kind of bugs to
the maintainers.

Please visit the official web page of GRUB 2, for more information.
The URL is <http://www.gnu.org/software/grub/grub.html>.

More extensive documentation is available in the Info manual,
accessible using 'info grub' after building and installing GRUB 2.

There are a number of important user-visible differences from the
first version of GRUB, now known as GRUB Legacy. For a summary, please
see:

  info grub Introduction 'Changes from GRUB Legacy'
  
  Example usage:
  
  after booting into grub:
  
  ```insmod vhd```
  
  ```vhd vhd0 test.vhd```
  
  ```ls (vhd0,msdos1)/ ```
  
or

  ```set root=(vhd0,msdos1)/ ```
  
  ```linux /vmlinuz ... ```
  
  ```initrd /initrd.img ```
  
  ```boot```
  
  ... but in this case we have to take care of the initramfs to mount the vhd as the root file system to continue boot on the vhd.
  
  
