● web:
flutter channel master | dev
flutter config --enable-web
flutter create .
flutter run -d chrome

● desktop:
flutter channel master
flutter config --enable-macos-desktop
flutter config --enable-windows-desktop
flutter config --enable-linux-desktop

flutter create --macos .
flutter create --windows .
flutter create --linux .

import 'package:flutter/foundation.dart'
void main() {
  debugDefaultTargetPlatformOverride = TargetPlatform.fuchsia;
  [...]
}

flutter run -d <device-name>