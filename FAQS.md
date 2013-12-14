Frequently Asked Questions
==========================


Q1) I am getting an error unzip command not found while executing this command. What to do?

    unzip ubuntu.zip (press enter)

    Solution
    --------

    sudo apt-get install unzip (press Enter)
    
Q2) After entering inside the terminal of Complete linux installer,I got the following error:

    mknod /dev/block/loop1 
    error: you must be root

    losetup /dev/block/loop1 error: operation not permitted

    mount -t devpts devpts $mnt/dev/pts
    error: /dev/pts no such file or directory
    
    How to resolve this error?

    Solution
    --------
    
    Option 1) 
    
    mknod /dev/block/loop1 b 7 1 (press Enter)

    losetup /dev/block/loop1 /mnt/extsd/ubuntu/ubuntu.img (press Enter)

    mount -t ext2 /dev/block/loop1 /data/local/ubuntu (press Enter)

    mount -t devpts devpts $mnt/dev/pts (press Enter)

    mount -t proc proc $mnt/proc (press Enter)

    mount -t sysfs sysfs $mnt/sys (press Enter)

    sysctl -w net.ipv4.ip_forward=1 (press Enter)

    echo "nameserver 8.8.8.8" > $mnt/etc/resolv.conf (press Enter)

    echo "nameserver 8.8.4.4" >> $mnt/etc/resolv.conf (press Enter)

    echo "127.0.0.1 localhost" > $mnt/etc/hosts (press Enter)

    chroot $mnt /bin/bash

    Note: At stage if you see

    root@localhost:/#

    then, you are now inside ubuntu on your device !!!

    Option 2)
    
    REBOOT the laptop and repeat continue from step 19 onwards of "running_ubuntu_inside_android.md" file
