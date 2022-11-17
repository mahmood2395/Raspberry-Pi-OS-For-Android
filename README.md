# Install Raspberry Pi OS on Android

This is a Raspbian disk image tuned to work on Pi Deploy (a fork of Linux Deploy).  It can be used on **any** rooted Android device with an **ARMv7 or newer CPU** running Android 5.0 (Lolipop) or newer.  Form factor is not important; it could be a phone, tablet, HDMI stick or **any device running Android**.  For very old devices running Android 4.x, see the [Legacy branch](https://github.com/DesktopECHO/Pi-hole-for-Android/tree/legacy)

### Requirements:

- Android device that has been rooted

### Note to users of previous builds:

- Uninstall any previous versions of Linux Deploy or Pi Deploy and reboot your device.
- Failure to heed this advice will cause issues!

### Installation:

- Download and Install the latest [Pi Deploy APK](https://github.com/DesktopECHO/Pi-hole-for-Android/releases/latest/download/pideploy.apk)
- Tap the **Options** menu (Three dots **⋮** at top right of screen)
- Tap **New Deployment**
- After a few moments the [Raspbian Image](https://github.com/DesktopECHO/linuxdeploy-images/releases/latest/download/raspbian.tgz) will download and install to your device.
- When deployment is complete, tap **[  ▷ START ]**  to launch the instance.
- _(Optional, post-install)_ To install PIXEL Desktop run `pideploy-gui-install` and restart the instance.  Next time you login via RDP you will have a full desktop session with audio support.

-----------------------------------------------------------
**INSTALLATION COMPLETE    ·    Raspberry Pi OS is running on your Android Device**

-----------------------------------------------------------
The Android device's IP is shown at the top of the Linux Deploy main window.  You can interact with Raspberry Pi OS in several ways, the examples below use IP **_10.73.0.31_** 

 - From a Windows desktop, connect via RDP **->** **```mstsc.exe /v:10.73.0.31```**

 - From a computer running Linux, connect via SSH **->** **```ssh android@10.73.0.31```**

 - Pi-hole administration is accessible from any browser on your network **->** **```http://10.73.0.31/admin```**

 - If your Android device has a display, you can RDP into the Pi-hole instance (as localhost) by installing the [Microsoft Remote Desktop](https://play.google.com/store/apps/details?id=com.microsoft.rdc.androidx) client.

**Additional Info:**

If you have a Samsung device, you will need to [De-Knox](https://www.google.com/search?q=de-knoxed+rom+site:forum.xda-developers.com) the stock ROM or flash a 3rd party ROM like LineageOS.  

RDP Sessions launch the Openbox window manager with QTerminal in fullscreen mode.  To open a new tab hit **[Ctrl-Shift-T]** and to un-hide the menubar hit **[Ctrl-Shift-M]**

You can restart (or "bounce") the Raspberry Pi OS instance in Pi Deploy by pressing **[ ■ STOP ]** and waiting a few seconds for the instance to indicate all services are stopped.  Restart the instance by pressing **[ ▸ START ]**

Adjust QT display scaling: ```~/startwm.sh``` 

Change the font size in QTerminal: ```~/.config/qterminal.org/qterminal.ini```

**If your Android device has a battery and was unused for months or years, replace its battery.**  Old, worn, or abused Li-ion batteries can fail when pushed back into service.  Failure appears as a bulge in the battery, or worse a [**_thermal event_**](https://www.urbandictionary.com/define.php?term=unexpected+thermal+event).  A good battery provides [UPS](https://en.wikipedia.org/wiki/Uninterruptible_power_supply) protection for your newly-provisioned Pi-hole.
