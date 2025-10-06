
# bv
Some notes about terminal emulators

https://github.com/unxed/bv

All non-pluses should have a link to a relevant issue

---

1. Clip: Bracketed paste или OSC52 read или far2l read
+tvision
+fvision
+far2l
+gnometerm
+konsole
+kitty

2. Clip: OSC52 write или kitty write или far2l write
+tvision
+fvision
+far2l
...gnometerm
https://gitlab.gnome.org/GNOME/vte/-/issues/2495
+konsole
+kitty

3. Keyup events
...tvision
https://github.com/magiblot/tvision/issues/186
...fvision
https://gitlab.com/freepascal.org/fpc/source/-/issues/34190
+far2l
...gnometerm
https://gitlab.gnome.org/GNOME/vte/-/issues/2601
https://gitlab.gnome.org/GNOME/vte/-/issues/2764
https://gitlab.gnome.org/GNOME/vte/-/merge_requests/9
...konsole
https://bugs.kde.org/show_bug.cgi?id=484044
https://bugs.kde.org/show_bug.cgi?id=435975
https://invent.kde.org/utilities/konsole/-/merge_requests/1133
--> patches welcome in both :) 1st win32, its simplier and gnome is ready to accept it
+kitty

4. Full set of keys/combinations (e.g. Ctrl+Enter) support
+tvision
+fvision
+far2l
...gnometerm
https://gitlab.gnome.org/GNOME/vte/-/issues/2601
https://gitlab.gnome.org/GNOME/vte/-/merge_requests/9
...konsole
https://bugs.kde.org/show_bug.cgi?id=484044
https://bugs.kde.org/show_bug.cgi?id=435975
+kitty

5. Correct hotkey handling via (3): any lang, any layout, w/wo modifiers, inside menus and not

...tvision
no support for base layout key field
https://github.com/magiblot/turbo/issues/87
https://github.com/magiblot/turbo/issues/90
patch uploaded, needs testing after it:
https://github.com/magiblot/tvision/pull/184
on how it should work from users point of view (comparing to GTK, Qt, Windows):
https://github.com/magiblot/tvision/issues/99

...fvision
bug with getting layout independent key code in kitty
https://gitlab.com/freepascal.org/fpc/source/-/merge_requests/1138#note_2734741741
needs testing after it

6. UI/UX patterns following best software design practices

6.1. Navigation wia arrow keys

...tv patch uploaded
PR: Enable arrow keys for navigation
https://github.com/magiblot/tvision/pull/188

+fv

6.2. Open file window as in FreeVision

...tv patch uploaded
https://github.com/magiblot/tvision/pull/185

+fv
minor (mr ready)
https://gitlab.com/freepascal.org/fpc/source/-/issues/41433

6.3. If no action uses ESC key, it should always close current dialog/window

...tv
- bug in Open file window
https://github.com/magiblot/turbo/issues/91
PR: Fix ESC key behavior in Open File dialog
https://github.com/magiblot/tvision/pull/190
- exit hotkey is not Esc
https://github.com/magiblot/turbo/issues/58

...fv
a bug with KeyDown->ESC in "Chosen file" field
https://gitlab.com/freepascal.org/fpc/source/-/issues/41430
- exit hotkey is not Esc

6.4. Clipboard working in all controls

...tv
input box bug
https://github.com/magiblot/tvision/issues/178
- copy by python script
https://github.com/magiblot/tvision/issues/191
in editor: +

...fv
- input line bugs
https://gitlab.com/freepascal.org/fpc/source/-/issues/41278
https://gitlab.com/freepascal.org/fpc/source/-/issues/41281
https://gitlab.com/freepascal.org/fpc/source/-/issues/41432
- copy by python script
https://gitlab.com/freepascal.org/fpc/source/-/issues/41434
in editor: -

---

FV issues:
https://gitlab.com/freepascal.org/fpc/source/-/issues?author_username=unxed

TV issues:
https://github.com/magiblot/tvision/issues?q=author%3Aunxed

turbo issues:
https://github.com/magiblot/turbo/issues?q=author%3Aunxed

