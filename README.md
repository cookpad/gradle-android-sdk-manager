# gradle-android-sdk-manager

Helper to manage android sdk for gradle.

## Installation

```
apply from: 'https://raw2.github.com/cookpad/gradle-android-sdk-manager/master/sdk_manager.gradle'
```

## Usage

- Read sdk or ndk dir

```
readSdkDir()
readNdkDir()
```

- Install required platform and build tool if necessary

```
android {
    compileSdkVersion 18
    buildToolsVersion '19.0.1'

    installRequiredSdk(android)

    ...
```


## Contributing

1. Fork it
2. Create your feature branch (`git checkout -b my-new-feature`)
3. Commit your changes (`git commit -am 'Add some feature'`)
4. Push to the branch (`git push origin my-new-feature`)
5. Create new Pull Request
