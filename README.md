# OpenBSD-router-for-raspberry-pi-4

OpenBSD router for the rasberry pi 4

WAN is asix 88179 usb ethernet

LAN is built in ethernet raspberry pi 4

Download install80.img

burn to the sd card with raspberry pi imager 

https://www.mtsapv.com/rpi4obsd/

On the resulting screen, select the OpenBSD installer USB device. The boot process will continue.

Install OpenBSD as per normal.

At the end, when the install process asks:

Exit to (S)hell, (H)alt or (R)eboot?
select "Shell". Some final changes need to be made.

Note that at this time, the newly installed partitions, including the boot partition, are still mounted.

Change the console on the new system
Set the console on the new system to HDMI:

echo 'set tty fb0' > /mnt/etc/boot.conf

https://cdn.openbsd.org/pub/OpenBSD/8.0/arm64/install80.img

type

boot> set tty fb0

boot> boot

install the operating system first before doing the router build

follow the instructions from the build

to enable dhcp on asix 88179 usb ethernet adapter

type command

sh /etc/netstart axen0 up

a couple times to get the dhcp address.

to upgrade and upgrade patches type

syspatch

pkg_add -u

check security update via 

https://www.openbsd.org/security.html

to shutdown type shutdown -h now

https://www.openbsdhandbook.com/upgrade/
