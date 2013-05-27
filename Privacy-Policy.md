# Android Terminal Emulator Privacy Policy

Android Terminal Emulator does not collect, store, transmit, or share any personally identifiable information with anyone or anything.

## Externally Observable Actions

If you use Android Terminal Emulator to run a command line application that connects to the network (such as an IRC chat program, or a ssh shell, or an FTP client, or a BitTorrent client), then it may be possible for third parties to observe your activities by observing your network traffic. The risks are similar to the risks of using "Incognito Mode" in a web browser.

## Logging of ANR and FC Events

If you experience an "Application Not Responding", or "Forced Close" event while using Android Terminal Emulator, you may be asked for permission to upload a crash report. If you agree, some information about the crash will be uploaded. This information is designed to not contain any personally identifiable information, but may include information such as the stack crawl of what the program was trying to do when it crashed, as well as limited information about your phone's software (such as which version of Android Terminal Emulator you were using.)

# Permissions

Android Terminal Emulator asks for several permissions on behalf of command line tools that run from within the emulator. The current set of permissions that are requested is.

* android.permission.INTERNET allows access the Internet. Examples of programs that use this permission are rcp, telnet, ssh, and ftp.
* WRITE_EXTERNAL_STORAGE allows writing to the SD card. Used by cp, mv, and any tool that writes files.
* ACCESS_SUPERUSER - this is a special permission, see "Access Superuser" below.
* WAKE_LOCK allows keeping the screen and/or CPU turned on. This is controlled using the "Take Wake Lock" menu items. This is helpful for people trying to run long-duration commands such as compilers.

## Access Superuser

This permission is not a standard Android system permission. It is an informal standard developed by
the enthusiast community. It allows a program to indicate that it would like to acquire super-user
permission. This permission is ignored by normal Android computers. It only does something if you have installed an enthusiast ROM (such as CyanogenMOD) that supports the permission.

Android Terminal Emulator does nothing with the Access Superuser permission by itself. It asks for the permission in order to allow command-line tools to run as root.
