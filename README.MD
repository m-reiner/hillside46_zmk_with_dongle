# Hillside 46 Ergonomic Keyboard with Dongle

(https://github.com/m-reiner/hillside46_zmk_with_dongle/blob/main/images/hillside46_wireless.jpeg)

**Hillside** is a collection of keyboards featuring 46, 48, 52, or 56 keys that were originally designed by [[mmccoyd]](https://github.com/mmccoyd/hillside).  Please check out their repo and Wiki for more information regarding ordering PCBs, building the keyboard, and so on.

This repo focuses on the 46-key variant of the Hillside ([[mmccoyd/hillside46]](https://github.com/mmccoyd/hillside)).  Specifically, this is a version that leverages ZMK firmware for wireless commumnication between the two halves of the split keyboard with the addition of a third microcontroller (MCU) to act as a "dongle" that can be plugged into USB (or connected via Bluetooth if externally powered) to a computer and will then communicate via Bluetooth Low Energy (BLE) to the two keyboard halves.

Current build status:

[![.github/workflows/build_hillside46_firmware.yml](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml/badge.svg)](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml)

The keymap definition file can be found in: [[.config/boards/shields/hillside46/hillside46.keymap]](config/boards/shields/hillside46/hillside46.keymap).

As with all ZMK setups, pushing changes to any of the non-README files in this repo will automatically trigger a job to build the firmware for all three boards (dongle, left keyboard side, right keyboard side).

After making a change to a file, you can find the firmware build status and download the generated firmware by:

- Click on "Actions" at the top of this page to see the build triggered by that change.
- Wait for the build to finish
- Click on the build link next to the green checkbox
- Download the artifact file with the firmware
- See Installing The Firmware for more details from there.

My Hillside keymap can be found in:

    ./config/hillside46.keymap
