# gradle-android-sdk-manager

Helper to manage android sdk for gradle.

## Installation

```groovy
apply from: 'https://raw2.github.com/cookpad/gradle-android-sdk-manager/master/sdk_manager.gradle'
```

## Usage

### Read value from local.properties

```groovy
readLocalPropertiesValue("sdk.dir") // => /usr/local/opt/android-sdk
readLocalPropertiesValue("ndk.dir") // => /usr/local/opt/android-ndk
```

### Read sdk or ndk dir

```groovy
readSdkDir()
readNdkDir()
```

Priority order of reading is as below

* local.properties
* System.getenv("ANDROID_HOME")
* System.getenv("ANDROID_SDK")
* "/usr/local/opt/android-sdk" // brew --prefix android-sdk
* "/Applications/Android Studio.app/sdk"

### Install required platform and build tool if necessary

```groovy
android {
    compileSdkVersion 18
    buildToolsVersion '19.0.1'

    // use "sdk.dir" value from local.properties
    installRequiredSdk(android)
    // or you can pass the sdk dir expressly
    installRequiredSdk(android, "/Applications/Android Studio.app/sdk")

    ...
```


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request

