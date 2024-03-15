# BPI-R3-bsp-5.15.77
Supports Banana Pi BPI-R3 (MT7986a) (Kernel 5.15.77)
Step1:
Building and Flashing Instructions for boot loader.
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15$./build.sh
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15$cd SD
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$ ls
BPI-BOOT  bpi-copy  BPI-R3-console-linux-5.15-boot.img  BPI-ROOT
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$ sudo ./bpi-copy BPI-R3-console-linux-5.15-boot.img /dev/sda
SRC=BPI-R3-console-linux-5.15-boot.img
DST=/dev/sda
COPYMODE=imagetodisk
imagetodisk
bpi-copy(v1.3.4(github)), bananapi image & disk tools

Usage: bpi-copy [OPTIONS]...
       bpi-copy [ --help | -v | --version ]
       bpi-copy IMGFILE
       bpi-copy IMGDIR
       bpi-copy IMGFILE DEVICE
       bpi-copy DEVICE IMGFILE

Warning: Try to write BPI-R3-console-linux-5.15-boot.img to BOOTDISK /dev/sda
==============================================================
Saturday 16 March 2024 12:23:34 AM IST
*** start COPY (blue led on ) .....
umount device: /dev/sda
umount /dev/sda5
umount /dev/sda6
==============================================================
IMGFILE=BPI-R3-console-linux-5.15-boot.img
==============================================================
img
1+1 records in
1+1 records out
11009536 bytes (11 MB, 10 MiB) copied, 0.0191967 s, 574 MB/s
10.5MiB 0:00:00 [ 627MiB/s] [   <=>                                                                                                                                                   ]
0+168 records in
0+168 records out
***  end  COPY (blue led off) .....
Saturday 16 March 2024 12:23:35 AM IST
==============================================================
RUNTIME 0:1
OK!! You can remove the BOOTDISK /dev/sda now!!
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$
Step2:
Flashing Instructions for Kernal.
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$ sudo cp -r BPI-ROOT/lib/modules/5.15.77 /media/rangaiah/BPI-ROOT/lib/modules/ 
rangaiah@rangaiah-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$ ls -al /media/rangaiah/BPI-ROOT/lib/modules/5.15.77/kernel
total 24
drwxr-xr-x 6 root root 4096 Mar 16 00:31 .
drwxr-xr-x 3 root root 4096 Mar 16 00:31 ..
drwxr-xr-x 2 root root 4096 Mar 16 00:31 crypto
drwxr-xr-x 7 root root 4096 Mar 16 00:31 drivers
drwxr-xr-x 3 root root 4096 Mar 16 00:31 lib
drwxr-xr-x 7 root root 4096 Mar 16 00:31 net
rangaiah@comcast-HP-ProBook-440-G8-Notebook-PC:~/yocto/code_push/BPI-R3-bsp-5.15/SD$ 
