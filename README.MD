# Hillside 46 Ergonomic Keyboard with Dongle

![Hillside 46](https://github.com/m-reiner/hillside46_zmk_with_dongle/blob/main/images/hillside46_wireless.jpeg)

**Hillside** is a collection of keyboards featuring 46, 48, 52, or 56 keys that were originally designed by [[mmccoyd]](https://github.com/mmccoyd/hillside).  Please check out their repo and Wiki for more information regarding ordering PCBs, building the keyboard, and so on.

This repo focuses on the 46-key variant of the Hillside ([[mmccoyd/hillside46]](https://github.com/mmccoyd/hillside/tree/main/hillside46).  

Specifically, this is a version that leverages ZMK firmware for wireless commumnication between the two halves of the split keyboard with the addition of a third microcontroller (MCU) to act as a "dongle" that can be plugged into USB to a computer (or connected via Bluetooth if externally powered) and will then communicate via Bluetooth Low Energy (BLE) to the two keyboard halves.

I am pursuing a wireless setup with a dongle for two primary reasons:
- My place of work has Bluetooth completely locked down, so creating a dongle MCU allows me to retain a completely wireless setup for the keyboard halves.
- Even when on a system where Bluetooth is not restricted, the keyboard half playing the "central" role (usually the left half) generally burns through battery life far faster than the non-central side.
    - Using a third MCU in the central role and (presumably) plugging it directly into the USB port of the machine with which you want to use your keyboard maximizes the battery life of both halves of the keyboard since they each just use a BLE connection to the "dongle" MCU.

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
