# 🎙 Mic To Speaker — Android App
## Live audio from phone mic → Bluetooth speaker

---

## 📁 Project Files

```
MicToSpeaker/
├── app/
│   ├── build.gradle
│   └── src/main/
│       ├── AndroidManifest.xml
│       ├── java/com/mictospeaker/
│       │   └── MainActivity.java
│       └── res/
│           └── layout/
│               └── activity_main.xml
├── build.gradle
└── settings.gradle
```

---

## 🔨 How to Build the APK (Step by Step)

### Step 1 — Install Android Studio
Download from: https://developer.android.com/studio
(Free, works on Windows / Mac / Linux)

### Step 2 — Open the Project
1. Launch Android Studio
2. Click **"Open"**
3. Select the **MicToSpeaker** folder

### Step 3 — Wait for Sync
Android Studio will download Gradle and dependencies automatically (~2 min first time).
Click **"Sync Now"** if prompted.

### Step 4 — Build the APK
Go to menu: **Build → Build Bundle(s) / APK(s) → Build APK(s)**

Wait ~1–2 minutes. A notification will appear:
> "APK(s) generated successfully"

Click **"locate"** to find the file.

### Step 5 — Find the APK
The APK will be at:
```
MicToSpeaker/app/build/outputs/apk/debug/app-debug.apk
```

### Step 6 — Send to Friends
- Send via WhatsApp, Telegram, email, or Google Drive
- Friends must enable **"Install unknown apps"** in their phone settings
  (Settings → Apps → Special app access → Install unknown apps)

---

## 📱 How to Use the App

1. **Connect your Bluetooth speaker** to your phone first
2. Open the app
3. Tap **"▶ START STREAMING"**
4. Grant microphone permission when asked
5. Speak into your phone — your voice plays through the Bluetooth speaker live!
6. Tap **"⏹ STOP"** when done

---

## ✅ Requirements
- Android 6.0 (API 23) or higher
- Bluetooth speaker connected via **A2DP** (standard speaker profile)
- Microphone permission granted

---

## 🔧 Troubleshooting

| Problem | Solution |
|---------|----------|
| No sound from speaker | Make sure speaker is connected BEFORE tapping START |
| Echo / feedback | Move phone away from speaker, or lower speaker volume |
| App crashes | Check Android Studio for error in Logcat |
| "Install blocked" | Enable "Install unknown apps" for your file manager |

---

## ⚡ Notes
- The app uses **44100 Hz PCM 16-bit** audio for best quality
- **A2DP profile** is used for Bluetooth speakers (auto-routed by Android)
- **SCO profile** fallback for Bluetooth headsets
- Thread priority is set to MAX for lowest latency
