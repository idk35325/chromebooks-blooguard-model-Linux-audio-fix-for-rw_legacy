# chromebooks-blooguard-model-Linux-audio-fix-for-rw_legacy
chromebook-14a-14b-ca0-rwlegacy-audio-fix

# 🎧 HP Chromebook x360 14a/14b-ca0 Audio Fix (rw_legacy)

This project provides a tested **audio fix** for the **HP Chromebook x360 14a-ca0 / 14b-ca0** models when running **Linux** with **MrChromebox rw_legacy firmware**.

If you’re using a **full ROM** flash, you probably don’t need this — this fix is designed for **rw_legacy users** who want to keep ChromeOS boot options but still have working audio in Linux.

---

## 🧩 Overview

Many Chromebook users (especially on HP x360 14a/14b models) lose sound after installing Linux via **rw_legacy**.  
This fix restores audio output by restoring known-good **GRUB + ALSA** configurations from a verified backup that has been tested and confirmed working.

**Confirmed working on:**
- ✅ HP Chromebook x360 14a-ca0
- ✅ HP Chromebook x360 14b-ca0

**Tested Linux distributions:**
- 🟢 Pop!_OS 22.04 / 24.04
- 🟢 Ubuntu 22.04 / 24.04

**May also work on:**
- 🟡 Linux Mint
- 🟡 Debian
- 🟡 Fedora
- 🟡 Elementary OS
- 🟡 Zorin OS
- 🟡 GalliumOS (if using custom kernel)

If you test and confirm it works on other distros, please open an **issue** or **pull request** so we can update the list!

---

## ⚙️ Installation

### 1. Clone this repository
```bash
git clone https://github.com/<yourusername>/hp-x360-14a-ca0-audio-fix.git
cd hp-x360-14a-ca0-audio-fix
