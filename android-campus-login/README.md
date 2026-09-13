# 校园网自动登录 Android App

用 Android Studio 打开本目录，等待 Gradle 同步后运行或生成 APK。

首次使用：

1. 安装并打开 App。
2. 授予 Wi-Fi/附近设备权限。
3. 输入学号和密码，点击“连接并认证”。
4. 如果手机尚未连接 `zzuli-student`，按系统提示确认连接。

账号按中国联通格式提交：`,0,学号@unicom`。密码使用 Android Keystore 加密保存，不写入日志。

Android 10 及以上不允许普通 App 完全静默加入陌生 Wi-Fi，首次连接可能出现一次系统确认框；已经连接该 Wi-Fi 时，认证请求可以在后台完成。

工程未附带 Gradle wrapper；使用 Android Studio 的内置 Gradle 即可构建。需要联网下载 Android Gradle Plugin 和依赖。

不安装 Android Studio 的构建方式：将本目录上传到 GitHub，新建或打开 Actions，运行 `Build APK` workflow；完成后在该 workflow 的 Artifacts 下载 `campus-auto-login-debug`，解压即可得到 APK。
