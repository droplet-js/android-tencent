# android-tencent

[![Build Status](https://cloud.drone.io/api/badges/v7lin/android-tencent/status.svg)](https://cloud.drone.io/v7lin/android-tencent)
[![GitHub tag](https://img.shields.io/github/tag/v7lin/android-tencent.svg)](https://github.com/v7lin/android-tencent/releases)
[![API](https://img.shields.io/badge/API-14%2B-brightgreen.svg?style=flat)](https://android-arsenal.com/api?level=14)

### snapshot

````
ext {
    latestVersion = '3.3.3-SNAPSHOT'
}

allprojects {
    repositories {
        ...
        maven {
            url 'https://oss.jfrog.org/artifactory/oss-snapshot-local'
        }
        ...
    }
}
````

### release

````
ext {
    latestVersion = '3.3.3'
}

allprojects {
    repositories {
        ...
        jcenter()
        ...
    }
}
````

### usage

android
````
...
android {
    ...
    defaultConfig{
        ...
        manifestPlaceholders = [TENCENT_APP_ID: "${appId}"]
        ...
    }
    ...
}
...
dependencies {
    ...
    implementation "io.github.v7lin:tencent-android:${latestVersion}"
    ...
}
...
````
