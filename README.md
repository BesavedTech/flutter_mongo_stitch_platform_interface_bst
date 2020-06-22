# flutter_mongo_stitch_platform_interface

A common platform interface for the [`flutter_mongo_stitch`][1] plugin.

This interface allows platform-specific implementations of the `flutter_mongo_stitch`
plugin, as well as the plugin itself, to ensure they are supporting the
same interface.

# Usage

To implement a new platform-specific implementation of `flutter_mongo_stitch`, extend
[`FlutterMongoStitchPlatform`][2] with an implementation that performs the
platform-specific behavior, and when you register your plugin, set the default
`FlutterMongoStitchPlatform` by calling
`FlutterMongoStitchPlatform.instance = MyFlutterMongoStitchPlatformLauncher()`.

# Note on breaking changes

Strongly prefer non-breaking changes (such as adding a method to the interface)
over breaking changes for this package.

See https://flutter.dev/go/platform-interface-breaking-changes for a discussion
on why a less-clean interface is preferable to a breaking change.

[1]: https://github.com/kfiross/flutter_mongo_stitch
[2]: lib/flutter_mongo_stitch_platform_interface.dart
