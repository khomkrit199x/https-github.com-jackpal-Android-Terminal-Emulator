## What is a terminal emulator?

A terminal emulator is a program that makes your Android phone act like an old fashioned computer terminal. It is useful for accessing the Linux command line shell that is built into every Android phone. This lets you run various Linux command line utilities.

If you don't know what all that means, and why it's cool, then this probably isn't the program for you. (Sorry!)

### Help, I'm lost. How do I use the Android shell?

I've written a brief, incomplete, guide to using the built-in Android shell: [[Android Shell Command Reference]]

### What sort of games does this emulator play?

Sorry, this is a terminal emulator, not a game emulator. It has nothing to do with games.

### Does the Android Terminal Emulator allow me to "Root" or "Hack" my phone?

Sorry, no. The Android Terminal Emulator does not help you root or hack your phone.

### Is the Android Terminal Emulator useful on an ordinary phone, that hasn't been rooted?

Yes! You can access the entire /sdcard file system, and you can install and run Linux command-line applications in the parts of the /data file system that are accessible to the Android Terminal Emulator process.

You can also run command-line programs that access the Internet.

### Why do I get "permission denied" errors when I try to run commands in the terminal?

This message is being printed out by the Android shell. It means one of two things:

1. It might simply mean that you have misspelled the command name, or are trying to use a command that is not installed on you device. The Android shell will print "permission denied" when it just can't find the command, instead of a more accurate error message like "command not found".

2. It could mean that the command exists, but you don't have permission to run it. By default the Android Terminal Emulator runs using the permissions of the Android Terminal Emulator application. You may need to become "root" in order to gain permissions to run some commands. You can use the "su" command to do this. Of course, most consumer Android devices don't have root access enabled by default, so you may not be able to use the "su" command on your device.

### Why does the Android Terminal Emulator request Internet and SD Card write permissions?

By itself, the Android Terminal Emulator doesn't access the Internet or write to the SD Card. However, many users of Android Terminal Emulator want to run command line programs that do these things.

The way Linux (and therefore Android) works, a child process inherits the permissions of the parent. Android Terminal Emulator requests the Internet and SD Card write permissions so that the command-line programs that it runs can have access to the Internet and write to the SD Card.

If giving these permissions to the terminal emulator makes you uncomfortable, you could always download the source code to Android Terminal Emulator and compile your own version. (Edit the AndroidManifest.xml file to remove the INTERNET and WRITE_EXTERNAL_STORAGE permissions.)

### Why don't the Arrow Keys / DPAD / Trackball work ?
They do work, sort of. They send the proper escape sequences for VT-100 terminal arrow keys. What's missing is that pre-Gingerbread (pre 2.3) versions of the default Android shell do not handle these escape sequences.  Gingerbread (Android 2.3) and later versions of Android work correctly. But that doesn't help people with older versions of Android.

If you have a Froyo (2.2) or earlier version of Android, you can fix this problem by installing an alternate shell, such as the one in Busybox. The Busybox "ash" shell recognizes the arrow escape sequences sent by the terminal emulator.

### Why doesn't the Back key work?

It sends the "ESC" character by default. Use the Preferences panel to change this behavior:

Menu Key -> "More"-> "Preferences" -> Back button behavior 

### Swype soft keyboard has problems typing a lowercase 'i'. Is there a work-around?

Several people have reported this bug. Unfortunately, I can't reproduce it using Swype 3.25 Beta on Android 2.3.6. Maybe it's fixed in the latest version of Swype. Please try installing Swype 3.25 or later and see if that fixes the problem.

### SlideIt soft keyboard always types upper-case letters. Is there a work-around?

I have reproduced this with SlideIt version 4.0.1 on Android 2.3.6. There is a work-around, which is to tap on the "ABC" button on the upper-right-hand-corner of the SlideIt soft keyboard. This switches SlideIt into letter-at-a-time mode.

### Could you make a full programmer soft keyboard with ctrl, tab, esc?

Many people report good results using the free [Hacker's Keyboard](https://market.android.com/details?id=org.pocketworkstation.pckeyboard) IME. Also available from [Hacker's Keyboard Download on github](http://code.google.com/p/hackerskeyboard/downloads/list)

### Why don't you include a telnet or ssh client?
That's a good question! I guess I really ought to. Maybe one of these days I'll get around to it. In the meantime, see [[Installing BusyBox and ssh without Rooting your Device]]

### Could you make tab completion work?
Similar to the "Arrow Keys" question above, tab completion is the job of the shell, not the terminal emulator. The built-in Android shell prior to the Ice Cream Sandwich release does not provide tab completion. You can turn on tab completion by installing an alternate shell, such as the one that comes with Busybox.

### What is Busybox?
Busybox is a collection of Linux utility programs that is designed to be run on small Linux devices, such as your Android phone.

### Where can I get Busybox for my Android Phone?
Do a web search for "Android Busybox" and read through the results.

### Do I need root access to install and use Busybox?
No! If you have Android 2.3 or newer, see [[Installing BusyBox and ssh without Rooting your Device]]

### I'm building my own Android ROM, can I include Android Terminal Emulator in my ROM?

Sure, go for it. [[Tips for Including ATE in a custom ROM]]

### How can I get the menu key to work with Android Terminal Emulator on my Nook?

The Nook does not have a physical menu key. If you want Android Terminal Emulator to work with a Nook, you will have to install a version of Android that supports soft menu keys. Android 3.0 (Honeycomb) provides support for soft menu keys.

### How can I contribute a localization?

See the instructions here: [[Translating to Other Languages]]

### Why does Android Terminal Emulator ask for certain permissions?

Please read the Android Terminal Emulator [[Privacy Policy]].