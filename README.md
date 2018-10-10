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

   output:
  
  
  
  
  
  
  
