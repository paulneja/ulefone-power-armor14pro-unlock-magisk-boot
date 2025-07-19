
# Ulefone Power Armor 14 Pro – Bootloader Unlock and Magisk Root Guide

This repository provides all the necessary resources and step-by-step instructions to unlock the bootloader and root the **Ulefone Power Armor 14 Pro (MT6768 / Helio G85)** using **Magisk**. It includes the patched boot image, stock boot image, and a full guide intended for advanced users.

---

## Disclaimer

Unlocking the bootloader and flashing custom images **will erase all data** on your device and may void your warranty. There is also a risk of bricking your phone if you do something wrong. Proceed **at your own risk**. Always make backups before continuing.

---

## Repository Content

| File Name            | Description                                        |
|----------------------|----------------------------------------------------|
| `boot.zip`           | Original stock boot.img extracted from firmware    |
| `magisk_patched.zip` | Boot image patched with Magisk v26.4               |
| `README.md`          | This instruction manual                            |

---

## Requirements

- Ulefone Power Armor 14 Pro
- USB cable and PC (Windows or Linux)
- ADB & Fastboot installed on your computer
- MTK/Android USB drivers installed
- Battery charged above 50%
- Magisk v26.4 APK (from official GitHub)
- Patience and care

---

## Step-by-Step Instructions

### 1. Enable Developer Mode and USB Debugging

1. On your phone, go to **Settings > About phone**.
2. Tap **Build number** repeatedly until developer mode is enabled.
3. Go to **Settings > Developer options**.
4. Enable both **OEM Unlocking** and **USB Debugging**.

---

### 2. Unlock Bootloader (⚠️ This will erase all your data)

1. Connect your phone to your PC via USB.
2. Open a terminal or command prompt.
3. Type:
   ```bash
   adb devices

Confirm the debug prompt on your phone if asked.

4. Reboot to bootloader:

adb reboot bootloader


5. Once in bootloader mode, unlock it:

fastboot flashing unlock


6. Confirm on your phone using the volume keys.


7. Wait until the device wipes all data and reboots automatically.




---

3. Flash the Magisk Patched Boot Image

1. Set up your phone again and re-enable USB Debugging.


2. Reboot to bootloader again:

adb reboot bootloader


3. Extract magisk_patched.zip to get magisk_patched.img.


4. Flash the patched image:

fastboot flash boot magisk_patched.img


5. Reboot the device:

fastboot reboot




---

4. Install Magisk on Device

1. Download Magisk v26.4 APK from official GitHub.


2. Transfer the APK to your phone and install it manually.


3. Open Magisk to verify if root access is active.




---

Optional – Restore Original Boot

If something fails or you want to unroot your device:

1. Extract boot.zip to obtain boot.img.


2. Flash the original image:

adb reboot bootloader
fastboot flash boot boot.img
fastboot reboot




---

Optional – Play Integrity / SafetyNet

For apps that detect root (banking, Google Wallet, etc.):

Enable Zygisk in Magisk settings

Install the following modules:

MagiskHide Props Config

Universal SafetyNet Fix


Use LSPosed (optional) for deeper system spoofing

Clear Play Store data after applying modules



---

Tested On

Device: Ulefone Power Armor 14 Pro

Chipset: MediaTek MT6768 (Helio G85)

Firmware: Stock Android 11/12

Magisk: v26.4



---

License

This repository is open-source under the MIT License.


---

Support

If you encounter issues, you can:

Open an issue on this GitHub repository.

Reflash the original firmware (scatter + SP Flash Tool).

Restore stock boot image if needed.
Maintained by: **[paulnejaa](https://github.com/paulnejaa)**  


This repository is licensed under the MIT License.
Use at your own risk. I am not responsible for bricked devices or data loss.
