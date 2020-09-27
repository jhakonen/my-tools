# Udev tools

## Installation

  $ sudo cp usb-device-path-by-id /usr/bin/
  $ sudo cp usb-device-authorize /usr/sbin/

## usb-device-path-by-id

This tool when given USB device's vendor and product id pair returns device's path in /sys/bus/usb/devices/ folder.

Usage:

  $ usb-device-path-by-id <vendorid>:<productid>

You can get the id pair with command `lsusb`.

## usb-device-authorize

This tool when given USB device's vendor and product id pair and authorize value either authorizes or deauthorizes a USB device. Effectively similar to plugging or unplugging the device.

Usage:

  $ sudo usb-device-authorize <vendorid>:<productid> <state>

You can get the id pair with command `lsusb`. The state is `0` for unauthorizing and `1` for authorizing.
