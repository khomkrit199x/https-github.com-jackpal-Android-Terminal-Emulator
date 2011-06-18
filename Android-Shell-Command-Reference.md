#The Android Shell

A "shell" is a program that listens to keyboard input from a user and performs actions as directed by the user. Android devices come with a simple shell program. This shell program is mostly undocumented. Since many people are curious about it I thought I'd write up some documentation for it.

#Built in Commands

The Android shell will run any program it finds in its PATH. The PATH is a list of directories. You can find out what your shell's PATH is set to by using the built-in echo command:

    $ echo $PATH
    /data/local/bin:/sbin:/vendor/bin:/system/sbin:/system/bin:/system/xbin

Depending upon your shell, you may see a different result.

To find out what commands you have available to you, use the "ls" command on each of the directories in the PATH variable:

    $ ls /data/local/bin
    /data/local/bin: No such file or directory

Notice that by default there is no /data/local/bin directory. You can create this directory using the "mkdir" command if you like.

    $ ls /sbin
    opendir failed, Permission denied

The /sbin directory exists, but you don't have permission to access it. You need root access. If you have a developer phone, or otherwise have root access to your phone you can see what's in this directory.

    $ su
    # ls /sbin
    ueventd
    adbd
    # exit
    $ 

Notice that the shell prompt changes from a '$' to a '#' to indicate that you have root access.

Notice also that neither of the /sbin commands are useful to the shell -- the adb and ueventd files are 'daemon' programs used to implement the Android Debugger "adb" program that is used by developers.

    $ ls /vendor/bin
    gpsd
    pvrsrvinit

Vendor/bin is where device vendors can put device-specific executables. These files are from a Nexus S.

    $ ls /system/sbin
    /system/sbin: No such file or directory

This directory does not exist on a Nexus S.

    $ ls /system/bin
    am
    amix
    aplay
    app_process
    applypatch
    arec
    audioloop
    bluetoothd
    bmgr
    bootanimation
    brcm_patchram_plus
    bugreport
    cat
    chmod
    chown
    cmp
    dalvikvm
    date
    dbus-daemon
    dd
    debuggerd
    dexopt
    df
    dhcpcd
    dmesg
    dnsmasq
    dumpstate
    dumpsys
    dvz
    fsck_msdos
    gdbserver
    getevent
    getprop
    gzip
    hciattach
    hd
    id
    ifconfig
    iftop
    ime
    input
    insmod
    installd
    ioctl
    ionice
    iptables
    keystore
    keystore_cli
    kill
    linker
    ln
    log
    logcat
    logwrapper
    ls
    lsmod
    lsof
    make_ext4fs
    mediaserver
    mkdir
    monkey
    mount
    mtpd
    mv
    nandread
    ndc
    netcfg
    netd
    netstat
    newfs_msdos
    notify
    omx_tests
    pand
    ping
    pm
    pppd
    printenv
    ps
    qemu-props
    qemud
    racoon
    radiooptions
    reboot
    record
    renice
    rild
    rm
    rmdir
    rmmod
    route
    rtp_test
    run-as
    schedtest
    schedtop
    sdcard
    sdptool
    sendevent
    service
    servicemanager
    setconsole
    setprop
    setup_fs
    sh
    showlease
    sleep
    smd
    stagefright
    start
    stop
    surfaceflinger
    svc
    sync
    system_server
    tc
    testid3
    toolbox
    top
    umount
    uptime
    vdc
    vmstat
    vold
    watchprops
    wipe
    wpa_cli
    wpa_supplicant
    $ ls /system/xbin
    add-property-tag
    btool
    check-lost+found
    dexdump
    dhdutil
    hcidump
    latencytop
    librank
    opcontrol
    oprofiled
    procmem
    procrank
    rawbu
    scp
    showmap
    showslab
    sqlite3
    strace
    su


#Versions of the Android Shell

- Android 1.0 used a shell that had no tab completion or history editing.
- Android 2.3 added history editing. You can for example use the up/down arrows to edit previous commands.

#Other shells

#Busybox

Busybox is a program that contains a shell and a set of command line utilities. Search Android Market for "Busybox" and you should find some versions you can install. The Busybox shell includes tab completion and history editing. Some versions of Busybox for Android do not require that you root your phone.

#Debian utilities

You can install the full Debian shell and utilities. (Debian is a popular desktop Linux distribution.) I don't know the details, and it may require a "rooted" phone. Try a web search for "Debian Android install".

#Custom ROMs

Some custom ROMs come with their own shells and utilities. If you are using a custom ROM, check its documentation to find out what's available.


