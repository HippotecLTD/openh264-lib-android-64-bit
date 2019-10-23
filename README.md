openh264-lib-android-64-bi
==========================
A repo for holding 64-bit versions of Cisco's OpenH264 binaries, because Cisco wouldn't do it for some reason

## The "why?"
OpenH264 is Cisco's implementation of the famous H264 codec. It resides here: https://github.com/cisco/openh264
For some strange reason Cisco will only compile its H264 binaries to 32-bit for Android.

This makes them quite useless since Google is [enforcing 64-bit](https://developer.android.com/distribute/best-practices/develop/64-bit) [across the board](https://android-developers.googleblog.com/2019/06/moving-android-studio-and-android.html) on the Android platform.

## The "how?"
All binaries in this repo were compiled from the corrsponding source, using the following commands:
```
make OS=android NDKROOT=/Users/vaiden/dev/tools/android-ndk-r17c TARGET=android-28 ARCH=arm64 NDKLEVEL=28 NDK_TOOLCHAIN_VERSION=clang
```
And
```
make OS=android NDKROOT=/Users/vaiden/dev/tools/android-ndk-r17c TARGET=android-28 ARCH=x86_64 NDKLEVEL=28 NDK_TOOLCHAIN_VERSION=clang
```
## The "where?"
Please take a look at the releases tab.

License
-------
BSD, see `LICENSE` file for details.
