# Buttonless Device Support

Some Android devices, such as the Amazon Kindle Fire and the Barnes and Noble Nook have no physical keys, so the normal "Control" and "Fn" key technique does not work.

As a work-around, two new menu items have been added to the long-press menu: "Send control key" and "Send Fn Key". They affect the next character that is typed.

For example, suppose we want to send "ctrl-x". We first long-press the screen to bring out the context menu. Then we tap "send control key". Finally, we press the letter "x" on the keyboard.

The "send control key" and "send fn key" here only modify the next key pressed. Let's say if we want to send "ctrl-x ctrl-c", then we need to tap the context menu, press "x", tap the context menu again, and press "c". This behavior is justified since in most cases we only need to modify a single key at a time.
