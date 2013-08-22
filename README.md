#Install Instructions

Below are instructions for both Phone Gap and native Android installation instructions. Please install both, as there are a few assignments thorughout the semester where you will be required to use both installations.

###Phone Gap Installation
_First off, make sure you are running Linux or Mac OSX. No Windows please._ If you do not have one of these two operating systems installed, please stop and install Linux (since presumably you will not install OXS) before continuing.

To install PhoneGap, we will be installing...

1. Android SDK Tools 
2. Java JDK 6 (Linux only)
3. Android Studio
4. Github
5. Node.Js
6. Cordova PhoneGap

####Android SDK Tools
1. Download the [Android SDK tools](http://developer.android.com/sdk/index.html) and unzip the file
2. Rename the folder to android-sdk, create another folder called dev-installs somewhere on your computer where you will not delete it, and move android-sdk inside dev-installs.
3. Open up your .bash_profile (OSX) or .bash_rc (Linux) and add the the android_sdk path
	* On OSX: `export PATH=<absolute path>/android-sdk/platform-tools:<absolute path>/android-sdk/tools:$PATH`
	* On Linux:
4. Start the SDK manager by typing `android` into the console. Install the Android 4.2.2 and the Intel Emulator (found under Extras)

###Java JDK 6 (Linux Only)
1. Download the [Java 6 JDK](http://www.oracle.com/technetwork/java/javase/downloads/index.html)
2. Evan will add more...

###Android Studio
1. Download [Android Studio](http://developer.android.com/sdk/installing/studio.html) for Mac or Linux
2. Follow the install instructions

###Github
If you are already set up with a Github username and Github installed on the command line...
Please [enter your Github info for us here](https://docs.google.com/forms/d/1ZsL6tvAlNkZu1AbBnvmJ4G7Yj_LOCbO0bjRS6SnXdIw/viewform) and skip to the Node.Js install

Otherwise...
1. Go to Github.com and make a username. Note: You probably want to keep this username professional if possible. 
2. Download the [Github command line tools](https://help.github.com/articles/set-up-git) and follow the instructions on the page to setup the Github command line
3. Follow all of the instructions (for Mac) and ignore the OSX keychain info for Linux

###Node.Js
1. Skip this if you have Node.Js already installed
2. Otherwise, download [Node.Js](http://nodejs.org/download/) and follow the install prompts
3. More from Tim...

###Cordova PhoneGap
1. Enter in the console: `npm install -g cordova`
2. Enter in the console: `npm install -g phonegap`
3. If you are getting error messages, add `sudo` in front of the npm commands

###Create a emulator
1. Enter in the console: `emulator -avd <avd_name>`
2. Create a emulator device. Go to town, make it as fancy as you want (:
3. Save the device

###Run your first PhoneGap app
```
phonegap create HelloWorld
cd HelloWorld
phonegap local build android
phonegap local run android
```
