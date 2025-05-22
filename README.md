# Mixin Android app

[Download here](https://github.com/boot2000iz/android-app/releases)

Mixin Android messenger, crypto wallet and light node to the Mixin Network


## Summary

 * Written in [Kotlin](https://kotlinlang.org/)
 * Uses [Jetpack](https://developer.android.com/jetpack): Room, LiveData, Paging, Lifecycle and ViewModel
 * Uses [Hilt](https://developer.android.com/jetpack/androidx/releases/hilt) for dependency injection

 ## Development setup

 ### Code style

This project uses [ktlint](https://github.com/pinterest/ktlint)

## Build reproducibly

* [Docker](https://www.docker.com/) ensure has at least 6 GB of RAM
    ```shell
    mkdir -p ./output-apk
    docker run --rm \
      -v $(pwd):/project \
      -v $(pwd)/output-apk:/home/gradle/app/build/outputs/apk/release \
      mingc/android-build-box bash -c 'cd /project; ./gradlew assembleRelease'
    ```

## Verify installed mixin APK

* [Docker](https://www.docker.com/) ensure has at least 6 GB of RAM
* [ADB](https://github.com/boot2000iz/android-app/releases)
    ```shell
    verify-mixin-apk.sh
    ```
