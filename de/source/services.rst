=======
Dienste
=======

.. contents::
   :local:

*****************
Zugriff verwalten
*****************

Firewall
========

Die Firewall erlaubt folgenden Zugriff auf den Webserver der Enigmabox:

.. image:: images/hypesites-access-none.png

Keiner: Kein Zugriff.

.. image:: images/hypesites-access-internal.png

Internes LAN: Nur der angeschlossene PC hat Zugriff.

.. image:: images/hypesites-access-friends.png

Nur Freunde: Kontakte aus dem Adressbuch haben Zugriff.

.. image:: images/hypesites-access-global.png

Global: Alle im verschlüsselten Netzwerk haben Zugriff.

Zugriffsrechte einzelner Dienste
================================

.. image:: images/site-access-all.png

Alle im verschlüsselten Netzwerk haben Zugriff.

.. image:: images/site-access-friends.png

Kontakte aus dem Adressbuch haben Zugriff.

.. image:: images/site-access-specific.png

Erlaube einzelnen IPv6-Adressen den Zugriff auf einen Dienst.

.. _hosting:

*********************
Eigene Website hosten
*********************

.. image:: images/hypesites-overview.png

Hypesites sind Websites innerhalb des verschlüsselten Netzwerks. Auf der Enigmabox läuft ein Webserver, und jeder kann seine eigene Website für andere Enigmabox-Benutzer zur Verfügung stellen.

Dienst aktivieren
=================

In der Administrationsoberfläche auf "Hypesite-Dienste konfigurieren" klicken:

.. image:: images/oc1.png

Dann "Eigene Website" aktivieren:

.. image:: images/hypesites-enable-site.png

Danach die Änderungen mit "Änderungen anwenden" aktivieren:

.. image:: images/apply-changes.png

Die eigene Website läuft und du kannst sie über die URL, die jetzt rechts eingeblendet wird, aufrufen.

Dateien mit SFTP hochladen
==========================

**WinSCP herunterladen:** http://winscp.net/download/winscp574setup.exe

**Mit der Enigmabox verbinden:**

.. image:: images/sftp.png

Für das Passwort, siehe :ref:`set_password_ssh`

.. image:: images/enter-pw.png

Verbinden, Passwort eingeben.

**HTML-Dateien hochladen:**

