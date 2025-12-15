# ⚠️ Personal Fork Notice

**This is a personal fork** of the original [Dose App by Waseef Akhtar](https://github.com/waseefakhtar/dose-android).

This version has been modified for **personal use only** with a focus on privacy and modern Android features:
- ✅ **No Firebase** - All analytics and crash reporting removed
- ✅ **Fully Offline** - Zero network access, all data stored locally
- ✅ **Android 16 Only** - Targets latest Android (API 36) exclusively
- ✅ **Privacy-First** - No external tracking or data collection
- ✅ **Manual Installation** - Build from source using Android Studio

## Original App

**Want the official version?** Download from Google Play Store:

[![Google Play](https://img.shields.io/badge/Download%20Original-Google%20Play-green?logo=android)](https://play.google.com/store/apps/details?id=com.waseefakhtar.doseapp)

**Original Repository:** [waseefakhtar/dose-android](https://github.com/waseefakhtar/dose-android)

**Original Author:** [Waseef Akhtar](https://github.com/waseefakhtar)

---

![Dose App](docs/images/play-store.png "Dose App")

<h1 align="center">Dose App 💊⏰</h1>
<p align="center">
  <a href="https://android-arsenal.com/api?level=36"><img alt="API" src="https://img.shields.io/badge/API-36%2B-brightgreen.svg?style=flat"/></a>
  <img alt="Android 16" src="https://img.shields.io/badge/Android-16-green.svg"/>
  <img alt="Privacy" src="https://img.shields.io/badge/Privacy-First-blue.svg"/>
  <img alt="Offline" src="https://img.shields.io/badge/Network-Offline-orange.svg"/>
</p>

<p align="center">
Dose is a medication reminder app for Android, designed to help you stay on top of your health by reminding you to take your medications on time.
</p>

<p align="center">
This fork is built with Jetpack Compose, Material Design 3, Room, Navigation Components, Kotlin Coroutines, and Hilt following the recommended <a href="https://developer.android.com/topic/architecture">Android Architecture Guidelines</a>.
</p>

## What's Different in This Fork?

This personal fork has been significantly modified from the original:

### Removed
- ❌ **Firebase Analytics** - No external tracking
- ❌ **Firebase Crashlytics** - Local crash logging only
- ❌ **All network dependencies** - 100% offline app
- ❌ **Backward compatibility** - Android 16 only (no legacy code)

### Added
- ✅ **Local crash logger** - Crashes saved to device storage
- ✅ **Privacy-focused** - Zero data collection
- ✅ **Secure signing configuration** - Personal keystore setup
- ✅ **Dependabot** - Automated dependency updates
- ✅ **Comprehensive documentation** - Security audit, signing guide, backup options

### Modified
- 🔄 **Backup configuration** - Explicit Google Drive backup for personal use
- 🔄 **Build configuration** - Optimized for Android 16
- 🔄 **Analytics** - Replaced with local-only logging

## Requirements

- **Android 16 (API 36) or higher** - This app will NOT run on older versions
- **Android Studio** - Required for building from source
- **Personal device** - Designed for personal use, not distribution

## Installation

This fork is **not available on Google Play Store**. You must build and install manually.

### Option 1: Build with Android Studio

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/dose-android.git
   cd dose-android
   ```

2. **Open in Android Studio:**
   - Launch Android Studio
   - Open the `dose-android` folder
   - Wait for Gradle sync to complete

3. **Set up signing (first time only):**
   - See `SIGNING_SETUP.md` for detailed instructions
   - Generate your personal keystore
   - Configure `app/keystore.properties`

4. **Build and install:**
   - Connect your Android 16 device via USB
   - Click Run ▶️ in Android Studio
   - Or build release: `./gradlew assembleRelease`

### Option 2: Build from Command Line

```bash
# Clone the repository
git clone https://github.com/YOUR_USERNAME/dose-android.git
cd dose-android

# Set up signing (see SIGNING_SETUP.md)
cp app/keystore.properties.template app/keystore.properties
# Edit keystore.properties with your values

# Build release APK
./gradlew assembleRelease

# Install on connected device
adb install app/build/outputs/apk/release/app-release.apk
```

## Documentation

This fork includes comprehensive documentation:

- **`SECURITY_AUDIT_REPORT.md`** - Complete security audit findings
- **`SIGNING_SETUP.md`** - How to set up release signing
- **`BACKUP_OPTIONS.md`** - Backup configuration guide
- **`FIREBASE_REMOVAL_SUMMARY.md`** - Changes from original app
- **`.github/DEPENDABOT_GUIDE.md`** - Dependency management

## Privacy & Security

This fork prioritizes privacy:

- 🔒 **No external connections** - App is 100% offline
- 🔒 **Local-only data** - All medication data stays on your device
- 🔒 **No tracking** - Zero analytics or telemetry
- 🔒 **Google Drive backup** - Optional, explicit backup to your account
- 🔒 **Open source** - All code is auditable

## Technology Stack

- **Jetpack Compose** - Modern declarative UI
- **Material Design 3** - Latest Material Design
- **Room Database** - Local data persistence
- **Hilt** - Dependency injection
- **Kotlin Coroutines** - Asynchronous programming
- **Navigation Component** - In-app navigation
- **AlarmManager** - Medication reminders

## Architecture

This app follows **MVVM architecture** with clean separation of concerns:

```
├── data/           # Data layer (Room, repositories)
├── domain/         # Business logic (models, use cases)
├── feature/        # Feature modules (UI + ViewModels)
├── di/            # Dependency injection
├── analytics/     # Local logging (no external services)
└── navigation/    # Navigation configuration
```

## Contributing

**This is a personal fork** and is not accepting contributions.

For the official version that welcomes contributions, please see:
- [Original Repository](https://github.com/waseefakhtar/dose-android)
- [Discussions](https://github.com/waseefakhtar/dose-android/discussions)

## Credits

**Original App Created By:** [Waseef Akhtar](https://github.com/waseefakhtar)

**Original Resources:**
- [Google DevLibrary](https://devlibrary.withgoogle.com/products/android/repos/waseefakhtar-dose-android)
- [Blog Post](https://www.waseefakhtar.com/android/form-using-jetpack-compose-and-material-design/)
- [YouTube Tutorial](https://www.youtube.com/watch?v=taWNluAoyaE)
- [Google Play Store](https://play.google.com/store/apps/details?id=com.waseefakhtar.doseapp)

This fork maintains the original MIT License while adding privacy-focused modifications for personal use.

## License

Dose App is distributed under the terms of the MIT License. See the [LICENSE](LICENSE) file for more information.

Original work Copyright © 2022 Waseef Akhtar
Modified work Copyright © 2025 (Personal Fork)

---

**Note:** This is a personal fork for individual use only. For the official app with community support and regular updates, please download the [original Dose App from Google Play Store](https://play.google.com/store/apps/details?id=com.waseefakhtar.doseapp).
