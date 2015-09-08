CyanogenMod 7.0 support clockwork recovery.img

GW620/KH5200 does not support a recovery partion but anyway you can use it with fastboot **boot** command like as
```
fastboot boot my-recovery.img
```

## Recovery mode ##
  1. download **gb-recovery.img**
  1. `fastboot.exe` **boot** `gb-recovery.img` (not `fastboot.exe` **flash** `boot` ...)

## mount USB storage and install **.zip ##
  1. select**mounts and storage**1. mount USB storage
    1. copy**.zip (a update.zip style file) into the USB storage (sdcard)
    1. unmount and press **BACK**
  1. select **install zip from sdcard**
    1. select **choose zip from sdcard**
    1. select your zip.
    1. select **YES**
    1. press **BACK**

---

  1. you have to install `boot*.zip` under RecoveryMode
  1. you can also install `gapps-gb-*zip/update-*.zip` under RecoveryMode

## Clockwork Recovery ##
Some useful guide for the clockwork recovery menu
  1. http://www.droidforums.net/forum/samsung-fascinate-development/137071-guide-how-clockwork-mod-recovery.html