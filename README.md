Broken with v1.15.2:

```
> yarn --version
1.15.2
> cd yarn-workspaces-bug/
> yarn
> cd workspace-1/

> yarn react-native
yarn run v1.15.2
error Command "react-native" not found.
info Visit https://yarnpkg.com/en/docs/cli/run for documentation about this command.

> ls -l ./node_modules/.bin/react-native
lrwxr-xr-x  1 thallada  staff  43 Mar 18 11:32 ./node_modules/.bin/react-native@  -> ../@react-native-community/cli/build/bin.js

> ./node_modules/.bin/react-native
Usage: react-native [options] [command]

Options:
  --version                          Print CLI version
  --projectRoot [string]             Path to the root of the project
  --reactNativePath [string]         Path to React Native
  -h, --help                         output usage information

Commands:
  start [options]                    starts the webserver
  run-ios [options]                  builds your app and starts it on iOS simulator
  run-android [options]              builds your app and starts it on a connected Android emulator or device
  new-library [options]              generates a native library bridge
  bundle [options]                   builds the javascript bundle for offline use
  ram-bundle [options]               builds javascript as a "Random Access Module" bundle for offline use
  eject [options]                    Re-create the iOS and Android folders and native code
  link [options] [packageName]       scope link command to certain platforms (comma-separated)
  unlink [options] <packageName>     unlink native dependency
  install [options] <packageName>    install and link native dependencies
  uninstall [options] <packageName>  uninstall and unlink native dependencies
  upgrade [options] [version]        Upgrade your app's template files to the specified or latest npm version using `rn-diff-purge` project. Only valid semver versions are allowed.
  log-android [options]              starts adb logcat
  log-ios [options]                  starts iOS device syslog tail
  dependencies [options]             lists dependencies
  info [options]                     Get relevant version info about OS, toolchain and libraries
  init [options]
```

Works with v1.14.0:

```
> yarn --version
1.14.0
> cd yarn-workspaces-bug/
> yarn
> cd workspace-1/

> yarn react-native
yarn run v1.14.0
$ /Users/thallada/yarn-executable-bug/workspace-1/node_modules/.bin/react-native
Usage: react-native [options] [command]

Options:
  --version                          Print CLI version
  --projectRoot [string]             Path to the root of the project
  --reactNativePath [string]         Path to React Native
  -h, --help                         output usage information

Commands:
  start [options]                    starts the webserver
  run-ios [options]                  builds your app and starts it on iOS simulator
  run-android [options]              builds your app and starts it on a connected Android emulator or device
  new-library [options]              generates a native library bridge
  bundle [options]                   builds the javascript bundle for offline use
  ram-bundle [options]               builds javascript as a "Random Access Module" bundle for offline use
  eject [options]                    Re-create the iOS and Android folders and native code
  link [options] [packageName]       scope link command to certain platforms (comma-separated)
  unlink [options] <packageName>     unlink native dependency
  install [options] <packageName>    install and link native dependencies
  uninstall [options] <packageName>  uninstall and unlink native dependencies
  upgrade [options] [version]        Upgrade your app's template files to the specified or latest npm version using `rn-diff-purge` project. Only valid semver versions are allowed.
  log-android [options]              starts adb logcat
  log-ios [options]                  starts iOS device syslog tail
  dependencies [options]             lists dependencies
  info [options]                     Get relevant version info about OS, toolchain and libraries
  init [options]
✨  Done in 0.23s.
```
