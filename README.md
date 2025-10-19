🚀 PM981-Hackintosh

EFI for macOS on systems using Samsung PM981 or PM981a SSDs
(You’ll need to customize this EFI to match your hardware.)

⚠️ Caution

This project is currently in development — it may be unstable on certain PCs since PM981/PM981a SSDs are not officially supported on macOS.

🧠 Important Notes:

❌ Do not delete any kexts included in this EFI.

💾 Back up your data before you begin.

🚫 Do not use macOS Tahoe Beta — it’s unsupported and won’t work with PM981 drives.

✅ Recommended macOS version: Catalina for best results.

⚖️ Disclaimer

By continuing, you acknowledge that you’ve read and understood the following disclaimer and agree to its terms.

⚠️ The process described here can potentially cause irreversible damage to your device.
I take no responsibility for any hardware damage, data loss, or software issues that may result.
This EFI is provided as-is, with no guarantees of stability or compatibility.

🧩 Requirements

🖥️ A working Hackintosh system with a supported SSD.

If you only have one SSD, you can attempt a direct installation — but make sure to include RestrictEvents.kext.

🧭 Follow either tylernguyen/x1c6-hackintosh#43

or my guide (below) if you don’t already have macOS installed.

⏳ Patience — installing macOS on a PM981 can take 3+ hours.

If it says “Less than a minute remaining,” it’s not stuck — it’s just very slow because of NVMe patches.

🧰 Installation Guide
🔹 Step 1 — Generate an SMBIOS

Download GenSMBIOS
.

Install Python (from the Microsoft Store or another trusted source).

Extract the folder and run GenSMBIOS.bat.

Select Option 3, then type your model identifier.

Recommended:

MacBookPro15,2


(Best for macOS Catalina)

For other macOS versions, check:
👉 SMBIOS Support – Dortania Guide

(Follow only that page — don’t continue to the next one.)

🔹 Step 2 — Modify the NVMe SSDT

Locate ssdt_nvme.aml inside the ACPI folder.

Decompile it using your preferred method (e.g., iasl).

Replace my BIOS Device Name with your drive’s actual BIOS device name.

Recompile and save it, then move on to Step 3.

Example (inside your DSDT/ACPI path):

Device (NVME)
    Name (_ADR, 0x00170000)


Replace the device path accordingly.

🔹 Step 3 — Edit config.plist

Download ProperTree
.

Get the EFI from the latest release
.

Open config.plist in ProperTree and edit it for your hardware.

Reference the config.plist section of the
👉 Dortania OpenCore Guide
.

If using my Offline Installer
:

Mount the EFI partition of your USB.

Copy the modified EFI folder to it.

If you can’t see the EFI partition, unplug and replug your USB.

If it’s still missing, you may have missed a step in the Offline Installer guide.

Reboot, select your USB from BIOS, and install macOS Catalina (or your preferred version).

✅ Installation Complete!

🎉 Congratulations! You now have macOS running on a Samsung PM981 / PM981a SSD.
Expect slower performance compared to supported drives — but it works!

🙌 Credits

Big thanks to everyone who made this possible:

OpenCore Team

Dortania for their detailed OpenCore Install Guide

zacharysalvatore for the NVMe patch

CorpNewt for ProperTree & GenSMBIOS

🍀 Good luck and happy Hackintoshing, my friends!
