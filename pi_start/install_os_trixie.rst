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

Bevor Sie Ihren Raspberry Pi verwenden, müssen Sie **Raspberry Pi OS** auf eine microSD-Karte installieren.  
Diese Anleitung erklärt, wie Sie dies mit **Raspberry Pi Imager** auf einfache und anfängerfreundliche Weise durchführen.

**Erforderliche Komponenten**

* Ein Computer (Windows, macOS oder Linux)
* Eine microSD-Karte (16 GB oder größer; empfohlene Marken: SanDisk, Samsung)
* Ein microSD-Kartenleser

-------------------

1. Raspberry Pi Imager installieren
-------------------------------------------


.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Besuchen Sie die offizielle Download-Seite von Raspberry Pi Imager: |shared_link_rpi_imager|. Laden Sie das passende Installationsprogramm für Ihr Betriebssystem herunter.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Folgen Sie den Installationsanweisungen (Sprache, Installationspfad, Bestätigung). Starten Sie nach der Installation **Raspberry Pi Imager** über Ihren Desktop oder das Anwendungsmenü.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%
      
--------------------------------------

.. end_imager


.. start_install_os

2. Installieren des Betriebssystems auf der microSD-Karte
---------------------------------------------------------------------------

1. Stecken Sie Ihre microSD-Karte mit einem Kartenleser in Ihren Computer. Sichern Sie wichtige Daten, bevor Sie fortfahren.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Wenn Raspberry Pi Imager geöffnet wird, sehen Sie die Seite **Device**. Wählen Sie Ihr Raspberry-Pi-Modell aus der Liste aus (z. B. Raspberry Pi 5, 4, 3 oder Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

.. end_install_os

3. Gehen Sie zum Abschnitt **OS** und wählen Sie die empfohlene Option **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

.. start_setup_os

4. Wählen Sie im Abschnitt **Storage** Ihre microSD-Karte aus.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. Klicken Sie auf **Next**, um mit dem Anpassungsschritt fortzufahren.

   .. note::

      * Wenn Sie einen Monitor, eine Tastatur und eine Maus direkt mit Ihrem Raspberry Pi verbinden, können Sie **SKIP CUSTOMISATION** auswählen.  
      * Wenn Sie den Raspberry Pi *headless* (über WLAN per Fernzugriff) einrichten möchten, müssen Sie die Anpassungseinstellungen konfigurieren.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

3. Anpassung der OS-Einstellungen
------------------------------------------

#. **Hostname festlegen**

   * Geben Sie Ihrem Raspberry Pi einen eindeutigen Hostnamen.  
   * Später können Sie sich über ``hostname.local`` mit ihm verbinden.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Lokalisierung festlegen**

   * Wählen Sie Ihre Hauptstadt oder Stadt aus.
   * Imager ergänzt automatisch die Zeitzone und das Tastaturlayout basierend auf Ihrer Auswahl. Sie können diese bei Bedarf anpassen. Wählen Sie anschließend **Next**.
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Benutzername und Passwort festlegen**

   Erstellen Sie ein Benutzerkonto für Ihren Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Wi-Fi konfigurieren**

   * Geben Sie Ihre Wi-Fi-**SSID** (Netzwerkname) und das **Passwort** ein.  
   * Ihr Raspberry Pi wird sich beim ersten Start automatisch verbinden.
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH aktivieren (optional, aber empfohlen)**

   * Durch Aktivieren von SSH können Sie sich von Ihrem Computer aus per Fernzugriff anmelden.  
   * Sie können sich mit Benutzername/Passwort anmelden oder SSH-Schlüssel konfigurieren.
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

.. end_setup_os

#. **Raspberry Pi Connect aktivieren (optional)**

   Raspberry Pi Connect ermöglicht es Ihnen, über einen Webbrowser auf den Desktop Ihres Raspberry Pi zuzugreifen.
   
   * Aktivieren Sie **Raspberry Pi Connect** und klicken Sie anschließend auf **OPEN RASPBERRY PI CONNECT**.
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Die Raspberry-Pi-Connect-Website wird in Ihrem Standardbrowser geöffnet. Melden Sie sich mit Ihrem Raspberry-Pi-ID-Konto an oder registrieren Sie sich, falls Sie noch keines besitzen.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Auf der Seite **New auth key** erstellen Sie Ihren einmaligen Authentifizierungsschlüssel.
      
      * Wenn Ihr Raspberry-Pi-ID-Konto keiner Organisation angehört, wählen Sie **Create auth key and launch Raspberry Pi Imager**.
      * Wenn Sie Mitglied einer oder mehrerer Organisationen sind, wählen Sie eine Organisation aus, erstellen den Schlüssel und starten anschließend Imager.
      * Stellen Sie sicher, dass Ihr Raspberry Pi eingeschaltet und mit dem Internet verbunden ist, bevor der Schlüssel abläuft.
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * Ihr Browser fragt möglicherweise, ob Raspberry Pi Imager geöffnet werden soll – bestätigen Sie dies.

     * Imager wird im Raspberry-Pi-Connect-Tab geöffnet und zeigt das Authentifizierungstoken an.
     * Wenn das Token nicht automatisch übertragen wird, öffnen Sie den Abschnitt **Having trouble?** auf der Raspberry-Pi-Connect-Seite, kopieren Sie das Token und fügen Sie es manuell in Imager ein.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

.. start_write_os

4. OS-Image schreiben
-----------------------------

#. Überprüfen Sie alle Einstellungen und klicken Sie auf **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Wenn sich bereits Daten auf der Karte befinden, zeigt Raspberry Pi Imager eine Warnung an, dass alle Daten auf dem Gerät gelöscht werden. Vergewissern Sie sich, dass Sie das richtige Laufwerk ausgewählt haben, und klicken Sie anschließend auf **I UNDERSTAND, ERASE AND WRITE**, um fortzufahren.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Warten Sie, bis der Schreib- und Verifizierungsvorgang abgeschlossen ist. Danach zeigt Raspberry Pi Imager **Write complete!** sowie eine Zusammenfassung Ihrer Auswahl an. Das Speichergerät wird automatisch ausgeworfen, sodass Sie es sicher entfernen können.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Entfernen Sie die microSD-Karte und setzen Sie sie in den Steckplatz auf der Unterseite Ihres Raspberry Pi ein. Ihr Raspberry Pi ist nun bereit, mit dem neuen Betriebssystem zu starten!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_write_os

