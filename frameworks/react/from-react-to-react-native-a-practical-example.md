# From React to React Native, a practical example

## Speaker: [Vasile Boris](https://www.linkedin.com/in/vasileboris/)
## Date: 28.05.2019
## Venue: Garmin
## Description
Vasile Boris will present his experience on migrating an existing web application implemented in React to an Android application implemented in React Native and Expo.

About Boris
I’m a senior programmer with the focus on JavaScript and Java. I recently moved from programming only duties to leading a group of highly skilled people. I like trying new things and sharing that experience on my personal blog
## Slides

### What to expect

* Why this meetup?
* The original project, the idea
* The choices and preparation
* The solution implemented with [React Native][react-native] and [Expo][expo-io]
* What is next?
* Questions?

### Why this meetup?
* My experience was not straightforward
* I had few challenges and **frustrations** 
* I wanted to share how I resolved them

### The original project, the idea

[library-web][library-web], [library-resources][library-resources] and [library-api][library-api].
* I started to work with JavaScript in 2017 so I needed a way to learn
* React, Redux + Saga, Spring Boot.
* Deploying live such a stack seemed too much for one person.
* A mobile solution looked simpler and the natural choice was React Native. 

### The choices and preparation

I followed [Getting Started][react-native-getting-started]:
* Expo CLI Quickstart - Advertised as "If you are coming from a web background"
* React Native CLI Quickstart - Advertised as "If you are familiar with native development"

Initially I wanted to reuse some [java code][library-api] so I went with ...

#### React Native CLI Quickstart

* Installed Android Studio
* Installed the Android SDK (Installed with Android Studio)
* Configured the ANDROID_HOME environment variable
```
export ANDROID_HOME=$HOME/Android/Sdk
export PATH=$ANDROID_HOME/platform-tools:$PATH
export PATH=$ANDROID_HOME/emulator:$PATH
export PATH=$ANDROID_HOME/tools/bin:$PATH
export PATH=$ANDROID_HOME/tools:$PATH
```
* Installed Watchman in case you want to continue with this path
* Example: [AwesomeProject React Native CLI][awesomeproject-rn-cli]
* Conclusion:
  * Setup looks complex for a beginner: React Native, Android, Gradle, React Native + Android
  * I see it appropriate for the ones who know more about React Native and Android.

#### Expo CLI Quickstart

* I chose "blank - minimal dependencies to run and an empty root component":
  * Example: [MyReads 00-app-structure tag][myreads-00-app-structure]
* Conclusion:
  * It looks good for JavaScript only development

#### Common for both

* You should
  * know how to start an emulator / connect real device. I recommend to start an emulator from command line like
  ```
  emulator -list-avds
  emulator -avd Pixel_2_XL_API_26
  ```
  * know how to deploy the app on emulator / real device
  * know how to debug the code
* Watch out for:
  * You have enough hardware resources. I notice that 8Gb are not enough (frozen system), 16Gb much better.
  * Possible alternative: [Android_x86 with VirtualBox][virtual-box-android-x86]. I did not manage to install it.
  * [Android SDK command line issue][android-sdk-emulator-command-line-issue] 
  ```
  export ANDROID_HOME=$HOME/Android/Sdk
  export PATH=$ANDROID_HOME/platform-tools:$PATH
  export PATH=$ANDROID_HOME/emulator:$PATH
  #export PATH=$ANDROID_HOME/tools/bin:$PATH
  #export PATH=$ANDROID_HOME/tools:$PATH
  ```

### The solution implemented with [React Native][react-native] and [Expo][expo-io]

#### What I wanted:

* Keep as much as possible from [library-web][library-web]

#### What I did:

* New project: [MyReads][myreads]
* Configure [i18next][i18next]
* Migrate presentational components
* Migrate redux code
* Migrate container components
* Remove API calls and use local storage

#### Configure [i18next][i18next]

[MyReads 01-configure-i18next tag][myreads-01-configure-i18next]

#### Migrate presentational components

[MyReads 02-migrate-first-component tag][myreads-02-migrate-first-component]
* I noticed an issue with android status bar

