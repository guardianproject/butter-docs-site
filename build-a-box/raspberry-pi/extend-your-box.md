---
description: How To Add a Router To Your Box Setup
---

# Extend Your Box

An extended Butter Box pairs the Raspberry Pi with a standalone Wi-Fi router, giving stronger signal and more simultaneous connections.&#x20;

With the router, the network can reach 10-30 m (32-98 feet),and can comfortably support 10–20 connected devices at the same time. This setup is ideal for a medium group of people in a medium room, like classrooms, events, or community spaces.

## Supplies

* [ ] Raspberry Pi 4, 5 or Raspberry Pi Zero 2W
* [ ] Router ([Opal (GL-SFT1200) Wireless Travel Router](https://store-us.gl-inet.com/products/united-states-opal-gl-sft1200-gigabit-wireless-router-dual-band-openwrt-ipv6-tor) or equivilent)
* [ ] Power outlet and power cords that accompany the Raspberry Pi and the Routeror an [alternative power supply](../power-supply.md)
* [ ] Micro SD Card: Images with the Butter software are usually under 16 GB (we suggest 256 GB). Media that people upload to the chat ends up on the card; it never gets cleared.
* [ ] USB Drive (min 32 GB)
* [ ] Adapters (as needed)

_No internet connection is required._

<figure><img src="../../.gitbook/assets/20250815_142438.jpg" alt=""><figcaption></figcaption></figure>



## Steps

To extend your box, you simply connect a GLi-Net router to the Butter Box with an ethernet cable. Instead of accessing the box from the portal Wi-Fi hotspot (eg. 'butter box' or whichever name you set in the admin settings), users will join the Wi-Fi network of the router.&#x20;

{% stepper %}
{% step %}
### Connect the Butter Box to its power supply.&#x20;

Connect the Butter Box to power.
{% endstep %}

{% step %}
### Connect Router

Connect the router to power. Then use the ethernet cable to connect to the Butter Box. Make sure to plug the Ethernet cable into the LAN port on your router.&#x20;
{% endstep %}

{% step %}
### Test Your Connection

oin the router Wi-Fi. If you have not setup or used this router before, enter the default password found in the user guide included in the package. After 30 seconds, open http://butterbox.local in a browser.
{% endstep %}

{% step %}
### Disable Butter Box Wi-Fi Access Point

Open the admin settings from the Butter Box portal. Navigate to **Secure Portal**. Turn off the Wi-Fi access point. This will hide the Wi-Fi network that broadcasts from the raspberry pi, so that users don’t get confused about which network to join.
{% endstep %}

{% step %}
### Invite Users to Join the Router Wi-Fi

Users will now join the Wi-Fi network of the router when they want to connect to the Butter Box.
{% endstep %}
{% endstepper %}
