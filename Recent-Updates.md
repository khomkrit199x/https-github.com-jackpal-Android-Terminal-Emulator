## v1.0.63

+ Built with Android Studio 1.0 / NDK r10d

+ new Serbian translation (pejakm)

+ improved Slovak translation (pylerSM)


## v1.0.62

+ Added a built-in file picker that's used by the Term short cut. (FrankWestlake)

+ Improved multi-byte text handling (Steven Luo)

+ Fixed crash when tapping on last character of a hyperlink (Steven Luo)

+ Updated Hungarian translation (gLes)

## v1.0.61

+ Term Shortcut dialog now uses Holo theme if available. (FrankWestlake)

+ Term Shortcut dialog no longer crashes on very old (cupcake) versions of Android.

+ Improved Hungarian (gles), Slovak (pyler), and Spanish (mcgivergim) translations.

## v1.0.60
+ a "Term" widget lets you create launcher icons to run favorite commands. Long-press on desktop, tap on Widgets, tap on Term, fill out dialog box. (FrankWestlake)

+ a "Term Here" intent lets you open Android Terminal Emulator at a given directory. Works with third-party file managers. Select "Term Here" in the file manager's "share" menu for a directory. (FrankWestlake)

+ Multi-Window support on Galaxy Tabs. (FrankWestlake)

+ auto-linkification now requires a "http://" or "https://" at the front of a link. (jackpal)

+ Bug fixes and API documentation improvements (Steven Luo)

+ Improved French translation. (Spanti Nicola)

## v1.0.59

 + Hardware-accelerated text drawing on devices running Android 3.0 or newer. (jackpal)
 + The cursor is now drawn correctly for "double-wide" characters. (maoabc)
 + The Help menu has been moved to the bottom of the menu. (godlessfather)
 + SK localization improved (pyler)

## 1.0.58

 + Add a "Help" menu item that links to a few simple help pages. (godlessfather)

## 1.0.57

 + Reverted close-extra-file-descriptors-on-fork patch. It turns out that some of the file descriptors
   that we were closing were used by the C runtime. Closing them meant that certain C APIs stopped working.
   The exact effect varied by C runtime version, but typical reports included getprops, ping, and su not
   working.

 + Updated Slovak translation (pylerSM) 
 + Updated Spanish translation (McGiverGim)

## 1.0.56

 + Disabled hardware acceleration for main terminal window, because the cursor doesn't render
   correctly. The Preferences pane is still hardware accelerated.

## 1.0.55

Features:

 + Enabled hardware acceleration. (sconosciuto).
 
Bug Fixes:

 + Make new ptty the controlling ptty. (phantom10111)
 + Close previously-opened file descriptors after fork and before exec. (phantom10111)

Updated Translations:

 + Updated French translation (euland).
 + Updated Hebrew translation (arthurzam).
 + Updated Hungarian translation (gLes).
 + Updated Italian translation (sconosciuto).
 + Updated Slovak translation (pylerSM).

## 1.0.54

Features:

 + Option to send xterm mouse tracking codes dan@stahlke.org

 + Option for keyboard shortcuts code@stefansk.name
    + Control-Shift-N creates new window.
    + Control-Tab cycles windows forward.
    + Control-Shift-Tab cycles windows backwards.
    + Control-Shift-V Pastes from clipboard.

 + xterm terminal emulation pfalcon@users.sourceforge.net
    + Alt buffer
    + Application mode escape sequences for cursor keys.
    + Numeric keypad support.

 + Improved terminal emulation druzus@poczta.onet.pl
  + Add support for ECMA-48 Status Report commands.
  + In 16-color mode blink attribute implies bright background color.

 + Tap on a URL to browse it kendallstewart@gmail.com

 + Updated launcher icons from nathanel.titane@gmail.com

Translations:

 + Improved Korean translation kimjongha@fasoo.com and koongchi123@naver.com
 + Improved Italian translation hubbit
 + Improved Hungarian translation gles@live.com
 + Improved Czeck translation jozka.j1@gmail.com
 + Improved Simplified Chinese translation cn.fyodor@gmail.com
 + Improved Norwegian translation odinuge@gmail.com
 + Improved Russian translation admin@nevergone.ru

Bug fixes:

 + Fix NPE in Telnet sample code.

Minor changes:

 + Now built with SDK version 23 and NDK version r9b.

## 1.0.53

