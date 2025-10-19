# 🚀 PM981-Hackintosh

EFI for macOS on systems using Samsung PM981 or PM981a SSDs
(You’ll need to customize this EFI to match your specific hardware.)

## ⚠️ Caution

This project is currently in development and may be unstable on certain PCs, as PM981 and PM981a SSDs are not officially supported on macOS.

## 🧠 Important Notes:

❌ Do not delete any kexts included in this EFI.

💾 Back up your data before you begin.

🚫 Do not use macOS Tahoe Beta — it’s unsupported and will not work with PM981 drives.

✅ Recommended version: macOS Catalina for best results.

# ⚖️ Disclaimer

By continuing, you acknowledge that you have read and understood the following disclaimer and agree to its terms.

⚠️ The process described here can potentially cause irreversible damage to your device.
I take no responsibility for any hardware damage, data loss, or software issues that may result.
This EFI is provided as-is, with no guarantees of stability or compatibility.

# 🧩 Requirements

🖥️ A working Hackintosh system with a supported SSD.

If you only have one SSD, you can attempt a direct installation — but make sure to include RestrictEvents.kext.

🧭 Follow either tylernguyen/x1c6-hackintosh #43

or my guide (below) if you don’t already have macOS installed.

⏳ Patience is required — installing macOS on a PM981 can take 3+ hours.

If the installer says “Less than a minute remaining,” it’s not stuck — just slow due to NVMe patches.

## 🧰 Installation Guide
🔹 Step 1 — Generate an SMBIOS

Download GenSMBIOS

Install Python (from the Microsoft Store or another trusted source).

Extract the folder and run GenSMBIOS.bat.

Select Option 3, then enter your model identifier.

Recommended Identifier:

MacBookPro15,2


(Best for macOS Catalina.)

For other macOS versions, check 👉 SMBIOS Support – Dortania Guide

(Follow only that page — don’t continue to the next.)

## 🔹 Step 2 — Modify the NVMe SSDT

Locate ssdt_nvme.aml inside the ACPI folder.

Decompile the file using your preferred method (e.g. iasl).

Replace my BIOS device name with your drive’s actual BIOS device name.

Recompile and save the file, then continue to Step 3.

Example snippet:

Device (NVME)
    Name (_ADR, 0x00170000)


Replace the device path as needed to match your system.

## 🔹 Step 3 — Edit config.plist

Download ProperTree
.

Download the EFI from the latest release
.

Open config.plist in ProperTree and edit it for your hardware.

Refer to the config.plist section of 👉 Dortania OpenCore Guide
.

If using my Offline Installer
:

Mount the EFI partition of your USB.

Copy the modified EFI folder to it.

If the EFI partition doesn’t appear, unplug and replug your USB.

Still missing? You likely missed a step in the Offline Installer guide.

Reboot, select your USB from the BIOS boot menu, and install macOS Catalina (or your chosen version).

# **✅ Installation Complete!**

🎉 Congratulations — you now have macOS running on a Samsung PM981 or PM981a SSD!
Keep in mind that these drives are unsupported, so performance may not be perfect — but it works! 💪

# 🙌 Credits

Huge thanks to everyone who made this project possible:

💻 OpenCore Team

📘 Dortania for their amazing OpenCore Install Guide

🧩 zacharysalvatore
 for the NVMe patch

🛠️ CorpNewt for ProperTree and GenSMBIOS

# 🍀 Good luck and happy Hackintoshing, my friends!

Would you like me to also add a top-level repository description + tags (for GitHub SEO) like:

EFI for running macOS on unsupported Samsung PM981 / PM981a NVMe SSDs using OpenCore. Experimental and slow, but works with Catalina.

It’ll help your repo appear in searches for “PM981 Hackintosh EFI” and similar terms.
