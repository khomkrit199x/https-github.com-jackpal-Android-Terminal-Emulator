#The Android Shell

A "shell" is a program that listens to keyboard input from a user and performs actions as directed by the user. Android devices come with a simple shell program. This shell program is mostly undocumented. Since many people are curious about it I thought I'd write up some documentation for it.

    Currently this documentation is incomplete, sorry!

##Common problems

The built-in shell has very limited error handling. When you type a command name incorrectly it will say "permission denied", even though the real problem is that it couldn't find the command:

    $ dir
    dir: permission denied  <---- this is a misleading error message, should say 'dir: not found'
    $ ls
    ... listing of current directory

#The PATH variable

The Android shell will run any program it finds in its PATH. The PATH is a colon (':') seperated list of directories. You can find out what your shell's PATH is set to by using the built-in echo command:

    $ echo $PATH
    /data/local/bin:/sbin:/vendor/bin:/system/sbin:/system/bin:/system/xbin

Depending upon your shell, you may see a different result.

#Built in Commands

Every shell has a few built-in commands. Some common built-in commands are:

- echo -- prints text to stdout. 
- set -- sets shell variables
- export -- makes shell variables available to command-line programs
- cd -- change the current directory.
- pwd -- print name of the current directory.

#Commands
To find out what commands you have available to you, use the "ls" command on each of the directories in the PATH variable.

##Finding documentation for the Android commands.

Many of the Android commands are based on standard Linux (or bsd) commands. If you're curious about a command, you can sometimes learn how it works by using the "man" command on a desktop Linux or OSX (Apple Macintosh) computer. The Linux or OSX version of the command may be different in details, but much of the documentation will still apply to the Android version of the command.

Another source of documentation for people without a Linux or OSX machine handy is to use a web browser and use a web search engine to search for the text: "man Linux command-name".

##List of commands

The following is a list of the commands that are present on a Nexus S phone running an Android 2.3.3 "user-debug" build. Many of these commands are not present on a "user" phone. (They are missing from a "user" phone because they are specific to developing or debugging the Android operating system.)

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

am is the Android Activity Manager. It's used to start and stop Android activities (e.g. applications) from
the command line. Type am by itself to get a list of options.

    amix
    aplay

Command line audio file player.

    app_process
    applypatch

Used to apply patches to android files.

    arec

Command line audio recorder.

    audioloop
    bluetoothd

BlueTooth daemon

    bmgr

Backup manager - type command by itself to get documentation.

    bootanimation

Draws the boot animation. You may have to reset your phone to get out of this.

    brcm_patchram_plus
    bugreport
    cat

Copy the contents of a file to standard output.

    chmod

Change the mode of a file (e.g. whether it can be read or written.)

    chown

Change the owner of a file.

    cmp

Compare two files byte-by-byte

    dalvikvm

The dalvik virtual machine. (Used to run Android applications.)

    date

Prints the current date and time

    dbus-daemon
    dd

Convert and copy a file. By default copies standard in to standard out.

    debuggerd
    dexopt
    df

Shows how much space is free on different file systems on your device.

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

Shows the current configuration of network interfaces (IP, MAC address etc)

    iftop

Shows the current processes using the network interfaces (top, but for networks)

    ime
    input
    insmod
    installd
    ioctl
    ionice
    iptables

Manage the firewall 

    keystore
    keystore_cli
    kill

Send signals to processes.

    linker
    ln

Used to set up a file system link.

    log
    logcat

Prints the Android runtime log.

    logwrapper
    ls

Lists files.

    lsmod
    lsof
    make_ext4fs
    mediaserver
    mkdir

Make a directory.

    monkey

A program that sends random events, used to test applications. (Like having a monkey playing with the device.)

    mount
    mtpd
    mv

Move a file from one directory to another. (Only on the same file system. Use "cat a > b" to copy a
file between file systems.

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

List active processes.

    qemu-props
    qemud
    racoon
    radiooptions
    reboot

Reboot the device.

    record
    renice
    rild
    rm

Remove a file.

    rmdir

Remove a directory.

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

Starts the Android runtime.

    stop

Stops the Android runtime.

    surfaceflinger
    svc
    sync
    system_server
    tc
    testid3
    toolbox
    top

Shows which processes are currently using the most CPU time.

    umount
    uptime

Prints how long your device has been running since it was last booted.

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

Secure copy program. (Used to copy files over the network.)

    showmap
    showslab
    sqlite3

Used to administer SQLite databases.

    strace

System trace command - use to see what system calls a program makes.

    su

Start a shell with root privileges.

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


