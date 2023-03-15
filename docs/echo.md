# Echo data server

Data collected at ToNI can be exported and archived on the Echo data server. Echo is also accessible for file transfers to personal and lab computers.

## Exporting to Echo from control computer
Currently, data export to Echo from the scanner control computer is a manual process. After each scan, make sure to export your data by following these steps:

1. Select the scan session from the participant search:
** image here **

2. Select the volumes you want to export (hold down shift or control when clicking to select multiple volumes):
** image here **

3. Click the export icon:
** image here **

4. In the export window, check that you selected the correct volumes which are listed in the left panel. It is also good practice to check the number of instances (i.e., the number of dicoms) and file size of the total export. Also, make sure the export path is set to `\\142.1.152.5\dicoms\buffer`.
** image here **

5. Finally, click the export button. As the dicoms are copied to Echo, a script will sort the incoming files into a directory for the scan session's study name (as defined in the participant ID for that session). The status of a running export can be viewed by clicking the CD icon in the bottom right system tray. This will open a window with export details and progress. Note: the CD icon is only available when an export is running. 

## Transferring from Echo 
Echo is accessible for data transfers via Secure FTP (sFTP). Users starting their first study will have an account created for them on Echo. The details for this account (i.e., username, temporary password, URL and port number) will be sent to the user. There are several methods for connecting to Echo's sFTP instance: 

### Terminal commands
Both macOS and Linux come with terminal commands for connecting to and transferring files from sFTP servers. For Windows, Powershell and and cygwin offer command line options for interacting with sFTP servers, however the syntax of specific commands may differ. The steps below describe typical terminal commands to use for macOS and Linux:

1. In a terminal, navigate to the location where you wish your files (or folder) to be downloaded.
2. Enter the following command: <br /> `sftp -P [PORT NUMBER] [YOUR USERID]@echo.toni.psych.utoronto.ca`
3. Enter your password when prompted
4. Change to the “DICOMS” folder: `cd DICOMS`
5. Each study has its own folder inside DICOMS. You will be able to see other study folder names but not their contents. You will only have the ability to see images in the folder related to your study. Navigate to the directory for your study: `cd [STUDY NAME]`
6. Enter the command: `get –r [folder]`
Where [folder] is the name of the new folders you wish to download, including subfolders and files (e.g. “000_20170229”). You may also use asterisk “*” as a wildcard.

### sFTP apps
There are several applications with graphical interfaces for connected to sFTP servers. Here are two examples:

* Windows: WinSCP - [https://winscp.net/eng/download.php](https://winscp.net/eng/download.php)
* macOS: CyberDuck - [https://cyberduck.io/](https://cyberduck.io/)

Each application is a little different, but all will offer the option of making a new connection (or adding a new server). Here's the information you will need to make the connection to Echo:

* File protocol: SFTP (or Secure FTP)
* Host name: echo.toni.psych.utoronto.ca
* Port number: The port number emailed to you when your account was created
* Username: Your username from the account creation email
* Password: Your password

Once this information has been entered, you should be able to log in to Echo. After logging in, navigate to your study's data directory by opening DICOMS and finding the directory with your study name. In these apps, you can copy folders and files from Echo to your computer with drag and drop actions. Depending on the app, you may be able to set up automatic data transfers, check your app's documentation. 


