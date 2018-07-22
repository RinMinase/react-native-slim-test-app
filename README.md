## Development Environment setup
### On GitHub
```
git clone https://github.com/RinMinase/react-native-test-app.git
cd react-native-test-app
```

### On GitLab
```
git clone https://gitlab.com/javascript-enthusiats/react-native-test-app
cd react-native-test-app
```

## Pre-requisites
1. Android SDK
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
2. Android Build Tools 26.0.3
3. Android Platform Tools
	- Install both of these by running the command below:
	- `sdkmanager platform-tools build-tools;26.0.3`
4. Gradle
	- Install the latest [Gradle binary-only release](https://gradle.org/releases/)
	- Similar to the steps above, unpack it to a folder of your preference
	- Similar to the steps above, add the `\bin` folder of your unpacked gradle folder to your environmental variables
5. Java JDK
	- Install the JDK for your system from [Java's JDK Download page](http://www.oracle.com/technetwork/java/javase/downloads/jdk8-downloads-2133151.html)
6. Setting of additional Environmental Variables
	- Follow the steps above on adding an environmental variable, but this time, instead of using `PATH` or `Path` for its variable / variable name follow the table below:

| Variable Name | Path |
| --- | --- |
| ANDROID_HOME | `<your root android-sdk folder>` (one level above `\tools`) |
| JAVA_HOME | `<your JDK folder>` (the root folder of your JDK) |

7. Yarn
	- Although you could setup this project using NPM, we recommend you to use yarn as it is a well created package manager that properly utilizes (by using parallel requests) the capabilites of your network to install the dependencies of your project faster
	- The installer is provided in [Yarn's Website](https://yarnpkg.com/en/)
	- After the installation has completed, run your terminal / command line and enter `yarn -v`
		- If it display's the version of the yarn proceed to the next step
		- If it does not, add the `\bin` folder of the installed yarn application (typically found in `C:\Program Files\yarn`) to your environmental variables
		- After doing the process above, verify by running your terminal again, then running the command `yarn -v` to validate if you have done it correctly.
8. React Native CLI
	- If you want to use NPM
		- Run `npm i -g react-native-cli` on your terminal
	- If you want to use Yarn
		- Run `yarn global add react-native-cli` on your terminal

After the tedious setup done above, you can now fully modify and build your test application.

## Setting up the project
```
yarn install
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

### Footnotes
> The latest version of React Native `0.56.0` and Babel's Preset on React Native `5.0.0` had an issue on compiling on Android, which is why we used the "latest" working version `0.55.4` on React Native and `2.1.0` on Babel's Preset for React native respectively.
