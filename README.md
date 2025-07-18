# Ulefone Power Armor 14 Pro - Magisk Rooted Boot Image and Firmware

This repository contains a **Magisk-patched boot image** and the original **stock firmware** for the Ulefone Power Armor 14 Pro.  
These files can be used to root your device using **SP Flash Tool** on Windows or Linux.

**DISCLAIMER**: This is for educational and personal use only. Rooting your device will void the warranty and may result in a **soft-brick or hard-brick** if not done properly. Proceed at your own risk.

---

## 🔧 Included Files

- `/img/boot.img` — Original unmodified boot image.
- `/img/magisk_patched.img` — Boot image patched using Magisk.
- `/firmware/` — Full official firmware for the Ulefone Power Armor 14 Pro.
- `/firmware/MT6768_Android_scatter.txt` — Scatter file used by SP Flash Tool.

---

## 📱 Device Information

- **Model:** Ulefone Power Armor 14 Pro  
- **Chipset:** MediaTek Helio G85 (MT6768)  
- **Architecture:** ARM64  
- **Android Version:** Android 12 (may vary by region)  
- **Status:** Tested and confirmed working on my personal device

---

## ⚠️ Warnings & Risks

- Rooting **voids the warranty** of your device.
- A wrong flash can **brick your phone**. Always double-check.
- This will **erase user data** if you perform a full firmware flash.
- Only flash the **boot image** if your goal is to root, not the full ROM.

---

## ✅ Prerequisites

1. **Unlocked Bootloader** (this is required).
2. A Windows or Linux PC.
3. **SP Flash Tool**: [Download SP Flash Tool](https://spflashtool.com/)
4. USB Cable and the proper drivers installed for MediaTek.
5. A full **backup** of your phone.

---

## 🧩 Step-by-Step Instructions (Root with Magisk)

### Step 1: Install Drivers (Windows)

- Install **MediaTek VCOM Drivers**:
  - You can find preloader drivers here: https://gsmusbdrivers.com/mediatek
  
- Disable driver signature enforcement in Windows if needed.

---

### Step 2: Install SP Flash Tool

- Download and extract SP Flash Tool from [official site](https://spflashtool.com/)
- Run `flash_tool.exe` as Administrator (Windows)

---

### Step 3: Load Scatter File

- In SP Flash Tool, click **“Choose”** next to **Scatter-loading File**.
- Select:  
  `firmware/MT6768_Android_scatter.txt`

---

### Step 4: Replace Boot Image

- In the partition list, **uncheck everything** except the **boot** partition.
- Click on the boot line, and **manually select** `img/magisk_patched.img`

---

### Step 5: Flash the Patched Boot

- Set **Download Only** mode (top dropdown).
- Power off your phone **completely**.
- Click **Download** (green arrow).
- Connect your phone via USB **while powered off**.
- Wait until the **green check** appears.

---

### Step 6: Reboot and Verify Root

- Power on your phone normally.
- Install the **Magisk App** on your phone.
- Open it — it should say **“Magisk Installed”** with root access enabled.

---

## 🔄 Restore Stock Boot Image (Optional)

If something goes wrong or you want to unroot your phone:

1. Repeat the steps above.
2. In **Step 4**, select `img/boot.img` instead of `magisk_patched.img`.
3. Flash as before.
4. Root will be removed.

---

## 📦 Firmware Use (Optional Full Flash)

You can also use the provided full firmware in `firmware/` to restore your phone to factory condition. Use this only if:

- Your phone is bricked.
- You want to completely revert all changes.
- You want to reinstall the stock system.

**Warning:** This will erase all data.

---

## 🧪 Testing and Status

- This has been tested on a **real Ulefone Power Armor 14 Pro**.
- Root access confirmed working with:
  - `Magisk`
  - `Root Checker`
  - `Termux su`
- Use at your own risk.

---

## 📜 License

This repository is licensed under the **MIT License**.

---

## ✉️ Author

Maintained by: **[paulnejaa](https://github.com/paulnejaa)**  
Contact: `jeremiasnejanky360@gmail.com`
