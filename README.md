# android-i2c-tools
=================================
1. add Android.mk for i2c-tools-4.1 on Android source.
```
Usage:  
$ cd <android sources diretory>
$ . build/envsetup.sh
$ cd external && git clone git@github.com:inugi-source/android-i2c-tools.git
$ mmm android-i2c-tools
```
2. you can find binaries in out directory as below.
```
out/target/product/generic/system/bin/
```
3. install binaries and run with adb
```
$ cd out/target/product/generic/system/bin
$ adb remount
$ adb push i2cdetect /data/local/tmp
$ adb shell /data/local/tmp/i2cdetect -y 0
     0  1  2  3  4  5  6  7  8  9  a  b  c  d  e  f
00:          -- -- -- -- -- -- -- -- -- -- -- -- --
10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
40: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
70: -- -- -- -- -- -- -- --
```
