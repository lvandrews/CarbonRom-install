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
Allow all apps to automatically install first (this will take time). Meanwhile, you can fine tune your customizations (for me, wallpaper was the same as was home screen configuration and widgets) and check your access to your network with the info you scribbled down in step 1 (my network was intact, but I did have to select the correct APN). When everything is settled down, update TWRP and reboot system.  Check Magisck through the Magisck Manager app that it is the latest version.   

**Step 7: Restore your messages and contacts with SuperBackup**  
Here's where I ran into problems. Some of the files on my SD card have a zero byte file size. This includes my backups I made just before the installation. The last time google updated my information was months ago so now I have a bunch of old conversations in my messages app. Tried reflashing the ROM over over everything which worked fine, but file size issue is unresolved. Also discovered the camera app will not start. This is worse than it was before where I could at least take pictures (but not video).  

**Step 8: Fix silly problems**  
It occurred to me that there may be differences in the way that Android 9 and 8.1 address the SD card. If I switched off the phone and inserted the SD card into my Linux computer, the files appeared to be just fine. On my Windows computer, same problem as with Android 9. Using my Linux system, I backed up all the files from the SD card, then formatted the card to FAT32. Then I inserted the card back into the phone and let Android format it, then switched phone off and swapped the card back to the computer to copy the files back over. Upon reinserting the card, all files were present *and* accessible so I was able to restore messages and contacts. For the camera problem I installed the Moto Camera app from the Play Store and disabled the stock camera. Tested camera and video function and both work correctly. Hotspot acts like its working and I can connect with my computer, but data actually gets to my computer. I still haven't done the rooting on the newest install and frankly not sure it is necessary or if it would cause nay new problems. Already started logging back into apps, syncing my music from the cloud and connecting to various devices so I'm inclined to use it as is for a while and see how things go. Hello Android 9!

**DONE!!**  
