# 🎓 EAU Galkacyo Portal App

[![Flutter](https://img.shields.io/badge/Built%20with-Flutter-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://flutter.dev)
[![Platform](https://img.shields.io/badge/Platform-Android-3DDC84?style=for-the-badge&logo=android&logoColor=white)](https://www.android.com)
[![Version](https://img.shields.io/badge/Version-1.0.0-blue?style=for-the-badge)]()

A seamless, native Android application for the **East Africa University (EAU) Galkacyo** student portal. Access exams, results, and student services directly from your phone.

---

## 📱 App Screenshots

<div align="center">
  <table border="0">
    <tr>
      <td align="center" width="250">
        <img src="app%20assets/App%20Login.jpeg" width="200" alt="Login Page" style="border-radius: 10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
        <br/><br/>
        <b>🔐 Secure Student Login</b>
      </td>
      <td align="center" width="250">
        <img src="app%20assets/APpp%20dashborad.jpeg" width="200" alt="Dashboard" style="border-radius: 10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
        <br/><br/>
        <b>📊 Dashboard Overview</b>
      </td>
    </tr>
    <tr>
       <td align="center" width="250">
        <img src="app%20assets/app%20student%20activity.jpeg" width="200" alt="Student Activity" style="border-radius: 10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
        <br/><br/>
        <b>📝 Exam & Activity Tracking</b>
      </td>
      <td align="center" width="250">
        <img src="app%20assets/App%20developer%20portfolio.jpeg" width="200" alt="Developer Portfolio" style="border-radius: 10px; box-shadow: 0 4px 8px 0 rgba(0, 0, 0, 0.2);"/>
        <br/><br/>
        <b>👨‍💻 Developer Information</b>
      </td>
    </tr>
  </table>
</div>

---

## ✨ Key Features

- **⚡ Native Experience**: Smooth, native Android feel with a clean user interface.
- **🔄 Session Persistence**: Stay logged in securely without re-entering credentials every time.
- **🎨 Modern Design**: Beautiful styling with a custom footer and app bar.
- **↩️ Smart Navigation**: 
  - Integrated back button for seamless browsing.
  - Pull-to-refresh functionality.
  - Easy access to developer portfolio with auto-appearing navigation controls.
- **📉 Optimized Performance**: Ultra-lightweight APK size (~15 MB) for fast downloads.

## 🚀 Installation Guide

1. **Download the APK**: Get the `app-arm64-v8a-release.apk` (Recommended) or `app-release.apk`.
2. **Allow Installation**: Go to `Settings > Security` and enable "Install from Unknown Sources".
3. **Install**: Open the file and tap "Install".
4. **Login**: Use your EAU student credentials to access the portal.

> **Note**: For detailed distribution and installation instructions, see [APK_DISTRIBUTION_GUIDE.md](APK_DISTRIBUTION_GUIDE.md).

## 🛠️ Tech Stack

- **Framework**: Flutter (Dart)
- **WebView**: Optimized `webview_flutter` implementation
- **Architecture**: Split ABI for minimized APK size
- **Design**: Material 3 with custom color palette (`#333D79`, `#FAEBEF`)

## 👨‍💻 Developer Guide

Want to run this project locally? Follow these simple steps:

### 📥 1. Clone Process
```bash
git clone https://github.com/yousumohamed/EAU-flutter-Apk.git
cd EAU-flutter-Apk
```

### 📦 2. Install Dependencies
<img src="https://img.shields.io/badge/Dart-Pub%20Get-0175C2?style=for-the-badge&logo=dart&logoColor=white" height="28">

```bash
flutter pub get
```

### 📱 3. Run the App
<img src="https://img.shields.io/badge/Run-Debug-3DDC84?style=for-the-badge&logo=android&logoColor=white" height="28">

```bash
flutter run
```

### 🔨 4. Build Release APK
<img src="https://img.shields.io/badge/Build-Release-FFCA28?style=for-the-badge&logo=flutter&logoColor=black" height="28">

```bash
flutter build apk --release --split-per-abi
```
> This generates optimized APKs in `build/app/outputs/flutter-apk/`

---

<div align="center">
  <h3>Developed with ❤️ by <a href="https://yusuf-abdi.vercel.app/" style="text-decoration: none; color: #333D79;">Jose</a></h3>
  <p>Self-Taught Developer | Relentless Learner | Turning Ideas into Code</p>
  
  [![Portfolio](https://img.shields.io/badge/Visit-Portfolio-333D79?style=for-the-badge&logo=firefox&logoColor=white)](https://yusuf-abdi.vercel.app/)
</div>
