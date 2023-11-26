# Palladium OS 4.0 Flashing Instructions for Munch

## Prerequisites (Important):

1. Ensure the bootloader is unlocked.
2. The ROM uses Stock MIUI Vendor and Atom kernel based on Stock Perf kernel.
3. Flash the 14.0.6.0 firmware of your region before flashing the ROM.
4. The phone must be connected to your laptop, and adb must be enabled.
5. Clean flash is mandatory.

## Steps:

1. **Download the following Files:**
   - ROM => [PalladiumOS-4.0-munch-OFFICIAL-GAPPS-0605-20231126.zip](https://palladiumos.org/download)
   - Recovery => [PalladiumOS-4.0-munch-OFFICIAL-GAPPS-0605-20231126.img](https://palladiumos.org/download)

2. **Run the following ADB Commands:**
   - Connect your phone to the laptop.
   - Open a terminal and run the following commands:

     ```bash
     adb reboot bootloader
     fastboot flash boot <DownloadPath>/PalladiumOS-4.0-munch-OFFICIAL-GAPPS-0605-20231126.img
     fastboot reboot recovery
     ```

3. **Install Update via ADB Sideload:**
   - In the recovery menu, select "Install Update" and choose "adb sideload."
   - Run the following command:

     ```bash
     adb sideload <DownloadPath>/PalladiumOS-4.0-munch-OFFICIAL-GAPPS-0605-20231126.zip
     ```

4. **Factory Reset:**
   - After flashing in the recovery, select "Factory Reset" and choose "Format data/factory reset."

5. **Reboot:**
   - Press the back button and select "Reboot to system."

**Note:** Replace `<DownloadPath>` with the actual path where you downloaded the Palladium OS files.

Ensure that you follow these steps carefully and double-check the prerequisites before proceeding with the flashing process.
