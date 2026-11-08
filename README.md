# OpenBSD router for raspberry pi 4

OpenBSD router for the rasberry pi 4

WAN is asix 88179 usb ethernet

LAN is built in ethernet raspberry pi 4

Download install80.img

burn to the sd card with raspberry pi imager 

edit the /etc/boot.conf and type

nano /etc/boot.conf

type in 

set tty fb0

in order to boot up via hdmi


https://cdn.openbsd.org/pub/OpenBSD/8.0/arm64/install80.img

type

boot> set tty fb0

boot> boot

install the operating system first before doing the router build

follow the instructions from the build

to enable dhcp on asix 88179 usb ethernet adapter

type command

sh /etc/netstart axen0

a couple times to get the dhcp address.

to upgrade and upgrade patches type

syspatch

pkg_add -u

check security update via 

https://www.openbsd.org/security.html

to shutdown type shutdown -h now

https://www.ports.to/


https://www.openbsdhandbook.com/upgrade/
