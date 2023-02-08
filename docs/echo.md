# Echo data server

Data collected at ToNI can be exported and archived on the Echo data server. 

## Exporting to Echo from control computer
To export the dicoms from a scan session, select the scan session from the participant search:

** image here **

Select the volumes you want to export (hold down shift or control when clicking to select multiple volumes):

** image here **

Click the export icon:

** image here **

In the export window, check that you selected the correct volumes which are listed in the left panel. It is also good practice to check the number of instances (i.e., the number of dicoms) and file size of the total export. Also, make sure the export path is set to `//142.1.152.5/dicoms/buffer`.

** image here **

Finally, click the export button. As the dicoms are copied to Echo, a script will sort the incoming files into a directory for the scan session's study name (as defined in the participant ID for that session).
