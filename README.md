## Development Environment setup
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
npm install
```

## To build an Android package file (APK) or an iOS package file (IPL)
The setup uses exp library to bundle an APK / IPL package files.

Although the readme in [create-react-native-app](https://github.com/react-community/create-react-native-app) explicitly stated that the `exp` library should be installed globally, this project has configured it by running the scripts located in `package.json` under the key `scripts.bundle-android`.

The maintainers wanted to reduce the clutter created on your global libraries since this is only a boilerplate project, and likewise, the dependencies can be modularly installed. This also reduces the amount of time and steps for the process of setting up the project for the cost of storage space (which would be noticeable if you were to create another project with an `exp` library installed in it).

### For Android
```
npm run bundle-android
```

### For iOS
```
npm run bundle-ios
```