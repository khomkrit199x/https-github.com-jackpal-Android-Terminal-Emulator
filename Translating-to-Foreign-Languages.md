# How to Localize Android Terminal Emulator

Android Terminal Emulator has been localized for these locales:

+ U.S. English <-- this is the default.
+ French (fr)
+ German (de)
+ Italian (it)
+ Japanese (ja)
+ Russian (ru)
+ Simplified Chinese (zh-rCN)
+ Turkish (tr)

All of these translations (besides American English) have been provided by volunteers. More translations and improved translations are gratefully accepted.

# How Android localization works

Android localization is done primarily using localized versions of XML files stored in the res/values* directories of the source tree. Please read the official documentation on [Android Resource Localization](http://developer.android.com/guide/topics/resources/localization.html)

All that you need to do to localize Android into a new language is make a copy of the res/values directory and update the strings (about 100) that are stored in those files. Then recompile Android Terminal Emulator to include your new translation. (And please send the new or updated localization files to me so I can include them in the official build of Android Terminal Emulator.) 

# Why the translations are not complete

Unfortunately my foreign language skills are very weak. "Guten Tag!" and "Ni Hao" are about all I know. That means I have to rely on the kindness of strangers for the localized versions of Android Terminal Emulator.

As new features are added to Android Terminal Emulator, I add the English strings for the new user interface features are added to files in the "res/values" directory.

When a new string is added, it appears (in English) in all translations. In order to appear in the localized language, the same string needs to be added to the corresponding file in the res/values-XX directory, where "XX" is the locale code. (That's the letters that appear in parentheses in the list of supported locales.  

# How to create or improve a localization

If you would like to contribute a localization for the Android Terminal Emulator, please:

1. Download these two files:
    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/arrays.xml]]
    * [[https://github.com/jackpal/Android-Terminal-Emulator/blob/master/res/values/strings.xml]]
2. Edit those two files to change the English strings to your language strings.
3. Email the localized copies of those files to jack.palevich@gmail.com

Alternately, if you know how to use github and write Android applications, you can fork the Android Terminal Emulator project, add the localization to your fork, and send me a pull request:

1. [Install Git](http://git-scm.com/)
2. Clone the Android Terminal Emulator git repository:

    $ git clone git://github.com/jackpal/Android-Terminal-Emulator.git

3. Edit the appropriate res/values-* files. (For example res/values-de has the German (Deutsch) localization.) You will need to manually look through the corresponding U.S. English res/values files to find out what strings are missing.

4. Build and test Android Terminal Emulator to make sure that you new translation works.

    + See docs/Building.txt for instructions on how to build Android Terminal Emulator.

5. Send me the changes you made, either as a "diff", a "patch" or as a "github pull request".

Back to [[Home]] page for the Android Terminal Emulator Wiki