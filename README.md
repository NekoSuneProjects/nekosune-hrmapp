# HRMAPP Pulsoid Discord RPC + OBS Overlay (Electron)

## Good News â€” macOS Build Working Again!

A fresh macOS build is now available and fully working!

**Important:** The app is currently **unsigned** because Apple requires a **$99/year Apple Developer ID** to notarize and sign apps.  
Because of this, macOS may show:

> **"Apple cannot verify that this app is free of malware."**

This is expected for unsigned Electron apps.

### How to Open the App Anyway  
If macOS blocks the app, you can still run it safely.

**Video tutorial:** https://www.youtube.com/watch?v=biIvAM94b98  

Or follow these steps manually:

1. Try to open the `.app` â€” macOS will block it.
2. Open **System Settings â†’ Privacy & Security**
3. Scroll until you see **â€œApp was blocked from openingâ€**
4. Click **Allow Anyway**
5. Re-open the app â†’ click **Open**

After this, the app will launch normally every time.

---

## Build & Run

### 1) Install & Start
```bash
npm install
npm run start
```

---

## Configure

Open **Settings** inside the app:

- Paste your **Pulsoid Access Token**  
  *(Required scope: `data:heart_rate:read`)*
- (Optional) Add **Discord Client ID**, then toggle **Discord RPC** on
- Toggle **Realtime** to start/stop Pulsoid streaming

---

## OBS Overlay Setup

- Click **Open OBS Overlay** inside the app  
- In OBS â†’ **Sources** â†’ **+** â†’ **Window Capture**
- Select the window titled **Overlay**
- Enable **Allow Transparency** (if supported)
- Make sure the overlay window is visible on the same desktop

>  **Tip:** The overlay window is resizable and click-through by default.

---

## Notes

- Settings are saved locally using **electron-store** and loaded at startup  
- Discord RPC requires the **Discord desktop app** running on the same machine  
- The live chart stores the latest ~120 heart-rate points for performance  

---
