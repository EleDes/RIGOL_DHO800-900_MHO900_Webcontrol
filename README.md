# RIGOL DHO800/900 & MHO900 Webcontrol

### A modified Webcontrol that has the features that it is supposed to have:
* Resizeable
* Remembers the last window state
* Fullscreen with double click

### For installation:

Download [Webcontrol.apk](https://github.com/EleDes/RIGOL_DHO800-900_MHO900_Webcontrol/releases/latest/download/Webcontrol.apk) (this is the latest version, all versions are available in [Releases](https://github.com/EleDes/RIGOL_DHO800-900_MHO900_Webcontrol/releases))  
Details in the [Release description](https://github.com/EleDes/RIGOL_DHO800-900_MHO900_Webcontrol/releases/latest/)  

You need ADB (Android Debug Bridge):
* [Windows](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
* [Linux](https://dl.google.com/android/repository/platform-tools-latest-linux.zip) or on Debian/Ubuntu/Pi OS/derivates: ```sudo apt install adb```  
* [Mac](https://dl.google.com/android/repository/platform-tools-latest-darwin.zip) or ```brew install --cask android-platform-tools```  

Connect Scope to the network


### On a command line:

```
adb connect [Scope IP address or network name]:55555
```
#### make backup of Webcontrol.apk:
```
adb pull /data/app/com.rigol.webcontrol-2/base.apk [path to backup directory]Webcontrol_backup.apk
```
#### install new Webcontrol.apk:
```
adb install -r [path to webcontrol.apk]Webcontrol.apk  
adb shell monkey -p com.rigol.webcontrol 1
```


### In your browser:
```
http://[Scope IP address or network name]
```
Click button "Web Control"  


### To restore original Webcontrol.apk:
```
adb connect [Scope IP address or network name]:55555
```
#### install original Webcontrol.apk:
```
adb install -r [path to backup directory]Webcontrol_backup.apk  
adb shell monkey -p com.rigol.webcontrol 1
```

### Restore original Webcontrol.apk without backup:
[install firmware update](https://www.rigolna.com/firmware/), it will overwrite Webcontrol.apk  
