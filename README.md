# CbusShare
A Windows Desktop based application to share a CBUS serial port with multiple networked CBUS utilities.

Runs in the background as a Notification Area (aka System Tray) application:
* Connects to a serial COM port attached to a MERG CANUSB interface module.
* Accepts network connections (TCP/IP, usually port 5550).
* Mirrors all data from each connection to all other connections.

Compatible applications which support network CBUS connections include the FLiM Configuration Utility (FCU), [LayoutMesh](https://github.com/Syspixie/LayoutMesh), and JMRI.

## Installation
The application does not have its own installer.  The installation process is simply to download a zip file, and extract its contents to a suitable directory.  Shortcuts to the program may be created on the desktop, the taskbar, or anywhere else that makes sense.

CbusShare requires '.NET Desktop Runtime 8.0' to be installed on your computer.  If this is not found when you run the application for the first time, a message box will appear providing a link to download .NET from Microsoft.  Clicking on the 'Download it now' link will download the .NET installer; double-clicking on the installer installs .NET - this is a very quick and simple operation, not requiring a reboot.

* Go to the release page on GitHub: https://github.com/Syspixie/CbusShare/releases.
* Click on the release required, e.g. 'v1.0.0'.
* Click on the specific zip file, e.g. 'CbusShare-1.0.0-win-x64.zip', to download it.
* Navigate to your download directory, and double-click the zip file.
* Extract the program to your chosen install directory.

#### Initial Setup
Make sure your CANUSB module is powered on and attached to the computer.

* Navigate to the install directory.
* Double-click the 'CbusShare.exe' file to run the application. The yellow CbusShare icon should appear in the Notification Area of the Taskbar. As it has not yet been configured, the Settings dialog will also be displayed.
* In the Settings dialog, enter the COM Port name associated with the CANUSB (e.g. COM2). Leave the Network Port number as 5550 (unless this conflicts with another app). Select the Auto Start option (unless you need CbusShare to remain stopped until manually stated).
* Click 'Start'; the status should change from 'Stopped' to 'Online: 0 connections'. You may now close the dialog box - CbusShare will remain running in the background.

#### Starting CbusShare on login.
There are many ways to have an application start up automatically. The simplest way to start CbusShare when the currently logged in user subsequently logs in (requires no privileges) is:

* Press the 'Windows + R' keys to display the 'Run' utility.
* Enter 'shell:startup' (without the quotes) and press the 'Enter' key. This will launch File Explorer with the startup folder open.
* Create a shortcut to CbusShare.exe in this folder. 
