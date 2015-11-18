====================
Firmware kompilieren
====================

.. contents::
   :local:

****************************************
Repository klonen, OpenWrt konfigurieren
****************************************

OpenWrt package feed for the Enigmabox software suite.

How to build that stuff::

    $ git clone https://github.com/enigmagroup/openwrt.git
    $ cd openwrt

    $ vi feeds.conf

Your feeds.conf should look like this::

    src-git packages https://github.com/enigmagroup/openwrt-packages.git
    src-git oldpackages https://github.com/enigmagroup/openwrt-oldpackages.git
    src-git management https://github.com/enigmagroup/openwrt-management.git
    src-git routing https://github.com/enigmagroup/openwrt-routing.git
    src-git telephony https://github.com/enigmagroup/openwrt-telephony.git

    src-git enigmabox https://github.com/enigmagroup/enigmabox-openwrt.git

Next use that package system to incorporate the Enigmabox software suite::

    $ ./scripts/feeds update -a
    $ ./scripts/feeds install -a

*******************
Image konfigurieren
*******************

Then configure for your system::

    $ make menuconfig

Building firmware for the Banana Pi
===================================

"Target System": Allwinner A1x/A20/A3x

"Target Profile": Bananapi

"Target Images": configure as you please. Example:

  * Root filesystem images:

    * ext4: yes

      * Maximum number of inodes in root filesystem: 200000
      * Create a journaling filesystem: yes

    * GZip images: no

  * Image Options:

    * Root filesystem partition size (in MB): 3600
    * Include kernel in root filesystem: yes
    * Include DTB in root filesystem: yes

Recently, OpenWrt decided to switch to musl by default.

Stick to uClibc manually:

"Advanced configuration options":

  * Toolchain Options

    * C Library implementation

      * Use uClibc

"Enigmabox":

  * cfengine-promises: yes

    * Network profile: Rasperry Pi

  * provision-grandstream: yes
  * roundcube: yes
  * teletext: yes
  * webinterface: yes

The "webinterface" is the most important part, since it's selecting all required dependencies.

Quit and save your .config

Build::

    $ make

After about 30mins (depending on your machine), your image is ready::

    bin/sunxi-uClibc/openwrt-sunxi-Bananapi-sdcard-vfat-ext4.img

Building firmware for the PC Engines APU (64-bit Enigmabox)
============================================================

"Target System": x86

"Subtarget": x86_64

"Target Profile": Default

"Target Images": configure as you please. Example:

  * Root filesystem images:

    * ext4: yes

      * Maximum number of inodes in root filesystem: 200000
      * Create a journaling filesystem: yes

    * GZip images: no

  * Image Options:

    * Root filesystem partition size (in MB): 3600
    * Include kernel in root filesystem: yes

Recently, OpenWrt decided to switch to musl by default.

Stick to uClibc manually:

"Advanced configuration options":

  * Toolchain Options

    * C Library implementation

      * Use uClibc

"Enigmabox":

  * cfengine-promises: yes

    * Network profile: APU

  * provision-grandstream: yes
  * roundcube: yes
  * teletext: yes
  * webinterface: yes

The "webinterface" is the most important part, since it's selecting all required dependencies.

Quit and save your .config

Build::

    $ make

After about 30mins (depending on your machine), your image is ready::

    bin/x86-uClibc/openwrt-x86-64-combined-ext4.img

Building firmware for the PC Engines ALIX (32-bit Enigmabox)
============================================================

"Target System": x86

"Subtarget": Generic

"Target Profile": Default

"Target Images": configure as you please. Example:

  * Root filesystem images:

    * ext4: yes

      * Maximum number of inodes in root filesystem: 200000
      * Create a journaling filesystem: yes

    * GZip images: no

  * Image Options:

    * Root filesystem partition size (in MB): 3600
    * Include kernel in root filesystem: yes

Recently, OpenWrt decided to switch to musl by default.

Stick to uClibc manually:

"Advanced configuration options":

  * Toolchain Options

    * C Library implementation

      * Use uClibc

"Enigmabox":

  * cfengine-promises: yes

    * Network profile: ALIX

  * provision-grandstream: yes
  * roundcube: yes
  * teletext: yes
  * webinterface: yes

The "webinterface" is the most important part, since it's selecting all required dependencies.

Quit and save your .config

Build::

    $ make

After about 30mins (depending on your machine), your image is ready::

    bin/x86-uClibc/openwrt-x86-generic-combined-ext4.img

