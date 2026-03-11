# ZMK CONFIG FOR THE LILY58

This repo is for the Splitkb Aurora Lily58 keyboard with Nice!Nano v2 with YADS (Yet Another Dongle Screen) configuration.
The main change between the yads repo and my repo is the usage of the central dongle unit. I couldn't manage to pair my left side to the dongle as it was configured on the yads repo.

Yads repo: https://github.com/janpfischer/zmk-dongle-screen

## BUILD CONFIGURATIONS

This repo builds the following firmware files:

| Artifact Name                          | Description                                            |
| -------------------------------------- | ------------------------------------------------------ |
| `splitkb-aurora-lily58-dongle-left`    | Left half configured as peripheral (for dongle setup)  |
| `splitkb-aurora-lily58-dongle-right`   | Right half configured as peripheral (for dongle setup) |
| `splitkb-aurora-lily58-ble-left`       | Left half with ZMK Studio support (BLE central)        |
| `splitkb-aurora-lily58-ble-right`      | Right half for BLE setup                               |
| `splitkb-aurora-lily58-dongle-yads`    | Dongle with YADS screen and ZMK Studio support         |
| `splitkb-aurora-lily58-settings-reset` | Settings reset firmware                                |

## HOW TO USE

### Setup with Dongle (YADS)

1. Fork this repo
2. `git clone` your repo to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [GitHub Desktop](https://desktop.github.com/))
3. Adjust the `config/splitkb_aurora_lily58.keymap` file (find all the keycodes on [the ZMK docs pages](https://zmk.dev/docs/codes/))
4. `git push` your changes to your fork
5. On the GitHub page of your fork navigate to "Actions"
6. Scroll down and unzip the `firmware.zip` archive that contains the latest firmware
7. Flash the dongle:
   - Connect the dongle to your PC, press reset twice
   - Drag'n'drop the `splitkb-aurora-lily58-dongle-yads-nice_nano_v2-zmk.uf2` file onto the storage device
8. Flash the left half:
   - Connect the left half, press reset twice
   - Drag'n'drop the `splitkb-aurora-lily58-dongle-left-nice_nano_v2-zmk.uf2` file onto the storage device
9. Flash the right half:
   - Connect the right half, press reset twice
   - Drag'n'drop the `splitkb-aurora-lily58-dongle-right-nice_nano_v2-zmk.uf2` file onto the storage device

### Setup with BLE (no dongle)

1. Flash the left half with `splitkb-aurora-lily58-ble-left-nice_nano_v2-zmk.uf2`
2. Flash the right half with `splitkb-aurora-lily58-ble-right-nice_nano_v2-zmk.uf2`

### Troubleshooting

If you have pairing issues, flash `splitkb-aurora-lily58-settings-reset-nice_nano_v2-zmk.uf2` on all devices to reset settings.
