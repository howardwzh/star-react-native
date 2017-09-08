# 参考资料
- [React-Native学习指南](https://github.com/reactnativecn/react-native-guide)
- [用 React Native + Firebase 开发跨平台行动应用程式](https://github.com/carlleton/reactjs101/tree/zh-CN/Appendix02)
- **[react-native中文文档-嵌入到现有原生应用](http://reactnative.cn/docs/0.40/integration-with-existing-apps.html#content)**

# 开始旅程

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