[MyReads 03-configure-app-top-margin tag][myreads-03-configure-app-top-margin]
* I fixed the issue with android status bar
* I used [babel-root-slash-import][babel-root-slash-import] to have absolute import. 
  I replace it later with [babel-plugin-module-resolver][babel-plugin-module-resolver].

[MyReads 04-flexbox-issue tag][myreads-04-flexbox-issue]
* Discuss about flex: 1 style config. In my tests I notice that it must be in the root element.

#### Migrate Redux code

[MyReads 05-redux-integration-issue tag][myreads-05-redux-integration-issue] 
* connect returns Object and not Function
* It was my mistake, I updated package.json with latest versions of everything
  
[MyReads 06-redux-integration tag][myreads-06-redux-integration] 
* I updated the versions
```
"react": "16.5.0",
"react-native": "https://github.com/expo/react-native/archive/sdk-32.0.2.tar.gz",
"react-redux": "^6.0.1",
"redux": "^4.0.1",
```
* I did not realised that react 16.5.0 is needed and I changed it
* I noticed that react-redux ^6.0.1 is the max version that works with redux ^4.0.1

#### Migrate container components

[MyReads 07-migrate-container-components tag][myreads-07-migrate-container-components]

#### Remove API calls and use local storage

[MyReads 08-use-local-storage tag][myreads-08-use-local-storage]
* I used [React Native AsyncStorage][react-native-asyncstorage]. 
* It is deprecated and the suggestion is to use [React Native Community AsyncStorage][react-native-async-storage], 
  but it [doesn't work][react-native-async-storage-expo] with [expo][expo-io].

### What is next?

* Understand how to release it
* Work without expo

### Questions?

[react-native]: https://facebook.github.io/react-native/
[react-native-getting-started]: https://facebook.github.io/react-native/docs/getting-started
[android-sdk-emulator-command-line-issue]: https://github.com/decosoftware/deco-ide/issues/289
[awesomeproject-expo-cli]: https://github.com/vasileboris/espressoprogrammer-blog-code/tree/master/from-react-to-react-native-a-practical-example/AwesomeProject-Expo-CLI
[awesomeproject-rn-cli]: https://github.com/vasileboris/espressoprogrammer-blog-code/tree/master/from-react-to-react-native-a-practical-example/AwesomeProject-RN-CLI
[library-web]: https://github.com/vasileboris/library-web
[library-resources]: https://github.com/vasileboris/library-resources
[library-api]: https://github.com/vasileboris/library-api
[myreads]: https://github.com/vasileboris/MyReads
[virtual-box-android-x86]: https://doc.nuxeo.com/blog/speeding-up-the-android-emulator/
[i18next]: https://www.i18next.com/
[myreads-00-app-structure]: https://github.com/vasileboris/MyReads/releases/tag/00-app-structure
[myreads-01-configure-i18next]: https://github.com/vasileboris/MyReads/releases/tag/01-configure-i18next
[myreads-02-migrate-first-component]: https://github.com/vasileboris/MyReads/releases/tag/02-migrate-first-component
[myreads-03-configure-app-top-margin]: https://github.com/vasileboris/MyReads/releases/tag/03-configure-app-top-margin
[babel-root-slash-import]: https://github.com/mantrajs/babel-root-slash-import
[babel-plugin-module-resolver]: https://github.com/tleunen/babel-plugin-module-resolver
[myreads-04-flexbox-issue]: https://github.com/vasileboris/MyReads/releases/tag/04-flexbox-issue
[myreads-05-redux-integration-issue]: https://github.com/vasileboris/MyReads/releases/tag/05-redux-integration-issue
[myreads-06-redux-integration]: https://github.com/vasileboris/MyReads/releases/tag/06-redux-integration
[myreads-07-migrate-container-components]: https://github.com/vasileboris/MyReads/releases/tag/07-migrate-container-components
[myreads-08-use-local-storage]: https://github.com/vasileboris/MyReads/releases/tag/08-use-local-storage
[react-native-asyncstorage]: https://facebook.github.io/react-native/docs/asyncstorage
[react-native-async-storage]: https://github.com/react-native-community/react-native-async-storage
[react-native-async-storage-expo]: https://github.com/react-native-community/react-native-async-storage/issues/72
[expo-io]: https://expo.io/

