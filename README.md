
# bv
Some notes about terminal emulators

https://github.com/unxed/bv

All non-pluses should have a link to a relevant issue

---

1. Clip: Bracketed paste or OSC52 read or far2l read
+tvision
+fvision
+far2l
+gnometerm
+konsole
+kitty

2. Clip: OSC52 write or kitty write or far2l write
+tvision
+fvision
+far2l
...gnometerm
https://gitlab.gnome.org/GNOME/vte/-/issues/2495
+konsole
+kitty

3. Keyup events & full set of keys/combinations (e.g. Ctrl+Enter) support
...tvision
https://github.com/magiblot/tvision/issues/186
...fvision
https://gitlab.com/freepascal.org/fpc/source/-/issues/34190
+far2l
...gnometerm
https://gitlab.gnome.org/GNOME/vte/-/issues/2601
https://gitlab.gnome.org/GNOME/vte/-/issues/2764
https://gitlab.gnome.org/GNOME/vte/-/merge_requests/9
at least they are ready to support win32im
...konsole
https://bugs.kde.org/show_bug.cgi?id=484044
https://bugs.kde.org/show_bug.cgi?id=435975
https://invent.kde.org/utilities/konsole/-/merge_requests/1133
+kitty

4. Correct hotkey handling via (3): any lang, any layout, w/wo modifiers, inside menus and not

...tvision
non-latin menu hot keys problem
https://github.com/magiblot/tvision/issues/99

...fvision
bug with getting layout independent key code in kitty
https://gitlab.com/freepascal.org/fpc/source/-/merge_requests/1138#note_2734741741
needs testing after it
also, non-latin menu hot keys problem
https://gitlab.com/freepascal.org/fpc/source/-/issues/41445

5. UI/UX patterns following best software design practices

5.1. Navigation wia arrow keys

...tv patch uploaded
PR: Enable arrow keys for navigation
https://github.com/magiblot/tvision/pull/188

+fv

5.2. Open file window as in FreeVision

...tv patch uploaded
https://github.com/magiblot/tvision/pull/185

+fv

5.3. If no action uses ESC key, it should always close current dialog/window

...tv
- bug in Open file window
https://github.com/magiblot/turbo/issues/91
PR: Fix ESC key behavior in Open File dialog
https://github.com/magiblot/tvision/pull/190
- exit hotkey is not Esc
https://github.com/magiblot/turbo/issues/58

...fv
- exit hotkey is not Esc

5.4. Clipboard working in all controls

...tv
input box bug
https://github.com/magiblot/tvision/issues/178
- copy by python script
https://github.com/magiblot/tvision/issues/191
in editor: +

...fv
- copy by python script
https://gitlab.com/freepascal.org/fpc/source/-/issues/41434
in editor: -

5.5. Misc

Navigation with arrow keys in TInputLine, fv
https://gitlab.com/freepascal.org/fpc/source/-/issues/41435

Ctrl+Arrows incorrectly behave on spaces in tv
https://github.com/magiblot/tvision/issues/193

TV/FV even have no mechanics to link top menu item to key code, not char code, if they differs.
Hotkey is defined as char from item name, like ~F~ile. So you can not link Файл to LatinA (same as Ф)
https://github.com/magiblot/tvision/issues/99#issuecomment-3395287967

---

FV issues:
https://gitlab.com/freepascal.org/fpc/source/-/issues?author_username=unxed

TV issues:
https://github.com/magiblot/tvision/issues?q=author%3Aunxed

turbo issues:
https://github.com/magiblot/turbo/issues?q=author%3Aunxed

