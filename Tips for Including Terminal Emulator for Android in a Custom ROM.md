You are welcome to include Terminal Emulator for Android in your custom ROM.

Here are some things you should keep in mind:

### Follow the license

* You are required to follow the rules of the license, which boil down to:
  * You can't change the license.
  * You must keep the license with the source code.

### Avoid conflicts with the Google Play version of Terminal Emulator for Android

Some custom ROMs package Terminal Emulator for Android in a way that causes conflicts with the Google Play version of Terminal Emulator for Android. The problem happens when:

  1. The custom ROM stores the JNI library that Terminal Emulator for Android uses in the system directory.

  2. The end user installs a new version of Terminal Emulator for Android from Google Play.

In this situation, the new version of Terminal Emulator for Android will end up using the JNI library that's in the system directory, instead of the JNI library that comes with the application.

I try to work around this problem by changing the name of the JNI library each time its contents change. However if your custom ROM happens to do the same thing, and you happen to choose the same name as me, then we'll run into a conflict! So, please, if you decide to update the JNI library, please pick a name like libMYROM-androidterm.so .

The Google Play version of Terminal Emulator for Android uses the following pattern for its JNI library names: libjackpal-androidtermN.so, where N is 1, 2, 3, 4, and so on. Stay away from this pattern and there should not be a conflict with the Google Play version.

