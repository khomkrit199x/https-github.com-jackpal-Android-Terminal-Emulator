Android Terminal Emulator can be launched programmatically from another Android application using the standard
Android Intent mechanism. You can optionally supply an intent extra to specify an initial command to
be passed to the terminal emulator.

## New 1.0.42 API

* jackpal.androidterm.OPEN_NEW_WINDOW opens a new terminal window.  No
  script execution is allowed, and no permissions are required to use
  this action.
* jackpal.androidterm.RUN_SCRIPT opens a new window and runs the script
  specified in the jackpal.androidterm.iInitialCommand extra.
  Applications using this intent must have the
  jackpal.androidterm.permission.RUN_SCRIPT permission, which must be
  approved by the user at install time.

Example:
    // opens a new window
    Intent i = new Intent("jackpal.androidterm.OPEN_NEW_WINDOW");
    i.addCategory(Intent.CATEGORY_DEFAULT);
    startActivity(i);
    
    // opens a new window and runs "echo 'Hi there!'"
    // application must declare jackpal.androidterm.permission.RUN_SCRIPT in manifest
    Intent i = new Intent("jackpal.androidterm.RUN_SCRIPT");
    i.addCategory(Intent.CATEGORY_DEFAULT);
    i.putExtra("jackpal.androidterm.iInitialCommand", "echo 'Hi there!'");
    startActivity(i);

## Old, pre-1.0.42 API, now removed.

(This API was removed because it allowed arbitrary applications to modify the SD Card and the Internet.)

Here's an example:

    Intent intent = new Intent(Intent.ACTION_MAIN);
    intent.setComponent(new ComponentName("jackpal.androidterm", "jackpal.androidterm.Term"));
    intent.putExtra("jackpal.androidterm.iInitialCommand", "echo Hi there!");
    startActivity(intent);