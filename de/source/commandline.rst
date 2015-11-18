======================
Kommandozeilenreferenz
======================

.. contents::
   :local:

*********
Enigmabox
*********

cfengine-apply
==============

Führt CFEngine aus und wendet die Systemkonfiguration gemäss den Templates und Einstellungen an.

Falls du mal irgendwas verbockt hast, führe diesen Befehl aus und alle von CFEngine verwalteten Dateien werden wieder in den definierten Zustand versetzt.

rebuild-iptables
================

Wendet die Firewallregeln an.

Template mit den Firewallregeln::

    /opt/enigmabox/cfengine-promises/system_network/templates/rebuild-iptables.mustache

Fertiges, gerendertes Skript::

    /usr/sbin/rebuild-iptables

setup-cjdns-networking
======================

Prüft die Netzwerkkonfiguration und setzt alle dafür benötigten Parameter wie Routen. Falls Internet nicht verfügbar ist, wechselt es das Land und fordert bei Bedarf die Peeringeinstellungen und Internet an.

speedtest
=========

Führt einen Geschwindigkeitstest direkt von der Box aus durch::

    root@box:~# speedtest 
    Retrieving speedtest.net configuration...
    Retrieving speedtest.net server list...
    Testing from Portlane Ab (46.246.93.74)...
    Selecting best server based on latency...
    Hosted by AltusHost B.V. (Stockholm) [0.00 km]: 78.179 ms
    Testing download speed........................................
    Download: 27.79 Mbit/s
    Testing upload speed..................................................
    Upload: 8.38 Mbit/s

**************************************
Funktionen für Benutzer mit Abonnement
**************************************

addressbook pull
================

Holt das globale Adressbuch vom Server.

addressbook push
================

Publiziert Änderungen ins globale Adressbuch.

updater check
=============

Prüft, ob Aktualisierungen vorhanden sind.

updater apply
=============

Installiert Aktualisierungen und startet danach die Enigmabox neu.

upgrader download
=================

Firmwareupgrade. Lädt das Image nach /tmp/fw.img herunter.

upgrader verify
===============

Überprüft das Firmwareimage */tmp/fw.img* mit der Signatur */tmp/fw.img.sig* und dem öffentlichen Schlüssel */etc/enigmabox/rsa-pubkey.pem*.

upgrader write
==============

Schreibt das Firmwareimage auf die Enigmabox. Das dauert bis zu 20min. Danach startet die Enigmabox automatisch neu.

***********
Cjdns-Tools
***********

cjdnslog ''
===========

