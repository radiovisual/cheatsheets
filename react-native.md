# React Native

## Learning React Native

* [The Essential Boilerplate to Authenticate Users on your React-Native app](https://medium.com/@alexmngn/the-essential-boilerplate-to-authenticate-users-on-your-react-native-app-f7a8e0e04a42#.9ghi2cd0p)
* [The Ultimate Guide to Mobile API Security](https://stormpath.com/blog/the-ultimate-guide-to-mobile-api-security)
* [Goodbye ../../../ Removing relative paths when importing](http://davidboyne.co.uk/2016/04/29/react-webpack-gem.html)
* [Testing React Native and Redux](https://blog.hellojs.org/testing-react-native-and-redux-e5a71b99e178)
* [Awesome Tutorial via makeitopen.com](http://makeitopen.com/)
* [http://facebook.github.io/react-native/](http://facebook.github.io/react-native/)
* [Custom Native iOS Views with React Native](http://almostobsolete.net/react-native/custom-ios-views-with-react-native.html)
* [5 Open Source React Native Projects To Learn From](https://medium.com/@bilalbudhani/5-open-source-react-native-projects-to-learn-from-fb7e5cfe29f2#.i8tor0vci)
* [FrontEnd Masters: React Native (feat. Redux)](https://frontendmasters.com/courses/react-native/)

## Testing React Native

* [Testing React Native with the New Jest - Part 1](https://blog.callstack.io/unit-testing-react-native-with-the-new-jest-i-snapshots-come-into-play-68ba19b1b9fe)
* [Testing React Native with the New Jest - Part 2](https://blog.callstack.io/unit-testing-react-native-with-the-new-jest-ii-redux-snapshots-for-your-actions-and-reducers-8559f6f8050b#.nu1a8mlnx)
* [Unit Testing with Jest](https://facebook.github.io/react-native/docs/testing.html)
- [React Native at Walmart Labs](https://medium.com/walmartlabs/react-native-at-walmartlabs-cdd140589560#.tkfs3hktj) - Some nice notes on the full RN test suite at Walmart.

## Tech Stacks
- [React Native App Stack (March 2017)](https://medium.com/react-native-development/react-native-app-stack-march-2017-f7605e02d46f#.q0y5lb4jp)

## Demos 

- [Expo Sketch](https://sketch.expo.io/) Quickly test and share RN ideas and demos from the browser. (Think JSFiddle for RN)

## Animations

- [React-native Animated API with PanResponder](http://browniefed.com/blog/react-native-animated-api-with-panresponder/)
- [React Native Animations Revisited Part 1](https://blog.callstack.io/react-native-animations-revisited-part-i-783143d4884#.xslc1bfy2)
- [Toolbar Animation in React Native (1/2)](https://medium.com/react-native-motion/toolbar-animation-in-react-native-fe89c4f8e4cf#.pk3ngfdtf)
- [Toolbar Animation in React Native (2/2)](https://medium.com/react-native-motion/toolbar-animation-in-react-native-2-2-f04ac45c7c11#.vsdhnhrnr)

## Layout

* [Understanding React Native Flexbox Layout](https://medium.com/the-react-native-log/understanding-react-native-flexbox-layout-7a528200afd4#.wo4v5rvrg)
* [A Mini Course on React Native Flexbox](https://medium.com/the-react-native-log/a-mini-course-on-react-native-flexbox-2832a1ccc6#.dour9qjai)

## Designing Cross Platform

* [A Tale of Two Platforms: Designing for Both Android and iOS](https://webdesign.tutsplus.com/articles/a-tale-of-two-platforms-designing-for-both-android-and-ios--cms-23616)

## Publishing to Google Play

* [Signed APK (Andriod)](https://facebook.github.io/react-native/docs/signed-apk-android.html)

## Live Code Updates

* [ReactNative: Zero to DevOps](https://www.youtube.com/watch?v=lfqZ8Uy2p3U&feature=youtu.be) Code Push, Analytics and Crash Reporting Setup
* [Code Push](https://microsoft.github.io/code-push/) by Microsoft
* [So You Want To Dynamically Update Your React Native App](https://medium.com/@clayallsopp/so-you-want-to-dynamically-update-your-react-native-app-d1d88bf11ede)

## Tips and Tricks

* [Handling the Keyboard in React Native](http://blog.arjun.io/react-native/mobile/cross-platform/2016/04/01/handling-the-keyboard-in-react-native.html)

## Adding Custom Fonts

- Create a `src/fonts` directory.
- Move your custom fonts into this directory.
- Add an `"rnpm"` entry into your `package.json` file:
```
"rnpm": {
  "assets": [
    "src/fonts"
    ]
  }
```
- Run `react-native link` to link your font assets. 
- That's it! Now you can start using the fonts by [PostScript name](http://stackoverflow.com/a/41636431/3960969) inside your project.
 
## Making Native Modules

- [How to Create a React Native iOS Native Module](http://blog.tylerbuchea.com/how-to-create-a-react-native-ios-native-module/)
- [Native Modules: Android](http://facebook.github.io/react-native/docs/native-modules-android.html)
- [Native Modules: iOS](http://facebook.github.io/react-native/docs/native-modules-ios.html)
