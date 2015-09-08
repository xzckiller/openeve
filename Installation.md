## UsbDriver ##

## Install system.img ##
```
fastboot flash system system.img
```

You have to install system.img first. (this image may contains older kernel modules)

## boot with gb-recovery.img ##
```
fastboot boot gb-recovery.img
```

## Install boot-gb-**.zip under RecoveryMode ##
for GB 2.3.5
  1. boot-gb235-224mb is recommended.
  1. boot-gb235-236mb is confirmed for V20G

---

for GB 2.3.7
  1. boot-gb237-224mb is recommended.
  1. boot-gb237-236mb is confirmed for V20G**

## Install gapps-gb-2011xxxx.zip ##
  1. goto gapps site http://goo-inside.me/google-apps/
  1. download gapps-gb-2011xxxx-signed.zip
  1. install gapps-gb under recovery mode

---

  1. for GB2.3.4, GB2.3.5 - gapps-gb-20110613-signed.zip recommended

See also
http://wiki.cyanogenmod.com/index.php?title=Latest_Version/Google_Apps

## Howto Manually Install boot.img with adb shell ##

**Step 1.** adb push boot img.
```
adb push boot-gb.img /cache/

 or

adb push boot-gb.img /sdcard/
```
**Step 2.** flash boot img onto boot partition.
```
adb shell flash_image boot /cache/boot-gb.img

 or

adb shell flash_image boot /sdcard/boot-gb.img
```
**Step 3** install kernel modules.
```
adb remount
adb shell umount /system/lib/modules
adb push modules.sqf /system/lib/modules/
adb push wireless.ko /system/lib/modules/
busybox mount -o loop /system/lib/modules/modules.sqf /system/lib/modules
```