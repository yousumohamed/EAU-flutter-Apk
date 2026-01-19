# EAU Galkacyo Portal - Android App Build Instructions

## 📱 Overview
This Flutter app converts the EAU Galkacyo student exam portal website into a native Android application with full WebView support.

## ✨ Features
- ✅ Full WebView integration with JavaScript support
- ✅ Session & cookie persistence (students stay logged in)
- ✅ Loading indicators for better UX
- ✅ Error handling with user-friendly messages
- ✅ Back button navigation support
- ✅ Pull-to-refresh functionality
- ✅ Native Android app experience
- ✅ Custom app bar with refresh button

## 📋 Prerequisites
- Flutter SDK installed (version 3.38.3 or compatible)
- Android Studio or VS Code with Flutter extensions
- Android SDK and build tools
- Java JDK 11 or higher

## 🚀 Step-by-Step Build Instructions

### Step 1: Install Dependencies
```bash
flutter pub get
```

### Step 2: Check Flutter Doctor
Ensure your Flutter environment is properly set up:
```bash
flutter doctor
```
Fix any issues reported before proceeding.

### Step 3: Connect Device or Start Emulator
**Option A: Physical Device**
- Enable Developer Options on your Android device
- Enable USB Debugging
- Connect via USB cable

**Option B: Emulator**
- Open Android Studio
- Start an Android Virtual Device (AVD)

Verify device is connected:
```bash
flutter devices
```

### Step 4: Test the App (Optional but Recommended)
Run the app in debug mode to test functionality:
```bash
flutter run
```

### Step 5: Build APK (Debug Version)
For testing purposes, build a debug APK:
```bash
flutter build apk --debug
```

### Step 6: Build APK (Release Version - Recommended)
For production/distribution, build a release APK:
```bash
flutter build apk --release
```

**The APK will be located at:**
```
build/app/outputs/flutter-apk/app-release.apk
```

### Step 7: Build App Bundle (For Google Play Store)
If you plan to publish on Google Play Store:
```bash
flutter build appbundle --release
```

**The bundle will be located at:**
```
build/app/outputs/bundle/release/app-release.aab
```

## 📦 APK Locations

| Build Type | Location |
|------------|----------|
| Debug APK | `build/app/outputs/flutter-apk/app-debug.apk` |
| Release APK | `build/app/outputs/flutter-apk/app-release.apk` |
| App Bundle | `build/app/outputs/bundle/release/app-release.aab` |

## 📲 Installing the APK

### On Physical Device:
1. Transfer the APK file to your Android device
2. Enable "Install from Unknown Sources" in Settings
3. Tap the APK file to install
4. Grant necessary permissions

### Using ADB (Android Debug Bridge):
```bash
adb install build/app/outputs/flutter-apk/app-release.apk
```

## 🔧 Customization Options

### Change App Name
Edit `android/app/src/main/AndroidManifest.xml`:
```xml
<application
    android:label="Your App Name"
    ...>
```

### Change App Icon
Replace the launcher icons in:
- `android/app/src/main/res/mipmap-hdpi/ic_launcher.png`
- `android/app/src/main/res/mipmap-mdpi/ic_launcher.png`
- `android/app/src/main/res/mipmap-xhdpi/ic_launcher.png`
- `android/app/src/main/res/mipmap-xxhdpi/ic_launcher.png`
- `android/app/src/main/res/mipmap-xxxhdpi/ic_launcher.png`

Or use the `flutter_launcher_icons` package for easier icon generation.

### Change Package Name
Edit `android/app/build.gradle`:
```gradle
defaultConfig {
    applicationId "com.yourcompany.eau_portal_app"
    ...
}
```

### Change App Theme Color
Edit `lib/main.dart` in the `ThemeData` section:
```dart
theme: ThemeData(
  primarySwatch: Colors.blue, // Change this color
  ...
),
```

## 🐛 Troubleshooting

### Issue: "Gradle build failed"
**Solution:** Update Gradle version in `android/gradle/wrapper/gradle-wrapper.properties`

### Issue: "SDK not found"
**Solution:** Run `flutter doctor` and follow instructions to install Android SDK

### Issue: "WebView not loading"
**Solution:** 
- Check internet connection
- Verify the URL is accessible
- Check Android permissions in `AndroidManifest.xml`

### Issue: "App crashes on startup"
**Solution:**
- Run `flutter clean` then `flutter pub get`
- Rebuild the app

### Issue: "Cookies/Session not persisting"
**Solution:** The WebViewController automatically handles cookies. Ensure you're using the latest version of `webview_flutter`.

## 📱 Permissions

The app requires the following permissions (already configured):
- Internet access
- Network state access

These are defined in `android/app/src/main/AndroidManifest.xml`

## 🔐 Security Notes

1. **HTTPS**: The portal uses HTTPS, ensuring secure communication
2. **Cookies**: Automatically managed by WebView
3. **Session**: Persists across app restarts
4. **JavaScript**: Enabled for full portal functionality

## 📊 App Size Optimization

To reduce APK size, build split APKs per ABI:
```bash
flutter build apk --split-per-abi
```

This creates separate APKs for:
- `app-armeabi-v7a-release.apk` (32-bit ARM)
- `app-arm64-v8a-release.apk` (64-bit ARM)
- `app-x86_64-release.apk` (64-bit x86)

## 🚀 Quick Build Command

For the fastest build (release APK):
```bash
flutter clean && flutter pub get && flutter build apk --release
```

## 📝 Version Management

Update version in `pubspec.yaml`:
```yaml
version: 1.0.0+1  # Format: major.minor.patch+buildNumber
```

## 🎯 Next Steps

1. ✅ Test the app thoroughly on different devices
2. ✅ Customize app icon and name
3. ✅ Test login and session persistence
4. ✅ Verify all portal features work correctly
5. ✅ Build release APK
6. ✅ Distribute to students

## 📞 Support

For issues specific to:
- **Flutter/App**: Check Flutter documentation
- **Portal Website**: Contact EAU Galkacyo IT support
- **WebView**: Check `webview_flutter` package documentation

---

**Built with Jose Dev 💙**
