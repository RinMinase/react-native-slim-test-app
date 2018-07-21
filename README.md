## Development Environment setup
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
```

## Pre-requisites
1. Android SDK
2. Android Build Tools 26.0.3
3. Android Platform Tools
4. Gradle
5. Setting of additional Environmental Variables
6. Yarn

## Setting up the project
```
yarn install
```

## To build an Android (APK) or an iOS (IPL) package files

### For Android
1. Plug in your android device
2. Turn on the {nav USB debugging} or {nav ADB} setting of your device.
    - This is most likely located in the {nav Developers Options} of your device.
3. Then run the command stated below:
```
react-native run-android
```

### For iOS
`<Additional readme content necessary here>`
```
react-native run-ios
```

## Built With
- Framework > React-Native [0.55.4]
- Testing > Jest [23.4.0]
- Transpiler > Babel's Preset for React Native [2.1.0]
- Test Renderer > React's Test Renderer [16.4.1]

### Footnotes
> The latest version of React Native (0.56.0) and Babel's Preset on React Native (5.0.0) had an issue on compiling on Android.