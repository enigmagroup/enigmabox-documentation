======
System
======

.. contents::
   :local:

.. _address_book:

*******************
Adressen verwalten
*******************

Das Adressbuch ist der Dreh- und Angelpunkt für die Kontaktverwaltung der Enigmabox. Die IPv6-Adresse wird zufällig generiert und dient als eindeutige Identifizierung im Netzwerk.

(Für technische Details, siehe :ref:`tech`).

.. image:: images/addressbook-1.png

Die IPv6 ist deine Telefonnummer. Die Enigmaboxen identifizieren sich nur anhand dieser IPv6.

Da es aber mühsam wäre, diese lange Folge von Zahlen und Buchstaben jedesmal am Telefon einzugeben, weist du der IPv6 eine Kurznummer für das Telefon, also eine Telefonnummer zu.

Kontakt hinzufügen
==================

.. image:: images/addressbook-add-number.png

Trage die IPv6 deines Kontakts (2) in das Feld "IPv6-Adresse" ein. Trage einen beliebigen Namen (Hostname) und eine Telefonnummer dazu ein.

Teile deine IPv6 (1) ("Meine Adresse") deinem Gegenüber mit. Er wiederholt den Vorgang.

Sobald die IPs gegenseitig im Adressbuch eingetragen sind, könnt ihr euch anrufen.

.. image:: images/addressbook-2contacts.png

Beispiel:

#. Meine IP ist "fccf:3286:feb2:cc8e:db0c:cf20:cc5d:e60"
#. Ich wähle die Telefonnummer "123"
#. Das Telefon ruft die IP "fc62:df23:6b65:2355:2efc:80b5:c0b9:7e11" (alexandra) an

Der Hostname (alexandra) wird für die E-Mail Adresse verwendet. Die E-Mail Adresse von alexandra ist in diesem Beispiel "mail@alexandra".

Wie man E-Mails sendet und empfängt, steht unter :ref:`email`.

**********************
Das globale Adressbuch
**********************

Das globale Adressbuch ist ein Verzeichnis, in dem jeder seine Adresse publizieren kann, wenn er möchte. Der Vorteil: Der gegenseitige Adressaustausch entfällt. Das ist z.B. bei einem Verkaufsladen von Vorteil; der Inhaber publiziert seine Nummer im globalen Adressbuch und ist so sofort für potentielle Kunden erreichbar.

.. image:: images/global-addressbook.png

Damit man überhaupt für alle erreichbar ist, muss dafür die Firewall freigeschaltet werden. Das wird über die *globale Erreichbarkeit* geregelt. Standardmässig ist das ausgeschaltet.

Globale Erreichbarkeit aktivieren
=================================

Klick im globalen Adressbuch auf den schwarzen Schalter "Deaktiviert".

Die Firewall wird für alle im verschlüsselten Netzwerk freigeschaltet und der Knopf hat sich geändert in "Ich bin global erreichbar":

.. image:: images/ga-activated.png

Bestätige diese Änderung mit "Änderungen anwenden".

Eigene Adresse im globalen Adressbuch publizieren
=================================================

sdf

.. image:: images/ga-enter-number.png

blaaa

.. image:: images/ga-pending.png

fuu

.. image:: images/ga-confirmed.png

baz

.. image:: images/ga-rejected.png

harr

.. _set_password:

*****************
Passwörter setzen
*****************

sdf

***********************
Passwörter zurücksetzen
***********************

sdf

.. _backup:

********************************
Eine Systemsicherung durchführen
********************************

sdf

***************************
Das System wiederherstellen
***************************

sdf

***************************
SSL-Zertifikate importieren
***************************

sdf

**************************
Die Firmware aktualisieren
**************************

sdf

