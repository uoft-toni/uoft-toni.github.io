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

4. In the export window, check that you selected the correct volumes which are listed in the left panel. It is also good practice to check the number of instances (i.e., the number of dicoms) and file size of the total export. Also, make sure the export path is set to `//142.1.152.5/dicoms/buffer`.

** image here **

5. Finally, click the export button. As the dicoms are copied to Echo, a script will sort the incoming files into a directory for the scan session's study name (as defined in the participant ID for that session).
