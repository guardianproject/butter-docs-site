---
description: Supply your Butter Box with the treasures you want
---

# Load USB

There are step-by-step instructions to guide you, depending on what content you’d like to add to your box and how you’d like it to appear.

## Media, Files and Digital Books

If you want to share media, files or digital books, simply drop them onto the USB drive. You can use folders and subfolders to organize your content.

**Things to Know**

* When you have the USB drive plugged in, the 'Explore USB' tile will show up in the portal
* The folder names you use will be displayed in the Butter Box portal

<figure><img src="../.gitbook/assets/Screenshot 2025-08-16 at 9.50.15 PM.png" alt=""><figcaption><p>Organization of the USB drive</p></figcaption></figure>

<figure><img src="../.gitbook/assets/files (1).png" alt=""><figcaption><p>View of files in the Butter Box portal</p></figcaption></figure>

{% hint style="info" %}
The name you give the folder will appear in your Butter Box portal.
{% endhint %}

## Html Pages

With html pages, you can create your own experience around the content you're sharing. To display content through a html page, simply add the html file and it's complementary folders to the jump drive.

**Things to Know**

* If a folder contains an html file, the web page will be displayed in the portal when the folder is opened.
* The html page needs to be available offline. That means that everything (media, pages, fonts, etc) need to be locally available and linked.

<figure><img src="../.gitbook/assets/Screenshot 2025-08-16 at 9.46.16 PM.png" alt=""><figcaption></figcaption></figure>

If you have one html file in the main directory, the html page will appear when users tap 'Explore USB' from the portal. If you have multiple folders in the directory, the folders will appear when users tap 'Explore USB'. Once they tap into the folder that contains an hmtl file, that webpage will be displayed \[show video demo].

{% hint style="info" %}
The name you give the folder will appear in your Butter Box portal.
{% endhint %}

## Maps

**Things to Know**

* Offline map support is for Android only

If you want to share offline map files, you need to provide the latest version of Open Street Map for Android, along with the map files for locations of interest.

* Download OSM map apk for Android: [Free Releases — Android | OsmAndosmand.net](https://osmand.net/docs/versions/free-versions/?current-os=ios&)
* Download OSM map files: [Osmand Local Indexes Listdownload.osmand.net](https://download.osmand.net/list.php)

Put these all in a folder named **osm-map-files**. Place that folder on your Butter Box USB drive.

<figure><img src="../.gitbook/assets/Screenshot 2025-08-16 at 9.44.40 PM.png" alt=""><figcaption></figcaption></figure>



## Apps

If you want to share apps from your Butter Box, you can create a repo for F-Droid (most secure) or feature apps and app downloads from an html page. Go to section **x** for full information about using the F-Droid web interface on the box to share.&#x20;

**Things to Know**

* There are 3 different ways to share apps from a Butter Box. We'll break the instructions down for each in the App Store section. For details on which to choose, visit the App Store section.
  * Easiest
  * More curated
  * Most secure
* To get an app store tile to show up, you need to put a folder in your USB directory called **appstore**. The folder must contain one of two things:&#x20;
  1. An HTML file that links to APK and other app downloads&#x20;
  2. Or the required F-Droid file
* As an alternative, you can simply share apk files directly on the USB the same way you can share media, files and digital books.



Use an html page to display: To load your drive via html page with apps, do this:

* Create a folder called **‘appstore**’. Put it in the main directory on your USB drive. Within that file place your html file with the apk files in the same folder or subfolder. When you insert your USB drive into the Butter Box, the App Store tile will show up in the portal.
* Note: You will need to develop your own local html page.&#x20;
* Note: You will need to download the app files. Apps are updated frequently. Be sure to manually update all of the app files frequently to ensure you are providing the highest security for the people who connect to the box.
* Note: Be sure to download apps from trusted sources.

<figure><img src="../.gitbook/assets/Screenshot 2025-08-16 at 9.48.26 PM.png" alt=""><figcaption></figcaption></figure>

\[image of different app displays-tbd]
