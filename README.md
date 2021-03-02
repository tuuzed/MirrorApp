# MirrorApp

[![](https://img.shields.io/badge/MirrorApp-v0.8.1--beta-green.svg?style=for-the-badge&logo=data:image/png;base64,iVBORw0KGgoAAAANSUhEUgAAACAAAAAgCAMAAABEpIrGAAAAAXNSR0IB2cksfwAAAAlwSFlzAAALEwAACxMBAJqcGAAAAYlQTFRFAAAA////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////////VkzjgAAAAIN0Uk5TAAELKE9mAiF3vuD1+w5q2/3/GJ/64aSGF6vohSsDKgiU/tFDEYKuPlTz0jQ/8rg6Mw/AUSTn+eNOBiex2ASQ9EsQjpcHtM0SxRsupuu/CYv3RgWauWP8V1jZvSPBGcQMFJsxaNwv1R1zE3wVu50WMNRB2jzprSweQq8tDV+38aBJH7Vf73Q+AAAB9ElEQVR4nIWT+1/SUBjGD1eVAe4RhgKSolY4wVJrKIkagYWXIpSheMVbGUhZEzLx+pc7Lm1jrE/PT+d5v8/OOe85O4TI0ukNRpPJaNDriJbMHZ1dFspqpSxdnR3mdm6zd9Noiu6229S8x+EEGFev3d7rYgCno6eV97kBj7ffV1/ridcDuPuUfGDQj6FhceGRp8+8z23m4SH4BwcUgcAo2LHaIEgBofEX5CWL0YDMJyYRmqqPXo2/5oCwkUyFMDkhBaYpuGaazUQCb6yYNURdoKalwBzmF+T53sZovCML85j7W4knsPhe2fIHzCZHFpGI1+1SbHkFqx+VTX1C6nN6FSvLsSXxAtZqZ7ceVwYy4LO+9Vp9TbyWjc0wh5yyabK1vb01kwMX3twQnW8nsovdvZaD3d8ne2IxsuNr+Dw8B0SlAw/ykjmk4VUHvKAPJZNkcXTcyo+PcPJFtl+tcJ8q+akb9DeFLxRBn5VkXzqjkSspv/j+A3TxPN0w6fMijZ9jrWv+YgHhIlOuVMqZCwE4+a3edf9lCuAFhhF4IHX5R80Juape3zT+2Zvr6lU7F6UPmm55/tYU1Gviuu447u7f9D8Bc+G+kqw6ndVk5b6g8bJIlmUYi+D3CxaGYbPtXJeHQnmN91t2PCSaenCUtTYRjUuKytVHP99YPfdanDQAAAAASUVORK5CYII=)](https://github.com/tuuzed/WMirror/releases/latest)

轻松投屏和远程协助Android手机


## ADB免Root版


[下载 libplugin.jar](https://github.com/tuuzed/MirrorApp/releases/download/v0.8.1-beta/libplugin.jar)

- 需要开启USB调试模式

- 支持全功能

### 启动命令参数说明

```
-p 端口号（取值范围，1024-65535）
-r 分辨率（取值范围，320 | 480 | 720 | 1080）
-q 清晰度（取值范围，1~100，支持设置数组以`,`分隔）
-f 压缩格式（取值，JPEG | WEBP | PNG）
```
### Windows启动命令

```bat

adb forward tcp:6688 tcp:6688

adb push .\libplugin.jar /data/local/tmp/classes.jar

adb shell "chmod 777 /data/local/tmp && export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp mirrorapp.ProcessMain -p 6688 -r 480 -q 100 -f JPEG -auth username:password"

```

or

```bat

adb forward tcp:6688 tcp:6688

adb push .\libplugin.jar /data/local/tmp/classes.jar

adb shell "chmod 777 /data/local/tmp && export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp mirrorapp.ProcessMain -p 6688 -r 480 -q 100 -f JPEG -auth username:password&"

```


### *nix启动命令

```sh

adb forward tcp:6688 tcp:6688

adb push ./libplugin.jar /data/local/tmp/classes.jar

adb shell "chmod 777 /data/local/tmp && export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp mirrorapp.ProcessMain -p 6688 -r 480 -q 100 -f JPEG  -auth username:password"

```

or

```sh

adb forward tcp:6688 tcp:6688

adb push ./libplugin.jar /data/local/tmp/classes.jar

adb shell "chmod 777 /data/local/tmp && export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp mirrorapp.ProcessMain -p 6688 -r 480 -q 100 -f JPEG  -auth username:password&"

```




## 已Root机型


[下载 mirrorapp.android-0.8.1-beta-armeabi-v7a.apk](https://github.com/tuuzed/MirrorApp/releases/download/v0.8.1-beta/mirrorapp.android-0.8.1-beta-armeabi-v7a.apk)

- 支持全功能

## Android5.0以上系统机型

[下载 mirrorapp.android-0.8.1-beta-armeabi-v7a.apk](https://github.com/tuuzed/MirrorApp/releases/download/v0.8.1-beta/mirrorapp.android-0.8.1-beta-armeabi-v7a.apk)

- 支持远程网页浏览器查看屏幕内容

- Android7.0及以上系统开启无障碍服务可远程控制

