# RIGOL DHO800/900 & MHO900 Webcontrol

### A modified Webcontrol that has the features that it is supposed to have:
* Resizeable
* Remembers the last position & size
* Fullscreen with double click

### For installation:

Download [Webcontrol.apk](http://TODO)

You need ADB (Android Debug Bridge):
* [Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
* [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip)
* [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip)

### On a command line:

adb connect [Scope IP address or network name]:55555  
adb install -r [path to webcontrol.apk]Webcontrol.apk  
adb shell monkey -p com.rigol.webcontrol 1

### In your browser:
http://[Scope IP address or network name]  
Click button "Web Control"
