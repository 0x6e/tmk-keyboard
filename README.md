# tmk-keyboard
To build the firmware just run `make` like:

    $ make

You will to install [dfu-programmer](https://dfu-programmer.github.io/) to flash the PCB.

Run `make dfu` to flash the firmware. This may need to be done using `sudo`.

## keymaps
The default keymap is [keymap_poker.c](keymap_poker.c) from the original [tmk_keyboad](https://github.com/tmk/tmk_keyboard/tree/master/keyboard/gh60) firmware. _It currently doesn't work perfectly, but is enough to get started._
