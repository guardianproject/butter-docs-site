# App Store

There are 3 different ways to share apps from a Butter Box.&#x20;

| Method                     | Supported Apps        | Security                                                   | Guidance     |
| -------------------------- | --------------------- | ---------------------------------------------------------- | ------------ |
| F-Droid repo               | Android               | Best                                                       | Most Secure  |
| Static offline website     | Android, iOS, Desktop | Limited (does not offer ease for distributing app updates) | More Curated |
| Files organized in folders | Android, iOS, Desktop | Limited (does not offer ease for distributing app updates) | Easiest      |

**Things to Know**

* You will need to download the app files. Apps are updated frequently. Be sure to manually update all of the app files frequently to ensure you are providing the highest security for the people who connect to the box.
  * You’ll need a copy of the app’s `.apk` file — make sure it’s from a safe and trusted source.
  * Butter won’t automatically verify the source, so it's up to you to confirm it's clean and legal to share.
* How to get apk files: There are mobile apps you can use to get access to apk files on an Android phone. Alternatively, you can download app files directly from the developer's website.



**Basic Instructions**

* To get an app store tile to show up, you need to put a folder in your USB directory called `appstore` . The folder must contain one of two things:&#x20;
  1. Required F-Droid files; or
  2. HTML file that links to APK and other app downloads&#x20;

<figure><img src="../.gitbook/assets/Screenshot 2025-08-16 at 9.48.26 PM.png" alt=""><figcaption></figcaption></figure>

**Instructions for Viewing Via F-Droid**

Learn more about creating a F-Droid repo at [https://gitlab.com/likebutter/butterbox-rpi/-/blob/main/docs/en/README.md#premade-content-packs-and-content-pack-recipes](https://gitlab.com/likebutter/butterbox-rpi/-/blob/main/docs/en/README.md#premade-content-packs-and-content-pack-recipes).

* [Docs for F-Droid webdash](https://gitlab.com/uniqx/fdroid-webdash)
* [Docs for fdroidserver](https://gitlab.com/fdroid/fdroidserver)



**Instructions for Viewing Via HTML (Offline Webpage)**

If you're using a static offline website, you will need to develop your own local html page.&#x20;

* All of the app files have to be linked to from the HTML page.&#x20;

