## 百度移动统计Cordova Demo
### iOS
1. clone此代码库
2. 打开$(home)/platforms/ios/HelloWorld.xcworkspace
3. 工程中已经集成了MTJ的SDK，以及百度移动统计Cordova插件，可以直接运行调试
4. JS Api调用示例，请查看$(home)/www/js/index.js 文件。

### Android
1. clone此代码库，并运行
	
	```
  	cordova plugin add cordova-plugin-baidumobstatistics --variable IOSAPPID=[your iOS AppKey] --variable ANDROIDAPPID=[your Android AppKey]
  	cordova prepare
  	```

2. 运行
	
	```
  	cordova run android
  	```
	
3. 调试
	
	需要在java代码中打开调试开关：
	
	```
	StatService.setDebugOn(true);
	```
	
	可以通过 `adb logcat -s sdkstat` 确认统计日志发送成功到服务器，logcat显示 `send log data over. result = true;`即发送成功。 
	
