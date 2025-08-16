# Get Software on Raspberry Pi

These are the same steps you take when you are setting a Butter Box up for the first time.

You will need:

* Desktop computer
* Internet Connection
* Butter Box

{% stepper %}
{% step %}
### Download our pre‑built image for Raspberry Pi&#x20;

{% embed url="https://www.dropbox.com/scl/fo/helpqh3q2oj7ti2ia038m/h?dl=0.&rlkey=cswt4w4zksiuj3eb1oca48yw0" %}

{% hint style="info" %}
Always choose the Latest Version of the file
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
### Run the Raspberry Pi Imager desktop app

Once you have your micro SD card plugged into your computer that has an internet connection, run the Raspberry Pi Imager desktop app. If you don't have it, you can download it here: [https://www.raspberrypi.com/software/](https://www.raspberrypi.com/software/)
{% endstep %}

{% step %}
### Choose device > **Raspberry Pi Zero 2 W**

Once the Raspberry Pi Image starts, you will be prompt with the screens below.&#x20;

* Click on **Choose Device**

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-15 at 11.20.32 AM.png" alt=""><figcaption><p>Select Choose device</p></figcaption></figure>

* Select **Raspberry Pi Zero 2 W**\
  If you have a different Raspberry Pi device than the standard recommendation for a Butter Box, choose it instead.

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-15 at 11.21.03 AM.png" alt=""><figcaption><p>Select Raspberry Pi Zero 2 W (or the device you have if it's not the standard box from Butter HQ)</p></figcaption></figure>
{% endstep %}

{% step %}
### Choose Operating System > Use Custom

* Click on **Choose OS** back in the main view
* Select **Use custom** and upload the custom .img file that you've downloaded from Dropbox

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-15 at 11.22.49 AM.png" alt=""><figcaption><p>Select Use Custom. You will upload the custom .img file that you downloaded from Dropbox.</p></figcaption></figure>
{% endstep %}

{% step %}
### Choose Storage > Select Micro SD Card

* Click on **Choose Storage** back in the main view
* Select the **Micro SD Card**

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-15 at 1.05.26 PM.png" alt=""><figcaption><p>Select the Micro SD Card.</p></figcaption></figure>

Your screen will look similar to this after all selections:

<figure><img src="../../.gitbook/assets/Screenshot 2024-04-15 at 1.05.07 PM.png" alt=""><figcaption><p>Final screen after selections.</p></figcaption></figure>

You may be prompt with _"Doing this will erase all data from selected external storage"_ and “_do you want to apply settings”_, click then on _“no clear settings”_.

After that select _"write"_ and begin writing process to the Micro SD card.
{% endstep %}

{% step %}
### Remove From Computer and Insert Micro SD Card into the Raspberry Pi (Butter Box)

Once you're done, remove the Micro SD card. Insert the Micro SD card into the Raspberry Pi (Butter Box) not powered on. Plug the Raspberry Pi (Butter Box) into power. Wait a few moments.
{% endstep %}

{% step %}
### Connect to the Butter Box Portal

From your phone, go to your Wi-Fi settings and find the Butter Box Wi-Fi. If you see if, you will know the Butter Box is working. You have successfully turned a Raspberry Pi into a Butter Box!&#x20;

Join the ‘butterbox’ Wi-Fi. After 30 seconds, scan the QR code below. This connects you to **http://**&#x62;utterbox.lan in a browser. When you open this view in a browser, you should see the portal for the box. Note: If you are unable to scan the code, simply type **http://**&#x62;utterbox.lan into the browser of your choice.

{% hint style="info" %}
This is an HTTP page, not HTTPS, because it's served from a local device with no internet connection. Your data never leaves the network, so it's still private and secure.
{% endhint %}

<figure><img src="../../.gitbook/assets/butterbox-qr-english.png" alt=""><figcaption><p>QR code for the Butter Box</p></figcaption></figure>
{% endstep %}
{% endstepper %}
