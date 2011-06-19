# How to Help Translate Android Terminal Emulator to a Foreign Language

Android Terminal Emulator is currently (at least partially) translated to these locales:

+ American English
+ French (fr)
+ German (de)
+ Italian (it)
+ Japanese (ja)
+ Russian (ru)
+ Simplified Chinese (zh-rCN)
+ Turkish (tr)

All of these translations (besides American English) have been provided by volunteers. More translations and improved translations are gratefully accepted.

# How Android Localization works

Android localization is done primarily using localized versions of XML files stored in the res/values* directories of the source tree. Please read the official documentation on [Android Resource Localization](http://developer.android.com/guide/topics/resources/localization.html)

All that you need to do to localize Android into a new language is make a copy of the res/values directory and update the strings (about 100) that are stored in those files. Then recompile Android Terminal Emulator to include your new translation. (And please send the new or updated localization files to me so I can include them in the official build of Android Terminal Emulator.) 

# Why the translations are not complete

Unfortunately my foreign language skills are very weak. "Guten Tag!" and "Ni Hao" are about all I know. That means I have to rely on the kindness of strangers for the localized versions of Android Terminal Emulator.

As new features are added to Android Terminal Emulator, I add the English strings for the new user interface features are added to files in the "res/values" directory.

When a new string is added, it appears (in English) in all translations. In order to appear in the localized language, the same string needs to be added to the corresponding file in the res/values-XX directory, where "XX" is the locale code. (That's the letters that appear in parentheses in the list of supported locales.  

# How to Create or Improve a Localization

To create or improve a localization, first you need to check out the source code for Android Terminal Emulator:

1. [Install Git](http://git-scm.com/)
2. Clone the Android Terminal Emulator git repository:

    $ git clone git://github.com/jackpal/Android-Terminal-Emulator.git

3. Edit the appropriate res/values-* files. (For example res/values-de has the German (Deutsch) localization.) You will need to manually look through the corresponding U.S. English res/values files to find out what strings are missing.

4. Build and test Android Terminal Emulator to make sure that you new translation works.

    + See docs/Building.txt for instructions on how to build Android Terminal Emulator.

5. Send me the changes you made, either as a "diff", a "patch" or as a "github pull request".