Zeigt, was cjdns im Hintergrund so treibt::

    root@box:~# cjdnslog ''
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.028b.702b] recvPath[0000.0000.028b.702b] ip[fce5:d84c:e4d2:05d8:d4d7:ea4d:0c85:536f] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.02fa.502b] recvPath[0000.0000.02fa.502b] ip[fc28:2c5b:3a46:5527:d518:bb20:ffb3:ccd1] discovered path
    1413917051 DEBUG NodeStore.c:1968 getPeers request for [2a62c5d9]
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.0005.302b] recvPath[0000.0000.0005.302b] ip[fcdf:5adb:f3ef:ab15:b512:4959:132f:351c] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.0004.b023] recvPath[0000.0000.0004.b023] ip[fcac:da6e:1974:5d3d:d570:22d2:4ebd:b783] discovered path
    1413917051 DEBUG Pinger.c:154 Invalid ping response handle [3112299211].
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0dbe.9c40.8d77.702b] recvPath[0dbe.9c40.8d77.702b] ip[fc38:d589:e0bd:fdd4:c04d:bb46:1638:9381] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.02ab.302b] recvPath[0000.0000.02ab.302b] ip[fc72:f765:7c0f:49a8:ed91:d915:1c58:3353] discovered path
    1413917051 DEBUG InterfaceController.c:350 Pinging lazy peer [3rj00tu2s2b96n5v7z9fdxvw1ds7dyskbb4hw2xp9f4kh3q7cr70.k] lag [0]
    1413917051 DEBUG InterfaceController.c:286 SwitchPing [3rj00tu2s2b96n5v7z9fdxvw1ds7dyskbb4hw2xp9f4kh3q7cr70.k]
    1413917051 DEBUG InterfaceController.c:350 Pinging lazy peer [1nukqsluxzn1nkpljsvxsqvrt8gh2gk18hpbkcuf6s7fy2qx35k0.k] lag [0]
    1413917051 DEBUG InterfaceController.c:286 SwitchPing [1nukqsluxzn1nkpljsvxsqvrt8gh2gk18hpbkcuf6s7fy2qx35k0.k]
    1413917051 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.001d]
    1413917051 DEBUG ControlHandler.c:178 got switch pong from [0000.0000.0000.001d]
    1413917051 DEBUG InterfaceController.c:242 got switch pong from node [v16.0000.0000.0000.001d.1nukqsluxzn1nkpljsvxsqvrt8gh2gk18hpbkcuf6s7fy2qx35k0.k]
    1413917051 DEBUG InterfaceController.c:259 Received [pong] from lazy endpoint [v16.0000.0000.0000.001d.1nukqsluxzn1nkpljsvxsqvrt8gh2gk18hpbkcuf6s7fy2qx35k0.k]
    1413917051 DEBUG Pathfinder.c:283 Peer [v16.0000.0000.0000.001d.1nukqsluxzn1nkpljsvxsqvrt8gh2gk18hpbkcuf6s7fy2qx35k0.k]
    1413917051 DEBUG ControlHandler.c:151 ctrl packet from [0000.0000.0000.001b]
    1413917051 DEBUG ControlHandler.c:178 got switch pong from [0000.0000.0000.001b]
    1413917051 DEBUG InterfaceController.c:242 got switch pong from node [v16.0000.0000.0000.001b.3rj00tu2s2b96n5v7z9fdxvw1ds7dyskbb4hw2xp9f4kh3q7cr70.k]
    1413917051 DEBUG InterfaceController.c:259 Received [pong] from lazy endpoint [v16.0000.0000.0000.001b.3rj00tu2s2b96n5v7z9fdxvw1ds7dyskbb4hw2xp9f4kh3q7cr70.k]
    1413917051 DEBUG Pathfinder.c:283 Peer [v16.0000.0000.0000.001b.3rj00tu2s2b96n5v7z9fdxvw1ds7dyskbb4hw2xp9f4kh3q7cr70.k]
    1413917051 DEBUG SessionManager.c:401 Buffering a packet to [fcb7:0714:2b45:0c5c:92f3:4720:c7fa:ec08] and beginning a search
    1413917051 DEBUG SessionManager.c:408 DROP message which needs lookup because new one received
    1413917051 DEBUG Pathfinder.c:267 Search req [fcb7:0714:2b45:0c5c:92f3:4720:c7fa:ec08]
    1413917051 DEBUG SessionManager.c:276 ver[0] send[0] recv[30145] ip[fcd8:e437:5656:a69a:f170:9f10:8416:2fa8] path[0000.0003.ea83.0e3d] new session nonce[0]
    1413917051 DEBUG CryptoAuth.c:642 0x137ffe8 inner [fcd8:e437:5656:a69a:f170:9f10:8416:2fa8]: Received a hello packet, using auth: 0
    1413917051 DEBUG SessionManager.c:305 ver[0] send[80345] recv[30145] ip[fcd8:e437:5656:a69a:f170:9f10:8416:2fa8] path[0000.0003.ea83.0e3d] received start message
    1413917051 DEBUG Pathfinder.c:317 Session [v0.0000.0003.ea83.0e3d.5l2b4xn0syj5b1x5hhsx07upv4ddklbvdpt3gn4sv4v8tpk4fzq0.k]
    1413917051 DEBUG NodeStore.c:1968 getPeers request for [7441f41]
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.0000.0013] recvPath[0000.0000.0000.0013] ip[fc1c:18cc:f95b:a2c0:a792:6c34:b2ae:bd0e] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0003.ea83.0e3d] recvPath[0000.0003.ea83.0e3d] ip[fcd8:e437:5656:a69a:f170:9f10:8416:2fa8] discovered path
    1413917051 DEBUG CryptoAuth.c:437 0x137ffe8 inner [fcd8:e437:5656:a69a:f170:9f10:8416:2fa8]: Sending key packet
    1413917051 DEBUG SessionManager.c:471 ver[15] send[80345] recv[30145] ip[fcd8:e437:5656:a69a:f170:9f10:8416:2fa8] path[0000.0003.ea83.0e3d] sending start message
    1413917051 DEBUG NodeStore.c:1500 Discover node [fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c@0047.78d0.648c.1023]
    1413917051 DEBUG NodeStore.c:1013 discoverLinkC( [fc67:9816:2ccc:c4c2:f76c:1d09:a7a5:044e]->[fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c] [0000.0000.0000.0019] )
    1413917051 DEBUG NodeStore.c:750 Linking [fc67:9816:2ccc:c4c2:f76c:1d09:a7a5:044e] with [fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c] with label fragment [0000.0000.0000.0019]
    1413917051 DEBUG NodeStore.c:1603 store full, removing worst node: [fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c@0000.0011.de26.182b] nodes [135] links [531]
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0011.de26.182b] recvPath[0047.78d0.648c.1023] ip[fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0011.de26.182b] recvPath[0047.78d0.648c.1023] ip[fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0047.78d0.648c.1023] recvPath[0047.78d0.648c.1023] ip[fcb3:000f:9f8a:332c:92c6:ce84:c581:5c1c] discovered path
    1413917051 DEBUG SessionManager.c:565 Session sendPath[0000.0000.0006.b02b] recvPath[0000.0000.0006.b02b] ip[fcd1:338e:e299:2104:aad5:90bf:db05:7cfe] discovered path

