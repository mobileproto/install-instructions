#Install Instructions

Below are instructions for both Phone Gap and native Android installation instructions. Please install both, as there are a few assignments thorughout the semester where you will be required to use both installations.

###Phone Gap Installation
_First off, make sure you are running Linux or Mac OSX. No Windows please._ If you do not have one of these two operating systems installed, please stop and install Linux (Ubuntu 12.04 recommended, we have installation drives if you need them) before continuing.

To install PhoneGap, we will be installing...


1. Java JDK 6 (Linux only)
2. Android Studio
3. Github
4. Node.Js
5. Cordova, PhoneGap



###Java JDK (Linux Only)
First check that you have Java installed:
``` java -version```
If you have version 1.6, or you see "openJDK" anywhere, let's fix that.

For those without Java installed, follow the instructions for downloading Java 7 JDK [here.](http://www.ubuntugeek.com/how-to-install-oracle-java-7-in-ubuntu-12-04.html)

You should only need the following commands if you are on a fresh install:
```
sudo apt-get purge openjdk*

sudo add-apt-repository ppa:webupd8team/java
sudo apt-get update
sudo apt-get install oracle-java7-installer
```

Now try ` java -version` again. You should see that you have version 1.7.


###Android Studio
1. Download [Android Studio](http://developer.android.com/sdk/installing/studio.html) for Mac or Linux
2. Follow the install instructions

#####Set up Android SDK Tools
Thankfully, Android SDK tools come bundled with Android Studio, so now we just need to set it up such that Phonegap knows where to find it.
1. Locate the directory where Android Studio was installed
2. Open up your .bash_profile (OSX) or .bashrc (Linux) inside your Home directory and add the the android-sdk path
	`export PATH=<path to android studio>/sdk/:<path to android studio>/sdk/platform-tools:<path to android studio>/sdk/tools:$PATH`
3. Open Android Studio, go to Tools -> Android -> SDK Manager
4. Install the Android 4.2.2, 2.3.3 SDK Platforms and the Intel Emulator (found under Extras).

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
1. In Android Studio go to Tools -> Android -> AVD Manager
2. Create a new emulator
3. Make sure you have some of the following settings
	* Name it whatever you want
	* Pick a preset Device, prefereably with a screen smaller than 5"
	* Target API should be 4.2.2
	* Depending on the device, you may want to reduce the RAM. 512 will be fine.
	* Leave everything else at their default values
4. Press OK

###Run your first PhoneGap app
```
cordova create HelloWorld
phonegap create HelloWorld
cd HelloWorld
cordova build android
phonegap local build android
cordova emulate android
phonegap local run android
```
