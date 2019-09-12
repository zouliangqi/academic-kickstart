---
title: "Flutter1"
date: 2019-09-12T14:25:49+08:00
draft: false
---

# Flutter 1、安装

## 官方镜像（配置环境变量）

```
export PUB_HOSTED_URL=https://pub.flutter-io.cn
export FLUTTER_STORAGE_BASE_URL=https://storage.flutter-io.cn
```

## SDK下载安装

1. flutter官网下载：https://flutter.io/sdk-archive/#windows

   GitHub下载：https://github.com/flutter/flutter/releases

2. 将安装包zip解压到你想安装Flutter SDK的路径

3. 在Flutter安装目录的`flutter`文件下找到`flutter_console.bat`，双击运行并启动**flutter命令行**，接下来，你就可以在Flutter命令行运行flutter命令了。

## 使用

用flutter命令行使用：

```commandline
flutter doctor   //查看是否需要安装任何依赖项来完成安装
flutter devices  //验证Flutter识别您连接的Android设备
cd 项目根目录
flutter pub get                //用pub工具获取所依赖的包
flutter run --release        //builds and installs the Flutter app
```

用Android studio：

1. 下载并安装 [Android Studio](https://developer.android.com/studio/index.html).
2. 打开插件首选项 File>Settings>Plugins
3. 选择 **Browse repositories…**, 选择 Flutter 插件并点击 `install`.
4. 重启Android Studio后插件生效.

## 创建新应用

1. 选择 **File>New Flutter Project**
2. 选择 **Flutter application** 作为 project 类型, 然后点击 Next
3. 输入项目名称 (如 `myapp`), 然后点击 Next
4. 点击 **Finish**
5. 等待Android Studio安装SDK并创建项目.

## 运行

1. 定位到Android Studio 工具栏:
   ![Main IntelliJ toolbar](https://flutterchina.club/images/intellij/main-toolbar.png)
2. 在 **target selector** 中, 选择一个运行该应用的Android设备. 如果没有列出可用，请选择 **Tools>Android>AVD Manager** 并在那里创建一个
3. 在工具栏中点击 **Run图标**, 或者调用菜单项 **Run > Run**.
4. 如果一切正常, 您应该在您的设备或模拟器上会看到启动的应用程序:

## 热重载

Flutter 可以通过 *热重载（hot reload）* 实现快速的开发周期，热重载就是无需重启应用程序就能实时加载修改后的代码，并且不会丢失状态（译者语:如果是一个web开发者，那么可以认为这和webpack的热重载是一样的）。简单的对代码进行更改，然后告诉IDE或命令行工具你需要重新加载（点击reload按钮），你就会在你的设备或模拟器上看到更改。

1. 将字符串
   `'You have pushed the button this many times:'` 更改为
   `'You have clicked the button this many times:'`
2. 不要按“Stop”按钮; 让您的应用继续运行。
3. 要查看您的更改, 只需调用 **Save All** (`cmd-s` / `ctrl-s`), 或点击 **热重载按钮** (带有闪电⚡️图标的按钮).

你就会立即看到更新后的字符串

