# SdkManager

Helper to manage android sdk for gradle.

## Installation

```
apply from: 'https://raw2.github.com/rejasupotaro/sdk_manager/master/sdk_manager.gradle'
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

## License

```
 Copyright 2014 rejasupotaro

 Licensed under the Apache License, Version 2.0 (the "License");
 you may not use this file except in compliance with the License.
 You may obtain a copy of the License at

 http://www.apache.org/licenses/LICENSE-2.0

 Unless required by applicable law or agreed to in writing, software
 distributed under the License is distributed on an "AS IS" BASIS,
 WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
 See the License for the specific language governing permissions and
 limitations under the License.
```
