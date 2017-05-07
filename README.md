
Flashable ZIPs
---

This repository hosts the source of a variety of flashable ZIPs. These are packages that can be flashed to Android devices, usually to extend the system. They need to be flashed by a [custom recovery](https://wiki.cyanogenmod.org/w/All_About_Recovery_Images) such as [TWRP](https://twrp.me/), CWM Recovery or [CyanogenMod Recovery](https://download.cyanogenmod.org/). 

This repository also contains `zippo` (a kind of [lighter](https://en.wikipedia.org/wiki/Zippo)), a small `bash` script to forge ready-to-_flash_ ZIPs.


## Instructions

Create all available ZIPs (one for each folder) by running this command:
```sh
./zippo
```

Restart your device into recovery and start `ADB sideload`. Then run:
```sh
adb sideload <flashable-zip-name>
```

Alternatively, copy the resulting ZIPs to your device storage, restart your device into recovery and use the GUI `Install` or `Install ZIP` option.


## List of flashable ZIPs

### Unroot FP2 Open 

Clean way to unroot Fairphone 2 [Open OS](http://code.fairphone.com/projects/fp-osos/index.html#id2), that came prerooted and with TWRP. Removes `bin/su` and `xbin/su` binaries from `/system`.
Needed to pass SafetyNet requirements for some apps. [Guide](https://forum.fairphone.com/t/pencil2-how-to-install-any-app-on-fp-open-os-for-beginners-and-experts/22516) and [motivation behind](https://forum.fairphone.com/t/how-to-be-able-to-install-and-use-any-app-on-fp-open-os-experimental/22327/34?u=roboe).


### EmojiOne v2 Installer

Replace Android's default [emoji set](https://www.google.com/get/noto/help/emoji/) with [EmojiOne v2](https://www.emojione.com/emoji/v2). EmojiOne v2 is an emoji set more comprehensible than Android's one [before Marshmallow](http://blog.emojipedia.org/android-6-0-1-emoji-changelog/).  
EmojiOne v2 is the last [open and free](https://github.com/Ranks/emojione/blob/2.2.7/LICENSE.md) version of EmojiOne. EmojiOne v3 and later are **not open** to the public anymore.  
The flashable ZIP saves a copy of the previous installed emoji on your device at `/system/fonts/NotoColorEmoji.ttf.old`.
