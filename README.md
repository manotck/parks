# Park

Park App is a new mobile app which is capable of spotting animals in Sri Lankan national parks and work as guiding app.

### Contributing to Park-Mobile APP

:+1::tada: First off, thanks for taking the time to contribute! :tada::+1:

1. Fork the [https://github.com/scorelab/park.git].

2. Generate a debug.keystore using `keytool -genkey -v -keystore debug.keystore -storepass android -alias androiddebugkey -keypass android -keyalg RSA -keysize 2048 -validity 10000`. (Keystore name: “debug.keystore”, Keystore password: “android”, Key alias: “androiddebugkey”, Key password: “android”, CN: “CN=Android Debug,O=Android,C=US”). (read guide: [https://rnavagamuwa.com/programming/android-programming/android-generate-release-debug-keystores/])

3. Place the copy of debug.keystore in MobileApp/android/app/.

4. Generate the key fingerprints using `keytool -list -v -keystore debug.keystore -alias androiddebugkey -storepass android -keypass android`.

5. Create a firebase project, add an android app to project settings, add sha1 to the project, download the google-services.json file and place in the MobileApp/android/app/. (read guide: [https://invertase.io/oss/react-native-firebase/quick-start/android-firebase-credentials]).

6. Add a config.js file in the MobileApp/src/config/config.js. Content of the file should looks like sampleConfig.js. Extract those client ids from **google-services.json**. If you are testing with the debug.keystore you only need to add the client id related to debug sha1 in devAndroidClientID. And use it in MobileApp/src/components/GoogleLogin/GoogleLogin.js file's 3rd and 12th line.

7. Create a gradle.properties file in **MobileApp/android/** and paste the content in the MobileApp/android/app/samplegradle.properties.

8. Run `npx install`, `react-native run-android`, `react-native start`

### Pull Request Process

1. Ensure any install or build dependencies are removed.
2. Submit changes as a pull request.

### Environment Info
#### System:
    OS: Linux 5.0 Ubuntu 19.04 (Disco Dingo)
    CPU: (4) x64 Intel(R) Core(TM) i5-7200U CPU @ 2.50GHz
    Memory: 309.14 MB / 7.55 GB
    Shell: 5.0.3 - /bin/bash
#### Binaries:
    Node: 10.15.2 - /usr/bin/node
    npm: 6.12.0 - /usr/local/bin/npm
#### npmPackages:
    react: 16.9.0 => 16.9.0 
    react-native: 0.61.2 => 0.61.2 
#### npmGlobalPackages:
    create-react-native-app: 2.0.2
    react-native-cli: 2.0.1

#### NOTE: Do not change the .gitignore file.
