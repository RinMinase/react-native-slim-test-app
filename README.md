## Development Environment setup
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
npm install
```

## To build an Android (APK) or an iOS (IPL) package files
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

The setup will ask you to login with your credentials in Expo, but if you have not yet created an account, please do so. This can be done in the terminal or through their [website](https://expo.io/signup), then follow through with the process.

The terminal upon running `npm run bundle-android` or `npm run bundle-ios` would return:
> How would you like to authenticate?
> - Create a new Expo Account
> - Log in with an existing Expo Account
> - Cancel

> ### Note:
> The whole process could take a while to process your request. The terminal should print out a `link` in which you will be able to see your current build log.

After the build steps have completed, the terminal will print out a `link` on where you can download the built file.