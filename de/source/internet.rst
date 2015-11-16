========
Internet
========

.. contents::
   :local:

.. _country_selection:

**************
Land auswählen
**************

Wähle, über welches Land du surfen willst. Also wenn du z.B. Ungarn als Land auswählst, dann verhält es sich so, als ob du wirklich grad in Ungarn in einem Internetcafé surfst. Und so mit allen Ländern.

Folgende Länder stehen zur Auswahl:

* Schweiz
* Ungarn
* Schweden
* Deutschland
* Vereinigte Daten von Amerika

.. image:: images/country-selection.png

In diesem Beispiel:

.. image:: images/country-selection-zoom.png

* Die Schweiz ist das aktuell gewählte Land.
* Falls die Verbindung zum Schweizer Server wegbricht, springt die Verbindung auf Ungarn.
* Die anderen Länder werden nicht berücksichtigt ("Inaktiv").
* Ist Ungarn nicht erreichbar, springt die Verbindung wieder auf die Schweiz.

Verändere die Reihenfolge, indem du ein Land mit der Maus an eine andere Stelle ziehst. Markiere Länder, die im Fehlerfall als Alternative berücksichtigt werden sollen.

Wie lautet meine IP? In welchem Land befinde ich mich?
======================================================

Wenn du herausfinden willst, wie die IP-Adresse lautet, die grad "von aussen" sichtbar ist und in welchem Land deine Verbindung rauskommt: Die Website http://www.whereisip.net/ gibt Auskunft darüber:

.. image:: images/whereisip.png

.. _webfilter:

**************************
Werbeblocker konfigurieren
**************************

Der Werbeblocker läuft als Proxyserver auf der Enigmabox. Sag deinem Browser, dass er sich via dieses Proxies ins Internet verbinden soll, und die Werbung wird gefiltert.

Proxyserver: *box*, Port *8888*

Windows 10 Stasi-Features blockieren
====================================

Windows 10 wurde von mehreren Seiten als Abhörmaschine bezeichnet.

Es baut im Hintergrund Verbindungen zu folgenden Diensten auf::

    vortex.data.microsoft.com
    vortex-win.data.microsoft.com
    telecommand.telemetry.microsoft.com
    telecommand.telemetry.microsoft.com.nsatc.net
    oca.telemetry.microsoft.com
    oca.telemetry.microsoft.com.nsatc.net
    sqm.telemetry.microsoft.com
    sqm.telemetry.microsoft.com.nsatc.net
    watson.telemetry.microsoft.com
    watson.telemetry.microsoft.com.nsatc.net
    redir.metaservices.microsoft.com
    choice.microsoft.com
    choice.microsoft.com.nsatc.net
    df.telemetry.microsoft.com
    reports.wes.df.telemetry.microsoft.com
    wes.df.telemetry.microsoft.com
    services.wes.df.telemetry.microsoft.com
    sqm.df.telemetry.microsoft.com
    telemetry.microsoft.com
    watson.ppe.telemetry.microsoft.com
    telemetry.appex.bing.net
    telemetry.urs.microsoft.com
    telemetry.appex.bing.net
    settings-sandbox.data.microsoft.com
    vortex-sandbox.data.microsoft.com
    survey.watson.microsoft.com
    watson.live.com
    watson.microsoft.com
    statsfe2.ws.microsoft.com
    corpext.msitadfs.glbdns2.microsoft.com
    compatexchange.cloudapp.net
    cs1.wpc.v0cdn.net
    a-0001.a-msedge.net
    statsfe2.update.microsoft.com.akadns.net
    sls.update.microsoft.com.akadns.net
    fe2.update.microsoft.com.akadns.net
    diagnostics.support.microsoft.com
    corp.sts.microsoft.com
    statsfe1.ws.microsoft.com
    pre.footprintpredict.com
    i1.services.social.microsoft.com
    i1.services.social.microsoft.com.nsatc.net
    feedback.windows.com
    feedback.microsoft-hohm.com
    feedback.search.microsoft.com
    rad.msn.com
    preview.msn.com
    ad.doubleclick.net
    ads.msn.com
    ads1.msads.net
    ads1.msn.com
    a.ads1.msn.com
    a.ads2.msn.com
    adnexus.net
    adnxs.com
    aidps.atdmt.com
    apps.skype.com
    az361816.vo.msecnd.net
    az512334.vo.msecnd.net
    a.rad.msn.com
    a.ads2.msads.net
    ac3.msn.com
    aka-cdn-ns.adtech.de
    b.rad.msn.com
    b.ads2.msads.net
    b.ads1.msn.com
    bs.serving-sys.com
    c.msn.com
    cdn.atdmt.com
    cds26.ams9.msecn.net
    c.atdmt.com
    db3aqu.atdmt.com
    ec.atdmt.com
    flex.msn.com
    g.msn.com
    h1.msn.com
    live.rads.msn.com
    msntest.serving-sys.com
    m.adnxs.com
    m.hotmail.com
    pricelist.skype.com
    rad.live.com
    secure.flashtalking.com
    static.2mdn.net
    s.gateway.messenger.live.com
    secure.adnxs.com
    sO.2mdn.net
    ui.skype.com
    www.msftncsi.com
    msftncsi.com
    view.atdmt.com
    msnbot-65-55-108-23.search.msn.com
    settings-win.data.microsoft.com
    schemas.microsoft.akadns.net
    a-0001.a-msedge.net
    a-0002.a-msedge.net
    a-0003.a-msedge.net
    a-0004.a-msedge.net
    a-0005.a-msedge.net
    a-0006.a-msedge.net
    a-0007.a-msedge.net
    a-0008.a-msedge.net
    a-0009.a-msedge.net
    msedge.net
    a-msedge.net
    lb1.www.ms.akadns.net
    pre.footprintpredict.com
    vortex-bn2.metron.live.com.nsatc.net
    vortex-cy2.metron.live.com.nsatc.net

