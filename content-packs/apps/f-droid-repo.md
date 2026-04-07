---
description: How to Create Your Own F-Droid Repo to Share as a Content Pack
---

# F-Droid Repo

You can build your own curated F-Droid repo using your computer's terminal. Once set up, users can connect their F-Droid app to your Butter Box and start downloading apps.



{% stepper %}
{% step %}
### Step 1: Install F-Droid Server Tools

Before you begin, you need to install a tool called **fdroidserver**. This helps you create and manage your app store.

**On Mac (using Homebrew):**

```
 brew install fdroidserver 
```

**On Linux (Debian/Ubuntu):**

```
 sudo apt install fdroidserver 
```
{% endstep %}

{% step %}
### Step 2: Check that it's installed correctly

After installation, run this command:

```
 fdroid version
```

If everything is working, you will see a version number printed on the screen.
{% endstep %}

{% step %}
### Step 3: Create Your Repo Folder

You need to create the folder where you will save the repo files in your computer, choose a name that aligns with the project or purpose of the apps in it, and replace my-fdroid-repo for that name in the command.

```
mkdir -p ~/my-fdroid-repo
```

```
cd ~/my-fdroid-repo
```
{% endstep %}

{% step %}
### Step 4: Initialize the repo

```
fdroid init
```

This creates the following directories in your repo file:

```
Config.yml 
```

```
repo/
```

```
metadata/
```
{% endstep %}

{% step %}
### Step 5: Add your APKs

Copy your signed APKs into the repo/ folder. Ensure you only use apps from trusted sources like the official F-Droid library or verified developers.

**Security Note:** Avoid downloading APKs from "mirror" sites or unknown sources, as they can contain malware or trackers that compromise your users' privacy.

```
cp /path/to/your/*.apk repo/
```

Example:

```
cp ~/Downloads/myapp.apk repo/
```
{% endstep %}

{% step %}
### Step 6: Generate (and Update) the Repository Index

Every time you add a new APK or a new version of an app to your repo/ folder, you must run the following command to "publish" those changes:

```
fdroid update --create-metadata
```

What this command does:

* **Scans APKs:** It reads the new files in your repo/ folder.
* **Generates Metadata:** It creates YAML files containing the app's name, version, and permissions.
* **Creates index.v1.jar:** This is the "catalog" file that the F-Droid app downloads to see what is available.
* **Signs the Repository:** It uses your secret key to sign the index, proving to the Android app that the files haven't been tampered with.
{% endstep %}

{% step %}
### Step 7: Test your Repo locally

To test your repo locally and ensure everything works before you share it on the Butter Box, you can serve its content locally and add it to F-Droid using a URL.&#x20;

```
cd repo
```

```
python3 -m http.server 8000
```

Once your repo is live, open the F-Droid app on your device and navigate to **Settings > Repositories > "+"**. Select **"Enter repository URL manually"** to add your new source.

Adding the repo manually allows you to verify the user experience by checking:

* **App Visibility:** Are all your apps appearing in the list?
* **Visual Assets:** Are icons and screenshots displaying correctly?
* **Categorization:** Are apps appearing in the correct sections (e.g., Internet, Security)?
* **Functionality:** Do the downloads and installations complete without errors?
* **Metadata:** Does the version number and description match your `repo/` files?



Your repo will be available  at:

`http://YOUR-IP:8000/repo`



**Find your IP:**

#### macOS:

```
ipconfig getifaddr en0
```

#### Linux:

```
hostname -I
```
{% endstep %}
{% endstepper %}
