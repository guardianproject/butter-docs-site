---
description: Install Butter Operating System (OS) on an SD card for Raspberry Pi
---

# Install Butter

You will need:

* Desktop computer
* Internet Connection
* Butter Box

{% stepper %}
{% step %}
### Download the Butter OS for Raspberry Pi&#x20;

Make sure the file size matches the size listed on the website. Sometimes browsers do not complete the download, which can result in a corrupted file.

{% embed url="https://www.dropbox.com/scl/fo/helpqh3q2oj7ti2ia038m/h?dl=0.&rlkey=cswt4w4zksiuj3eb1oca48yw0" %}

{% hint style="info" %}
Always choose the Latest Version of the file.&#x20;
{% endhint %}
{% endstep %}

{% step %}
### Plug the micro SD card into your computer

To plug the micro SD card into your computer, you may need an adapter to do this:

<div align="center"><figure><img src="../../.gitbook/assets/image.png" alt="" width="375"><figcaption><p>Example adapter (USB-C to Micro SD)</p></figcaption></figure></div>

{% hint style="info" %}
You don't need to connect the box to the computer.
{% endhint %}
{% endstep %}

{% step %}
### Run Raspberry Pi Imager&#x20;

Once you have your micro SD card plugged into your computer that has an internet connection, run Raspberry Pi Imager from a desktop computer. It will walk you through the steps to install the Butter operating system on the micro SD card.&#x20;

If you don't have Raspberry Pi Imager, you can download it here: [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
{% endstep %}

{% step %}
### Choose device > **Raspberry Pi Zero 2 W**

Once the Raspberry Pi Image starts, you will be prompt to select your Raspberry Pi device.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 9.56.27 AM.png" alt=""><figcaption><p>Select Raspberry Pi Zero 2 W (or the device you have if it's not the standard box from Butter HQ)</p></figcaption></figure>
{% endstep %}

{% step %}
### Choose Operating System > Use Custom

* On the OS tab, select **Use custom** and upload the custom Butter OS .img file. Confirm that you have **unzipped the file** before using it.&#x20;

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 9.57.31 AM.png" alt=""><figcaption><p>Select Use Custom. You will upload the custom .img file that you downloaded from Dropbox.</p></figcaption></figure>
{% endstep %}

{% step %}
### Choose Storage > Select Micro SD Card

* From the **Storage** tab, select the **Micro SD Card.**

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.27.37 PM.png" alt=""><figcaption><p>Select the Micro SD Card.</p></figcaption></figure>

Your screen will look similar to this after all selections:

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.27.43 PM.png" alt=""><figcaption><p>Final screen after selections.</p></figcaption></figure>

You may be prompt with _"Doing this will erase all data from selected external storage"_ and “_do you want to apply settings”_, click then on _“no clear settings”_.

After that select _"write"_ and begin writing process to the Micro SD card.
{% endstep %}

{% step %}
### Remove From Computer and Insert Micro SD Card into the Raspberry Pi (Butter Box)

Once you're done, remove the Micro SD card. Insert the Micro SD card into the Raspberry Pi (Butter Box) not powered on.&#x20;
{% endstep %}

{% step %}
### Go to Quick Start

Plug the Raspberry Pi (Butter Box) into power. Wait a few moments and connect to the Butter Box Portal. Go to the [Quick Start](../../quick-start.md) section for more details.
{% endstep %}
{% endstepper %}

**If you are building an extended box, continue in the next section: Extend Your Box.**

{% content-ref url="extend-your-box.md" %}
[extend-your-box.md](extend-your-box.md)
{% endcontent-ref %}



### Troubleshooting

If you see an error stating that the input file is not a valid disk image, check the file you downloaded.

Make sure the file size matches the size listed on the website. Sometimes browsers do not complete the download, which can result in a corrupted file.

Also confirm that you have **unzipped the file** before using it.

<figure><img src="../../.gitbook/assets/Screenshot 2026-02-24 at 1.28.37 PM.png" alt=""><figcaption></figcaption></figure>
