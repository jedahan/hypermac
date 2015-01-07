How to run:

    ./minivmac system608.dsk 020M.dsk


Now try running "Hard Drive" "Bard Stacks" "Draw Me"

### mini vmac

   This repo contains an custom version of minivmac jedahan made, to redraw the entire screen on mousemove.
   Otherwise, there are crazy artifacts everywhere on linux.
   The modified source is in the `src/` directory. It should really be version controlled at some point...

   The most relevant file is MYOSGLUE.c :)


### src/system

   There is disk1of2.sea and disk2of2.sea. These are self-extracting archives that used to be hosted on
   apple.com/oldsoftware.html , but apple silently pulled them. Required for making a system additions
   disk, which is required to install system 6 on a hard drive.

#### Disks

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

   * `020M.dsk`

   This is the current working image. Latest development is done here.

   * utilities/

   This folder contains the original source disks for utilties made specifically to work with minivmac - 
   importfl, exportfl, and binunpack.

#### Utilities

  There are two utilities in the system_utilities.dsk disk image - ImportFl, and ExportFl. These let you
  move files between the host operating system and your system6 disk. Drag'n'drop works, as does the menu entries.
  Files will be places in the `out/` folder with ExportFl.
