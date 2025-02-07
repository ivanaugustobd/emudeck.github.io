# Rosalie's Mupen GUI (RMG) is a Nintendo 64 Emulator.

Github: [https://github.com/Rosalie241/RMG](https://github.com/Rosalie241/RMG)

**This page is for Rosalie's Mupen GUI, a standalone N64 emulator. This page is not for the Mupen64Plus-Next RetroArch core. For more information on RetroArch and the Mupen64Plus-Next RetroArch core, visit the [RetroArch Page](../steamos/retroarch.md).**

***

## RMG Table of Contents

1. [Getting Started with RMG](#getting-started-with-rmg)
    - [Configuration](#rmg-configuration)
    - [How to Update RMG](#how-to-update-rmg)
    - [How to Launch RMG in Desktop Mode](#how-to-launch-rmg-in-desktop-mode)
    - [File Formats](#rmg-file-formats)
    - [Hotkeys](#rmg-hotkeys)

2. [RMG Tips and Tricks](#rmg-tips-and-tricks)
    - [How to Install Custom Textures](#how-to-install-custom-textures)
    - [How to Configure VRU](#how-to-configure-vru)
 
***

## Getting Started with RMG
[Back to the Top](#rmg-table-of-contents)

RMG is a fairly straight-forward emulator to set up. If you are strictly playing Nintendo 64 ROMs, place your ROMs in `Emulation/roms/n64`. No additional setup is required. Read the [Configuration](#rmg-configuration) section to learn more about RMG and its folder locations. 

To launch your ROMs in game mode, use Steam ROM Manager and use one of the following parsers to play your N64 ROMs:

* `EmulationStation-DE`
* `Nintendo 64 - RMG` 
* `Emulators`

***

### RMG Configuration
[Back to the Top](#rmg-table-of-contents)

* Type of Emulator: Flatpak
* Config Location: `/home/deck/.var/app/com.github.Rosalie241.RMG`
* Nintendo 64 ROM Location: `Emulation/roms/n64`
* Nintendo 64DD ROM Location: `Emulation/roms/n64dd`
* Nintendo 64DD BIOS Location: `Emulation/bios`
    * Nintendo 64DD BIOS: 
        * `64DD_IPL_US.n64`
        * `64DD_IPL_JP.n64`
        * `64DD_IPL_DEV.n64`
        * **Note:** These BIOS are only required if you are playing Nintendo 64DD games. These BIOS are not required for base Nintendo 64 games
* Saves: `Emulation/saves/RMG/saves`
* Savestates: `Emulation/saves/RMG/states`
* Storage Location: `Emulation/storage/RMG`
    * Contains the following folders: 
        * `Emulation/storage/RMG/cache`
        * `Emulation/storage/RMG/HiResTextures`
        * `Emulation/storage/RMG/screenshots`

**Note:** `~/.var` is an invisible folder by default. In Dolphin (file manager), click the hamburger menu in the top right, click `Show Hidden Files` to see these folders.

#### Works With
* Steam ROM Manager
* EmulationStation-DE

***

### How to Update RMG
[Back to the Top](#rmg-table-of-contents)

**How to Update RMG**

* Update through `Discover` (Shopping bag icon)
* Through the `Update your Emulators & Tools` section on the `Manage Emulators` page in the `EmuDeck` application


***

### How to Launch RMG in Desktop Mode
[Back to the Top](#rmg-table-of-contents)

**How to Launch RMG in Desktop Mode**

* Launch `Rosalie's Mupen GUI` from the Applications Launcher (Steam Deck icon in the bottom left of the taskbar)
* Launch the script from `Emulation/tools/launchers`, `rosaliesmupengui.sh`
* Launch the emulator from `Steam` after adding it via the `Emulators` parser in `Steam ROM Manager`


***

### RMG File Formats
[Back to the Top](#rmg-table-of-contents)

* .bin
* .n64
* .ndd
* .u1
* .v64
* .z64
* .zip

***

### RMG Hotkeys
[Back to the Top](#rmg-table-of-contents)

RMG comes with a Steam Input profile for Hotkeys. Activate the Steam Input profile by clicking the `Game Controller` icon in `Game Mode`, change the template to `Emudeck - RMG`. The hotkeys below can only be used if you have the Steam Input profile active.

**Long Press** to activate hotkeys on the left trackpad radial menu. 

| Hotkey         | EmulationStation-DE       |
|----------------|---------------------------|
| Quick Menu     | Left Trackpad Radial Menu |
| Save State     | Left Trackpad Radial Menu |
| Save State Menu| Left Trackpad Radial Menu |
| Load State     | Left Trackpad Radial Menu |
| Pause          | Left Trackpad Radial Menu |
| Cheats         | Left Trackpad Radial Menu |
| Controller Menu| Left Trackpad Radial Menu |
| Graphics Menu  | Left Trackpad Radial Menu |
| Screenshot     | Left Trackpad Radial Menu |
| Stop Emulation | Left Trackpad Radial Menu |
| Reset          | Left Trackpad Radial Menu |

**Note:** 

* [How to Select a Steam Input Profile](../../emudeck-essentials/steamos/hotkeys.md#how-to-select-a-steam-input-profile)
* [Steam Deck Button Layout](../../emudeck-essentials/steamos/hotkeys.md#steam-deck-button-layout)

***

## RMG Tips and Tricks
[Back to the Top](#rmg-table-of-contents)

***

### How to Install Custom Textures
[Back to the Top](#rmg-table-of-contents)

#### Preface

HTS & HTC are cache formats. PNG is the 'source' of the texture packs before it's converted to a cache file.

Before installing a texture pack, you will need to determine if it is HTC, HTS, or PNG. This can usually be confirmed by checking the file extension or reading the attached documentation. Follow the respective section below for installing texture packs.

#### Keep in Mind

* This section specifically requires the GLideN64 plugin. GLideN64 is the default graphics plugin if you are using EmuDeck settings 
* Texture packs are placed in the various subfolders within `Emulation/storage/RMG`
    * This folder contains the following sub-folders:
        * `cache`
            * `cache` is for HTC and HTS texture packs 
        * `HiResTextures`   
            * `HiResTextures` is for PNG texture packs

#### How to Install Custom Textures

##### HTC

1. Open the `Emulation/storage/RMG/cache` folder
2. Place your texture pack file directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Make sure `Use file storage instead of memory cache` is unchecked
    * <img src="https://user-images.githubusercontent.com/108900299/220504844-73ad1aae-9525-4e07-aa46-a47bcf953a8e.png" height="300">
    * This setting is unchecked by default

##### HTS

1. Open the `Emulation/storage/RMG/cache` folder
2. Place your texture pack file directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Check `Use file storage instead of memory cache`
    * <img src="https://user-images.githubusercontent.com/108900299/220504446-d29fc261-9194-43ee-ba19-2c15562ac716.png" height="300">
    * **Note:** To save this setting on a per game basis, you can open the graphics settings while in-game and it will save to the per-game profile

##### PNG

This section goes over enabling `file storage instead of memory cache` in RMG's settings. This is optional, but recommended. 

1. Open the `Emulation/storage/RMG/HiResTextures` folder
2. Place your texture pack folder directly into this folder
3. Open RMG
4. Click `Settings` at the top, select `Graphics`
5. Click the `Texture enhancement` tab
6. Check `Use file storage instead of memory cache`
    * <img src="https://user-images.githubusercontent.com/108900299/220504446-d29fc261-9194-43ee-ba19-2c15562ac716.png" height="300">
    * **Note:** To save this setting on a per game basis, you can open the graphics settings while in-game and it will save to the per-game profile


***

### How to Configure VRU
[Back to the Top](#rmg-table-of-contents)

The VRU (Voice Recognition Unit) was a peripheral for the Nintendo 64 that allowed you to use a microphone in "Hey You, Pikachu!" and "Densha de Go! 64". 

Since the Steam Deck comes with an internal built in microphone, you can use the Steam Deck's microphone to utilize VRU in Rosalie's Mupen GUI.

**Note:** Make sure Rosalie's Mupen GUI is up to date. VRU support was added in v0.4.2, on July 7th, 2023. 

#### How to Set up VRU

1. Open RMG
2. Open the `Input` settings under the `Settings` tab at the top
3. Click on `Player 4`
4. Change the `Input Device` to `Voice Recognition Unit`
    * ![RMG VRU](../../assets/rmg-vru.png) 
5. Click `OK` in the bottom right
6. VRU is now enabled

***