Features:

 + Added 2 new color schemes based on Solarized Light and Solarized Dark. Nick Shvelidze<shveloo@gmail.com>
 + Add android.permission.ACCESS_SUPERUSER permission, which means Android Terminal Emulator will request
   super-user permission. Note that this does not automatically enable super-user permission. In order to
   actually receive super-user permission you must have a ROM or super-user utility that supports granting
   this permission to apps that request it. Do a web search for "android.permission.ACCESS_SUPERUSER" to
   learn more. (By Jacob Müller <jacob.mueller.elz@gmail.com>)
 + Set the HOME directory to an application-specific writable home directory. User can override by using
   a newly added Preference setting. By Hans-Christoph Steiner <hans@eds.org>
 + Add a preference setting for locking screen rotation to landscape or portrait.
   By Masaki Muranaka <monaka@monami-ya.jp>
 + Support newer version of clipboard on newer versions of Android. By Masaki Muranaka <monaka@monami-ya.jp>

Translations:

 + New Korean translation by Jongha Kim <kimjongha@fasoo.com>
 + Updated Polish translation from Michał Kasprzak <mkasprzak@mail.com>
 + Updated Russian and Ukrainian translations from serjbog <bogdanov.sergey.vyacheslavovich@gmail.com> 
 + Updated French translations from euland.
 + Add Japanese translation of the "intents" example. Masaki Muranaka <monaka@monami-ya.jp> 

Bug fixes:

 + Fix for hardware control key remaining stuck down if you switch screens while the control key is pressed.
   By Stefan Schneider-Kennedy <code@stefansk.name>

Minor changes:

 + Now built with SDK version 22 and NDK version r8e.

## 1.0.52

Features:

 + New icon designed by Nathanel Titane, nathanel.titane@gmail.com, TNDesigns
 + Cursor now shows toggle state of ctrl/shift/alt/Fn keys. (Inspired by ConnectBot)
 + Combining accents now work on physical keyboards. (Inspired by ConnectBot)

Bug fixes:

 + Fixed large text paste ANR (Issue #198).


## 1.0.51

Added partial translations from CyanogenMOD version of Android Terminal Emulator for several languages / locales:

 + nb nl pl pt-rPT sk sv zh-rTW

Improved Japanese translation. Thanks monaka!

Bug fix:

 + Function keys F1 to F4 now send correct escape sequences for all TERM types.
 + External Hardware keyboard Ctrl key processing improved.
 + External Hardware keyboard Fn key processing improved.


## 1.0.50

New Feature:

 + Can now choose larger font sizes: 24, 28, 32, 36, etc.

Bug fixes:

 + Fix the escape sequences that are transmitted for function keys F1 to F4.

New translation:

 + Ukrainian

Improved translation:

 + Russian

## 1.0.49

Improved translations:

 + Hungarian
 + Russian
 + Spanish

## 1.0.48

### New features

+ Spanish translation

### Bug fixes

+ Alt Key should work again for typing characters on phones with physical keyboards.

## 1.0.47

### Changes

+ Alt Sends ESC is now off by default. (Having it on by default broke devices with physical keyboards where the Alt key was used to obtain special characters.)

## 1.0.46

### New features

+ Alt / Meta key can now be configured to send Esc or set high bit.
+ Improved Hungarian translation.

### Changes

+ Default text colors are now white text on black background.
+ Default initial command string is now empty.

### Bug fixes

 + Better emulation of terminal escape sequences.
 + Better processing of Alt and Meta keys on Hacker's Keyboard IME, Bluetooth and USB keyboards.
 + Fixed a crash related to displaying wide-character Unicode
 + F1-F4 function keys send standard codes.

## 1.0.45

+ Added support for:
  + 256-color mode
  + Setting  window title via escape sequences.
  + Re-enabled bold & underline text.
+ Smoother fling scrolling.
+ Less sensitive side-to-side flipping between windows.
+ Added Intent Chooser support for "Email To" menu item.
+ Improved translations for Russian, Portugese

### 1.0.44

 + Improved French and Hungarian translations.

 + Added new text color option: Holo blue text on black

 + Removed READ_LOGS permission. It worried some users. Developers who want this feature will have to build
their own version of ATE.

### 1.0.43

 + "Return" key now works correctly in editors like nano and vi.

 + Added "Read Logs" permission so that "adb logcat" command can be used to read logs.

 + Other projects can now use ATE as a library. (See wiki for details.)
 + New intents for:
   + Sending commands to an existing ATE window.
   + Adding directories to the PATH

 + Improved French translation
 + Improved German translation
 + Added Hungarian translation
 + Added MIPS CPU support


### 1.0.42

 + Bug fixes for UTF-8 text, various crashes on ICS. (Steven Luo)

 + Added Czech Republic translation. (Jozka.1@seznam.cz)

 + Improved Basque translation (Asier Iturralde Sarasola)

 + Improved French translations. (eauland)

 + Added formal API for intent-based script execution. (Steven Luo)

 + Status bar now visible by default.

### 1.0.41

 + Fixed sticky-control-key issue with Android 3.0+ devices that have full keyboards. (Debugged by Klaus Weidner, fixed by Jack Palevich)

 + Fixed terminal window size off-by-one error on Android 3.0+ tablet devices. (Steven Luo)

 + Added Portugese translation. (damor)

 + Improved French (eauland) and German (damor) translations.

### 1.0.40

 + [[Action Bar (Android 3.0+) UI]] (Thanks Steven Luo!)
 + [[Buttonless Device Support]] (Thanks Yang Tang!)
 + Improved French Translation (Thanks eauland!)
 + Display toast when resetting terminal. (Thanks damor!)

### 1.0.39

 + Fix bug where "Reset Term" was not automatically refreshing the display.
 + The "Window #" toasts are now localizable.
 + Additional improvements to French localization courtesy eauland@github
 + Fixed syntax error in menu.xml file. (Not sure how it built with that error. :-) )

