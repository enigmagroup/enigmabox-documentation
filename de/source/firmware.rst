.. _firmware:

====================
Firmware kompilieren
====================

.. contents::
   :local:

****************************************
Repository klonen, OpenWrt konfigurieren
****************************************

Klone das OpenWrt-Repository via Git::

    $ git clone https://github.com/enigmagroup/openwrt.git
    $ cd openwrt

    $ vi feeds.conf

Deine feeds.conf sollte so aussehen::

    src-git packages https://github.com/enigmagroup/openwrt-packages.git
    src-git oldpackages https://github.com/enigmagroup/openwrt-oldpackages.git
    src-git management https://github.com/enigmagroup/openwrt-management.git
    src-git routing https://github.com/enigmagroup/openwrt-routing.git
    src-git telephony https://github.com/enigmagroup/openwrt-telephony.git

    src-git enigmabox https://github.com/enigmagroup/enigmabox-openwrt.git

Aktualisiere die Paketliste und installiere alle benötigten Pakete::

    $ ./scripts/feeds update -a
    $ ./scripts/feeds install -a

*******************
Image konfigurieren
*******************

Starte die Imagekonfiguration mit::

    $ make menuconfig

Firmware kompilieren für den Banana Pi
======================================

  * Target System: Allwinner A1x/A20/A3x
  * Target Profile: Bananapi
  * Target Images:
  
    * Root filesystem images:
  
      * ext4: yes
  
        * Maximum number of inodes in root filesystem: 200000
        * Create a journaling filesystem: yes
  
      * GZip images: no
  
    * Image Options:
  
      * Root filesystem partition size (in MB): 3600
      * Include kernel in root filesystem: yes
      * Include DTB in root filesystem: yes

Die OpenWrt Entwickler haben entschieden, standardmässig die musl-Bibliothek zu nutzen. Die Software der Enigmabox setzt noch auf uClibc. Wähle diese explizit aus:

  * Advanced configuration options:
  
    * Toolchain Options
  
      * C Library implementation
  
        * Use uClibc

Konfiguration der Enigmabox-Pakete:

  * "Enigmabox":
  
    * cfengine-promises: yes
  
      * Network profile: Rasperry Pi
  
    * provision-grandstream: yes
    * roundcube: yes
    * teletext: yes
    * webinterface: yes

"webinterface" ist der wichtigste Teil, da dieses Paket automatisch alle benötigten Abhängigkeiten selektiert.

Beende die Imagekonfiguration und speichere deine .config.

Kompilierungsvorgang starten::

    $ make

Nach ungefähr 30min (je nach Leistungsfähigkeit deines Rechners) ist das Image bereit::

    bin/sunxi-uClibc/openwrt-sunxi-Bananapi-sdcard-vfat-ext4.img

Firmware kompilieren für die PC Engines APU (64-bit Enigmabox)
==============================================================

  * Target System: x86
  * Subtarget: x86_64
  * Target Profile: Default
  * Target Images:
  
    * Root filesystem images:
  
      * ext4: yes
  
        * Maximum number of inodes in root filesystem: 200000
        * Create a journaling filesystem: yes
  
      * GZip images: no
  
    * Image Options:
  
      * Root filesystem partition size (in MB): 3600
      * Include kernel in root filesystem: yes

Die OpenWrt Entwickler haben entschieden, standardmässig die musl-Bibliothek zu nutzen. Die Software der Enigmabox setzt noch auf uClibc. Wähle diese explizit aus:

  * Advanced configuration options:
  
    * Toolchain Options
  
      * C Library implementation
  
        * Use uClibc

Konfiguration der Enigmabox-Pakete:

  * "Enigmabox":
  
    * cfengine-promises: yes
  
      * Network profile: APU
  
    * provision-grandstream: yes
    * roundcube: yes
    * teletext: yes
    * webinterface: yes

"webinterface" ist der wichtigste Teil, da dieses Paket automatisch alle benötigten Abhängigkeiten selektiert.

Beende die Imagekonfiguration und speichere deine .config.

Kompilierungsvorgang starten::

    $ make

Nach ungefähr 30min (je nach Leistungsfähigkeit deines Rechners) ist das Image bereit::

    bin/x86-uClibc/openwrt-x86-64-combined-ext4.img

Firmware kompilieren für das PC Engines ALIX (32-bit Enigmabox)
===============================================================

  * Target System: x86
  * Subtarget: Generic
  * Target Profile: Default
  * Target Images:
  
    * Root filesystem images:
  
      * ext4: yes
  
        * Maximum number of inodes in root filesystem: 200000
        * Create a journaling filesystem: yes
  
      * GZip images: no
  
    * Image Options:
  
      * Root filesystem partition size (in MB): 3600
      * Include kernel in root filesystem: yes

Die OpenWrt Entwickler haben entschieden, standardmässig die musl-Bibliothek zu nutzen. Die Software der Enigmabox setzt noch auf uClibc. Wähle diese explizit aus:

  * Advanced configuration options:
  
    * Toolchain Options
  
      * C Library implementation
  
        * Use uClibc

Konfiguration der Enigmabox-Pakete:

  * "Enigmabox":
  
    * cfengine-promises: yes
  
      * Network profile: ALIX
  
    * provision-grandstream: yes
    * roundcube: yes
    * teletext: yes
    * webinterface: yes

"webinterface" ist der wichtigste Teil, da dieses Paket automatisch alle benötigten Abhängigkeiten selektiert.

Beende die Imagekonfiguration und speichere deine .config.

Kompilierungsvorgang starten::

    $ make

Nach ungefähr 30min (je nach Leistungsfähigkeit deines Rechners) ist das Image bereit::

    bin/x86-uClibc/openwrt-x86-generic-combined-ext4.img