dumptable
=========

Zeigt die Routingtabelle von cjdns an::

    root@box:~# dumptable 
    fcd7:c111:7264:82b5:36a1:76fe:b94f:b859 0000.0000.0671.682b 52195780 16
    fc58:a55d:e005:1172:33f9:cc7f:fc23:51c7 0000.0000.0006.502b 212118879 16
    fcc1:624f:8bf7:ae7e:2421:fd32:023f:b923 0000.0000.0007.102b 152266092 16
    fc41:56f4:0d8f:6f5a:19ee:f2e5:11e5:01a2 0000.0000.0000.0019 24301450 16
    fcbb:98bd:d44f:40dc:426c:4971:b6b1:7bd6 0000.001e.5e26.182b 53687088 17
    fceb:f9fd:5079:10ab:4152:f0f3:fb3e:9b0f 0000.0000.0000.082b 212118880 16
    fc04:f0f2:884a:6fa8:3ef4:035a:1c93:f335 0000.0000.021e.182b 53687088 17
    fc34:8675:ed95:600c:38d7:6eb8:f5b9:5bfa 0000.0000.0000.982b 53687088 17
    fccb:084a:918f:b20f:6655:eafc:98c7:2bde 0000.0000.0025.602b 200735032 16
    fc10:c4f8:fa32:58cd:5dad:b50c:56b5:5d10 0000.0000.0025.a02b 184621602 16
    fc29:2b03:f5da:7443:5370:26ce:c332:bb82 0000.0000.0000.001d 526648413 16
    fc2f:a0e2:2f43:8a94:4dfe:2bb7:603c:6acd 0000.0000.0000.0017 87019374 16
    fc1c:18cc:f95b:a2c0:a792:6c34:b2ae:bd0e 0000.0000.0000.0013 137324553 16
    fcef:1061:cc30:743b:7f3f:3980:c123:4b63 0000.0000.03e5.602b 100640779 16
    fcec:ae97:8902:d810:6c92:ec67:efb2:3ec5 0000.0008.580a.182b 25565281 16

findnodes
=========

Sucht nach cjdns-Nodes.

peerStats
=========

Zeigt den Verbindungsstatus von direkten Peers an::

    root@box:~# peerStats 
    fc29:2b03:f5da:7443:5370:26ce:c332:bb82 0000.0000.0000.001d     in 265570750    out 597255897   ESTABLISHED     dup 0 los 7 oor 0       'Local Peers'
    fc4f:37ec:6363:df11:fa13:ccf3:ec3b:c693 0000.0000.0000.001b     in 599998481    out 354949986   ESTABLISHED     dup 0 los 186 oor 0
    fc41:56f4:0d8f:6f5a:19ee:f2e5:11e5:01a2 0000.0000.0000.0019     in 35123931     out 28923293    ESTABLISHED     dup 0 los 13 oor 0
    fc2f:a0e2:2f43:8a94:4dfe:2bb7:603c:6acd 0000.0000.0000.0017     in 62783863     out 42307626    ESTABLISHED     dup 0 los 10 oor 0
    fc3f:ec6a:273a:5908:da68:1dae:3abc:b0db 0000.0000.0000.0015     in 1539111953   out 849151552   ESTABLISHED     dup 0 los 2769 oor 0
    fc1c:18cc:f95b:a2c0:a792:6c34:b2ae:bd0e 0000.0000.0000.0013     in 191229295    out 119774653   ESTABLISHED     dup 0 los 21 oor 0