### 1.0.38

(Thanks to Steven Luo for most of the following features and bug fixes.)

New features:

 + Back key now leaves the terminal session running.
   + Back key can also be configured to send "ESC" or "TAB".
 + $TERM is set to "screen"
 + Exiting a terminal session (e.g. by typing "exit" or "control-D") closes the window.
 + Preferences can be used to change the default behavior for all of the above.
 + Improved terminal emulation. Pretty much everything termcap uses on popular Linux distros for "vt100",
   "screen", and "linux" style terminals should be supported.
     + Half-bright black now supported.
     + vt100 extended characters are now supported. (Boxes and lines.)
     + Fixed bug related to tabbing while on a tab stop.
 + Improved French Translation (Thanks eauland@github!)

Bug Fixes:

 + Reset Terminal now resets the state of the terminal emulator while keeping the terminal session active.
   + Use this when the terminal emulator is in a strange mode and you want to restore it to normal
     operation.
     + This might happen if you cat a binary file.
   + Use "Close Window" to get the old behavior of Reset Terminal.
 + The soft keyboard should now be visible by default on devices which don't
   have a hard keyboard.

Internal changes:

 + The JNI library name is now jackpal-androidterm3.so
   + This change was made because the library API has changed incompatibly.
   + The hope is that this new name will help avoid problems with custom ROMs that
     include their own version of Android Terminal Emulator's JNI library.

(Special thanks and apologies to tshirtman @ Github -- he sent me a pull request for changing the Back key to send ESC back in September, but I spaced out and forgot about it until now. D'Oh!)

### 1.0.35

Fixed status bar icon style for 2.2+ devices.

### 1.0.34

Fix two bugs:

 + Swype Keyboard didn't work. (Reverted a seemingly innocent change. IMEs are error prone.)
 + Wouldn't start on some versions of Android. (Was accidentally using an API level 11 API in a class
   that got loaded in API level 10 devices.)

### 1.0.33

[[Unicode UTF-8 Support]]. Thanks to Steven Luo, steven+android@steven676.net

Many bug fixes, again thanks to Steven Luo.

Updated status bar icon to match ui guidelines.

Improved Italian localization thanks to fireb33@gmail.com

Basque localization thanks to asier.iturralde@gmail.com

### 1.0.32

Added multiple terminal windows! (Use menu item New Window to create.)  You can swipe left/right to switch between windows. Thanks to Steven Luo, steven+android@steven676.net

Improved text rendering for non-integer-width font sizes.

Improved Italian localization (bug fixes). Thanks to fireb33@gmail.com

### 1.0.31

Improved Italian localization. Thanks to fireb33@gmail.com

You can now specify an initial command string when starting Android Terminal Emulator from another program using an intent. Thanks to Christoph Schmidt-Hieber, M.D. c.schmidt-hieber@ucl.ac.uk

The Control-0-9 and Fn-0-9 key assignments have been reworked to be more compatible with Debian Xterm. Thanks to Steven Luo, steven+android@steven676.net

### 1.0.30

Fix bugs in terminal emulation: Some versions of 'vi' may work better. Thanks Sam Jacobson for bug report and patch!

You can now choose 'none' as a control key or fn key. Useful if you have a full keyboard (such as on the Acer Transformer). Thanks Eli Grey for idea.

You can now install the Terminal Emulator to the SD card if you like.

Added some missing French translations. Thanks cpasmoi for the pull request!

Made the 'Special Keys' dialog localizable.

### 1.0.29

