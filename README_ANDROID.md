# Chaos Study Room - Android App

## Quick Start

This is a **web-based Android application** built with **Capacitor**, allowing you to run your Pomodoro timer, study tracker, and CBSE board map natively on Android.

### What's Included
- ✅ **Complete Pomodoro Timer** with customizable work/break durations
- ✅ **Study Log** - Track focus time by subject and topic
- ✅ **To-Do Manager** - Organize tasks by subject
- ✅ **CBSE Board Map** - Syllabus tracker with live countdown to Feb 20
- ✅ **Music Player** - Upload and play study music
- ✅ **Offline Support** - All data saved locally, works without internet
- ✅ **Dark Theme** - Harley Quinn styled UI optimized for reduced eye strain

## Installation

### Option 1: Build from Source (Recommended)

**Requirements:**
- Node.js v16+
- npm or yarn
- Android Studio (for emulator/device testing)
- JDK 11+

**Steps:**
```bash
# 1. Clone the repo
git clone https://github.com/govindrkumar/radha-pomodoro.git
cd radha-pomodoro

# 2. Install dependencies
npm install

# 3. Generate Android project
npm run build:android

# 4. Open in Android Studio
npm run open:android

# 5. Run on device/emulator
# In Android Studio: Run > Run 'app' or press Shift+F10
```

### Option 2: Use Pre-built APK
(Coming soon to releases)

## Usage

### 1. Pomodoro Timer
- Select mode: Focus (25min), Short Break (5min), Long Break (15min)
- Click "Start" and enter what you're studying
- Timer runs in background; lock your screen if needed
- Bell sound plays when session ends
- Study session auto-logs to your Study Log

### 2. Study Log
- View daily focus time by subject (Bio, Chem, Physics, Eng, Painting)
- See week-at-a-glance summary
- Manual session logging option
- 7-day aura farming graph showing study trends

### 3. To-Do List
- Add tasks by subject
- Track completion percentage
- Clear completed tasks
- Tabs for each subject + "All" view

### 4. CBSE Board Map
- Live countdown to February 20, 2027 exam
- Filter by subject (Physics, Chemistry, Biology, English, Painting)
- Check off chapters as you complete them
- Overall syllabus completion percentage

### 5. Music Box
- Drag & drop audio files (or tap to browse)
- Playlist management
- Play, pause, skip, shuffle, repeat controls
- Volume adjustment
- Now-playing display

## Data & Privacy

✅ **All data is stored locally** on your device via browser localStorage  
✅ **No cloud sync** - your study data never leaves your phone  
✅ **No login required** - instant privacy  
✅ **Backup:** Data persists across app updates (Capacitor native storage)  

**To backup manually:**
- Open browser DevTools on Android (chrome://inspect)
- Application → LocalStorage → index.html
- Copy all data to safe location

## Performance Tips

1. **Reduce distractions:** Enable app lock during study sessions
2. **Battery:** App uses minimal power; timer runs in background
3. **Memory:** Unload large audio files if phone runs low on RAM
4. **Notifications:** Enable system notifications (Settings → Notifications)

## Troubleshooting

### App won't start
```bash
npm run sync:android
npm run open:android
# Then Run from Android Studio
```

### Timer sound not working
- Check device volume (not mute)
- Verify media permission granted in Settings
- Try restarting app

### Study log not saving
- Check if localStorage is enabled in Android WebView
- Clear app cache: Settings → Apps → Chaos Study Room → Storage → Clear Cache

### Build fails
```bash
# Update Capacitor
npm install @capacitor/cli@latest
npm install @capacitor/core@latest
npm install @capacitor/android@latest
npm run build:android
```

## Development

### Local Testing
```bash
# Test in browser before building
npm run start
# Open http://localhost:8000
```

### Debug APK
```bash
# Build debug version
npm run open:android
# In Android Studio: Build → Build APK(s)
```

### Release Build
```bash
# In Android Studio:
# Build → Generate Signed Bundle / APK
# Follow wizard to sign your app
# Upload to Google Play Console
```

## Project Structure

```
radha-pomodoro/
├── index.html              # Main web app (Pomodoro, logs, etc.)
├── capacitor.config.json   # Android app configuration
├── manifest.webmanifest    # PWA manifest
├── package.json            # Dependencies & build scripts
├── android/                # Generated Android project (after npm run build:android)
└── README_ANDROID.md       # This file
```

## Supported Devices

- **Minimum:** Android 6.0 (API 24)
- **Recommended:** Android 12+ (API 31+)
- **Screen sizes:** Phone optimized; tablets supported

## License

Free to use. Built with ❤️ for CBSE students.

## Contributing

Found a bug? Want to add a feature?  
Open an issue or PR on GitHub: https://github.com/govindrkumar/radha-pomodoro

---

**Happy studying! ♥ CBSE Chaos Room**
