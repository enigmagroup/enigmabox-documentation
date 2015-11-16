.. _telephony:

=========
Telefonie
=========

.. contents::
   :local:

**********************
Das Telefon einrichten
**********************

Verbinde das mitgelieferte Grandstream-Telefon mit der Enigmabox und warte ein paar Minuten. Das Telefon holt die Einstellungen von der Enigmabox und konfiguriert sich von alleine.

Für andere `SIP-kompatible Telefone <hhttps://de.wikipedia.org/wiki/SIP-Telefon>`_, hier die Verbindungsdaten für den Telefonserver:

| **Server:** box
| **Benutzer:** 100
| **Passwort:** 100
|

*************
Statusabfrage
*************

Die Telefonnummer "1" gibt Informationen zur Verbindung der Enigmabox, das Abo, erhaltene E-Mails und erreichbare Kontakte im Adressbuch aus.

******************
Telefonkonferenzen
******************

Telefonkonferenzen funktionieren heute meistens so, dass sich alle Teilnehmer in einen zentralen Server einwählen und danach wie in einem Sitzungszimmer miteinander reden können.

Nun - bei der Enigmabox gibt es keine solchen zentralen Server, die das ermöglichen. Deshalb haben wir ein wenig nachgedacht und sind zu folgendem Schluss gekommen:

**Jede Enigmabox ist ein Konferenzserver!**

Dem Konferenzraum auf deiner Enigmabox beitreten
================================================

Wähle die Nummer "8" auf dem Telefon. \*Dadü* - du bist in deinem Konferenzraum.

Einem Konferenzraum auf einer anderen Enigmabox beitreten
=========================================================

Bei jedem Anruf ertönt zuerst ein "du-diit"-Signalton. Du hast nun eine Sekunde Zeit, die Taste "8" zu betätigen - dann landest du im Konferenzraum der angerufenen Enigmabox.

Falls du nach dem Signalton nichts unternimmst, wird der Anruf normal durchgestellt und das Telefon klingelt.

So können sich ganz viele Teilnehmer in eine Enigmabox einwählen und dann eine Telefonkonferenz miteinander führen.

****************
Anrufbeantworter
****************

Der Anrufbeantworter springt automatisch an, wenn nach 30 Sekunden klingeln das Telefon nicht abgenommen wurde. Die aufgezeichnete Nachricht wird als E-Mail gespeichert und landet in der Inbox des Angerufenen.

************************
Videotelefonie mit Jitsi
************************

Jitsi ist ein Open-Source-Softwaretelefon. Wenn du eine Webcam besitzt steht einer verschlüsselten Videotelefonie am PC oder Laptop nichts entgegen!

Jitsi herunterladen
===================

Download von folgender URL: https://jitsi.org/Main/Download

Jitsi einrichten
================

Klicke auf "Datei/Konto hinzufügen...", um ein neues Konto zu erstellen:

.. image:: images/jitsi1.png

Verwende *100@box* als SIP-Kennung, und *100* als Passwort:

.. image:: images/jitsi2.png

Klicke auf "Hinzufügen".

Blende die Wähltastatur ein und rufe zum Test die Nummer 1 an.

.. image:: images/jitsi3.png

Wenn alles geklappt hat, wirst du eine Stimme hören, die den Systemstatus vorliest.

Einen Kontakt hinzufügen
========================

Klicke mit der rechten Maustaste im Kontaktfeld und dann auf "Kontakt hinzufügen...".

.. image:: images/jitsi-add-contact.png

Trage dort die Telefonnummer des Kontaktes ein, den du hinzufügen möchtest. Das ist die gleiche Telefonnummer wie im Enigmabox-Adressbuch. Vergib einen Namen.

Videoanruf starten
==================

Klicke mit der rechten Maustaste auf den neu hinzugefügten Kontakt, und dann auf "Videoanruf":

.. image:: images/jitsi-videocall.png

Der Videoanruf startet.

.. image:: images/jitsi-videocall-running.png


********************************************
Telefonie auf einem Android-Handy einrichten
********************************************

Hier wird Schritt für Schritt gezeigt, wie Sie ihr Android-Handy in ein EnigmaTelefon umfunktionieren können. Voraussetzung ist, dass Sie ihre EnigmaBox über ein WLAN erreichen können, Sie also am LAN-Anschluss ihrer EnigmaBox einen WLAN-Accesspoint angeschlossen haben:

* Tippen Sie zuerst auf dem Home-Bildschirm Ihres Android-Handys auf "Telefon"
  
.. image:: images/home.jpg

* Tippen Sie nun links unten auf Ihrem Android-Handy auf die Menü-Taste:

.. image:: images/menuetaste.jpg

* Im sich darauf öffnenden Menü tippen Sie auf "Anrufeinstellungen":

.. image:: images/anrufeinstellungen.jpg

* Scrollen Sie im sich darauf öffnenden Einstellungsmenü ganz nach unten und tippen Sie auf "Konten":

.. image:: images/konten.jpg

* Im neu geöffneten Untermenü setzen Sie zuerst den Hacken bei "Eingehende Anrufe annehmen" und tippen anschliessend auf "Konto hinzufügen":

.. image:: images/add_konto.jpg

* Bei Benutzernamen und Passwort ist "100" einzugeben und der Server lautet "box":

.. image:: images/set_konto.jpg

* Die Einstellungen werden gespeichert, sobald sie zum vorherigen Menü zurückkehren. Dort werden Sie zu unterst den Menüeintrag "Internetanrufe tätigen" finden. Tippen Sie darauf und wählen Sie die Option "Bei jedem Anruf fragen" aus.
* Nun sollten Sie - solange Sie sich im WLAN befinden - fähig sein, Anrufe von ihrem Android-Handy auf andere Enigmaboxen tätigen zu können oder Anrufe von anderen auf ihre Box mit ihrem Android-Handy entgegen zu nehmen.


