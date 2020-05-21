[toc]



# demo_0518_2

A new Flutter project.

## Getting Started

This project is a starting point for a Flutter application.

A few resources to get you started if this is your first Flutter project:

- [Lab: Write your first Flutter app](https://flutter.dev/docs/get-started/codelab)
- [Cookbook: Useful Flutter samples](https://flutter.dev/docs/cookbook)

For help getting started with Flutter, view our
[online documentation](https://flutter.dev/docs), which offers tutorials,
samples, guidance on mobile development, and a full API reference.



# MethodChannel

## flutter 调 native

### Dart实现

1. 定义特定的MethodChannel，标识为“com.sicilyliu”
2. 定义点击触发的Future方法，里面调用的MethodChannel.invokeMethod

### swift实现

1. 初始化FlutterViewController，FlutterMethodChannel
2. 定义methodChannel.setMethodCallHandler，里面根据调过来的方法名和参数做相应处理

## native 调 flutter

### swift实现

1. 初始化FlutterViewController，FlutterMethodChannel
2. 调用methodChannel.invokeMethod，传参方法名和参数

### Dart代码

1. 唤醒监听nativeMessageListener()，可以放在initState()里面
2. 定义监听处理nativeMessageListener()的Future方法，根据调过来的方法名和参数做处理

