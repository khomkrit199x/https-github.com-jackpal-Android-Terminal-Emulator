You are welcome to include Android Terminal Emulator in your Custom ROM.

Here are some things you should keep in mind:

### Follow the license

* You are required to follow the rules of the licence, which boil down to:
  * You can't change the license.
  * You must keep the license with the source code.

### Avoid conflicts with the Play store version of Android Terminal Emulator

Some custom ROMs package Android Terminal Emulator in a way that causes conflicts with the Google Play store version of Android Terminal Emulator. The problem happens when:

  1. The custom ROM stores the JNI library that Android Terminal Emulator uses in the system directory.

  2. The end user installs a new version of Android Terminal Emulator from the Play store.

In this situation, the new version of Android Terminal Emulator will end up using the JNI library that's in the system directory, instead of the JNI library that comes with the application.

I try to work around this problem by changing the name of the JNI library each time its contents change. However if your custom ROM happens to do the same thing, and you happen to choose the same name as me, then we'll run into a conflict! So, please, if you decide to update the JNI library, please pick a name like libMYROM-androidterm.so .

The Play version of Android Terminal emulator uses the following pattern for its JNI library names: libjackpal-androidtermN.so, where N is 1, 2, 3, 4, and so on. Stay away from this pattern and there should not be a conflict with the Play version.

