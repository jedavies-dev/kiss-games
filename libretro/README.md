# RetroArch & libRetro for KISS Linux

## Install

```
~ $ git clone https://github.com/sdsddsd1/kiss-games
~ $ export KISS_PATH=$KISS_PATH:$HOME/kiss-games/equipment
~ $ export KISS_PATH=$KISS_PATH:$HOME/kiss-games/libretro
~ $ kiss b retroarch
~ $ kiss i retroarch
```

The emulators, so called 'cores', start with `libretro-` followed by the  
corresponding name. Once installed, retroarch will pick them up.

```
~ $ kiss b libretro-$core
~ $ kiss i libretro-$core
```

## Usage

The user config file is located at:
```
~ $ $HOME/.config/retroarch/retroarch.cfg
```
Firmware goes inside:
```
~ $ $HOME/.config/retroarch/system/
```
Roms have no specified path and can live anywhere on the system. They are added  
inside the menu of retroarch.

 * `Import content -> Scan directory`

A more complete documentation can be found [here](https://docs.libretro.com).

## KISS way

The online updater is disabled as retroarch's buildsystem is targeted at `glibc`  
and therefore the whole suite is managed by the package manager. Only preview  
thumbnails are downloaded once at runtime.
