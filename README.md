# Logitech-F710-Windows-driver

<p><img src="https://img.shields.io/badge/Windows-supported-0078D6?logo=windows&logoColor=white" alt="Windows"></p>

*An unofficial, unsigned driver for Windows 10 or 11 that allows the Logitech F710 wireless controller to function in XInput mode*

Following a change to Windows back in May 2020, the XBox 360 driver for the Logitech F710 wireless controller (in XInput mode) no longer works reliably with Windows 10 or Windows 11. Although it can be installed, it does not survive a reboot with the error message "*Device not migrated*". To date, neither Microsoft or Logitech have offered a solution for either version of Windows.

I am not the author. This page simply collates information from [here](https://answers.microsoft.com/en-us/windows/forum/windows_10-hardware/logitech-f710-on-windows-10-may-2020-update-2004/ec92ae61-24be-4a01-9905-d97b20d6d493), [here](https://www.reddit.com/r/Windows10/comments/hf5pre/logitech_f710_gamepad_wont_install_anymore_since/) and a file hosted on Google Drive into a single zip file which installs a modified XBox 360 driver that works with Windows 10/11 and the Logitech F710. As soon as Microsoft or Logitech provide an official solution that continues to work after a reboot, this content will be removed.

## Alternative workarounds

I've been advised that it is still possible to use the stock driver supplied with Windows to operate the Logitech F710. Although a yellow exclamation mark is displayed in Device Manager, the controller can often be revived by switching briefly into DirectInput (D mode), then back to XInput (X mode), and pressing a button to wake it. In some cases this fails, in which case unplugging and re-inserting the USB receiver may be required.

I have not personally tested this workaround. If you are prepared to put up with the inconvenience, it will be a safer option than installing an unofficial driver. By contrast, the modified driver avoids these extra steps.

## Installation

> [!WARNING]
>  **By following these instructions, you will be installing an unsigned driver which has been modified in unknown ways by an unknown third party.** This driver is not approved or endorsed by Logitech. You should be absolutely clear on the risks before proceeding.

1. Download the file from https://github.com/mrsilver76/Logitech-F710-Windows-driver/archive/main.zip and unzip it to somewhere easy to find.
2. Ensure that the unifying receiver for the F710 is plugged into the computer, the F710 is on and the switch on the F710 is set to X (Xinput mode).
3. Verify that the device appears in Device Manager as **Wireless Gamepad F710** under **Other devices**.
4. Select the Start icon, then **Power** and click **Reboot** while holding down the <kbd>Shift</kbd> key.
5. Select **Troubleshoot**.
6. Select **Advanced options**.
7. Select **Startup Settings**.
8. Select **Restart** to restart the computer into the Startup Settings screen.
9. Once the Startup Settings screen appears, select the option to disable driver signature enforcement.
10. Allow Windows to boot normally and log in.
11. Launch Device Manager.
12. Right click on the F710 entry and select **Update driver**.
13. Click on **Browse my computer for drivers**.
14. Point Windows to the folder you created in step #1 and your drivers should begin installing. If a warning appears about the unsigned driver, select **Install this driver anyway**.
15. One the driver is installed, double-click on `Install.reg` and confirm that you want to modify the registry.
16. Verify that the F710 is now listed under **Xbox Peripherals** and is correctly identified as the F710.
17. Reboot Windows to re-enable driver signature enforcement.
18. Launch Device Manager and verify that nothing has changed.

Congratulations, you now have a working Logitech F710 wireless controller with Windows.

:black_nib: Think you can improve these instuctions? Raise an issue or submit a pull request!

## Changelog

2025-09-11
* Added "Alternative workarounds" section describing use of the stock Windows driver.
* Minor wording and formatting tweaks for clarity and tone consistency. 

2024-10-29
* Reformatted warning message to use Github "warning" icon.

2024-07-04
* Confirmed these instructions work for Windows 11 and updated description accordingly.
* Corrected instructions when accessing startup settings.
* Added additional instructions if a pop-up warning appears prior to driver installation.

2021-06-07
* Initial version.
