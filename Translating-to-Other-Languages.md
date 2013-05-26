# How to Localize Android Terminal Emulator

Android Terminal Emulator has been localized for these locales:

+ U.S. English <-- this is the default.
+ Basque (eu)
+ Czech (cz)
+ Dutch (nl)
+ French (fr)
+ Georgian (ka)
+ German (de)
+ Hungarian (hu)
+ Italian (it)
+ Japanese (ja)
+ Korean (ko)
+ Norwegian (Bokmål) (nb)
+ Polish (pl)
+ Portuguese (pt)
+ Portuguese (pt-rPT)
+ Romanian (ro)
+ Russian (ru)
+ Simplified Chinese (zh-rCN)
+ Spanish (es)
+ Slovak (sk)
+ Swedish (sv)
+ Traditional Chinese (zh-rTW)
+ Turkish (tr)
+ Ukrainian (uk)

All of these translations (besides American English) have been provided by volunteers. More translations and improved translations are gratefully accepted.

You don't have to be a programmer to create the translations, all you need is a text editor, some knowledge of technical English, and of course knowledge of the technical version of your own language.

# How Android localization works

Android localization is done primarily using localized versions of XML files stored in the res/values* directories of the source tree. Please read the official documentation on [Android Resource Localization](http://developer.android.com/guide/topics/resources/localization.html)

All that you need to do to localize Android into a new language is make a copy of the res/values directory and update the strings (about 100) that are stored in those files. Then recompile Android Terminal Emulator to include your new translation. (And please send the new or updated localization files to me so I can include them in the official build of Android Terminal Emulator.) 

# Why the translations are not complete

Unfortunately my foreign language skills are very weak. "Guten Tag!" and "Ni Hao" are about all I know. That means I have to rely on the kindness of strangers for the localized versions of Android Terminal Emulator.

As new features are added to Android Terminal Emulator, I add the English strings for the new user interface features are added to files in the "res/values" directory.

When a new string is added, it appears (in English) in all translations. In order to appear in the localized language, the same string needs to be added to the corresponding file in the res/values-XX directory, where "XX" is the locale code. (That's the letters that appear in parentheses in the list of supported locales.  

# How to improve a localization or create a brand-new localization.

First, send me an email so I know you're working on it!

The process is slightly different depending upon whether you are improving an existing localization or creating a brand new localization.

# Please try to use a text editor that supports UTF-8

Android resource files are encoded using the UTF-8 character set. If possible, please use a text editor
that can read and write UTF-8 encoded files to edit the resource files. For example, on Windows you should
use an editor like the free (Notepad++)[http://notepad-plus-plus.org/] editor. Or try the free test version
of (Sublime Text 2)[http://www.sublimetext.com/2], which works on Windows, Mac OS and Linux.

If you can't figure out how do this, no worries, send me your files anyway, and I'll do my best to
convert them into UTF-8.

## Improving an existing localization

To improve an existing localization you'll need both the English version of the files as well as the existing localized versions of the files.

1. Download these two files (they are the U.S. English version of the UI:

    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/arrays.xml]]
    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/strings.xml]]

2. Download the corresponding two files for your locale. (instead of XX use your locale's locale code).

    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values-XX/arrays.xml]]
    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values-XX/strings.xml]]

3. Edit the localized files to add the new strings from the original English files.
4. Email the localized copies of those files to jack.palevich@gmail.com

## Creating a brand new localization

To contribute a new localization for the Android Terminal Emulator, please:

1. Download these two files:

    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/arrays.xml]]
    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/strings.xml]]

2. Edit those two files to change the English strings to your language strings.
3. Email the localized copies of those files to jack.palevich@gmail.com

## If you know how to use github and compile Android apps

Alternately, if you know how to use github and write Android applications, you can fork the Android Terminal Emulator project, add the localization to your fork, build and test the fork to make sure that it works, and send me a pull request:

1. [Install Git](http://git-scm.com/)
2. Clone the Android Terminal Emulator git repository:

    $ git clone git://github.com/jackpal/Android-Terminal-Emulator.git

3. Edit the appropriate res/values-* files. (For example res/values-de has the German (Deutsch) localization.) You will need to manually look through the corresponding U.S. English res/values files to find out what strings are missing.

4. Build and test Android Terminal Emulator to make sure that you new translation works.

    + See docs/Building.txt for instructions on how to build Android Terminal Emulator.

5. Send me the changes you made, either as a "diff", a "patch" or as a "github pull request".

## Example format

If you open the first file, arrays.xml, in a text editor you will see that it starts like this:

    <resources>
        <string-array name="entries_statusbar_preference">
            <item>Show status bar</item>
            <item>Hide status bar</item>
        </string-array>

In this section of text you only need to localize the "Show status bar" and "Hide status bar" text. Here is the same section of the file, "localized" by being changed to upper case:

    <resources>
        <string-array name="entries_statusbar_preference">
            <item>SHOW STATUS BAR</item>
            <item>HIDE STATUS BAR</item>
        </string-array>

Back to [[Home]] page for the Android Terminal Emulator Wiki