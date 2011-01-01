1.0.19:

The UI has been localized for several languages, courtesy the CyanogenMod project.

You can now copy rectangular blocks of text (thanks pelya !)

1. Long-press to bring up an "Edit text" menu
2. Choose 'Select text'
3. Use your finger to drag-select a block of text. (Note that the text selection occurs 40 pixels above where you touch, so you can see what you are selecting.)
4. The selected text is automatically copied to the clipboard.


1.0.18:

Improved Bluetooth keyboard support.

1.0.17:

1.0.16:

Add support for Swype IME cursor keys. If you install the Swype IME, and switch to the Editing keyboard, you can tap on the Up/Down/Left/Right buttons in the IME and the terminal emulator will send the corresponding escape sequences.

Before you get too excited about this feature, note that the default Android shell doesn't know what to do with the escape sequences. But if you happen to have an advanced shell (such as the ash shell that comes with Busybox) installed, you can use the cursor buttons to edit your command line and navigate through your command history.

Thanks to Todd Musall for contributing this feature.

1.0.15:

Fix the Swype IME backspace key. Previously tapping it did nothing. Now tapping it sends a "DEL" key, which most shells interpret as deleting the character to the left of the cursor.

Thanks to Todd Musall for contributing this feature.

1.0.14:

Fixed crash that sometimes occurred when rotating portrait to landscape.

1.0.13:

You can now use the volume-up or volume-down key as the control key. This is especially useful on phones that lack any other hard keys, such as the Samsung Galaxy S. Thanks to Todd Musall for writing and contributing this feature!

1.0.12:

By popular demand, implement a work around for determining the visible portion of the terminal screen when the soft keyboard is visible. Should work for portrait and landscape, and with or without status bar. Whew!

1.0.11:

reset everyone's status bar to 'on'. If they want the status bar off, they have to set the preference again. I did this because the soft keyboard works better if the status bar is on. People who upgraded to 1.0.9 had the status bar automatically turned off, which broke their soft keyboard. Now it should work again. (Software development is hard!)

1.0.10:

default the status bar to "on", because turning the status bar off causes the app to become a "full screen" app, and the IME system doesn't resize the view for full screen apps.

1.0.9:

show/hide status bar preference.
toggle soft keyboard menu item.

1.0.8:

longpress to copy/paste.

1.0.5:

Add Internet and SD Card permissions to allow apps run from the emulator to access
the Internet and write to the SD card.
