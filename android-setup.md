# Android App Setup Guide

## Prerequisites
- Node.js & npm installed
- Android Studio installed
- Java Development Kit (JDK) 11+
- Android SDK (API level 24+)

## Setup Instructions

### 1. Install Dependencies
```bash
npm install
```

### 2. Build Android Project
```bash
npm run build:android
```

This will:
- Add the Android platform via Capacitor
- Generate native Android project structure
- Build the app

### 3. Open in Android Studio
```bash
npm run open:android
```

### 4. Build & Deploy

**For Development:**
- Select your device/emulator in Android Studio
- Click "Run" or press `Shift + F10`

**For Release:**
1. In Android Studio: Build → Generate Signed Bundle/APK
2. Follow the wizard to sign your app
3. Upload to Google Play Store

## App Features (Already Built-In)
✓ Pomodoro Timer with customizable durations
✓ Study Log with subject tracking
✓ To-Do list with progress tracking
✓ CBSE Board Syllabus Map with chapter checkboxes
✓ Music player for study ambiance
✓ Local data persistence (localStorage)
✓ PWA capabilities
✓ Dark mode (Harley Quinn themed)
✓ Offline support

## Key Configuration Files

### capacitor.config.json
- App metadata
- Android-specific settings
- Splash screen & status bar configuration

### index.html
- Already includes Capacitor core script
- PWA manifest included
- Mobile-optimized viewport

## Troubleshooting

**Build fails with Java errors:**
- Ensure JDK 11+ is installed
- Set JAVA_HOME environment variable

**Android SDK not found:**
- Open Android Studio
- SDK Manager → Install API 24+
- Set ANDROID_HOME environment variable

**App crashes on launch:**
- Check logcat: `adb logcat`
- Ensure index.html is in project root
- Verify Capacitor plugins are synced: `npm run sync:android`

## Development Tips

- Use Chrome DevTools for debugging: `chrome://inspect`
- Test locally first: `npm run start`
- Keep localStorage data for offline functionality
- Test on actual device for best performance

## Release Checklist
- [ ] Update version in package.json
- [ ] Test all features on Android device
- [ ] Create signed APK/Bundle
- [ ] Update screenshots/descriptions for Play Store
- [ ] Submit for review
