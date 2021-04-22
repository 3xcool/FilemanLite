# FilemanLite

[![Maven Central](https://maven-badges.herokuapp.com/maven-central/com.3xcool/filemanlite/badge.svg)](https://maven-badges.herokuapp.com/maven-central/com.3xcool/filemanlite)

Very Lightweight Library for File Management based on Fileman Library.

# Dependency

In build.graddle (Project)
```kotlin
  allprojects {
    repositories {
        google()
        mavenCentral
    }
  }
```

    
In build.graddle (app)
```kotlin
dependencies {
implementation 'com.3xcool:filemanlite:$LATEST_VERSION'
}
```

# Drivers

Use FilemanDrivers enum class:
1) **SandBox:** Where the app is installed (can't be accessed by other apps)
2) **Internal:** Device storage (can be accessed by other apps)
3) **External:** SD Card if available

# Simple CRUD

Don't call these functions on the Main Thread to avoid UI freeze.

```kotlin
Fileman.write(fileContent: String, context: Context, drive: Int, folder: String, filename: String, append: Boolean)
```

```kotlin
Fileman.read(context: Context, drive: Int, folder: String, filename: String)
```

```kotlin
Fileman.delete(context: Context, drive: Int, folder: String, filename: String)
```

# License

Copyright 2020 André Filgueiras

Licensed under the Apache License, Version 2.0 (the "License");
you may not use this file except in compliance with the License.
You may obtain a copy of the License at

   http://www.apache.org/licenses/LICENSE-2.0

Unless required by applicable law or agreed to in writing, software
distributed under the License is distributed on an "AS IS" BASIS,
WITHOUT WARRANTIES OR CONDITIONS OF ANY KIND, either express or implied.
See the License for the specific language governing permissions and
limitations under the License.
