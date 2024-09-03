# Hillside 46 Ergonomic Keyboard with Dongle

Build status:

[![.github/workflows/build_hillside46_firmware.yml](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml/badge.svg)](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml)

**Hillside** is a collection of different keyboards and keypads that were originally designed by [[mmccoyd]](https://github.com/mmccoyd/hillside). This repo contains ZMK firmware for the smallest version, the [[mmccoyd/hillside46]](https://github.com/mmccoyd/hillside).  Please check out their original repo to find the PCB layouts and review their WiKi for build and other instructions if you want to make one of your own.

This is the ZMK firmware for my versionof the Hillside46 split keyboard, including my modifications for use with a third MCU to be used as a "dongle".

The keymap definition file can be found in: [[.config/boards/shields/hillside46/hillside46.keymap]](config/boards/shields/hillside46/hillside46.keymap).

As with all ZMK setups, pushing changes to any of the files in this repo will automatically trigger a job to build the firmware for all three boards (dongle, left keyboard side, right keyboard side).

After making a change to a file, you can find the firmware build status by:

- Click on "Actions" at the top of this page to see the build triggered by that change.
- Wait for the build to finish
- Click on the build link next to the green checkbox
- Download the artifact file with the firmware
- See Installing The Firmware for more details from there.

My Hillside keymap can be found in:

    ./config/hillside46.keymap
