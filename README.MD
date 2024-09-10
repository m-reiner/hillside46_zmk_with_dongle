# Hillside 46 Ergonomic Keyboard with Dongle

![Hillside 46](https://github.com/m-reiner/hillside46_zmk_with_dongle/blob/main/images/hillside46_keyboard_halves_with_dongle.jpeg)

[![.github/workflows/build_hillside46_firmware.yml](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml/badge.svg)](https://github.com/m-reiner/hillside46_zmk_with_dongle/actions/workflows/build_hillside46_firmware.yml)

_**Hillside**_ is a collection of keyboards featuring 46, 48, 52, or 56 keys that were originally designed by [[mmccoyd]](https://github.com/mmccoyd/hillside).  Please check out their repo and Wiki for more information regarding ordering PCBs, building the keyboard, and so on.  This repo focuses on the 46-key variant of the Hillside [[mmccoyd/hillside46]](https://github.com/mmccoyd/hillside/tree/main/hillside46).  

Specifically, this is a version of the hillside46 that leverages ZMK firmware to facilitate wireless commumnication between the two halves of the split keyboard as well as an additional third microcontroller (MCU) to act as a "dongle".  The "dongle" MCU can be plugged into the USB port of a computer or phone (or connected via Bluetooth if externally powered), and will then communicate via Bluetooth Low Energy (BLE) to the two keyboard halves.  

The keymap definition file can be found in: [[.config/boards/shields/hillside46/hillside46.keymap]](config/boards/shields/hillside46/hillside46.keymap).

I am pursuing a wireless setup with a dongle for two primary reasons:
- My place of work has Bluetooth completely locked down, so creating a dongle MCU allows me to retain a completely wireless setup for the keyboard halves.
- Even when on a system where Bluetooth is not restricted, the keyboard half playing the "central" role (usually the left half) generally burns through battery life far faster than the non-central side.
    - Using a third MCU in the central role and (presumably) plugging it directly into the USB port of the machine with which you want to use your keyboard maximizes the battery life of both halves of the keyboard since they each just use a BLE connection to the "dongle" MCU.

Despite the keyboard being designed to use the nice!nano MCUs on the keyboard halves, I chose the Seeed Studio XIAO nRF52840 Sense as the dongle MCU due to its small size.  **Please ensure you are flashing the correct firmware to each board to avoid issues.**

As with all ZMK setups, pushing changes to any of the non-README files in this repo will automatically trigger a job to build the firmware for all three boards (dongle, left keyboard side, right keyboard side).

After making a change to a file, you can find the firmware build status and download the generated firmware by:

- Click on "Actions" at the top of this page to see the build triggered by that change.
- Wait for the build to finish
- Click on the build link next to the green checkbox
- Download the artifact file with the firmware
- See Installing The Firmware for more details from there.

## Case and Tenting

I created a very simple case for the Seeed Studio XIAO nRF52840, which can be found [[here]](https://www.printables.com/model/992291-seeed-studio-xiao-nrf52840-case-with-lid).

![Seeed Studio XIAO nRF52840 Case](https://raw.githubusercontent.com/m-reiner/hillside46_zmk_with_dongle/main/images/seeed_studio_xiao_nrf52840_case.jpeg)

I also designed a modified version of rmwphd's excellent case and cover for the Hillside 46, which can be found [[here]](https://www.printables.com/model/958628-hillside-46-case-with-magnetically-mounted-tenting).  

In my version, I created a tenting attachment with magnet holes, removed the threaded hole from the bottom of the original case model, and added spaces to insert magnets into the bottom of the case.  This allows a user to both magnetically attach the tenting model to the case bottom if you want to use this board with tenting, as well as magnetically attach the case halves (and tenting halves) to eachother for easier transport.

![Keyboard case base, lid, and tenting objects](https://raw.githubusercontent.com/m-reiner/hillside46_zmk_with_dongle/main/images/keyboard_case_components.jpeg)
