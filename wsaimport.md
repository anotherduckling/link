---
visibility: hidden
---
![](https://cdn.discordapp.com/attachments/1015131233824538624/1085458787890110504/yHJjHhz.png)

# Import Files into WSA

1. Download and Extract [**ADB tools**](https://dl.google.com/android/repository/platform-tools-latest-windows.zip)
2. Make a text file and save as `filename.bat`
3. Put the commands in the bat file with the **Folder Locations**

```
echo
cd [Platform-tools Folder Location]
adb connect 127.0.0.1:58526
adb push %1 [Android Folder Location]
pause
```
4. Drag and drop files or folders you want on the bat file to transfer into WSA,

!!!light Example
```
echo
cd E:\DL\platform-tools
adb connect 127.0.0.1:58526
adb push %1 /storage/emulated/0/DCIM
pause
```
!!!