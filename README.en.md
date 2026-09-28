# DesktopStream

[日本語](README.md) | English

Software for viewing and controlling a Windows PC's screen from a phone or another PC.

- It can also show and control the UAC prompt and the lock screen, so you can get past an administrator prompt even when you are away
- It works on the same Wi-Fi and from outside (from outside it connects directly, P2P)
- You can also show the video you receive to other people, with comments

Requirements: Windows 10 / 11 (64-bit)

The screens are in English when your device's language is not Japanese. The logs are written in Japanese.

---

## Getting started

### 1. Download

**[Download the latest version](https://github.com/brad-55/DesktopStream/releases/latest)**

| File | Which to choose |
|---|---|
| `DesktopStream-...-setup.exe` | The installer. Choose this one normally |
| `DesktopStream-...-portable.zip` | A version you just extract and place. Choose it if you prefer not to use the installer |

### 2. Start

The [Quick Start](https://brad-55.github.io/DesktopStream/quickstart.en.html) walks you through getting the screen to appear (about 5 minutes).
Details of each feature and troubleshooting are in the [User Guide](https://brad-55.github.io/DesktopStream/guide.en.html).

### Pages for the controlling side

| Purpose | URL |
|---|---|
| Control from anywhere | https://brad-55.github.io/DesktopStream/client.html |
| Watch a restream (view only) | https://brad-55.github.io/DesktopStream/secondclient.html |

On the same Wi-Fi, you can also open `https://PC-IP:8080`, served by the PC itself (no room ID needed).

---

## ⚠️ This software is not signed

The author has not obtained a code-signing certificate, so Windows SmartScreen and antivirus software show warnings.
In addition, this software combines "a service with SYSTEM rights + screen capture + input injection + network communication", the same characteristics as remote-access malware, which makes it likely to be flagged.

You can confirm that the downloaded file has not been altered by checking its SHA256.
The correct values are listed in each release's notes.

```powershell
Get-FileHash .\DesktopStream-v0.8.1-setup.exe -Algorithm SHA256
```

Change the file name to match the version you downloaded.

## Using it safely

- **The room ID is effectively a password.** Anyone who knows it can connect to and control your screen. Do not show it to others
- A device connecting for the first time must be approved on the PC
- When you are done, press Stop or disconnect from the console

## License

GStreamer / GLib (LGPL-2.1-or-later) are included. The full license texts are in `licenses/` in the distribution. The GPL-licensed x264 / x265 are not included.
