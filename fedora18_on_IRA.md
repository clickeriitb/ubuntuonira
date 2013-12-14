Another method of running Linux on IRA laptop is as follows:


Step 1) Dowload the Fedora 18 image from the below mentioned url:

        http://http://scotland.proximity.on.ca/contrib-images/hansg/
        
        Note: Download the "Fedora-18-a10-armhfp-r1.img.xz" image

Step 2) save it on desktop and then, insert an sdcard into an SD card reader that is attached to usb port of the computer.

Step 3) Write the image file to the card, ie as root do:

        xzcat Fedora-18-a10-armhfp-r1.img.xz > /dev/mmcblk0 [PRESS ENTER]
        sync [PRESS ENTER]
        
Step 4) Remove the card, and re-insert it. The uboot partition should get automatically mounted.

Step 6) type:

        sudo sh /run/media/ashish/uboot/select-board.sh [PRESS ENTER]
        
        
        Note: 
        a)ashish is the name of partiton on SD card. It could be different at your end.
        
        b)select "A13_mid" amongst the boards which are being listed.
        
    
Step 7) umount the uboot partition, ie type:

        umount /run/media/ashish/uboot [PRESS ENTER]
        
Step 8) Your sdcard is now ready for use.

Step 9) Insert the SD Card in the SD card slot of IRA Laptop.

Step 10) power on the device.

Step 11) While booting fedora may reboot or go blank for some couple of minutes only for the first time while configuring.

Step 12) A screen shall appear asking for creating a "New" user along with password.

Done!!
