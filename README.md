# touch_indicator

When you are recording a screencast of your app, you often want to give visual indication of where your fingers are touching the screen. Showing that on Android is easy. On iOS it's less intuitive. `touch_indicator` makes it easier and consistent on both platforms.

You add this widget as the main widget where you want to display user touches. Usually this will be the direct child of your `MaterialApp`. It will show an indicator on every touching finger and is completely customizable.

![](https://raw.githubusercontent.com/mardaneus86/touch_indicator/master/screenshots/touch_indicator_example.gif)

## Installation
Add the plugin to your pubspec.yaml:

```yml
dependencies:
  touch_indicator: ^1.0.2
```

## Usage
Import the package in your Dart code:

```dart
import 'package:touch_indicator/touch_indicator.dart';
```

Wrap your app in the `TouchIndicator` widget:

```dart
class MyApp extends StatelessWidget {
  MaterialApp(
    title: 'Touch indicator example',
    home: TouchIndicator(
      child: MyHomePage(title: 'Flutter Demo Home Page'),
    ),
  );
}
```

## Customization options
### indicatorColor
Changes the color of the backdrop and icon. Default is `Colors.blueGrey`.

### indicatorSize
Changes the size of the indicator. Default is `40.0`.

### indicator
By adding a `Widget` here, you can change the complete look of the touch indicators. Make sure to supply a proper `indicatorSize` in order for the indicators to be positioned at the center of your touchpoints.

### forceInReleaseMode
When you want to show indicators when the app is running in release mode, make sure to enable this option. Default is `false`.

### enabled
You can enable or disable display of the indicators on the fly with this option. Default is `true`.