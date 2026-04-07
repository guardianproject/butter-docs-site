# Apps

You can share apps as a content pack, via a static website.

If you give a folder the name  `appstore`  and place it in the root directory of the USB drive, the **Apps** tile will appear in the Butter Box portal.&#x20;

### Things To Know

* If you are sharing apps from Butter Box, you will need to download the app files you want to share. Apps are updated frequently. Be sure to manually update all of the app files frequently to ensure you are providing the highest security for the people who connect to the box.
  * You’ll need a copy of the app’s `.apk` file — make sure it’s from a safe and trusted source.
  * Butter won’t automatically verify the source, so it's up to you to confirm it's clean and legal to share.
* How to get apk files: There are mobile apps you can use to get access to apk files on an Android phone. Alternatively, you can download app files directly from the developer's website.

### Support For F-Droid

Additionally, Butter Box supports app distribution via F-Droid. In your content pack, you can include the F-Droid  `.apk`  and a QR code for your repo. Anyone with access to the Box can then download the F-Droid app (while offline), and add the repo.

As long as they are connected to the Butter Box, they can download any of the apps within your repo.

Once they are connected to the internet (if they are), they can receive app updates from any apps in your repo that are also included in the main F-Droid repo. If you update the apps in your repo, they will also have access to those.

What is a F-Ddroid Repo?

* A hosted library of apps
* Anyone can host their own repo

\
Why use it?

* It offers a secure process for sharing apps. The F-Droid team builds apps in the official F-Droid repo from the source code themselves. This ensures that the app you download exactly matches the code the developer published.
* Users installing from F-Droid have access to app updates remotely (away from the Butter Box)

Technical skills are required. Here are the instructions to create your own repo.
