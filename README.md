# HP Chromebook x360 14a/14b Audio Fix for Linux (rw_legacy)



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
- 🟡 GalliumOS (with custom kernel)  

If you test and confirm it works on other distros, please open an **issue** or **pull request** so we can update the list!

---

⚙️ Installation (Manual Method)

If you already have nano installed, you can manually add the audio fix to GRUB.

1. Open the GRUB configuration file
sudo nano /etc/default/grub

2. Find the line

GRUB_CMDLINE_yourusername_DEFAULT=3.

GRUB_CMDLINE_yourusername_DEFAULT="quiet splash snd_intel_dspcfg.dsp_driver=3"

💡 Important: Do not change the _DEFAULT part — that’s the correct GRUB variable name.

only your username

4. Save and exit nano

Press Ctrl + O → then Enter to save

Press Ctrl + X to exit

5. Update GRUB
sudo update-grub

6. Reboot your Chromebook
sudo reboot


✅ After reboot, your sound (speakers and headphone jack) should now work.

## ⚡ Features / Why It Works

- Forces the Intel audio driver to use the legacy HDA interface.
- Works with rw_legacy firmware (no full ROM update required).
- Tested on Pop!_OS and Ubuntu.

