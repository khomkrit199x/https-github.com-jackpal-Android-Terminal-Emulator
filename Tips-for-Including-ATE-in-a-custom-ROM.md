You are welcome to include Android Terminal Emulator in your custom ROM.

Here are some things you should keep in mind:

* You are required to follow the rules of the licence, which boil down to:
  * You can't change the license.
  * You must keep the license with the source code.

* Please change the package name from jackpal.androidterm to something specific to your ROM, such as MyROM.
  * This will enable your users to install and update the Market version of ATE if they choose.

* Please change the name of the JNI shared library from libjackpal-androidterm3.so to something specific to your ROM, such as MYROM-androidterm3.so
  * This will enable your users to install and update the Market version of ATE if they choose.
  * Don't choose a name like libjackpal-androidterm4.so, because that's very likely to be used by future
    versions of the Market version of Android Terminal Emulator.
