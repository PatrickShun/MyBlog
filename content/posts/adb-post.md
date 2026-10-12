---
title: "常用命令集"
date: 2026-10-09T18:00:00+08:00
draft: false
tags: ["Linux", "技术", "学习笔记", "adb"]
categories: ["技术分享"]
description: "记录工作常用指令"
---


### 录屏
```bash
adb shell screenrecord /sdcard/demo.mp4
```

### 查进程的包名
```bash
adb shell ps -A | grep 'com.jidouauto'
```

### 查已安装的包名
```bash
adb shell pm list packages | grep 'jidou'
```

### 输入文本
```bash
adb shell input text "xxxx"
```

### 断开adb继续抓日志
```bash
adb shell "nohup logcat -v threadtime -f /data/local/tmp/1.log &"
```

### Dolby音频播放
```bash
adb shell setprop persist.vendor.cinemo.cars.cin_id.backend unprotected
```

### 日志等级 
```bash
adb shell setprop persist.log.tag E （降级） 
adb shell setprop persist.log.tag D （还原）
```
