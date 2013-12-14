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
    
Q3) I got the following errors after typing:

    apt-get update

    Err http://ports.ubuntu.com karmic/main Packages
    404 Not Found

    Err http://ports.ubuntu.com karmic/universe Packages 
    404 Not Found

    W: Failed to fetch http://ports.ubuntu.com/ubuntu-ports/dists/karmic/main/binary-armel/Packages.gz 404 Not Found

    W: Failed to fetch http://ports.ubuntu.com/ubuntu-ports/dists/karmic/universe/binary-armel/Packages.gz 404 Not Found

    E: Some index files failed to download, they have been ignored, or old ones used instead.

   What should I resolve this error?

    Solution
    --------

    cat > /etc/apt/sources.list (press enter)

    deb http://old-releases.ubuntu.com/ubuntu/ karmic main universe

    Then hit Ctrl+D twice and Enter.

    apt-get update (press enter)

    This will update the Ubuntu sources.


Q4) I got the following error:

    android-vcn error: connection refused unable to connect

    Solution
    --------

    change to Port: 5900 instead of 5901 and click on connect button.
