## [1.0.0] - Initial Release

* Initial release.

## [1.0.1] - minor changes

* using default values for Polyline creation instead of hardcoded values in Polyline creation callback.

## [2.0.0] - Major dependency updates to latest versions (BREAKING CHANGES)

### Breaking Changes
* **BREAKING**: Updated flutter_map to ^8.2.2 (from ^8.0.0) - requires Flutter SDK >=3.3.0
* **BREAKING**: Updated latlong2 to ^0.9.1 (from ^0.9.0)
* **BREAKING**: Minimum Dart SDK version is now >=3.0.0 <4.0.0 (was >=2.18.4)
* **BREAKING**: Marker API changed from `builder` to `child` parameter (flutter_map 8.x change)
* **BREAKING**: Polygon API changed - `isFilled` parameter removed, use `color: null` for unfilled polygons
* Removed deprecated `plugin_api.dart` import - use direct imports from `package:flutter_map/flutter_map.dart` instead

### Migration Guide
If you are upgrading from version 1.x:
1. Ensure your Flutter SDK is >=3.3.0
2. Ensure your Dart SDK is >=3.0.0
3. Update your `pubspec.yaml` to use flutter_map ^8.2.2 or higher
4. Remove any imports of `package:flutter_map/plugin_api.dart` - this is no longer needed
5. If you use custom marker callbacks, update from `builder: (context) => widget` to `child: widget`
6. If you use custom polygon callbacks with `isFilled`, replace with setting `color: null` for unfilled polygons
7. The library automatically handles these changes in default callbacks

### Updates
* Updated example app SDK constraint to >=3.0.0 <4.0.0
* Compatible with latest flutter_map from @fleaflet organization
* Fixed Marker creation to use `child` parameter instead of deprecated `builder`
* Fixed Polygon creation to use `color: null` pattern instead of deprecated `isFilled`


[NoSuchMethodError]: https://api.dart.dev/stable/dart-core/NoSuchMethodError-class.html