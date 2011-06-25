Android Terminal Emulator can be launched programmatically from another Android application using the standard
Android Intent mechanism. You can optionally supply an intent extra to specify an initial command to
be passed to the terminal emulator. Here's an example:

    Intent intent = new Intent(Intent.ACTION_MAIN);
    intent.setComponent(new ComponentName("jackpal.androidterm", "jackpal.androidterm.Term"));
    intent.putExtra("jackpal.androidterm.iInitialCommand", "echo Hi there!");
    startActivity(intent);
