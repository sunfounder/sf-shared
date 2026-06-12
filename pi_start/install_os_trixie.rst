.. note::

    Hallo, willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Community auf Facebook! Tauchen Sie mit anderen Enthusiasten tiefer in Raspberry Pi, Arduino und ESP32 ein.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Probleme nach dem Kauf und technische Herausforderungen mit Hilfe unserer Community und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Tutorials aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und Sneak Peeks.
    - **Sonderrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Bereit, mit uns zu entdecken und zu gestalten? Klicken Sie auf [|link_sf_facebook|] und treten Sie noch heute bei!

.. _install_os:

Installation des Betriebssystems
===================================

.. start_imager

Bevor Sie Ihren Raspberry Pi verwenden können, müssen Sie **Raspberry Pi OS** auf eine microSD-Karte installieren.  
Diese Anleitung erklärt auf einfache, anfängergerechte Weise, wie das mit dem **Raspberry Pi Imager** funktioniert.

**Benötigte Komponenten**

* Ein Computer (Windows, macOS oder Linux)
* Eine microSD-Karte (16 GB oder größer; empfohlene Marken: SanDisk, Samsung)
* Ein microSD-Kartenlesegerät

-------------------

Raspberry Pi Imager installieren
-------------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Besuchen Sie die offizielle Download-Seite des Raspberry Pi Imagers: |shared_link_rpi_imager|. Laden Sie das Installationsprogramm für Ihr Betriebssystem herunter.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Folgen Sie den Installationsanweisungen (Sprache, Installationspfad, Bestätigung). Starten Sie nach der Installation den **Raspberry Pi Imager** über Ihren Desktop oder das Anwendungsmenü.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%
      
--------------------------------------

.. end_imager

.. start_install_os

Installieren des Betriebssystems auf die microSD-Karte
----------------------------------------------------------------------

1. Stecken Sie Ihre microSD-Karte mit einem Kartenlesegerät in Ihren Computer. Sichern Sie vor dem Fortfahren alle wichtigen Daten.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Wenn der Raspberry Pi Imager geöffnet wird, sehen Sie die Seite **Gerät**. Wählen Sie Ihr Raspberry Pi-Modell aus der Liste aus (z. B. Raspberry Pi 5, 4, 3 oder Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. Gehen Sie zum Abschnitt **Betriebssystem** und wählen Sie die empfohlene Option **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. tip::
      Installieren Sie nicht die 32-Bit-Version, da einige erforderliche Abhängigkeiten möglicherweise nicht verfügbar sind.

.. start_storage

4. Wählen Sie im Abschnitt **Speicher** Ihre microSD-Karte aus.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

.. end_storage

-------------------

.. start_cutomization_os

.. _imager_custom:

Anpassungseinstellungen des Betriebssystems
-----------------------------------------------

#. Fahren Sie mit dem Anpassungsschritt fort.

   * Wenn Sie einen Monitor, eine Tastatur und eine Maus direkt an Ihren Raspberry Pi anschließen, können Sie auf **ANPASSUNG ÜBERSPRINGEN** klicken.
   * Wenn Sie den Raspberry Pi *headless* (Fernzugriff über WLAN) einrichten möchten, müssen Sie die Anpassungseinstellungen vornehmen.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

#. **Hostname festlegen**

   * Geben Sie Ihrem Raspberry Pi einen eindeutigen Hostnamen.
   * Sie können später über ``hostname.local`` eine Verbindung zu ihm herstellen.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Lokalisierung festlegen**

   * Wählen Sie Ihre Hauptstadt aus.
   * Der Imager vervollständigt automatisch die Zeitzone und das Tastaturlayout basierend auf Ihrer Auswahl, Sie können diese bei Bedarf jedoch anpassen. Klicken Sie auf Weiter.

   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Benutzername und Passwort festlegen**

   Erstellen Sie ein Benutzerkonto für Ihren Raspberry Pi.

   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **WLAN konfigurieren**

   * Geben Sie Ihre WLAN-**SSID** (Netzwerkname) und Ihr **Passwort** ein.
   * Ihr Raspberry Pi wird sich beim ersten Booten automatisch verbinden.

   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH aktivieren (optional, aber empfohlen)**

   * Die Aktivierung von SSH ermöglicht Ihnen die Remote-Anmeldung von Ihrem Computer aus.
   * Sie können sich mit Ihrem Benutzernamen/Passwort anmelden oder SSH-Schlüssel konfigurieren.

   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_cutomization_os

.. start_enable_connection

#. **Raspberry Pi Connect aktivieren (optional)**

   Raspberry Pi Connect ermöglicht Ihnen den Zugriff auf den Raspberry Pi Desktop über einen Webbrowser.

   * Schalten Sie **Raspberry Pi Connect** ein und klicken Sie dann auf **RASPBERRY PI CONNECT ÖFFNEN**.

     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Die Raspberry Pi Connect-Website wird in Ihrem Standardbrowser geöffnet. Melden Sie sich mit Ihrem Raspberry Pi ID-Konto an oder registrieren Sie sich, falls Sie noch keins haben.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Erstellen Sie auf der Seite **Neuer Authentifizierungsschlüssel** Ihren einmaligen Authentifizierungsschlüssel.

      * Wenn Ihr Raspberry Pi ID-Konto keiner Organisation angehört, wählen Sie **Authentifizierungsschlüssel erstellen und Raspberry Pi Imager starten**.
      * Wenn Sie einer oder mehreren Organisationen angehören, wählen Sie eine aus, erstellen Sie dann den Schlüssel und starten Sie den Imager.
      * Stellen Sie sicher, dass Sie Ihren Raspberry Pi einschalten und mit dem Internet verbinden, bevor der Schlüssel abläuft.

     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%

   * Ihr Browser fragt möglicherweise, ob der Raspberry Pi Imager geöffnet werden soll – erlauben Sie dies.

     * Der Imager öffnet sich auf dem Raspberry Pi Connect-Tab und zeigt das Authentifizierungstoken an.
     * Wenn das Token nicht automatisch übertragen wird, öffnen Sie den Abschnitt **Haben Sie Probleme?** auf der Raspberry Pi Connect-Seite, kopieren Sie das Token und fügen Sie es manuell in den Imager ein.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

.. end_enable_connection

-------------------

.. start_write_os

Schreiben des Betriebssystem-Images
-----------------------------------------------------

#. Überprüfen Sie alle Einstellungen und klicken Sie auf **SCHREIBEN**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Wenn die Karte bereits Daten enthält, zeigt der Raspberry Pi Imager eine Warnung an, dass alle Daten auf dem Gerät gelöscht werden. Überprüfen Sie erneut, ob Sie das richtige Laufwerk ausgewählt haben, und klicken Sie dann auf **ICH VERSTEHE, LÖSCHE UND SCHREIBE**, um fortzufahren.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Warten Sie, bis das Schreiben und die Überprüfung abgeschlossen sind. Wenn der Vorgang abgeschlossen ist, zeigt der Raspberry Pi Imager **Schreiben abgeschlossen!** und eine Zusammenfassung Ihrer Auswahl an. Das Speichergerät wird automatisch ausgeworfen, sodass Sie es sicher entfernen können.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Entfernen Sie die microSD-Karte und stecken Sie sie in den Steckplatz auf der Unterseite Ihres Raspberry Pi. Ihr Raspberry Pi ist jetzt bereit, mit dem neuen Betriebssystem zu starten!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

.. end_write_os
