.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!


.. _install_all_modules:

Strom konfigurieren & Software installieren (Wichtig)
================================================================

In diesem Kapitel installieren Sie die benötigte Software, konfigurieren die Audioeinstellungen, richten ein sicheres Powermanagement ein und lernen, wie Sie Abschaltungen korrekt durchführen.

.. _install_fusion_hat:

``fusion-hat``-Modul installieren
----------------------------------

Für dieses Kit werden alle GPIO-Funktionen über das Fusion HAT verwaltet. Daher müssen Sie die zugehörige ``fusion-hat``-Bibliothek verwenden, um darauf zuzugreifen und es zu steuern.

Führen Sie im Terminal folgenden Befehl aus, um das ``fusion-hat``-Modul zu installieren:

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. note:: Ausführliche Informationen zum Fusion HAT finden Sie unter |shared_link_fusion_hat|.


Nach Abschluss der Installation starten Sie den Raspberry Pi neu. Danach führen Sie das Audio-Setup-Skript aus:

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Damit ist die Softwareinstallation für das Fusion HAT abgeschlossen.

Sicheres Herunterfahren konfigurieren und verwenden
----------------------------------------------------

Das Fusion HAT stützt sich auf das Shutdown-Signal des Raspberry Pi, um die Stromversorgung vollständig zu verwalten.  
Um einen sicheren und zuverlässigen Ausschaltvorgang zu gewährleisten, müssen Sie das **Herunterfahrverhalten** abhängig vom Raspberry-Pi-Modell konfigurieren und anschließend die **Powertaste** korrekt verwenden.

**Für Raspberry Pi 5 und 4B**

Diese Modelle unterstützen vollständiges Ausschalten nach dem Shutdown. Das Fusion HAT überwacht die 3,3V-Leitung, um den Stromzustand des Pi zu erkennen.

1. Setzen Sie den Jumper auf **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Öffnen Sie die EEPROM-Konfiguration:

   .. code-block::

      sudo raspi-config

3. Navigieren Sie zu **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Wählen Sie **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Speichern Sie die Änderungen. Sie werden aufgefordert, neu zu starten, damit die Einstellungen wirksam werden.

**Für Raspberry Pi Zero 2W, 3B, 3B+**

Diese Modelle unterstützen **kein** vollständiges Ausschalten über die 3,3V-Leitung. Stattdessen muss GPIO26 als Shutdown-Indikator konfiguriert werden.

1. Setzen Sie den Jumper auf **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Bearbeiten Sie die Datei ``/boot/firmware/config.txt``:

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Fügen Sie folgende Zeile am Ende hinzu, um GPIO26 beim Shutdown auf Low und beim Start auf High zu setzen:

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Starten Sie neu, um die Änderungen zu übernehmen:

   .. code-block::

      sudo reboot

**Die Powertaste für einen sicheren Shutdown verwenden**

Nach erfolgreicher Konfiguration können Sie die PiCar-X sicher über die Powertaste des Fusion HAT ausschalten.

* **Soft Shutdown (Empfohlen)**

  * Powertaste **2 Sekunden lang** gedrückt halten.  
  * Die beiden Power-LEDs beginnen schnell zu blinken.  
  * Taste loslassen → Fusion HAT initiiert das Herunterfahren des Raspberry Pi.  
  * Nach Abschluss des Shutdowns trennt das Fusion HAT automatisch die Stromversorgung.  
  * Dies schützt Ihre SD-Karte und Dateien.

* **Hard Shutdown (Nur im Notfall)**

  * Wenn das System nicht reagiert, Powertaste **länger als 5 Sekunden** gedrückt halten.  
  * Fusion HAT erzwingt ein sofortiges Abschalten.  
  * Warnung: Dies kann die SD-Karte oder Systemdateien beschädigen. Verwenden Sie diese Methode nur im Notfall.
