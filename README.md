# kb-hotkeys
Map linux hotkeys to mimic POK3R's caps lock function key functionality through xmodmap.

Use command line tool `xev` to find keycodes and key names to add to or change existing new_keys.

### new_keys

```
keycode 66 = Mode_switch

keycode 31 = i I Up
keycode 45 = k K Down
keycode 44 = j J Left
keycode 46 = l L Right

keycode 30 = u U Prior
keycode 32 = o O Next
keycode 43 = h H Home
keycode 57 = n N End
keycode 9 = Escape asciitilde grave
keycode 22 = BackSpace BackSpace Delete
```
The `setup.sh` script will handle placing the necessary files, and calling the correct commands. All it's doing is placing a
xmodmap.desktop file into your autostart directory, so the keybindings are set on start up, creating a ~/.config/kb-hotkeys directory
to place the new_keys config file, and then calling the actual `xmodmap ~/.config/kb-hotkeys/new_keys` command to set your hotkeys.