Im Webinterface kann ein zusätzlicher Filter eingeschaltet werden, der diese Verbindungen ins Leere laufen lässt.

.. image:: images/win10stasi.png

Wir raten grundsätzlich davon ab, Windows 10 zu verwenden.

Firefox
=======

Proxy-Einstellungen für den Browser konfigurieren, ohne dass das ganze System davon betroffen ist:

Gehe im Firefox über den Button rechts oben im Browserfenster auf "Einstellungen":

.. image:: images/firefoxoptions.jpg

Nun klickst du zuerst auf "Erweitert" und anschliessend auf "Einstellungen...":

.. image:: images/advanced.jpg

Stelle alles so ein, wie auf dem folgenden Bild ersichtlich:

.. image:: images/proxysettingsfirefox.jpg

Windows
=======

Öffne über das Startmenü die Systemeinstellungen deines Computers:

.. image:: images/systemeinstellungen_win.jpg

Je nach eingestellter Oberfläche klick als nächstes auf "Internetoptionen":

.. image:: images/internetoptionen.jpg
   
oder auf "Netzwerk und Internet":

.. image:: images/netzwerk_undinternet.jpg
   
und anschliessend auf "Internetoptionen":

.. image:: images/internetoptionen2.jpg

Im sich darauf öffnenden Fenster wählst du zuerst "Verbindungen" und dann "LAN-Einstellungen":

.. image:: images/lan_settings.jpg

Stelle alles so ein, wie auf dem folgenden Bild ersichtlich:

.. image:: images/proxysettings.jpg

Bestätige zum Abschluss mit OK.

Kontrolliere in deinem Browser, ob du auch dort die richtigen Einstellungen gesetzt hast. Dafür gehst du z.B. im Firefox über den Button rechts oben im Browserfenster auf "Einstellungen":

.. image:: images/firefoxoptions.jpg

Nun klickst du zuerst auf "Erweitert" und anschliessend auf "Einstellungen...":

.. image:: images/advanced.jpg

* Im sich anschliessend öffnenden Fenster kontrollierst du, dass die rot umkreiste Option ausgewählt ist. Wenn nicht, wählst du sie aus und bestätigst mit OK:

.. image:: images/firefoxproxy.jpg

Mac
===

Öffne die Einstellungen deines Macs:

.. image:: images/systemeinstellungen.jpg

Klicke auf "Netzwerk":

.. image:: images/netzwerk.jpg

Wähle nun als erstes die Netzwerkverbindung aus, über welche du mit der Enigmabox verbunden bist (In diesem Fall ist das ein WLAN). Danach klickst du auf "Weitere Optionen...":

.. image:: images/weiteroptionen.jpg

Klicke im neu geöffneten Fenster zuerst auf "Proxies". Danach setzt du den Haken bei "Web-Proxy (HTTP)" und Schreibst als drittes die Adresse "box" in das entsprechende Eingabefeld. Wichtig ist auch, den Port 8888 mit anzugeben! Wiederhole den Vorgang für "Sicherer Web-Proxy (HTTPS)":

.. image:: images/proxy.jpg

Schliesse das Fenster mit OK

Kontrolliere in deinem Browser, ob du auch dort die richtigen Einstellungen gesetzt hast. Dafür gehst du z.B. im Firefox über den Button rechts oben im Browserfenster auf "Einstellungen":

.. image:: images/firefoxoptions.jpg

Nun klickst du zuerst auf "Erweitert" und anschliessend auf "Einstellungen...":

.. image:: images/advanced.jpg

Im sich anschliessend öffnenden Fenster kontrollierst du, dass die rot umkreiste Option ausgewählt ist. Wenn nicht, wählst du sie aus und bestätigst mit OK:

.. image:: images/firefoxproxy.jpg

iPad
====

Tippe auf dem Startbildschirm von iPhone oder iPad auf das Zahnrad-Symbol "Einstellungen":

.. image:: images/HomeBildschirmIPad.jpg

Wechsle zum Bereich "WLAN" und wähle dein WLAN aus, welches mit der Enigmabox verbunden ist.
Tippe in der Zeile des Netzwerks, mit dem du verbunden bist, rechts auf das kleine blaue i im Kreis:

.. image:: images/WlanIPad.jpg

Im Bereich "HTTP-Proxy" stellst du den Schalter auf "Manuell". Darunter trägst du im Feld "Server" den Namen "box" ein und als Port gibst du *8888* an:

.. image:: images/ProxySettingsIPad.jpg

Betätige den Home-Button, um die Einstellungen zu speichern.

**Tipp:** Um den Proxyserver wieder auszuschalten, wiederhole die obigen Schritte. In Schritt 4. tippe aber auf "Aus".

