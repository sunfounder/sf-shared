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
================================

.. start_imager

Bevor Sie Ihren Raspberry Pi verwenden können, müssen Sie **Raspberry Pi OS** auf eine microSD-Karte installieren.  
Diese Anleitung erklärt auf einfache und anfängerfreundliche Weise, wie Sie dies mit dem **Raspberry Pi Imager** durchführen.

**Erforderliche Komponenten**

* Ein Computer (Windows, macOS oder Linux)
* Eine microSD-Karte (16 GB oder größer; empfohlene Marken: SanDisk, Samsung)
* Ein microSD-Kartenleser

-------------------

**1. Raspberry Pi Imager installieren**
---------------------------------------


.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Besuchen Sie die offizielle Download-Seite des Raspberry Pi Imager: |shared_link_rpi_imager|. Laden Sie das passende Installationsprogramm für Ihr Betriebssystem herunter.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Folgen Sie den Installationsanweisungen (Sprache, Installationspfad, Bestätigung). Starten Sie nach der Installation den **Raspberry Pi Imager** über den Desktop oder das Anwendungsmenü.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. Betriebssystem auf die microSD-Karte installieren**
--------------------------------------------------------

1. Stecken Sie Ihre microSD-Karte mithilfe eines Kartenlesers in Ihren Computer. Sichern Sie zuvor alle wichtigen Daten.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Nach dem Start des Raspberry Pi Imager sehen Sie die **Device**-Seite. Wählen Sie Ihr Raspberry-Pi-Modell aus der Liste aus (z. B. Raspberry Pi 5, 4, 3 oder Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

3. Wechseln Sie zum Bereich **OS** und wählen Sie die empfohlene Option **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

4. Wählen Sie im Bereich **Storage** Ihre microSD-Karte aus. Entfernen Sie zur Sicherheit andere USB-Laufwerke, sodass nur die SD-Karte in der Liste erscheint.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. Klicken Sie auf **Next**, um mit dem Anpassungsschritt fortzufahren.

   .. note::

      * Wenn Sie Monitor, Tastatur und Maus direkt an den Raspberry Pi anschließen, können Sie **SKIP CUSTOMISATION** auswählen.  
      * Wenn Sie den Raspberry Pi *headless* (per WLAN und Fernzugriff) einrichten möchten, müssen Sie die Anpassungseinstellungen ausfüllen.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. Betriebssystem-Anpassungseinstellungen**
---------------------------------------------

#. **Hostname festlegen**

   * Geben Sie Ihrem Raspberry Pi einen eindeutigen Hostnamen.  
   * Sie können später eine Verbindung über ``hostname.local`` herstellen.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Lokalisierung festlegen**

   * Wählen Sie Ihre nächstgelegene Großstadt aus.
   * Der Imager ergänzt automatisch Zeitzone und Tastaturlayout, Sie können diese bei Bedarf anpassen. Wählen Sie anschließend **Next**.
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Benutzername & Passwort festlegen**

   Erstellen Sie ein Benutzerkonto für Ihren Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **WLAN konfigurieren**

   * Geben Sie Ihre WLAN-**SSID** (Netzwerkname) und das **Passwort** ein.  
   * Ihr Raspberry Pi verbindet sich beim ersten Start automatisch mit dem Netzwerk.
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **SSH aktivieren (optional, aber empfohlen)**

   * Durch das Aktivieren von SSH können Sie sich aus der Ferne von Ihrem Computer anmelden.  
   * Sie können sich mit Benutzername/Passwort anmelden oder SSH-Schlüssel konfigurieren.
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Raspberry Pi Connect aktivieren (optional)**


   Raspberry Pi Connect ermöglicht den Zugriff auf den Desktop Ihres Raspberry Pi über einen Webbrowser.
   
   * Aktivieren Sie **Raspberry Pi Connect** und klicken Sie anschließend auf **OPEN RASPBERRY PI CONNECT**.
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Die Website von Raspberry Pi Connect wird in Ihrem Standardbrowser geöffnet. Melden Sie sich mit Ihrem Raspberry Pi ID-Konto an oder registrieren Sie sich, falls Sie noch keines haben.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Erstellen Sie auf der Seite **New auth key** Ihren einmaligen Authentifizierungsschlüssel.
      
      * Wenn Ihr Raspberry Pi ID-Konto keiner Organisation angehört, wählen Sie **Create auth key and launch Raspberry Pi Imager**.
      * Wenn Sie Mitglied einer oder mehrerer Organisationen sind, wählen Sie eine aus, erstellen Sie den Schlüssel und starten Sie den Imager.
      * Stellen Sie sicher, dass Ihr Raspberry Pi eingeschaltet ist und mit dem Internet verbunden ist, bevor der Schlüssel abläuft.
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * Ihr Browser fragt möglicherweise, ob Raspberry Pi Imager geöffnet werden soll – erlauben Sie dies.

     * Der Imager öffnet sich im Tab „Raspberry Pi Connect“ und zeigt das Authentifizierungstoken an.
     * Falls das Token nicht automatisch übertragen wird, öffnen Sie den Abschnitt **Having trouble?** auf der Raspberry Pi Connect-Seite, kopieren Sie das Token und fügen Sie es manuell in den Imager ein.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. Betriebssystem schreiben**


#. Überprüfen Sie alle Einstellungen und klicken Sie auf **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Wenn sich bereits Daten auf der Karte befinden, zeigt der Raspberry Pi Imager eine Warnung an, dass alle Daten gelöscht werden. Vergewissern Sie sich, dass Sie das richtige Laufwerk ausgewählt haben, und klicken Sie dann auf **I UNDERSTAND, ERASE AND WRITE**, um fortzufahren.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Warten Sie, bis der Schreib- und Überprüfungsvorgang abgeschlossen ist. Danach zeigt der Raspberry Pi Imager **Write complete!** sowie eine Zusammenfassung Ihrer Auswahl an. Das Speichermedium wird automatisch ausgeworfen, sodass Sie es sicher entfernen können.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Entfernen Sie die microSD-Karte und stecken Sie sie in den Steckplatz auf der Unterseite Ihres Raspberry Pi. Ihr Raspberry Pi ist nun bereit, mit dem neuen Betriebssystem zu starten!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os
