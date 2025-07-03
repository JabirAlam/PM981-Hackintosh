# PM981-Hackintosh
macOS EFI for any PC using PM981a/PM981 (you'll have to customize the EFI to make it compatible with your PC.)

⚠️ Caution: This Project is in development release. The EFI may be unstable in some PC's. As PM981 and PM981a are not supported in macOS. I patched the EFI. Please make sure you DONT delete any of the kexts.
Please Backup your data. Please do NOT use MacOS Tahoe Beta, as that is unsupported, it wont work with the PM981, i recommend using macOS Catalina or macOS Big Sur for this EFI.


Requirements:

A already hackintoshed system on a Supported SSD (if you have only one SSD, You can try to direct install, but you'll need to add RestrictEvents.)

You'll have to follow this https://github.com/tylernguyen/x1c6-hackintosh/issues/43 guide, or follow my guide here if you DONT have a macOS installation.


Guide:


Step 1.

first. you have to get a SMBIOS, for that, use GenSMBIOS, download it, install python from the Microsoft Store or other places. and run the .bat file after extracting the GenSMBIOS folder, choose option 3,
then type your Model Identifier. I recommend MacBookPro15,2. but if your using another version instead of Catalina, then to find that, follow this guide https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#macbook. FOLLOW ONLY THAT PAGE, DONT GO TO THE NEXT PAGE.

Step 2.

Now get Propertree and open the config.plist file of the EFI from the releases page. Download the EFI if not already https://github.com/JabirAlam/PM981-Hackintosh/releases/tag/v1.0.0, then use propertree to customize to your PC's liking. 

You can now try to boot from the EFI if you used macrecovery.py. if you didnt, then use this guide. https://dortania.github.io/OpenCore-Install-Guide/installer-guide/windows-install.html#making-the-installer, FOLLOW only THAT PAGE, DONT go to the NEXT PAGE.

Install macOS Catalina (or what version you choosed).

Done!