Fix JNI global reference bug. (Program would crash at start when run on post-3.0 versions of Android.)

This bug has been present in all versions of Android Terminal Emulator, but was not caught until now.

### 1.0.28:

Change shared library name from libandroidterm2 to libjackpal-androidterm2

This avoids a conflict with CyanogenMod, which also uses the library name libandroidterm2.

Thanks to Steven Luo for finding this bug and contributing a patch that fixes it.

### 1.0.27:

Fix java.lang.UnsatisfiedLinkError error.
    
Change shared library name from libandroidterm to libandroidterm2
    
My theory is that this bug is happening on systems that have system versions of the libandroidterm shared library.

Version 1.0.26 of Android Terminal Emulator added a new API, hangupProcessGroup, to the libandroidterm library.
    
I think on devices that have libandroidterm in their system library,
that version takes precedence over the version in the application,
and so the hangupProcessGroup API is not found.
    
By changing the name of the libandroidterm library to libandroidterm2
we should avoid loading the system version of the
libandroidterm library.

### 1.0.26

Many improvements thanks to new contributor Steven Luo <steven+android@steven676.net>:

 + Add a "Fn" key, makes it easier to type special characters.
     by default the "Fn" key is bound to the Volume Up key.

 + Added menu options to hold the Wake Lock and/or WiFi Lock
   + Wake Lock keeps phone from sleeping while running a command.
   + WiFi Lock keeps WiFi on while talking to a remote computer.

 + Added a service to avoid being killed while in the background.

 + Avoid leaking shell process tree when exiting.

### 1.0.25

Added Turkish localization, courtesy Doğukan Korkmaztürk <d.korkmazturk@gmail.com>.

1.0.24:

Show Options Menu button on Honeycomb devices.

### 1.0.23

Declare that we don't require touch screen support. Currently this doesn't make any difference, but perhaps in the
future Android Market will work on devices that don't have touch screens.

1.0.22:

Add support for Android 1.5 (Cupcake) devices. Welcome Cupcake owners!

There should be no difference in behavior for devices with newer versions of Android. Nothing added, nothing removed.

### 1.0.21

### 1.0.20

### 1.0.19

The UI has been localized for several languages, courtesy the CyanogenMod project.

You can now copy rectangular blocks of text (thanks pelya !)

1. Long-press to bring up an "Edit text" menu
2. Choose 'Select text'
3. Use your finger to drag-select a block of text. (Note that the text selection occurs 40 pixels above where you touch, so you can see what you are selecting.)
4. The selected text is automatically copied to the clipboard.

### 1.0.18

Improved Bluetooth keyboard support.

### 1.0.17

Don't remember what changed. :-(

### 1.0.16

Add support for Swype IME cursor keys. If you install the Swype IME, and switch to the Editing keyboard, you can tap on the Up/Down/Left/Right buttons in the IME and the terminal emulator will send the corresponding escape sequences.

Before you get too excited about this feature, note that the default Android shell doesn't know what to do with the escape sequences. But if you happen to have an advanced shell (such as the ash shell that comes with Busybox) installed, you can use the cursor buttons to edit your command line and navigate through your command history.

Thanks to Todd Musall for contributing this feature.

### 1.0.15

Fix the Swype IME backspace key. Previously tapping it did nothing. Now tapping it sends a "DEL" key, which most shells interpret as deleting the character to the left of the cursor.

Thanks to Todd Musall for contributing this feature.

### 1.0.14

Fixed crash that sometimes occurred when rotating portrait to landscape.

### 1.0.13

You can now use the volume-up or volume-down key as the control key. This is especially useful on phones that lack any other hard keys, such as the Samsung Galaxy S. Thanks to Todd Musall for writing and contributing this feature!

### 1.0.12

By popular demand, implement a work around for determining the visible portion of the terminal screen when the soft keyboard is visible. Should work for portrait and landscape, and with or without status bar. Whew!

### 1.0.11

reset everyone's status bar to 'on'. If they want the status bar off, they have to set the preference again. I did this because the soft keyboard works better if the status bar is on. People who upgraded to 1.0.9 had the status bar automatically turned off, which broke their soft keyboard. Now it should work again. (Software development is hard!)

### 1.0.10

default the status bar to "on", because turning the status bar off causes the app to become a "full screen" app, and the IME system doesn't resize the view for full screen apps.

### 1.0.9

show/hide status bar preference.
toggle soft keyboard menu item.

### 1.0.8

longpress to copy/paste.

### 1.0.5

Add Internet and SD Card permissions to allow apps run from the emulator to access
the Internet and write to the SD card.