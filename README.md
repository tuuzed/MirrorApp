# WMirror

[![](https://img.shields.io/badge/WMirror-v0.5.4-green.svg)](https://github.com/tuuzed/WMirror)

轻松使用Chorme浏览器或Android手机控制您的Android手机


## ADB免Root版


[下载 wmirror.jar](https://github.com/tuuzed/WMirror/releases/download/v0.5.4-beta/wmirror.jar)

- 需要开启USB调试模式

- 支持全功能

### 启动命令参数说明

```
-p 端口号（取值范围，1024-65535）
-s 缩放率（取值范围，0.1~1.0）
-q 清晰度（取值范围，1~100，支持设置数组以`,`分隔）
-f 压缩格式（取值，JPEG | WEBP | PNG）
```
### Windows启动命令

```bat

adb forward tcp:6688 tcp:6688

adb push .\wmirror.jar /data/local/tmp/classes.jar

adb shell "export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp wmirror.ProcessMain -p 6688 -s 0.5 -q 100 -f JPEG"

```

### *nix启动命令

```sh

adb forward tcp:6688 tcp:6688

adb push ./wmirror.jar /data/local/tmp/classes.jar

adb shell "export CLASSPATH=/data/local/tmp/classes.jar && app_process /data/local/tmp wmirror.ProcessMain -p 6688 -s 0.5 -q 100 -f JPEG"

```



## 已Root机型


[下载 wmirror.android-0.5.4-beta-armeabi-v7a.apk](https://github.com/tuuzed/WMirror/releases/download/v0.5.4-beta/wmirror.android-0.5.4-beta-armeabi-v7a.apk)

- 支持全功能

## Android5.0以上系统机型

[下载 wmirror.android-0.5.4-beta-armeabi-v7a.apk](https://github.com/tuuzed/WMirror/releases/download/v0.5.4-beta/wmirror.android-0.5.4-beta-armeabi-v7a.apk)

- 支持远程网页浏览器查看屏幕内容

- Android7.0及以上系统开启无障碍服务可远程控制

