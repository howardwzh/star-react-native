# 参考资料
- [React-Native学习指南](https://github.com/reactnativecn/react-native-guide)
- [用 React Native + Firebase 开发跨平台行动应用程式](https://github.com/carlleton/reactjs101/tree/zh-CN/Appendix02)
- **[react-native中文文档-嵌入到现有原生应用](http://reactnative.cn/docs/0.40/integration-with-existing-apps.html#content)**

# 开始旅程

## 环境配置（mac）

1. [（Mac平台）ReactNative Android开发环境搭建小计](https://segmentfault.com/a/1190000004068339)
2. [react native android开发环境搭建（mac系统）](https://www.jianshu.com/p/cb8bbb499841)
3. [Mac环境下安装Genymotion](https://www.jianshu.com/p/0498a6fa7694)
4. [Genymotion安装模拟器报错“unable to create virtual device connection timeout occurred”](http://www.voidcn.com/article/p-rokjianw-ku.html)

## jdk

1. [下载安装包](http://www.oracle.com/technetwork/java/javase/overview/index.html)
1. 移动java到bin中 `sudo ln -s /Library/Java/JavaVirtualMachines/jdk /usr/bin/`
2. 缷载

```bash
I was able to unistall jdk 8 in mavericks successfully doing the following steps:

Run this command to just remove the JDK

sudo rm -rf /Library/Java/JavaVirtualMachines/jdk<version>.jdk
Run these commands if you want to remove plugins

sudo rm -rf /Library/PreferencePanes/JavaControlPanel.prefPane
sudo rm -rf /Library/Internet\ Plug-Ins/JavaAppletPlugin.plugin
sudo rm -rf /Library/LaunchAgents/com.oracle.java.Java-Updater.plist
sudo rm -rf /Library/PrivilegedHelperTools/com.oracle.java.JavaUpdateHelper
sudo rm -rf /Library/LaunchDaemons/com.oracle.java.Helper-Tool.plist
sudo rm -rf /Library/Preferences/com.oracle.java.Helper-Tool.plist
```

## 启动

### ios
1. Xcode->Preferences->locations->Command Line Tools->[select something]
2. shut down "Simulator" first
3. Terminal->`proxy`->`react-native run-ios`
4. wait~~~

### android

## debug

1. [调试](https://reactnative.cn/docs/0.51/debugging.html)
2. [React Native Debugger + Expo = AWESOME](https://www.gravitywell.co.uk/latest/rd/posts/react-native-debugger-expo-awesome/) 
3. [Create React Native App + React Native Debugger](https://www.youtube.com/watch?v=JY279kbJ0KM)



## 样式

- 使用JavaScript来写样式, 所有的核心组件都接受名为style的属性
- 使用了驼峰命名法，例如将background-color改为backgroundColor
- 按顺序声明和使用style属性，以借鉴CSS中的“层叠”做法（即后声明的属性会覆盖先声明的同名属性）

```
import React, { Component } from 'react';
import { AppRegistry, StyleSheet, Text, View } from 'react-native';

class LotsOfStyles extends Component {
  render() {
    return (
      <View>
        <Text style={styles.red}>just red</Text>
        <Text style={styles.bigblue}>just bigblue</Text>
        <Text style={[styles.bigblue, styles.red]}>bigblue, then red</Text>
        <Text style={[styles.red, styles.bigblue]}>red, then bigblue</Text>
      </View>
    );
  }
}

const styles = StyleSheet.create({
  bigblue: {
    color: 'blue',
    fontWeight: 'bold',
    fontSize: 30,
  },
  red: {
    color: 'red',
  },
});

AppRegistry.registerComponent('LotsOfStyles', () => LotsOfStyles);
```


- [listView](http://reactnative.cn/docs/0.41/using-a-listview.html#content)
- [Navigator](http://reactnative.cn/docs/0.41/using-navigators.html#content)
- [布局样式属性](http://reactnative.cn/docs/0.41/layout-props.html#content)
- [React Native style -- 样式的使用](https://segmentfault.com/a/1190000004031633)
- [在原生和React Native间通信](http://reactnative.cn/docs/0.41/communication-ios.html#content)
- [TabNavigator](https://github.com/exponent/react-native-tab-navigator)
