# HRMAPP Pulsoid Discord RPC + OBS Overlay (Electron)

## 🚀 Good News — macOS Build Working Again!

A fresh macOS build is now available and fully working!

⚠️ **Important:** The app is currently **unsigned** because Apple requires a **$99/year Developer ID** to notarize and sign apps.  
Because of this, macOS may show:

> **"Apple cannot verify that this app is free of malware."**

This is expected for unsigned Electron apps.

### ✔️ How to Open the App Anyway  
If macOS blocks the app, follow this simple guide:  
📺 **Video tutorial:** https://www.youtube.com/watch?v=biIvAM94b98  

Or follow these steps manually:

1. Try to open the `.app` normally — macOS will block it.
2. Open **System Settings → Privacy & Security**
3. Scroll down until you see **“App was blocked from opening”**
4. Click **Allow Anyway**
5. Launch the app again → click **Open**

After this, it will run normally every time.

---

### 1) Install
```bash
npm install
npm run start
```

### 2) Configure
Open **Settings** inside the app:
- Paste your **Pulsoid Access Token** (scope: `data:heart_rate:read`)
- (Optional) Add **Discord Client ID**, then toggle **Discord RPC** on
- Toggle **Realtime** to start/stop Pulsoid streaming

### 3) OBS Overlay
- Click **Open OBS Overlay** in the app
- In OBS → *Sources* → **+** → **Window Capture** → choose the window titled **Overlay**
- Enable **Allow Transparency** if available; ensure the overlay window is visible on the same desktop

> Tip: You can resize the overlay window to taste. It’s click‑through by default.

### Notes
- Settings are saved locally via `electron-store` and loaded at startup
- Discord RPC requires the **Discord desktop** client running on the same machine
- The live chart is capped to the latest ~120 points
