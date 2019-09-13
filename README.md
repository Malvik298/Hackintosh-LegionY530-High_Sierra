# Hackintosh-LegionY530-HighSierra

### NOTE : I AM NOT RESPONSIBLE FOR ANY DAMAGES DONE TO YOUR COMPUTER. YOU SHOULD KNOW WHAT YOU ARE DOING, AND YOU SHOULD KNOW HOW TO RECOVER FROM ANY PROBLEMS. DO IT AT YOUR OWN RISK.

#### Hardware 

|                 |             Hardware             |                 HighSierra Compatibility                  |
| :-------------: | :------------------------------: | :-------------------------------------------------------: |
|       CPU       |          Intel i5-8300H          | Works perfectly base clock 2.4 Ghz and boost upto 4.00Ghz |
|      dGPU       |         Nvidia GTX1050Ti         |                  Disabled in High Sierra                  |
|       GPU       | Intel UHD Graphics 630 (1536MB)  |                         No issues                         |
|     Storage     |   SSD : Toshiba 120Gb PCIe M.2   |                         No issues                         |
|     Screen      | 15.6" Full HD@60Hz,1920x1080 IPS |                         No issues                         |
|      WiFI       |      Intel Wireless-AC 9560      |                       Incompatible                        |
|    Touchpad     |     I2C HID Touchpad (TPD0)      |                        Not Working                        |
|       USB       |          USB 3.1 Gen1x3          |                         No issues                         |
|                 |         Type-C 3.1 Gen1          |                         No issues                         |
| HDMI and MiniDP | Not Working due to disabled dGPU |                      Nvidia disabled                      |
|     Battery     |             52.3 Wh              |                 2-3 hours battery Backup                  |

### Steps to get High Sierra working

1. Create a Clover Bootable USB drive.
2. Copy the above three folders to the Bootable USB drive and replace them.
3. Boot via USB drive and select your High Sierra drive.
4. Download the Clover Configurator.
5. Mount the EFI partition of the Bootable USB.
6. Copy the contents to the EFI partition of the System.
7. Reboot the system and boot again from the USB.
8. Select **Clover Boot Options**, and then **Add Clover Boot Entries** , now you have the Clover in your system and set it default from the BIOS menu.

#### After getting the working clover :

1. Open Clover Configurator.
2. Mount the EFI partition.
3. Navigate to config.plist in the clover folder.
4. Open it in clover configurator.
5. navigate to SMBIOS section.
6. Generate a new serial key and check for its coverage.
7. **YOU SHOULD NOT USE A VALID SERIAL KEY.**

#### What's Working : 

- Brightness control (Use Fn+P and Fn+K, Key mapping can be changed)
- Intel UHD Graphics (1536Mb) -Two Fan Speed (Default and Max) 
- All USB 3.1 and type-C (basic USB Functions)
- And other Basic Functionality
- TrackPad Detected and Working

#### Not able to get working touchpad ?
 1. If you are on the same BIOS as me then enter BIOS.
 2. Press Fn+Tab, Fn+asdfgh and then Fn+O and then save changes and reboot. Press F2 when you see a Blue Box.
 3. Enter Advance BIOS Menu and go to ACPI Menu.
 4. Set it to Auto configuration.
 5. Find Toucpad Delay Option in the IO settings and set the delay to 0 from 68.
 6. Save the changes and Reboot.
 7. Delete AppleHPM.kext, AppleIntelLpssI2C.kext, AppleIntelLpssI2CController.kext from Extensions Folder
 8. Reboot the OS

#### What's Not Working:

- Wifi and Bluetooth
- ~~Trackpad (Still working on it) ~~
- Facetime,iMessages due to no valid serial key
- Numpad
- Unable to use type-C to hdmi convertor

#### ToDo

- ~~I2C Touchpad~~
- ~~Brightness Control~~
- ~~Sound~~
- Fix Black Screen when laptop sleeps

#### Credits

[InsanelyMac](insanelymac.com)

[RehabMan](https://github.com/RehabMan)

[MaLd0n](https://www.insanelymac.com/forum/profile/557433-mald0n/)

[Olarila.com](olarila.com)
