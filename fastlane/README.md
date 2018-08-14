fastlane documentation
================
# Installation

Make sure you have the latest version of the Xcode command line tools installed:

```
xcode-select --install
```

Install _fastlane_ using
```
[sudo] gem install fastlane -NV
```
or alternatively using `brew cask install fastlane`

# Available Actions
### all_setup_fastlane
```
fastlane all_setup_fastlane
```
Setup fastlane enviroment
### all_test
```
fastlane all_test
```
Build and run tests
### all_travistest
```
fastlane all_travistest
```
Travis Test
### all_userbuild
```
fastlane all_userbuild
```
User Setup
### all_updatePlistForBranch
```
fastlane all_updatePlistForBranch
```
Updates the bundle id and app name if a beta build
### all_plist_reset
```
fastlane all_plist_reset
```
Resets the bundle id and app name after build
### all_beta
```
fastlane all_beta
```
Push a new beta build to TestFlight
### all_alpha
```
fastlane all_alpha
```
Push a new alpha build to Hockeyapp
### all_add_badge
```
fastlane all_add_badge
```
Add proper badge to icon
### all_certificates
```
fastlane all_certificates
```
Setup Certs for Match - New Devs - Readonly
### all_create_certificates
```
fastlane all_create_certificates
```
Create Certs for Match
### all_update_devices
```
fastlane all_update_devices
```
Update device list
### all_derived_data
```
fastlane all_derived_data
```
Clear your DerivedData
### all_reset_checkout
```
fastlane all_reset_checkout
```
Reset build enviroment

Use this lane if you're having build issues

Use `git stash` first to save any changes you may want to keep.
### carthage_bootstrap
```
fastlane carthage_bootstrap
```
Lane to run bootstrap carthage in new checkout

Option: `platform` tvos,ios
### carthage_build
```
fastlane carthage_build
```
Lane to run build all carthage dependencies

Option: `platform` tvos,ios
### carthage_update
```
fastlane carthage_update
```
Lane to update all carthage dependencies to latest versions

Option: `platform` tvos,ios

----

## iOS
### ios test
```
fastlane ios test
```

### ios beta
```
fastlane ios beta
```

### ios alpha
```
fastlane ios alpha
```

### ios add_badge
```
fastlane ios add_badge
```

### ios userbuild
```
fastlane ios userbuild
```

### ios travistest
```
fastlane ios travistest
```

### ios plist_reset
```
fastlane ios plist_reset
```

### ios certificates
```
fastlane ios certificates
```

### ios derived_data
```
fastlane ios derived_data
```

### ios reset_checkout
```
fastlane ios reset_checkout
```

### ios setup_fastlane
```
fastlane ios setup_fastlane
```

### ios update_devices
```
fastlane ios update_devices
```

### ios create_certificates
```
fastlane ios create_certificates
```

### ios updatePlistForBranch
```
fastlane ios updatePlistForBranch
```


----

## tvos
### tvos test
```
fastlane tvos test
```

### tvos beta
```
fastlane tvos beta
```

### tvos alpha
```
fastlane tvos alpha
```

### tvos add_badge
```
fastlane tvos add_badge
```

### tvos userbuild
```
fastlane tvos userbuild
```

### tvos travistest
```
fastlane tvos travistest
```

### tvos plist_reset
```
fastlane tvos plist_reset
```

### tvos certificates
```
fastlane tvos certificates
```

### tvos derived_data
```
fastlane tvos derived_data
```

### tvos reset_checkout
```
fastlane tvos reset_checkout
```

### tvos setup_fastlane
```
fastlane tvos setup_fastlane
```

### tvos update_devices
```
fastlane tvos update_devices
```

### tvos create_certificates
```
fastlane tvos create_certificates
```

### tvos updatePlistForBranch
```
fastlane tvos updatePlistForBranch
```


----

This README.md is auto-generated and will be re-generated every time [fastlane](https://fastlane.tools) is run.
More information about fastlane can be found on [fastlane.tools](https://fastlane.tools).
The documentation of fastlane can be found on [docs.fastlane.tools](https://docs.fastlane.tools).
