Chameleon Terminal Emulator can be launched programmatically from another Android application using the standard
Android Intent mechanism. You can optionally supply an intent extra to specify an initial command to
be passed to the terminal emulator.

## Intents

* jackpal.chameleonterm.OPEN_NEW_WINDOW opens a new terminal window.  No
  script execution is allowed, and no permissions are required to use
  this action.
* jackpal.chameleonterm.RUN_SCRIPT opens a new window and runs the script
  specified in the jackpal.chameleonterm.iInitialCommand extra.
  Applications using this intent must have the
  jackpal.chameleonterm.permission.RUN_SCRIPT permission, which must be
  approved by the user at install time.

Example:

    // opens a new window
    Intent i = new Intent("jackpal.chameleonterm.OPEN_NEW_WINDOW");
    i.addCategory(Intent.CATEGORY_DEFAULT);
    startActivity(i);
    
    // opens a new window and runs "echo 'Hi there!'"
    // application must declare jackpal.chameleonterm.permission.RUN_SCRIPT in manifest
    Intent i = new Intent("jackpal.chameleonterm.RUN_SCRIPT");
    i.addCategory(Intent.CATEGORY_DEFAULT);
    i.putExtra("jackpal.chameleonterm.iInitialCommand", "echo 'Hi there!'");
    startActivity(i);

Sample code:

There's an example application showing how to use these intents here:

[CTE Intent Sample Application](https://github.com/jackpal/Android-Terminal-Emulator/tree/master/examples/intents )