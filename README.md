# Logitech-F710-Windows-driver
*An (unofficial and unapproved) unsigned Windows 10 driver that actually works with the Logitech F710 wireless controller*

Following the release of the Windows 10 May 2020 Update (2004), the driver for the Logitech F710 wireless controller can no longer be used. Although it can be installed, it does not survive a reboot. To date, Logitech have not provided a working signed replacement.

This page collates information from [here](https://answers.microsoft.com/en-us/windows/forum/windows_10-hardware/logitech-f710-on-windows-10-may-2020-update-2004/ec92ae61-24be-4a01-9905-d97b20d6d493), [here](https://www.reddit.com/r/Windows10/comments/hf5pre/logitech_f710_gamepad_wont_install_anymore_since/) and a file hosted on Google Drive into a single zip file which will install a modified XBox 360 driver which will work with Windows 10 and the Logitech F710. As soon as Logitech provide an official working and signed alternative driver then this content will be removed.

> :warning: **By following these instructions, you will be installing an unsigned driver which has been modified in unknown ways by an unknown third party.** This driver is not approved or endorsed by Logitech. You should be extremely clear on the risks of doing this before you start.

## Installation

1. Download the file from https://github.com/mrsilver76/Logitech-F710-Windows-driver/archive/main.zip and unzip it to somewhere easy to find
2. Ensure that the unifying receiver for the F710 is plugged into the computer, the F710 is on and the switch on the F710 is set to X (Xinput mode)
3. Verify that the device appears in Device Manager as **Wireless Gamepad F710** under **Other devices**
4. Select the start icon, then power and click on reboot whilst holding down the <kbd>Shift</kbd> key.
5. Select **Troubleshoot**
6. Select **Advanced options**
7. Select **Startup Settings**
8. Select **Restart** to restart the computer into the Startup Settings screen
9. Once the Startup Settings screen appears, press **7** to disable driver signature enforcement
10. Allow Windows to boot normally and log in
11. Launch Device Manager
12. Right click on the F710 entry and select **Update driver**
13. Click on **Browse my computer for drivers** 
14. Point Windows to the folder you created in step #1, your drivers should be installed
15. Double-click on `Install.reg` and confirm that you want to modify the registry
16. Verify that the F710 is now listed under **Xbox Peripherals** and is correctly identified as the F710
17. Reboot Windows to re-enable driver signature enforcement
18. Launch Device Manager and verify that nothing has changed

Congratulations, you now have a working Logitech F710 wireless controller with Windows 10.

:black_nib: Think you can improve on these instuctions? Submit a pull request!
