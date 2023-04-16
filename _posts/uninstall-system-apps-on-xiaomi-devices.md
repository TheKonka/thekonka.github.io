---
layout: post
title: '小米手机通过ADB卸载内置软件'
---

> 酷安下载需从官网下载，应用商店里面的是社区版，搜不到应用

> 到应用商店里面升级 Google Play 商店

> 手机打开开发者选项，并开启 USB 调试

> 运行 adb devices 命令， 返回手机设备编号表示 ADB 连接正常

```
// 列出所有软件
adb shell pm list packages
```

```
adb shell pm uninstall --user 0 com.miui.systemAdSolution (小米系统广告解决方案)
adb shell pm uninstall --user 0 com.miui.analytics (小米广告分析)
adb shell pm uninstall --user 0 com.xiaomi.gamecenter.sdk.service (小米游戏中心服务)
// 使用 pm uninstall 会报错：Failure [-1000]
adb shell pm disable-user com.xiaomi.gamecenter (小米游戏中心)
adb shell pm uninstall --user 0 com.sohu.inputmethod.sogou.xiaomi (搜狗输入法)
adb shell pm uninstall --user 0 com.baidu.input_mi (百度输入法小米版)
adb shell pm uninstall --user 0 com.iflytek.inputmethod.miui (讯飞输入法小米版)
adb shell pm uninstall --user 0 com.miui.player (小米音乐)
adb shell pm uninstall --user 0 com.miui.video (小米视频)
adb shell pm uninstall --user 0 com.android.browser (浏览器)
adb shell pm uninstall --user 0 com.miui.translation.kingsoft (金山翻译)
adb shell pm uninstall --user 0 com.miui.miservice (服务与反馈)
adb shell pm uninstall --user 0 com.xiaomi.shop (小米商城)
adb shell pm uninstall --user 0 com.mi.health (手机管家)
adb shell pm uninstall --user 0 com.xiaomi.smarthome (米家)
```
