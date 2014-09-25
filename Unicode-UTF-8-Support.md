Chameleon Terminal Emulator (as of 1.0.33) has partial Unicode UTF-8 support.

[Unicode](http://en.wikipedia.org/wiki/Unicode) is a standard for encoding all the world's written languages.

[UTF-8](http://en.wikipedia.org/wiki/UTF-8) is a character encoding that encodes Unicode characters into a byte stream that is compatible with 7-bit ASCII.

# Enabling UTF-8 Support

Menu -> Preferences -> Enable UTF-8 Support
Then reset your terminal:
Menu -> More -> Reset Term


# Disabling UTF-8 Support

Menu -> Preferences -> uncheck Enable UTF-8 Support
Then reset your terminal:
Menu -> More -> Reset Term

# What works

* Single-character UTF-8 characters
* East-Asian scripts (Japanese, Chinese, Korean)
* Some form, line-drawing, math, currency characters

# What doesn't work

* Combining diacritical marks.
* Right-to-left characters (e.g. Middle-Eastern languages.)
* Characters like Brail that are not present in the Android fonts.
