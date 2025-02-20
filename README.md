# libretro-pcsx2-launcher

![pcsx2](https://github.com/new-penguin/libretro-pcsx2-launcher-antimicrox/assets/139792946/6ab78f2f-0db3-4841-b8b9-c60c318b4120)



Based on [libretro-dolphin-launcher](https://github.com/RobLoach/libretro-dolphin-launcher).

Launch Sony PlayStation 2 games through [PCSX2](https://pcsx2.net/), directly from [RetroArch](http://www.libretro.com/) with full controller support using [antimicrox](https://github.com/AntiMicroX/antimicrox/).


## Installation

Download the Linux core from releases and skip to step 2 or...

1. Compile the core
  ``` bash
  git clone https://github.com/new-penguin/libretro-pcsx2-launcher-antimicrox.git
  cd libretro-pcsx2-launcher-antimicrox
  make
  ```

2. Copy the core file to the RetroArch cores directory. For example, to copy to the default core directory
  ``` bash
  cp pcsx2_launcher_libretro.so /usr/lib/libretro/pcsx2_launcher_libretro.so
  cp pcsx2_launcher_libretro.info /usr/share/libretro/info/pcsx2_launcher_libretro.info
  ```

3. Make sure [PCSX2](https://pcsx2.net/) [is installed](https://pcsx2.net/download.html) as well as [antimicrox](https://github.com/AntiMicroX/antimicrox/) via your distro's repo. If not, you have the option to use the flatpak or appimage versions. You should be able to run both of the following commands:

  ``` bash
  PCSX2
  antimicrox
  ```
  or via flatpak
  
  ```
  flatpak run net.pcsx2.PCSX2
  flatpak run io.github.antimicrox.antimicrox
  ```
You can also use the appimage versions of the respective programs. Just copy both to your ~/.config/retroarch/system folder and make sure they're named pcsx2.AppImage and antimicrox.AppImage. Also don't forget to make them executable.

## Usage

1. Scan Sony PlayStation 2 games in RetroArch

2. Associate your games with the Sony - Playstation 2 (PCSX2 Launcher) core

3. Configure antimicrox to use your distro's 'close window' binding to your controller button preference. Or you can use my pre-configured controller mappings [here](https://ufile.io/9t4vnq6m) for the 360 and Xbox One controllers. Place in your user ~/ directory. In the provided examples I've mapped LS click + RS click to exit PCSX2.
  
3. And once done you should be able to launch and switch games directly from the RetroArch menu

3. Alternatively, you can run games through the command line
  ``` bash
  retroarch -L pcsx2_launcher_libretro.so Crash.iso
  ```

## Contributors

- [Rob Loach](http://github.com/robloach)
- [Alcaro](https://github.com/Alcaro)
- [Eduardo Mozart de Oliveira](https://github.com/coldscientist)
