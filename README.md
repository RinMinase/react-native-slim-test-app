## Pre-requisites
1. **Android SDK**

    &nbsp;&nbsp;&nbsp;&nbsp;This is a command-line tool which would help you install the other needed prerequisites below. Although this can be achieved graphically by using Android Studio, this was opted to be used instead, due to its smaller file size (Android Studio is 800+MB, while the command-line tools is only 150+MB) since this project would not be using the Android Studio for the creation of the application.

	- The installation file is located in the [Command line tools section](https://developer.android.com/studio/#command-tools) in the Android Developers page.
	- Download the installation file for your system (Windows/Linux/Mac)
	- Unpack the zip file to any location of your preference (preferrably in the `C:\Program Files\android\` folder)
	- Set the environmental variables of your unpacked folder (`<folder name>\tools`)
		- To set your environmental variables, open your file manager (Windows Explorer) and navigate to Computer
		- Right click on a blank space on the window and select `Properties`, this would open a new window with the properties of your system listed or displayed
		- On the window (System) that just opened, select `Advanced system settings`, this would open another window which would be directed and opened at the `Advanced` tab
		- On the window (System properties) that just opened, select `Environment Variables`
		- Go to the `System Variables` and look for the entry for `PATH` or `Path`, then click the button `Edit`
			- (Replace the `<folder name>` with the path of your android-sdk folder which you have unpacked earlier)
			- Prior to Windows 10 machines:
				- Add the folder android-sdk folders `<folder name>\tools` and `<folder name>\tools\bin` each separated with a semi-colon
			- To Windows 10 machines
				- Click the `New` button
				- Add the entry `<folder name>\tools`
				- Click the `New` button again
				- Add the entry `<folder name>\tools\sdk`
	- To verify the setup above, open a terminal and input: `sdkmanager --version`
		- It should pop out the version of your installed android sdk, if not retry the steps done above

2. **Android Build Tools 26.0.3 and Android Platform Tools**

    &nbsp;&nbsp;&nbsp;&nbsp;Android Build and Platform Tools are components of the Android SDK and are required for Android app development. The Build Tools is required for building Android apps and the  Platform Tools are tools that connects with Android, such as `adb`, a debugging utility which lets you control your Android device with your computer.

	- Install both of these by running the command below:

      `sdkmanager platform-tools build-tools;26.0.3`

3. **Gradle**

    &nbsp;&nbsp;&nbsp;&nbsp;Gradle is a dependency or library management software for Java projects (or in this case, Android). It helps you to download them and to configure your listed dependencies automatically.

	- Install the latest [Gradle binary-only release](https://gradle.org/releases/)
	- Similar to the steps above, unpack it to a folder of your preference
	- Similar to the steps above, add the `\bin` folder of your unpacked gradle folder to your environmental variables

4. **Java JDK**

    &nbsp;&nbsp;&nbsp;&nbsp;Java Development Kit (JDK) is a software development environment used for developing Java (or in this case, Android) applications. This builds your the Java source code generated by React Native to a usable software.

	- Install the JDK for your system from [Java's JDK 8 Download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)

5. **Setting of additional Environmental Variables**

    &nbsp;&nbsp;&nbsp;&nbsp;These are pre-requisites of React Native to specify the folder locations of your Android SDK and your Java Development Kit (JDK).

	- Follow the steps above on adding an environmental variable, but this time, instead of using `PATH` or `Path` for its variable / variable name follow the table below:

| Variable Name | Path |
| --- | --- |
| ANDROID_HOME | `<your root android-sdk folder>` (one level above `\tools`) |
| JAVA_HOME | `<your JDK folder>` (the root folder of your JDK) |

6. **Yarn**

    &nbsp;&nbsp;&nbsp;&nbsp;Although you could setup this project using NPM, it is recommended that you should be using yarn instead. Yarn is a well created package manager that properly utilizes (by using parallel requests) the capabilites of your network to install the dependencies of your project way faster.

	&nbsp;&nbsp;&nbsp;&nbsp;Do note that although Yarn is better than NPM on most of the use cases of a typical developer, since it takes the most of the limitations of NPM in consideration.

	These limitations include:

	- Synchronous (non parallel) downloading to speed up acquisition of libraries
	- Synchronous downloading to efficiently use the network bandwidth
	- Slow acquisition of libraries from cache storage due to the folder structure of its cached libraries
	- No flat installation for reducing the complexity of installed libraries
	- No library version resolution to reduce conflicts of different versions of the same library installed.

	&nbsp;&nbsp;&nbsp;&nbsp;But despite these, Yarn could not be used without NPM, since all the packages installed by Yarn are from the repository of NPM. It is just an alternative manager for the repository of NPM, since Yarn does not have its own collection of libraries.

	- The installer is provided in [Yarn's Website](https://yarnpkg.com/en/)
	- After the installation has completed, run your terminal / command line and enter `yarn -v`
		- If it display's the version of the yarn proceed to the next step
		- If it does not, add the `\bin` folder of the installed yarn application (typically found in `C:\Program Files\yarn`) to your environmental variables
		- After doing the process above, verify by running your terminal again, then running the command `yarn -v` to validate if you have done it correctly.

7. **React Native CLI**

    &nbsp;&nbsp;&nbsp;&nbsp;This is for you to be able to create or build React Native code from the command-line to your Android or Apple device.

	_It is recommended that you should **NOT** use `yarn` on installing **global** modules due to conflicts with npm_

	- Run the command below on your terminal:

	  `npm install --global react-native-cli`

    &nbsp;&nbsp;&nbsp;&nbsp;After the tedious setup done above, you can now fully modify and build your test application.

## Development Environment setup
### On GitHub
```
git clone https://github.com/RinMinase/react-native-test-app.git
cd react-native-test-app
yarn install
```
or if you did not install Yarn
```
git clone https://github.com/RinMinase/react-native-test-app.git
cd react-native-test-app
npm install
```

### On GitLab
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
yarn install
```
or if you did not install Yarn
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
npm install
```

## To build an Android (APK) or an iOS (IPL) package files

### For Android
1. Plug in your android device
2. Turn on the `USB debugging` or `ADB` setting of your device.
	- This is most likely located in the `Developers Options` of your device.
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

## Additional Information
&nbsp;&nbsp;&nbsp;&nbsp;Other projects may include Expo to improve React-Native's way of compiling your source code. This also helps you build native iOS and Android apps using JavaScript and React easier. But for this approach, this increases the build size of the APK file from 15mb to around 45mb. This may be due to the previous setup of this project, so instead this project opted to remove Expo to reduce the build size and likewise the complexity of understanding the other dependencies of the project.

## Footnotes
> The latest version of React Native `0.56.0` and Babel's Preset on React Native `5.0.0` had an issue on compiling on Android, which is why this project used the "latest" working version `0.55.4` on React Native and `2.1.0` on Babel's Preset for React native respectively.
