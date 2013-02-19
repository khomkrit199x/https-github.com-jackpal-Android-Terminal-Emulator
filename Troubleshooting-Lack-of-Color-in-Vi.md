Problem

Can't see colors when using a program like vi that is supposed to support colored output.

Possible Solutions

+ Perhaps your version of vi doesn't support colors. Consult the documentation for your version of vi.

+ Perhaps you don't have the $TERM environment variable set correctly. Do

    $ echo $TERM

and see what it's set to. Try using the "Menu : Preferences : Terminal Type  to cycle through the different choices. (I think you need to open a new terminal window each time you change the terminal type in order to have the new type take effect.)

You can verify that colors are working in Android Terminal Emulator by copying this file to your device and catting it:

https://raw.github.com/jackpal/Android-Terminal-Emulator/master/tests/controlSequences/256color.txt

