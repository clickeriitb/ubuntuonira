Steps to get inside ubuntu terminal
-----------------------------------

Step 1) put sdcard (8Gb) inside the sdcard reader

Step 2) put the card reader into usb port of your computer

Step 3) to download "ubuntu.zip" visit [here] and click on "CLICK HERE to Download".

Step 4) save the file on desktop

Step 5) open the terminal and type:

	      cd ~/Desktop (press ENTER)

	      unzip ubuntu.zip (press ENTER)

Note: A folder named ubuntu shall appear on Desktop.

Step 6) copy the “ubuntu” folder in sd card

	      cp  -dpR ubuntu /media/boot (press ENTER)

Note: Here, boot is the name of my sdcard. The name of your sdcard could be something like an alpha-numeric number like c7e9b0a1-6bb5-2246. 

Step 7) after ubuntu folder has been copied, umount the sdcard

	      sudo umount /media/boot (press ENTER)

Step 8) power on the cubieboard

Step 9) insert the SDcard into IRA Laptop sdcard slot

Step 10) power on the Laptop

Step 11) click on web browser and type:

          https://play.google.com/store/apps?hl=en
          
Step 12) click on Sign in and enter your gmail account and password and type:    

          https://play.google.com/store/apps/details?id=com.zpwebsites.linuxonandroid
        
Step 13) click on Install button then, Accept. It will be installed.

Step 14) On the browser type:

          https://play.google.com/store/apps/details?id=android.androidVNC
          
Step 15) click on Install button then, Accept. It will be installed.

Step 16) On laptop click on "menu" option and click on Complete Linux Installer icon

Step 17) click on "launch" button.

Step 18) Select "Settings" option go to "Edit" and select the path of external SD card slot where ubuntu image is being copied. 

Step 19) click on "Save Changes" and then, click on "Start Linux" button

Step 20) If you see something like this on the terminal of your laptop:

root@localhost:/#

Then, congratulations !!! you are now running Ubuntu on your device!!

Step 21) type:

          sudo apt-get update [PRESS ENTER]
          
Now, you are ready to install any package within Ubuntu.

[here]: http://mirror22.downloadandroidrom.com/download/AndroidUbuntu/ubuntu.zip?token=841322312
