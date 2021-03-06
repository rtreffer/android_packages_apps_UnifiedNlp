UnifiedNlp
==========
The next generation NetworkLocationProvider, based on plugins

Installation
------------
Release builds may be found on the [release page](https://github.com/microg/android_packages_apps_UnifiedNlp/releases).
Installation requires a rooted system.

### Android 4.1 - 4.3 (Jelly Bean)
Download `LegacyNetworkLocation.apk`, copy it to `/system/app/NetworkLocation.apk` and reboot. The following shell commands will do the job:

	adb root && adb remount
	adb push path/to/LegacyNetworkLocation.apk /system/app/NetworkLocation.apk
	adb reboot

### Android 4.4 (KitKat)
Download `NetworkLocation.apk`, copy it to `/system/priv-app/NetworkLocation.apk` and reboot. The following shell commands will do the job:

	adb root && adb remount
	adb push path/to/NetworkLocation.apk /system/priv-app/NetworkLocation.apk
	adb reboot

Usage
-----
UnifiedNlp as it does not provide any location provider features, but acts as a middleware for multiple backends. 

Here is an open list of backends known to me:

-	[AppleWifiNlpBackend](https://github.com/microg/AppleWifiNlpBackend) - backend that uses Apple's service to resolve wifi locations
-	(...) Create issue or pull request to extend this list :)

As part of a custom ROM
-----------------------
UnifiedNlp can be build as part of Android when building an Android ROM from source.

Add the repo to your (local) manifest.xml and extend the `PRODUCT_PACKAGES` variable with `NetworkLocation` for KitKat and `LegacyNetworkLocation` for Jelly Bean.

Backend-development
-------------------
Take a look at the API documentation in `/api/README.md`. You might also be interested in the sample backends in `/sample/`

Building
--------
To be build with Android Build System using `make UnifiedNlp`, `make LegacyNetworkLocation` or `make NetworkLocation`

Attribution
-----------
Some components: Copyright (C) 2013 The Android Open Source Project
