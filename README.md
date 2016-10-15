**This library is no longer maintained. Use https://github.com/JakeWharton/sdk-manager-plugin instead.**

# gradle-android-sdk-manager

This plugin manages Android SDK and build tools for gradle.

## Installation

```groovy
apply from: 'https://raw.githubusercontent.com/cookpad/gradle-android-sdk-manager/master/sdk_manager.gradle'
```

## Usage

### Read SDK path from local.properties

```groovy
readLocalPropertiesValue("sdk.dir") // => /usr/local/opt/android-sdk
readLocalPropertiesValue("ndk.dir") // => /usr/local/opt/android-ndk
```

### Find SDK or NDK dir

```groovy
guessSdkDir()
guessNdkDir()
```

Find the following paths for a SDK directory in the following order:

* local.properties
* System.getenv("ANDROID_HOME")
* System.getenv("ANDROID_SDK")
* "/usr/local/opt/android-sdk" // brew --prefix android-sdk
* "/Applications/Android Studio.app/sdk"

### Install required SDK and build tools if necessary

`android(1)` has a headless mode to install android development tools from terminals.
`installRequiredSdk()` installs build tools with specified versions declared in `build.gradle`.

```groovy
android {
    compileSdkVersion 18
    buildToolsVersion '19.0.1'

    // installs Android SDK 18 and build tools 19.0.1
    // with "sdk.dir" value from local.properties
    installRequiredSdk(android)
    // or you can pass the sdk dir explicitly
    installRequiredSdk(android, "/Applications/Android Studio.app/sdk")

    ...
```

## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

