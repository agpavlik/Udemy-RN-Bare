Create project with Bare Workflow:

```
npx create-expo-app <app-name> --template bare-minimum
```

> Experience of Launching an Android App:

1. Lounch Android-studio and create a device.

2. Tried `npm run android` but encountered an error: <i> ERROR: JAVA_HOME is not set and no 'java' command could be found in your PATH.</i>

Solution - install the Java Runtime Environment: <b>sudo apt-get install default-jre</b>

3. Tried `npm run android` but encountered an error: <i>Android Gradle plugin requires Java 17 to run. You are currently using Java 11</i>

Solution: <b>sudo apt-get install openjdk-17-jdk</b>

Check version: <b>java --version</b>

4. Tried `npm run android` but encountered an error: <i>SDK location not found. Define a valid SDK location with an ANDROID_HOME environment variable or by setting the sdk.dir path in your project's local properties file...</i>

Solution: Go to your react-native project then go to the `Android` directory. Create a file with the following name: `local.properties`. Open the file and paste your Android SDK path like below:

<b>sdk.dir = /home/USERNAME/Android/Sdk</b>

Please note that `Sdk` may appear as `sdk`, and the address may not include `USERNAME`, depending on your settings.

5. Tried `npm run android` but encountered an error: <i>Error: adb: failed to install /home/.../android/app/build/outputs/apk/debug/app-debug.apk: cmd: Can't find service: package</i>

Solution - install the Android Debug Bridge: <b>sudo apt install adb</b>
