.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _install_os:

Installation des Betriebssystems
===================================

.. start_imager

Bevor Sie Ihren Raspberry Pi verwenden können, müssen Sie **Raspberry Pi OS** auf eine microSD-Karte installieren.  
Diese Anleitung zeigt, wie Sie dies mit dem **Raspberry Pi Imager** einfach und anfängerfreundlich durchführen.

**Benötigte Komponenten**

* Ein Computer (Windows, macOS oder Linux)
* Eine microSD-Karte (16 GB oder größer; empfohlene Marken: SanDisk, Samsung)
* Ein microSD-Kartenleser

-------------------

**1. Raspberry Pi Imager installieren**
-------------------------------------------

#. Besuchen Sie die offizielle Downloadseite des Raspberry Pi Imagers: |shared_link_rpi_imager|. Laden Sie das passende Installationsprogramm für Ihr Betriebssystem herunter.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Folgen Sie den Installationsanweisungen (Sprache, Installationspfad, Bestätigung).  
   Nach Abschluss starten Sie **Raspberry Pi Imager** über den Desktop oder das Anwendungsmenü.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. Das Betriebssystem auf die microSD-Karte installieren**
-----------------------------------------------------------

#. Stecken Sie Ihre microSD-Karte mithilfe eines Kartenlesers in Ihren Computer.  
   Sichern Sie wichtige Daten, da sie überschrieben werden.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

#. Beim Start zeigt der Raspberry Pi Imager die Seite **Device** an. Wählen Sie das Modell Ihres Raspberry Pi aus (z. B. Raspberry Pi 5, 4, 3 oder Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

#. Gehen Sie zum Abschnitt **OS** und wählen Sie die empfohlene Option **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

#. Wählen Sie im Abschnitt **Storage** Ihre microSD-Karte aus.  
   Ziehen Sie zur Sicherheit andere USB-Laufwerke ab, damit nur die SD-Karte angezeigt wird.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

#. Klicken Sie auf **Next**, um zu den Anpassungsoptionen zu gelangen.

   .. note::

      * Wenn Sie Monitor, Tastatur und Maus direkt anschließen, können Sie **SKIP CUSTOMISATION** auswählen.  
      * Für ein *Headless-Setup* (WLAN-Fernzugriff) müssen Sie die Anpassung abschließen.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. Betriebssystem-Anpassungen**
------------------------------------------

#. **Hostname festlegen**

   * Vergeben Sie einen eindeutigen Hostnamen für Ihren Raspberry Pi.  
   * Sie können später per ``hostname.local`` eine Verbindung herstellen.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Lokalisierung festlegen**

   * Wählen Sie Ihre Hauptstadt oder nächstgelegene Stadt aus.  
   * Zeitzone und Tastaturlayout werden automatisch zugeordnet, können aber angepasst werden.  
     Wählen Sie **Next**.

   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Benutzername & Passwort festlegen**

   Erstellen Sie ein Benutzerkonto für Ihren Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **WLAN konfigurieren**

   * Geben Sie Ihr WLAN-**SSID** (Netzwerkname) und **Passwort** ein.  
   * Ihr Raspberry Pi verbindet sich beim ersten Start automatisch.

   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH aktivieren (optional, aber empfohlen)**

   * Damit können Sie sich per Fernzugriff anmelden.  
   * Anmeldung per Benutzername/Passwort oder SSH-Schlüssel möglich.

   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Raspberry Pi Connect aktivieren (optional)**

   Raspberry Pi Connect ermöglicht den Zugriff auf den Raspberry-Pi-Desktop direkt im Webbrowser.

   * Aktivieren Sie **Raspberry Pi Connect** und klicken Sie auf **OPEN RASPBERRY PI CONNECT**.

     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Die Raspberry-Pi-Connect-Website öffnet sich. Melden Sie sich mit Ihrem Raspberry-Pi-ID-Konto an oder registrieren Sie sich.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Auf der Seite **New auth key** erstellen Sie Ihren einmaligen Auth-Schlüssel.
      
      * Wenn Ihr Raspberry-Pi-ID-Konto zu keiner Organisation gehört, wählen Sie **Create auth key and launch Raspberry Pi Imager**.  
      * Wenn Sie zu einer oder mehreren Organisationen gehören, wählen Sie eine aus und erstellen Sie den Schlüssel.  
      * Schalten Sie Ihren Raspberry Pi ein und verbinden Sie ihn mit dem Internet, bevor der Schlüssel abläuft.

     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%

   * Ihr Browser fragt eventuell, ob Raspberry Pi Imager geöffnet werden soll — erlauben Sie dies.

     * Imager öffnet sich im Raspberry-Pi-Connect-Tab und zeigt den Auth-Token an.  
     * Falls der Token nicht automatisch übertragen wird, öffnen Sie im Browser den Bereich **Having trouble?**, kopieren Sie den Token und fügen Sie ihn manuell in Imager ein.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. OS-Image schreiben**
-------------------------

#. Überprüfen Sie alle Einstellungen und klicken Sie auf **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Wenn sich bereits Daten auf der Karte befinden, warnt der Imager, dass diese gelöscht werden.  
   Prüfen Sie das richtige Laufwerk und klicken Sie dann auf  
   **I UNDERSTAND, ERASE AND WRITE**.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Warten Sie, bis Schreiben und Verifizieren abgeschlossen sind.  
   Anschließend zeigt der Imager **Write complete!** und eine Zusammenfassung an. Die Karte wird automatisch ausgeworfen.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Entfernen Sie die microSD-Karte und stecken Sie sie in den Slot auf der Unterseite Ihres Raspberry Pi.  
   Ihr Raspberry Pi ist nun bereit zum Start mit dem neuen Betriebssystem!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os
