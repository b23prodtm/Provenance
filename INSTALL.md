Build Provenance with the help of @fastlane/fastlane
=============
# Requirements
* Xcode installed on a Mac
* fastlane : ```brew cask install fastlane```
* bundle : ```gem install bundle```
* carthage : ```brew install carthage```
    * Spotlight and Topshelf requirements
        * Developer and Distribution certificates
        * Empty Git Private repository to store team certificates
        * [Fastlane Match](https://docs.fastlane.tools/actions/match/) that can generate all provisioning signatures from a Mac
* An iOS/tvOS device with USB/USB-C cable
*  [the _wiki_ installing guide](https://github.com/Provenance-Emu/Provenance/wiki/Installing-Provenance) : There are useful information there.
# Build latest source code
To get a working local build, run the shell commands below :
## Build from workspace folder
Perform a build test with the cmd : ```bundle exec fastlane ios test```
> [see available fastlane actions](fastlane/README.md) ```fastlane ios actions```
## Build with code signing enabled (paid developer account):
1. Copy&paste the public ssh key to Github’s repository deployment keys with write access to allow fast lane’s match to manage certificates repository. ```cat ~/.ssh/id_rsa.pub ```
2. Initialize the git repository :```bundle exec fastlane match init ios```
3. Perform a build test with the cmd :```bundle exec fastlane ios test```
### To generate SSH keys in Mac OS X, follow these steps:
1. Enter the following command in the Terminal window: ```ssh-keygen -t rsa -b 4096```. ...
2. Press the ENTER key to accept the default location.
3. The ssh-keygen utility prompts you for a passphrase.
4. Enter a passphrase.
5. Edit ```.fastlane/Appfile``` and ```fastlane/Keys``` according to your coordinates.
6. Then try to create the signing provisioning profiles with the following command:  ```bundle exec fastlane ios create_certificates```
7. There are a few steps to complete…
8. (optional) Setup a cipher password (aka _MATCH_PASSWORD_) as a secret variable
### Use SSH URLs everywhere
> Most services support SSH key based authentication only for SSH URLs (ex: git@github.com:bitrise-io/bitrise.git), and not for HTTPS URLs (ex: https://github.com/
bitrise-io/bitrise.git)! This means, that every private repository you want to use have to be addressed with the SSH url. If you have direct private git repo references in your Podfile you'll have to use the SSH url there as well! Same applies for submodules and every other private git repository url you want to use with the SSH key you register on Bitrise.io!
> Launch IOS beta TestFlight build process with : ```bundle exec fastlane ios beta```
>> A bundle unique identifier (with XC bundle id) must be already registered
>Working from any continuous integration system, the above lines must result in a successful build.
## Publish to application services
In case fastlane failed to validate provisioning profiles stored in *git repository*, you must regenerate new one from *fastlane match*
* Generate new .mobileprovision and upload to git ```bundle exec fastlane match nuke distribution
bundle exec fastlane match appstore```
# Sideloading archives to iOS/tvOS devices
1. Use Xcode _Devices and Simulators_ in the *Window* menu.
2. Your device must be connected to the Mac with USB/USB-C.
3. Hit the `+`button right below the device information panel.
4. Sideload latest produced applications.
