Start by opening [Mini vMac](./Mini\ vMac.app) on osx, or `./minivmac` on linux.

Once the emulator is running, dry out the "Draw Me" application!

### mini vmac

   This repo contains an custom version of minivmac, modified to redraw the entire screen on mousemove by jedahan.
   Otherwise, there are crazy artifacts everywhere on linux.
   The modified source is in the `src/` directory. It should really be version controlled at some point...

   The most relevant file is MYOSGLUE.c :)

### src/system

   There is disk1of2.sea and disk2of2.sea. These are self-extracting archives that used to be hosted on
   apple.com/oldsoftware.html , but apple silently pulled them. Required for making a system additions
   disk, which is required to install system 6 on a hard drive.

#### Disks

   * `disk1.dsk`

   This is a fresh startup disk for system 6.0.8

   * `disk2.dsk`

   This houses hypercard 2.1, and the bard stacks. Its a 20mb 'hard drive' where development is done

   * hypercard/

    All of these images were dumped using a [kryoflux] from the original disks. If you do not own a copy of the original,
    please do not use these images.

   `hypercard.img` Hypercard 1.0, can create and play cards

   `hypercard2.img` Hypercard 2.0, player only. Claris split the player and development version.

   `hypercard2.11.img` Hypercard 2.11 development kit. Full hypercard. Latest version that can run on system 6.

   * system/

   `system_utilities.dsk` Useful utilities

   `system_startup.dsk` Boot off of here if you want

   `system_additions.dsk` Required when installing System 6 to a new hard drive

   * utilities/

   This folder contains the original source disks for utilties made specifically to work with minivmac - 
   importfl, exportfl, and binunpack.

#### Utilities

  There are two utilities in the system_utilities.dsk disk image - ImportFl, and ExportFl. These let you
  move files between the host operating system and your system6 disk. Drag'n'drop works, as does the menu entries.
  Files will be places in the `out/` folder with ExportFl.
