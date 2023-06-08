### [Simplified Chinese](/README.md) | [Traditional Chinese (Chinese Taipei)](/README_TP.md) | ENGLISH (U R HERE)
### *Translated by DeepL. If there are problems with translation, or you want to add other languages, use pull requests!*
### *If you have any problem, you can use issues!*
##### If you are a lazy guy, you can download the already made sigpatches directly from [Release](https://github.com/feiyangjun-1/ns-sigpatches/releases/latest).
#### Note: The final sigpatches generated following this tutorial will only work with your chosen system firmware version and atmospheric version and are not up or down compatible.

# What do you need to prepare?
* The latest version of [IPS Patch Creator](https://github.com/mrdude2478/IPS_Patch_Creator/releases/latest)
* [`Lockpick_RCM.bin`](https://codeberg.org/attachments/466940a5-9bcb-42db-a0de-1038b2a132ad) (this is a backup, [original repository](https://github.com/shchmue/Lockpick_RCM) has been taken down because of the DMCA takedown notice).
* Download the system firmware of the device you are currently using. It can be found at [Darthsternie's Firmware Archive](https://darthsternie.net/switch-firmwares/) or [THZoria/NX_Firmware](https://github.com/THZoria/NX_Firmware/releases) for download.
* Download the version of [Atmosphere](https://github.com/Atmosphere-NX/Atmosphere/releases) that you need to use.

# Step 1 - Extracting the keys
1. Boot your device in RCM mode and inject `Lockpick_RCM.bin`.

2. Press the volume keys to select *Dump from EmuNAND*. Press the power button to confirm.
   * If you don't have EmuMMC (EmuNAND), select *Dump from SysNAND*
3. Wait for a moment and when the export is complete, press the Power button to exit and select Shutdown (you can also select other options as appropriate). 
4. Remove the SD card and use the computer to read it. Open the `prod.keys` file in the `/switch/` folder in the root directory of the SD card using Notepad (or other software).
5. Create a folder named Firmware in the extracted folder and extract all the files from the downloaded system firmware package to the `/Firmware/` folder. 
6. Open the `/tools/` folder in the IPS Patch Creator folder and fill in the `keys.dat` file with the data from `prod.keys`.

# Step 2 - Generate signature patches (sigpatches)
1. Unzip the downloaded atmospheric zip package in the IPS Patch Creator folder.
2. Open `IPS_Patch_Creator.exe`. In the Loader tab under IPS Creator, click *Make Patch* below the text box. In the pop-up dialog box, select the `package3` file in the `/atmosphere/` folder of the unpacked atmosphere and Open. 
3. Switch to the ES tab and click *Make Patch*. In the pop-up dialog box, select the `/Firmware/` folder in the IPS Patch Creator folder and click OK.
4. Switch to the ES2 tab and click *Make Patch*. In the pop-up dialog box, select the `/Firmware/` folder in the IPS Patch Creator folder and click OK.
5. Switch to the FS tab and click *Make Patch*. In the pop-up dialog box, select the `/Firmware/` folder in the IPS Patch Creator folder and click OK.
6. Switch to the NFIM tab and click *Make Patch*. In the pop-up dialog box, select the `/Firmware/` folder in the IPS Patch Creator folder and click OK.

# Step 3 - Finish
1. Copy the `atmosphere` and `bootloader` two folders from the IPS Patch Creator folder to the root directory of the SD card.
    * If prompted for the same files, select Overwrite.
2. Enjoy!
