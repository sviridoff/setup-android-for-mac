# Setup `Android` for mac

## Install `brew`.

```sh
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
```

## Install `Java`.

```sh
brew tap caskroom/versions
brew cask install java8
```

## Install `Android` and dependencies.

```sh
brew install ant
brew install maven
brew install gradle
brew install cask android-sdk
brew install cask android-ndk
```

## Add environment variables to `.bashrc` or `.zshrc`.

```sh
export ANT_HOME=/usr/local/opt/ant
export MAVEN_HOME=/usr/local/opt/maven
export GRADLE_HOME=/usr/local/opt/gradle
export ANDROID_NDK_HOME="/usr/local/share/android-ndk"
export ANDROID_SDK_ROOT="/usr/local/share/android-sdk"
```

## Install `Android SDK components`.

```sh
sdkmanager "platform-tools" "platforms;android-23"
sdkmanager "build-tools;23.0.1"
```

## Update

```sh
brew update
brew cask update
sdkmanager --update
```


