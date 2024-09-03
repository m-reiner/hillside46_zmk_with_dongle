This is the ZMK firmware for my versionof the Hillside46 split keyboard, including my modifications for use with a third MCU to be used as a "dongle".

The keymap definition file can be found in ./config:

    Hillside 46 with 3x6+5 keys

As with all ZMK setups, pushing changes to any of the files in this repo will automatically trigger a job to build the firmware for all three boards (dongle, left keyboard side, right keyboard side).

After making a change to a file, you can find the firmware build status by:

    Click on "Actions" at the top of this page to see the build triggered by that change.
    Wait for the build to finish
    Click on the build link next to the green checkbox
    Download the artifact file with the firmware
    See Installing The Firmware for more details from there.

My Hillside keymap can be found in:

    ./config/hillside46.keymap
