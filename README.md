# Integrating-Android-App-with-React-native

I hope this setup helps to easily integrate existing Android application to new React Native application. 

1.	Install Node in the system:

    You can find additional installation options on the Node's Downloads page(https://nodejs.org/en/download/).

    If you have already installed Node on your system, make sure it is Node 8.3 or newer. If you already have a JDK on your system, make sure it is version 8 or newer.

2.	React Native CLI:

    Node comes with npm, which lets you install the React Native command line interface.
    Run the following command in a Command Prompt or shell:

    `npm install -g react-native-cli`

3.	Android Development setup:

    Download and install Android Studio (https://developer.android.com/studio/) Choose a "Custom" setup when prompted to select an installation type. Make sure the boxes next to all of the following are checked:
    -	Android SDK
    -	Android SDK Platform
    -	Performance (Intel ® HAXM)
    -	Android Virtual Device
    Then, click "Next" to install all of these components.
4.	Setup the environment path for Android:

    Add both the below path in System environment variables:
    -	C:\Users\Username\AppData\Local\Android\Sdk\tools
    -	C:\Users\ Username \AppData\Local\Android\Sdk\platform-tools
    
    Username equals to OSX name of the system.
5.	Create a new Application:

    `react-native init Testproject`

6.	Start Android Emulator:

    You can see the list of available Android Virtual Devices (AVDs) by opening the "AVD Manager" from within Android Studio. Click the Green triangle button to start the emulator.
    
7.	Add a file:

    Create and add a local.properties file in `C:\Users\Username\Code-setup\dump\react-native\Testproject\android`

    Add the below line:

    `sdk.dir = C:\\Users\\Username\\AppData\\Local\\Android\\Sdk`


8.	Start the React native project:

    `cd Testproject
    react-native run-android`
    
    ![alt text](https://github.com/niladri30/Integrating-Android-App-with-React-native/blob/master/img1.png)
    

For, error output on AVD:

![alt text](https://github.com/niladri30/Integrating-Android-App-with-React-native/blob/master/error1.png)

    To Solve this below are the required steps:

    - Create a folder assets in C:\Users\Username\Code-setup\dump\react-native\Testproject\android \app\src\main

    - Execute the below command:

    `adb reverse tcp:8081 tcp:8081`

c.	Run the project:

    `react-native run-android`

    If the error still persists, than execute the below command:

    `react-native bundle --platform android --dev false --entry-file index.js --bundle-output android/app/src/main/assets/index.android.bundle --assets-dest android/app/src/main/res/`

Finally after running the command:

`react-native run-android`

## Integrating old Android App:

    Copy the contents of android sdk into react native code base.

    Run gradlew :app:installDebug

    Once done successfully

    Run the command: 
       `react-native run-android –appFolder “name of the app folder”`
       
## Black screen error:

    error: bundling failed: Error: Unable to resolve module `./../../react-transform-hmr/lib/index.js


    Open cmd for the project path and execute `react-native start --reset-cache`, and then in another terminal window for the project path execute `react-native run-android` 


