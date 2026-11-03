# OpenBSD-router-for-raspberry-pi-4

OpenBSD router fpr the rasberry pi 4

Download install80.img

https://cdn.openbsd.org/pub/OpenBSD/8.0/arm64/install80.img

type

boot> set tty fb0
boot> boot

to enable dhcp on asix 88179 usb ethernet adapter

type command

sh /etc/netstart axen0 up

a couple times to get the dhcp address.
