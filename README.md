<h1>How to instalation React Native On Mac iOS & Android</h1>

open terminal and follow this following comman
- Install brew copy from this website https://brew.sh/index_id
- brew --version

- brew install node
- node --version
- npm --version
- brew install watchman

  
<h2>Instalation React Native iOS On Mac</h2>

- now open Appstore download XCODE, then install,
- while the installation is in progress, they ask to install ROSETTA or not now, this step is optional, I clicked not now, because there is no need for now.
- open XCODE
- click the xcode text in the top left corner => clik Preferences => then
- click Tab Locations => click Command Line Tools, and select XCODE version,
- click Tab Components => download simulator =>
If the latest iOS version is 16.XX, my advice is to download 2 or 3 versions below, namely iOS version 13.XX or 14.XX, because it’s more stable version, exactly, it's up to you

- open terminal command => gem install -n /usr/local/bin ffi cocoapods, if you get error no have permission, you run this command "sudo gem install -n /usr/local/bin ffi cocoapods" // it will take a few minutes
if you got an error about activesupport version, you should type this command first "sudo gem install activesupport -v 6.1.7.6", pay attention to the version requested when you get an error "activesupport", maybe the version requested is different from this, after run install activesupport, you can try this command again"gem install -n /usr/local/bin ffi cocoapods, if you get error no have permission, you run this command "sudo gem install -n /usr/local/bin ffi cocoapods" 
- pod --version

- now you can testing create new project using commad "npx react-native init newProject"
- cd newProject
- cd ios
- run "pod install"
- cd ..
- run ios project by command "npx react-native run-ios" or simply by "npm start" then press "i" to run iOS emulator



<h2>Instalation React Native Android On Mac</h2>

- brew tap homebrew/cask-versions
- brew install --cask zulu11
- brew info --cask zulu11
- now open Safari or your other website download Android Studio dmg version Mac(64-bit, ARM), then install,

- open terminal, if you are using zsh then command ~/.zprofile or ~/.zshrc, command like “open ~/.zprofile“.
- now add this config:
	export ANDROID_HOME=$HOME/Library/Android/sdk
	export PATH=$PATH:$ANDROID_HOME/emulator
	export PATH=$PATH:$ANDROID_HOME/platform-tools

- save and close the file
- now open Android Studio => clik More Actions => click SDK Manager => click Languages & Framework => click Android => click SDK Platforms => select android version what's your need => click Apply and download

- now you can testing create new project using command "npx react-native init newProject"
- cd newProject
- cd android
- run "./gradlew clean"
- cd ..
- run "npx react-native run-android" or simply run "npm start" then press "a" to run android emulator
- add new terminal, and command npx react-native run-android 
if you got an error about "sdk location not found" read this "https://stackoverflow.com/questions/27620262/sdk-location-not-found-define-location-with-sdk-dir-in-the-local-properties-fil"
