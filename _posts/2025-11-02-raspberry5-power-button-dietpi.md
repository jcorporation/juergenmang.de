---
layout: post
title: "How to use Raspberry 5 Power Button with DietPi"
tag: raspberry
image: /assets/garden/raspberry5-j2.webp
permalink: /garden/raspberry5-power-button-dietpi
---

With Raspberry 4, I used the SLC pin together with [myGPIOd](https://github.com/jcorporation/myGPIOd) to create an On/Off switch, but Raspberry 5 ships with a power button and you can add an external Button to the J2 jumper.

![Raspberry 5 J2 Jumper](/assets/images/raspberry5-j2.webp)

This is described in the [Raspberry documentation](https://github.com/raspberrypi/documentation/blob/develop/documentation/asciidoc/computers/raspberry-pi/power-button.adoc).

You can enable the button easily in [DietPi](https://github.com/MichaIng/DietPi/discussions/7359):

- Set `HandlePowerKey=poweroff` in `/etc/systemd/logind.conf`
- Make sure that ACPI, DBus is installed and activate systemd-logind:

  ```sh
  apt install acpi dbus
  systemctl unmask systemd-logind
  systemctl start systemd-logind
  ```
