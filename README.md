# Note-of-React-Native
总结React-Native开发经验

##### 主要使用的第三方控件以及相关笔记
> ###### react-native-cli ```环境搭建```
> ```npm install --save-dev react-native-cli```
> [Github地址]()
> 创建简易的React-Native项目
***
> ###### react-native-network-image ```第三方控件```
> ```npm install --save react-native-network-image```
> [Github地址]()
> 调整网络图片的显示大小
***
> ###### react-native-tab-navigator ```第三方控件```
> ```npm install --save react-native-tab-navigator```
> [Github地址]()
> App常见底部导航
***
> ###### art ```第三方控件```
> ```npm install --save art```
> [Github地址]()
> 创建和编辑App当中的SVG
***
> ###### native-base ```第三方控件```
> [官网地址](http://nativebase.io)
> 跨平台的基础组件库
***
> ###### react-native-elements ```第三方控件```
> [Github地址](https://github.com/react-native-community/react-native-elements)
> 跨平台的基础组件库
***
> ###### react-native-storage  ```第三方控件```
> ```npm install --save react-native-storage```
> [Github地址]()
> App本地持久存储
***
> ###### ListView ```开发教程```
> 
***
> ###### react-native-audio ```第三方控件```
> ```npm install --save react-native-audio```
> [Github地址](https://github.com/jsierles/react-native-audio)
> App音频录制和播放
***
> ###### React-Native 手势 ```开发教程```
> [Github地址](https://github.com/jabez128/jabez128.github.io/issues/1)
***
> React-Native 声明属性和属性确认 ```开发问题```
> [依旧采用React的声明属性](http://www.jianshu.com/p/19c1838a6a89)
> 但是存在常见类型不对应的情况,例如:
> ```
<Image source={inputSource} />
inputSource:PropTypes.object //错误
inputSource:PropTypes.number //正确
> ```
***
> ###### 输入框被键盘遮挡 ```开发问题```
> [解决方法](https://www.debugnode.com/react-native-keyboard-avoid/)
***
> ###### react-native-image-picker ```第三方控件```
> ```npm install --save react-native-image-picker```
> [Github地址](https://github.com/marcshilling/react-native-image-picker)
> 选择图片并操作
***
> ###### ESLint ```环境搭建```
* [相关文章](https://medium.com/the-react-native-log/getting-eslint-right-in-react-native-bd27524cc77b#.6p9j7c3m3)
* [相关文章](https://medium.com/@franzejr/how-to-use-eslint-in-react-native-ed9c53dde0d0#.homat6nvd)
* [ESLint文档](http://eslint.cn)
> 在项目当中启用Eslint代码检查
***
> ######开发过程中遇到的问题 ```开发问题```
> 1. react-native在iOS9以后默认默认只发送https请求，对于http请求的图片存在加载不上的问题，需要在info.list当中配置，[解决方法如下](https://segmentfault.com/q/1010000005882935/a-1020000005951234)：
```
add row:App Transport Security Settings
add item:Allow Arbitrary Loads-YES
```
> 2. 相册当中显示英文，需要在info.list当中配置，[解决方法如下](https://my.oschina.net/frank9527/blog/220306)：
```
add row:Localized resources can be mixed-YES
```
> 3. React-Native上传的文件并不是blob的二进制形式，而只是一个包含了name、uri、type三个属性的JSON对象 
```
{
  uri: fileuri,
  type: "image/jpeg",
  name: filename
}
```
> 4. KeyboardAvoidingView使用注意事项，KeyboardAvoidingView标签外部不能包裹其他标签，否则容易导致输入框上移失效
> 5. 关于React-Native跨平台的解决方案,有下列文章可供参考:
[Better Cross-Platform React Native Components](https://medium.com/differential/better-cross-platform-react-native-components-cb8aadeba472#.i1bprd320)
> 6. [闪退处理](http://www.jianshu.com/p/5aec8051f787),[闪退原因](http://blog.csdn.net/sinat_34194127/article/details/52948513)
> 7. ListView第一次加载出现不渲染数据,需要拉动或者点击才能触发渲染数据的情况.解决方法可以参考下列问题:[问题A](https://github.com/facebook/react-native/issues/1831#issuecomment-222106476),[问题B](http://facebook.github.io/react-native/releases/0.42/docs/performance.html#listview-initial-rendering-is-too-slow-or-scroll-performance-is-bad-for-large-lists)
