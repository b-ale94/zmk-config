

# ZMK CONFIG FOR THE LILY58

This repo is for the SPlitkb lily58 keyboard with nice nano v2 with YADS (yet another dongle screen) configuration.
The main change between the yads repo and my repo is the usage of the central dongle unit. I couldn't manage to pair my lef side to the dongle as it was configured on the yads repo.
Ble firmware probably doesn't work correctly since my intend was to make this work donglefully :D

Yads repo: https://github.com/janpfischer/zmk-dongle-screen

## HOW TO USE

- fork this repo
- `git clone` your repo, to create a local copy on your PC (you can use the [command line](https://www.atlassian.com/git/tutorials) or [github desktop](https://desktop.github.com/))
- adjust the totem.keymap file (find all the keycodes on [the zmk docs pages](https://zmk.dev/docs/codes/))
- `git push` your repo to your fork
- on the GitHub page of your fork navigate to "Actions"
- scroll down and unzip the `firmware.zip` archive that contains the latest firmware
- connect the left half of the TOTEM to your PC, press reset twice
- the keyboard should now appear as a mass storage device
- drag'n'drop the `totem_left-seeeduino_xiao_ble-zmk.uf2` file from the archive onto the storage device
- repeat this process with the right half and the `totem_right-seeeduino_xiao_ble-zmk.uf2` file.
