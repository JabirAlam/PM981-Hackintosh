# PM981-Hackintosh
macOS EFI for any PC using PM981a/PM981 (you'll have to customize the EFI to make it compatible with your PC.)

⚠️ Caution: This Project is in development release. The EFI may be unstable in some PC's. As PM981 and PM981a are not supported in macOS. I patched the EFI. Please make sure you DONT delete any of the kexts.
Please Backup your data. Please do NOT use MacOS Tahoe Beta, as that is unsupported, it wont work with the PM981, i recommend using macOS Catalina or macOS Big Sur for this EFI.

⚠️ Mandatory Disclaimer
By continuing, you acknowledge that you have read and understood the contents of the following disclaimer, and consent to their terms.

The process described in this document could cause irreversible damage to your laptop, and you should prepare yourself for that outcome before you begin. I accept absolutely no responsibility for the consequences of anyone choosing to follow or ignore any of the instructions in this document, and make no guarantees about the quality or effectiveness of the software in this repo.



Requirements:

A already hackintoshed system on a Supported SSD (if you have only one SSD, You can try to direct install, but you'll need to add RestrictEvents.)

You'll have to follow this https://github.com/tylernguyen/x1c6-hackintosh/issues/43 guide, or follow my guide here if you DONT have a macOS installation and only have 1 SSD.


Guide:


Step 1.

first. you have to get a SMBIOS, for that, use GenSMBIOS, download it, install python from the Microsoft Store or other places. and run the .bat file after extracting the GenSMBIOS folder, choose option 3,
then type your Model Identifier. I recommend MacBookPro15,2. but if your using another version instead of Catalina, then to find that, follow this guide https://dortania.github.io/OpenCore-Install-Guide/extras/smbios-support.html#macbook. FOLLOW ONLY THAT PAGE, DONT GO TO THE NEXT PAGE.

Step 2.

Now get Propertree and open the config.plist file of the EFI from the releases page. Download the EFI if not already https://github.com/JabirAlam/PM981-Hackintosh/releases/tag/v1.0.0, then use propertree to customize to your PC's liking. 

You can now try to boot from the EFI if you used a offline installer. if you didnt, follow this guide: https://github.com/JabirAlam/Offline-Installer. if you are using another version, go to the community.

then put the EFI we edited to the "EFI" partition of the USB drive, if no EFI partition is shown, unplug the USB drive and replug it, IF its still NOT SHOWING, you didnt follow the offline installer guide then.

boot from the USB drive after adjusting BIOS settings and Install macOS Catalina (or what version you choosed)

Done!


Credits:

---------------------------------------------------

OpenCore Team,

Dortania OpenCore Install Guide,

https://github.com/zacharysalvatore for the Patch,

Corpnewt for ProperTree and GenSMBIOS.

-----------------------------------------------------

Good luck hackintoshing!
