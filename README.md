# dumpDex - Android Unpacking

> This plugin requires the Xposed environment and supports most encryption shells available on the market. The software is for educational purposes only and should not be used for other purposes. The project is not a finished product and may cause software crashes.

### Build Environment

Android Studio 3.0

**If you are unable to unpack, go to the [PackerInfo.java](app/src/main/java/com/wrbug/dumpdex/PackerInfo.java#L31) file and add the app’s package name to the packages field. Then compile and install it. Pull Requests are welcome to make the software more comprehensive.**

### Supported Devices

Most Xposed-environment phones. Emulators are not supported yet.

### APK Download

[https://github.com/WrBug/dumpDex/releases](https://github.com/WrBug/dumpDex/releases)

[https://github.com/WrBug/DeveloperHelper](https://github.com/WrBug/DeveloperHelper)  **Recommended Download**

Easy Developer has integrated dumpdex functionality.

Branches

[develop](https://github.com/WrBug/dumpDex/tree/develop) Development Branch


[master](https://github.com/WrBug/dumpDex/tree/master) Stable Branch

### How to Use

Download and compile the source code or download the APK package and install it. After applying the Xposed module and restarting, the plugin will automatically dump dex files into the **/data/data/package_name/dump** directory once a protected app is run.

**The APK file will not be updated in real-time. To get the latest APK, please compile the source code yourself**




### Source Code Compilation

Download or clone the source code to your local machine, open it with Android Studio, and after successful compilation, install the APK. Then copy **lib/armeabi-v7a/libnativeDump.so** to */data/local/tmp/libnativeDump.so* ，and set the permissions to 777. For ARM64 devices, also copy **lib/arm64-v8a/libnativeDump.so** to */data/local/tmp/libnativeDump64.so*You can do this via a file manager or by using the following ADB shell command:

```bash
# Only applicable for 32-bit phones
adb shell
su
cp /data/data/com.wrbug.dumpdex/lib/libnativeDump.so /data/local/tmp
chmod 777 /data/local/tmp/libnativeDump.so

```

After configuration, activate Xposed and restart.

### For More Content, Visit the Blog

[https://www.wrbug.com/](https://www.wrbug.com/)

### Related Articles (Shared by Users)

[dumpDex Unpacking Principle](http://liteng1220.com/blog/articles/dumpdex-principle/)

[The Road to Android Reverse Engineering - 360 Encryption Shell Unpacking Analysis](https://juejin.im/post/5c1934226fb9a04a0b221c3c)

### Support Development, Donations Welcome

![](/pay.png)


