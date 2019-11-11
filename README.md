# CarbonRom-install
Updating CarbonRom on my Motorolla Moto G5 Plus from CR 6.1 (Android 8.1) to CR 7.0 (Android 9). Phone is acting funny, so this will be a complete wipe and clean install.


**Step 1: Take down access point information**  
This is important since your new install may be missing some crucial information that your phone needs to access the network you pay for. In my current CR installation, I go to "Settings" then "Network & Internet" then "Mobile Network". Expand "Advanced" and select "Access Point Names." Select the APN that is currently in use and copy down each setting. You may need this if your network needs to be added to your fresh install.  

**Step 2: Download necessary files**  
I am redoing the recovery and everything. I unlocked my bootloader a long time ago. Easy to do, google it and void your warranty as I did mine. Good decision!  

  1) CarbonRom. Device-specific, so make sure you get the right one! I am getting a Release file from Oct 30, 2019 for my Moto G5 Plus (potter). https://get.carbonrom.org/device-potter.html  
  2) GApps. I am getting Stock GApps for Android 9.0 with ARM64 architecture. https://opengapps.org/  
  3) TWRP. This is your recovery image. Also specific to your device so make sure you get the right one. https://dl.twrp.me/potter/  
  4) Magisck. For systemless root so you can keep using the Google stuff you love even though you hate it a little. https://forum.xda-developers.com/apps/magisk/official-magisk-v7-universal-systemless-t3473445, https://github.com/topjohnwu/Magisk/releases/ (get the zip).  
  5) Magisck Manager. App that helps manage your root access. https://github.com/topjohnwu/Magisk/releases/tag/manager-v7.4.0  
  6) no-verity-opt-encrypt. https://www.androidinfotech.com/no-verity-opt-encrypt-versions/  

Transfer all files to your SD card for your phone. I switch the phone off and physically insert the SD card from the phone into my computer for the transfer rather than do a USB transfer or download files directly to the phone.  

**Step 3: Backup your contacts and messages to your SD card with SuperBackup**  
I found this app useful enough to purchase and it does daily backups for me in the background and uploads to my Google Drive account for safekeeping. Also use your files app to dig through your storage and move anything you value to your external SD card before you begin. We will be wiping the phone. Meanwhile, ensure you have adequate battery (75% is good) and access to quality WiFi.

**Step 4: Unlock bootlader and root**  
Follow steps here: https://appuals.com/root-motorola-moto-g5-g5-plus/  

**Step 5: Wipe phone, then flash ROM and GApps**  
  1) Boot to recovery  
  2) Select "Wipe"  
  3) Select "Advanced wipe"  
  4) Select "Dalvik", "System", "Data", "Internal Storage" and "Cache"  
  5) Back out to main TWRP screen  
  6) Select "Install"  
  7) Install ROM  
  8) Install GApps  
  9) Just to be safe, install no-verity-opt-encrypt.zip, then Magisck.zip  
  10) Reboot system. My phone went to splash screen, then boot screen for a few seconds, then restarted again. Splash again, then boot screen for quite a while. Be patient! When phone finally wakes up, setup system.  

**Step 6: Install old apps and update important things like TWRP**  
Allow all apps to automatically install first (this will take time). Meanwhile, you can fine tune your customizations and check your access to your network with the info you scribbled down in step 1. When everything is settled down, update TWRP and reboot system.  Check Magisck through the Magisck Manager app that it is the latest version.   

**Step 7: Restore your messages and contacts with SuperBackup**  

**DONE!!**  
