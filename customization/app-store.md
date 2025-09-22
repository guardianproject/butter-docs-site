---
cover: ../.gitbook/assets/media-type-apps.png
coverY: 0
---

# Apps

There are 3 different ways to share apps from a Butter Box.&#x20;

| Method                     | Supported Apps        | Security                                                   | Guidance     |
| -------------------------- | --------------------- | ---------------------------------------------------------- | ------------ |
| F-Droid Repo               | Android               | Best                                                       | Most Secure  |
| Static Website             | Android, iOS, Desktop | Limited (does not offer ease for distributing app updates) | More Curated |
| Files organized in folders | Android, iOS, Desktop | Limited (does not offer ease for distributing app updates) | Easiest      |

To get an app store tile to display in your Butter portal, you need to put a folder in your USB directory called `appstore` . The folder must contain the **required F-Droid files for an F-Droid Repo** or **a Static Website** that links to application files (eg. apk, exe, etc.)

### Option 1: F-Droid Repo

Learn more about creating a F-Droid repo at [https://gitlab.com/likebutter/butterbox-rpi/-/blob/main/docs/en/README.md#premade-content-packs-and-content-pack-recipes](https://gitlab.com/likebutter/butterbox-rpi/-/blob/main/docs/en/README.md#premade-content-packs-and-content-pack-recipes).

* [Docs for F-Droid webdash](https://gitlab.com/uniqx/fdroid-webdash)
* [Docs for fdroidserver](https://gitlab.com/fdroid/fdroidserver)

### Option 2: Static Website

Visit the [Content Packs](content-packs.md) section for information on **Using Static Websites**.



### Things To Know

* If you are sharing apps from Butter Box, you will need to download the app files you want to share. Apps are updated frequently. Be sure to manually update all of the app files frequently to ensure you are providing the highest security for the people who connect to the box.
  * You’ll need a copy of the app’s `.apk` file — make sure it’s from a safe and trusted source.
  * Butter won’t automatically verify the source, so it's up to you to confirm it's clean and legal to share.
* How to get apk files: There are mobile apps you can use to get access to apk files on an Android phone. Alternatively, you can download app files directly from the developer's website.
