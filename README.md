# React Native + Hermes

:fire: React Native with Hermes

## Enable Hermes with Android
Edit File wtih below code - **android/app/build.gradle** and clean build using **cd android && ./gradlew clean**

```
...
project.ext.react = [
    enableHermes: true,  // clean and rebuild if changing
]
...
def enableHermes = project.ext.react.get("enableHermes", true);
...
```

## Enable Hermes with iOS

edit **ios/Podfile** and run **pod install**

```
use_react_native!(
   :path => config[:reactNativePath],
   # to enable hermes on iOS, change `false` to `true` and then install pods
   :hermes_enabled => true
)
```

## Common Commands

- `npx react-native run-android` OR `npm run android` Runs dev server for android
- `npx react-native run-ios` OR `npm run ios` Runs dev server for ios
