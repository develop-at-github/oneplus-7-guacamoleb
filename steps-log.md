Starting Ubuntu Touch UB-ports for OnePlus 7 aka guacamoleb (not a typo, since guacamole is 7 Pro)

Starting point is [official UB-ports porting doc](https://docs.ubports.com/en/latest/porting/introduction/index.html).

As advised in the doc, this doc is a log of steps performed to attempt porting UT to OP7 since no such port exists.7

```
Thus an Ubuntu Touch port is composed of the these components:
1. The Ubuntu Touch (UT) root filesystem (rootfs)
2. Halium (contained in the boot and system images)
3. The vendor blobs
```

Build Halium?
Install LineageOS? -> readily available

install adb and fastboot, developer tools, usb debugging, oem unlock
cmd `fastboot oem unlock` failed with error "FAILED (remote: 'Device cannot be unlocked for technical reason.')"
Solution is to downgrade to Android 11 and retry. https://droidwin.com/downgrade-oneplus-7-7t-7t-pro-android-12-to-android-11-2-methods/
Trying zip method. -> worked

flashing TWRP now -> flashed

Should I try lineage OS first? -> tried and worked. IMEI 2 is all zeroes 00000 :( but show up in settings :')

UT needs python >= 3.66
python3 command is already present v3.11.2

installed other tools needed as per UT page for debian as well as ubuntu >= 20

build standalone kernel image using steps in doc and gitlab 
