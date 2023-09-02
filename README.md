<h1>How to instalation React Native On Mac iOS & Android</h1>

<h2>Instalation React Native iOS On Mac</h2>

- open terminal command this line :
- Install brew copy from this website https://brew.sh/index_id
- brew --version

- brew install node
- node --version
- npm --version

- brew install watchman

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
- run ios project by command "npx react-native run-ios"



<h2>Instalation React Native Android On Mac</h2>

- Instal brew https://brew.sh/index_id
- brew —-version
- brew install git
- git —version
- brew install node
- node —version
- npm —version
- brew install watchman
- brew install --cask adoptopenjdk/openjdk/adoptopenjdk11
- now open Safari or your other website download Android Studio dmg version Mac(64-bit, ARM), then install,
- open terminal, if you are using zsh then command ~/.zprofile or ~/.zshrc, command like “ open ~/.zprofile “.
- now add config in this file, not replace :
	export ANDROID_HOME=$HOME/Library/Android/sdk
	export PATH=$PATH:$ANDROID_HOME/emulator
	export PATH=$PATH:$ANDROID_HOME/tools
	export PATH=$PATH:$ANDROID_HOME/tools/bin
	export PATH=$PATH:$ANDROID_HOME/platform-tools
- save and close this file
- now open Android Studio => clik More Options => click AVD Manager => Creative Virtual Device => Phone => Choose Emulator => Next => Download Android version (my advice is to download 2 or 3 versions below from latest, then
- click finish => select android downloaded version => click next => then running emulator
- now you can testing create new project using commad npx react-native init newProject
- open your newProject in VSCODE
- running command npm start then 
- add new terminal, and command npx react-native run-android 
       note : if you getting error like :
       (Unable to make field private final java.lang.String java.io.File.path accessible: module java.base does not "opens java.io" to unnamed module @62081f85) follow this step : 
       - check compatible yout java(jdk) and gradlew in https://docs.gradle.org/current/userguide/compatibility.html 
       - if your jdk version 17, use this line to change  distributionUrl = https\://services.gradle.org/distributions/gradle-7.3-all.zip (location : \android\gradle\wrapper)


- dont’ forget to SMILE :D
