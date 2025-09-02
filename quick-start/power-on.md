---
cover: ../.gitbook/assets/20250815_143947.jpg
coverY: 0
---

# Power On

{% stepper %}
{% step %}
### Check supplies

Make sure you have the supplies for a basic box:

* Power source
* USB drive
* USB Adapters (as needed)
* Butter Box Device (with micro SD card inserted)
* Case

<figure><img src="../.gitbook/assets/signal-2025-08-21-140334_003.jpeg" alt=""><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Make sure the micro SD card is inserted into the device

The micro SD card should have the latest version of Butter OS running on it.
{% endstep %}

{% step %}
### Plug it in to power on

Connect the power supply to the first micro USB port and correct wall outlet.

<figure><img src="../.gitbook/assets/1.png" alt="" width="375"><figcaption></figcaption></figure>

You will know the box is working if ‘butterbox’ wifi appears in the wifi list on your phone or computer. If it doesn’t, unplug the box and plug it back in.



_If using a solar battery or other means of power, use one with the correct specs to ensure adequate power and avoid damage to the unit. For a Pi Zero 2 W use Micro USB power supply with at least 2.0A._

[Link to Power Supply Options](../build-a-box/power-supply.md)


{% endstep %}

{% step %}
### Insert USB drive

Connect the USB adapter to the open port. Then plug in the USB drive. Learn more about loading the USB drive with treasures in the [Load USB](load-usb.md) section.

<figure><img src="../.gitbook/assets/2.png" alt="" width="375"><figcaption></figcaption></figure>
{% endstep %}

{% step %}
### Access the Butter Box Portal

Join the ‘butterbox’ Wi-Fi. After 30 seconds, scan the QR code on the box. This connects you to http://butterbox.lan in a browser.

{% embed url="https://youtu.be/KB5O9MSoaAg" %}

<div align="center"><figure><img src="../.gitbook/assets/qr code.png" alt="" width="375"><figcaption></figcaption></figure></div>

_If this page does not load, wait a few minutes to ensure connectivity. Refresh the page. If you’re connecting from a smartphone, turn off your mobile data or turn on airplane mode. Then try again._

{% hint style="info" %}
This is an HTTP page, not HTTPS, because it's served from a local device with no internet connection. Your data never leaves the network, so it's still private and secure.
{% endhint %}

The Wi-Fi does not have a password by default. Though, you can easily add one. Learn more in the [Set Wi-Fi Password ](add-wifi-password.md)section.
{% endstep %}

{% step %}
### Once connected, explore the portal!

Explore the portal for yourself! Once you share with others, they will connect to it in the same way you just did.
{% endstep %}
{% endstepper %}

{% hint style="info" %}
For a Pi Zero 2 W: Up to 5 people can connect to the box at any time. After people connect and get what they need, encourage them to leave the box to give others a turn.\
The physical reach of the Box varies. But as a rule of thumb, people in the same room as the box (or in talking distance) will be able to access it.
{% endhint %}
