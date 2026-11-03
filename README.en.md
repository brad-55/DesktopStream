# DesktopStream

[日本語](README.md) | English

Software for viewing and controlling a Windows PC's screen from a phone or another PC.

- It can also show and control the UAC (Windows administrator) prompt and the lock screen, so you can clear an administrator prompt without walking over to the PC
- It works on the same Wi-Fi and from outside (from outside, the two devices connect to each other directly)
- You can also show the screen displayed on your phone to other people, with comments

Requirements: Windows 10 / 11 (64-bit)

The screens are in English when your device's language is not Japanese. The logs are written in Japanese.

---

## Getting started

### 1. Download

**[Download the latest version](https://github.com/brad-55/DesktopStream/releases/latest)**

| File | Which to choose |
|---|---|
| `DesktopStream-...-setup.exe` | The installer. Choose this one normally |
| `DesktopStream-...-portable.zip` | A version you unzip into any folder. Choose it if you prefer not to use the installer |

### 2. Start

The [Quick Start](https://brad-55.github.io/DesktopStream/quickstart.en.html) walks you through getting the screen to appear (about 5 minutes).
Details of each feature and troubleshooting are in the [User Guide](https://brad-55.github.io/DesktopStream/guide.en.html).

### Pages you open on the phone

| Purpose | URL |
|---|---|
| Control from anywhere | https://brad-55.github.io/DesktopStream/client.html |
| Watch a stream (view only) | https://brad-55.github.io/DesktopStream/secondclient.html |

On the same Wi-Fi, you can also open `https://PC-IP:8080`, served by the PC itself (no room ID needed; the first visit shows a certificate warning — choose "Advanced" then "Proceed").

---

## ⚠️ This software is not signed

The author has not obtained a code-signing certificate, so Windows SmartScreen and antivirus software show warnings.
In addition, this software combines "a service running with deep Windows privileges", "screen capture", "sending keyboard and mouse input" and "network communication". Those are the same traits as remote-access malware, which makes warnings more likely.

You can confirm that the downloaded file has not been altered by checking its SHA256.
The correct values are listed in each release's notes.

```powershell
Get-FileHash .\DesktopStream-v0.8.1-setup.exe -Algorithm SHA256
```

Replace `DesktopStream-v0.8.1-setup.exe` in the command above with the file you actually downloaded.

## Using it safely

- **The room ID is effectively a password.** Anyone who knows it can view and control your screen. Do not show it to others
- A device connecting for the first time stays blocked until you press Yes on the PC
- When you are done, press Stop, or disconnect from the console (open it from the tray icon on the PC)

## License

GStreamer / GLib (LGPL-2.1-or-later) are included. The full license texts are in `licenses/` in the distribution. The GPL-licensed x264 / x265 are not included.