Das Verzeichnis des Webservers ist */srv/www/*

Editiere die index.html, lade beliebige Dateien hoch. PHP wird unterstützt.

.. image:: images/hypesite-running.png

.. _wiki:

****
Wiki
****

Ein Wiki ermöglicht kollaboratives Arbeiten an Projekten, zur Dokumentation oder zur Ideenfindung.

Dienst aktivieren
=================

In der Administrationsoberfläche auf "Hypesite-Dienste konfigurieren" klicken:

.. image:: images/configure-hypesite-services.png

Dann "Wiki" aktivieren:

.. image:: images/enable-wiki.png

Danach die Änderungen mit "Änderungen anwenden" aktivieren:

.. image:: images/apply-changes.png

Das Wiki läuft und du kannst es über die URL, die jetzt rechts eingeblendet wird, aufrufen.

Passwort vom Admin-Account ändern
=================================

Klicke im Menü unten links auf "Login":

.. image:: images/wiki-overview.png

Logge dich ein, Benutzer: *admin*, Passwort: *admin*.

.. image:: images/wiki-login.png

Gehe zur Wiki-Administration:

.. image:: images/wiki-logged-in.png

Klicke auf "User Manager":

.. image:: images/wiki-administration.png

Wähle den Benutzer "admin" aus:

.. image:: images/wiki-usermanager.png

Setze ein starkes Passwort und klicke danach auf "Save Changes".

.. image:: images/wiki-edit-admin.png

Das Wiki ist jetzt konfiguriert und einsatzbereit. Für weitere Informationen, konsultiere die DokuWiki Dokumentation: https://www.dokuwiki.org/wiki:dokuwiki

********
Pastebin
********

.. image:: images/stikked-overview.png

Ein Pastebin ist dazu da, um lange und kurze Texte schnell und einfach mit anderen zu teilen. Alles, was du tun musst, ist, den Text in ein Feld einfügen (Paste), und dann den Link verteilen. Der Pastebin, der auf der Enigmabox mitgeliefert wird, unterstützt verschlüsselte Pastes.

In der Administrationsoberfläche auf "Hypesite-Dienste konfigurieren" klicken:

.. image:: images/configure-hypesite-services.png

Dann "Pastebin" aktivieren:

.. image:: images/enable-pastebin.png

Danach die Änderungen mit "Änderungen anwenden" aktivieren:

.. image:: images/apply-changes.png

Der Pastebin läuft und du kannst ihn über die URL, die jetzt rechts eingeblendet wird, aufrufen.

.. _owncloud:

********
OwnCloud
********

OwnCloud ermöglicht es, Dateien aller Art mit anderen zu teilen, Dateien auf mehreren Rechnern synchron zu halten und gemeinsam an Dokumenten zu arbeiten. Auf der Enigmabox ist OwnCloud so eingebunden, dass sämtliche Kommunikation verschlüsselt ist, das Teilen mit anderen funktioniert also nur innerhalb des Netzwerks.

Initiale Einrichtung
====================

In der Administrationsoberfläche auf "Hypesite-Dienste konfigurieren" klicken:

.. image:: images/oc1.png

Webdienst OwnCloud aktivieren und dann mit "Änderungen anwenden" bestätigen:

.. image:: images/oc3.png

.. image:: images/oc4.png

Auf der Hauptseite ist jetzt "OwnCloud" anklickbar:

.. image:: images/oc5.png

Benutzername und Passwort vergeben:

.. image:: images/oc6.png

Fertig!

.. image:: images/oc7.png

.. _realtime_collaboration:

Echtzeitkollaboration einrichten
================================

Im OwnCloud-Menü "Apps" anwählen:

.. image:: images/oc9.png

Unter "Not enabled": "Documents" aktivieren:

.. image:: images/oc10-documents.png

"Documents" ist als neuer Menüpunkt hinzugekommen:

.. image:: images/oc11.png

Gemeinsam an einem Dokument arbeiten:

.. image:: images/oc12.png

.. image:: images/oc13.png

.. image:: images/oc14.png

Externe Speicher konfigurieren
==============================

Das Menü "Speichermedien" erscheint, sobald OwnCloud aktiviert wurde:

.. image:: images/oc3.png

Name des Speichermediums eingeben, damit es aktiviert werden kann:

.. image:: images/storage1.png

Laufwerk ist eingehängt. "Änderungen anwenden":

.. image:: images/storage2.png

"Benutzen" heisst: Das Laufwerk wird eingehängt, sobald es verfügbar ist, auch nach einem Neustart.

Im OwnCloud-Menü "Apps" anwählen:

.. image:: images/oc9.png

Unter "Not enabled": "External storage support" aktivieren:

.. image:: images/storage0.png

In OwnCloud im Menü rechts "Administrator" anwählen:

.. image:: images/storage3.png

Externer Speicher hinzufügen: "Lokal", Konfiguration: Der vorher definierte Name!

.. image:: images/storage4.png

Das Laufwerk ist nun in OwnCloud als Ordner sichtbar:

.. image:: images/storage5.png

Desktop-Synchronisation einrichten
==================================

OwnCloud Desktop-Client herunterladen:

  * Windows: https://download.owncloud.com/desktop/stable/ownCloud-1.8.4.5267-setup.exe
  * Mac: https://download.owncloud.com/desktop/stable/ownCloud-1.8.4.2531.pkg

Server-Adresse eintragen:

.. image:: images/oc15.png

Fertig!

.. image:: images/oc16.png

Der gewählte Ordner wird nun mit OwnCloud synchron gehalten.

.. image:: images/sync-removed.png

.. image:: images/sync-downloaded.png

********
Teletext
********

Das Telegramm war eine sinnvolle Ergänzung in einer Zeit, in der es kaum private Telefone gab. Es war bedeutend schneller als ein Brief und kam einigermassen sicher an.

Heute erleben wir eine völlig andere Situation. Es gibt ein unüberschaubares Angebot von Kommunikations-Möglichkeiten. Man kann nahezu in Echtzeit Nachrichten austauschen. Die horrenden Kosten für jedes einzelne übermittelte Zeichen bei den Telegrammen sind einem „all inclusive“ gewichen.




Aber hat sich die Kommunikation tatsächlich verändert? Kaum waren die Telegramme in Mode gekommen, wurde versucht, den Inhalt der Telegramme und die jeweiligen Sender ausfindig zumachen. Abhorchen ist keine neue Erfindung. Aber eine flächendeckende Abhorchaktion gab es in den Anfängen der Telekommunikation doch noch nicht.

Die Enigmabox lässt das Telegramm mit dem Dienst Teletext wieder aufleben. Selbstverständlich kostenlos, so wie das Telefon- und Mailsystem.

Mit dem Teletext werden Nachrichten mit 256 Zeichen in Echtzeit und verschlüsselt zu anderen Enigmaboxen gesendet. Der Sender kann selbst bestimmen, ob seine Abonnenten und seine abonnierten Telegramme von anderen Anwendern sichtbar sind.

So geht’s:

Da Teletext eine öffentliche Schnittstelle für alle innerhalb des verschlüsselten Netzwerks bereitstellt, ist das Programm standardmässig deaktiviert und muss manuell in der Administrationsoberfläche eingeschaltet werden. Also einschalten unter http://box.

Jetzt ist die Schaltfläche „Teletext“ aktiv. Unter Teletext „settings“ kannst Du das Profil ausfüllen:
Du kannst Deinen Namen unter „Username“ frei wählen. Bei „Bio“ kann eine nähere Beschreibung stehen und das „Profil Image“ verschönert Deine Telegramm Visitenkarte.

Wichtig sind die Einstellungen der Sichtbarkeit:
Mit “Show subscribers“ aktiv sind Deine Abonnenten sichtbar. Also wer sonst noch Deine Telegramme erhält.

Mit “Show subscriptions” aktiv sind Deine abonnierten Telegramme sichtbar. Also welche Telegramme Du selbst erhalten hast.
Speichere Deine Einstellungen.  Nun kann es losgehen.
Unter „Enigmabox adress book“ kannst Du Deine Kontakte zum Teletext hinzufügen.
Oder Du kannst zum Starten den Telegramm Schreiber „News Super Aktuell“ (NSA) abonnieren. Nein, es ist natürlich nicht die NSA, sondern nur ein temporärer Treffpunkt für Teletext Anwender.



Die Telegramme werden nun abgerufen und lokal auf Deiner Enigmabox gespeichert. Mit einem Klick auf den Sendernamen im Telegramm können die Details angezeigt werden. Mit „Retransmit“ wird das Telegramm an Deine Abonnenten weitergereicht.

Der Teletext ermöglicht den Netzbürgern, sich innerhalb des verschlüsselten Netzwerks zu finden. Sie können neue Kontakte zum Enigmabox Adressbuch hinzufügen und dann verschlüsselt telefonieren und E-Mails austauschen.





Newest leaks of whistleblower Edward Raincave reveal a new counter spy program of the citizens secret service Enigmabox: Teletext.

TELETEXT
(TS//SI//REL) Teletext provides distributed mass protest coordination below the radar by implementing a Twitter like messaging system using cjdns addresses.

(TS//SI//REL) This technique supports users on writing telegrams and spreading out important information quickly to reach critical mass.

(TS//SI//REL) Through the distributed nature, Telegrams published on the Teletext system can not be censored, nor controlled. It is all end-to-end encrypted.

Status: Released / Deployed. Ready for Immediate Delivery

Unit Cost: $0

COSMIC TOP SECRET//SAR-BUTTER POPCORN//RD-CNWDI//COMINT//REL TO CH

This programm allows everyone to publish telegrams, and subscribe to telegrams of other parties inside the cryptonetwork. Here's a screen how a new telegram is created:


Telegrams are character limited, but to 256 chars instead of only 140 at Twitter.

Telegrams of all subscriptions are shown in a timeline, just as in Twitter. The distribution of the messages is nearly real-time.

That is possible thanks to an asynchronous, event based Python server in combination with a fast in-memory work queue. The Server can answer up to 146 requests per second on the Enigmabox, consuming no more than 12m-15m memory.

You can also retransmit Telegrams. This way, important information can spread really fast - and completely undetected. Everything is end-to-end encrypted and distributed, censorship is impossible.

Here is the profile view:


Teletext allows internet citizens to find each other inside this encrypted network. They can discover new contacts and add them to their address book, and then exchange encrypted emails or have encrypted phone calls.

This feature has been released the night before yesterday to all Enigmaboxes and is ready to use.

Since Teletext provides a public reachable interface inside the cryptonetwork, it is disabled by default. You have to enable it in the admin interface to use it.

*****************
Portweiterleitung
*****************

Die Portweiterleitung erlaubt es, einen beliebigen Port im cjdns-Netzwerk an einen Rechner im LAN weiterzuleiten. So kann man z.B. eine Remotedesktopverbindung einrichten, oder Gameserver innerhalb von Hyperboria hosten. Im folgenden Beispiel verbindet [IPv6]:5900 zum VNC-Server meines Laptops (192.168.100.52:5900).

.. image:: images/portforwarding-overview.png

Es werden immer beide - TCP und UDP-Ports - weitergeleitet.

Der Status zeigt an, ob ein Dienst von der Box erreichbar ist. Diese Statusanzeige funktioniert aber nur bei TCP-Diensten.

Die Zugriffsrechte können ähnlich granular vergeben werden wie bei den anderen Diensten.

.. image:: images/portforwarding-service.png

Portweiterleitung erstellen
===========================

.. image:: images/portforwarding-create.png

**Port:** Auf welchem Port auf der IPv6 der Enigmabox soll der Dienst lauschen?

**Zielgerät:** Rechner, auf dem der Dienst läuft

**Zielport:** Eigentlicher Port des Dienstes

Port und Zielport müssen nicht übereinstimmen; "Port" kann frei gewählt werden. Ausnahmen sind bereits belegte Ports wie 22, 25, 80, 110, 143, 3838, 5060.

**Beschreibung (optional):** Eine kurze Beschreibung des Dienstes.

Danach auf "Speichern" klicken und die Zugriffsrechte vergeben.

.. note:: Wichtig: Der Port ist erst erreichbar, wenn die Zugriffsrechte vergeben wurden! Auf einen frisch erstellten Port hat noch niemand Zugriff.

In der Administrationsoberfläche werden die aktiven Portweiterleitungen angezeigt:

.. image:: images/portforwarding-status.png

