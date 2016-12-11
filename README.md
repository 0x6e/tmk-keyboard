# tmk-keyboard

A repository storing just the things I need for my keyboard. It is based on
[tmk_keyboad](https://github.com/tmk/tmk_keyboard) but contains only the things
I need for my GH60 based keyboard.

## Setup
This project requires the following dependencies, both of which were available
through [Homebrew](http://brew.sh/) for macOS:
* [avr-gcc](http://www.nongnu.org/avr-libc/)

        $ brew tap osx-cross/avr
        $ brew install avr-libc

* [dfu-programmer](https://dfu-programmer.github.io/)

        $ brew install dfu-programmer

After cloning tmk-keyboard, you will need to initialise the
[tmk_core](https://github.com/tmk/tmk_core) submodule:

    $ git submodule init
    $ git submodule update

## Build
To build the firmware just run `make`:

    $ make

## Flash
You will to install  to flash the PCB.

Run `make dfu` to flash the firmware (this may need to be done using `sudo`):

    $ make dfu

## Keymaps
The default keymap is [keymap_poker.c](keymap_poker.c) from the original
[tmk_keyboad](https://github.com/tmk/tmk_keyboard/tree/master/keyboard/gh60)
firmware.

To add create your own keymap, create and configure your new keymap in a file
called `keymap_<keymap-name>.c`. Build and flash with the following commands:

    $ make KEYMAP=<keymap-name>
    $ make dfu KEYMAP=<keymap-name>
