# Vita Plugin Linux loader

## What's this?

This is an application for checking and downloading the files you need to load the [Linux kernel on your PS Vita](https://github.com/xerpi/linux_vita).

[Xepri's original repository.](https://bitbucket.org/xerpi/vita_plugin_loader/src/master/)

[Improvements and userfriendly interface from CreepNT.](https://github.com/xerpi/vita-linux-loader/pull/2/)

## File paths

By default, all necessary files will be expected in the path `ux0:linux/*`, namely:

- `ux0:linux/baremetal-loader.skprx` - `main.c:14`;
- `ux0:linux/payload.bin` - `main.c:15`;
- `ux0:linux/zImage` - `main.c:116` (only check availability, not loading on the plugin side);
- `ux0:linux/vita.dtb` - `main.c:117` (only check availability, not loading on the plugin side).

You can change any of these paths if you wish.

> :warning: If you use [SD2VITA](https://github.com/xyzz/gamecard-microsd), copy all necessary files and `uma0:` (to the [official PS Vita SD card](https://wiki.henkaku.xyz/vita/Memory_Card)).

## Build

1. Make sure that you have [`cmake`](https://cmake.org/) installed.
2. Make sure you have [VitaSDK](https://vitasdk.org/) installed and configured (try [vdpm](https://github.com/vitasdk/vdpm)).
3. Build the project with the following commands:

   ```bash
   mkdir build && cd build
   cmake .. && make -j
   ```

## Credits

Thanks to everybody, who contributed to the launch of the Linux kernel on PS Vita:

- [xerpi](https://github.com/xerpi);
- [Team Molecule](https://twitter.com/teammolecule) (formed by [Davee](https://twitter.com/DaveeFTW), Proxima, [xyz](https://twitter.com/pomfpomfpomf3), and [YifanLu](https://twitter.com/yifanlu));
- [TheFloW](https://twitter.com/theflow0)
- [motoharu](https://github.com/motoharu-gosuto)
- verybody at the [HENkaku](https://discord.gg/m7MwpKA) Discord channel;
- [CreepNT](https://github.com/CreepNT) for improvements to this app.
