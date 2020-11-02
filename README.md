# OneNote-2016-64bit-Setup
How to setup properly OneNote2016 (64bit) in the era of Windows deciding for you which version of Office you should install

## 1st Step: Proper Download & Install

* Download the 64bit version of OneNote from this site: <a href="https://www.techspot.com/downloads/5164-microsoft-onenote.html" target="_blank">techspot.com</a> 
* Install from the file the OneNote version (32 bit/64 bit) you chose

## 2nd Step: Update for applying your system's default language

* Open the freshly installed OneNote 2016
* In the top left of the ribbon click on "File"
* In the bottom left of the newly opened page click on "Account"
* In the center of the "Account Page" click on "Update Options" and then on "Update Now"

## 3rd Step: Try it Out and fix in case of the mshwLatin.dll Error

* Try to write with a pen input (Wacom and similar) for a bit
* If the app works fine, **you're done**, otherwise follow the other points
* Open "Event Viewer" from the Windows Menu (Windows key -> Windows Administrative Tools -> Event Viewer)
* Click on the "Windows Log" Folder, then on "Application"
* Select the most recent Error, in the general description in the middle bottom windows there must be ONENOTE.exe as cause of the error
* If the error is generated because of the module "mshwLatin.dll" scroll the general description to the part where you can see the  mshwLatin.dll path, copy it, open any folder and paste it in the top bar (should be somthing like "_C:\Program Files\Common Files\microsoft shared\ink_")
* Download the right .dll file from this site: <a href="https://www.dll.website/mshwlatin-dll" target="_blank">dll.website</a> 

## Fix Step: Change User Permissions over folder and file

* Navigate a folder up (in the previous example path was "_ink_")
* Right Click on that same folder
* Properties -> Security -> Advanced 
* In the new Window "Change" Owner to your User (your Windows Account email) and close the Window
* Now, back in the Properties -> Security windows, click on Modify
* Select Administrator from "Users & Groups" tab and then click on the "Complete Control" Allow tickbox
* Apply changes, close Properties and enter again the folder you just became owner of
* Repeat the same procedure right clicking on the broken .dll file and once you became owner of it delete it
* Now just drag and drop the healthy .dll file you downloaded before and restart the computer
* **You're done! Enjoy your favourite OneNote 2016 version!**
