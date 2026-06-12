.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!


.. _install_all_modules_fusion_hat:

Stromversorgung konfigurieren & Software installieren (Wichtig)
==================================================================

In diesem Kapitel installieren Sie die erforderliche Software, konfigurieren die Audioausgabe, richten ein sicheres Energiemanagement ein und lernen, wie Sie den Raspberry Pi korrekt herunterfahren.

.. start_install_fusion_hat



Installation des ``fusion-hat``-Moduls
----------------------------------------

Bei diesem Kit werden alle GPIO-Funktionen über das Fusion HAT+ verwaltet.  
Daher müssen Sie die zugehörige Bibliothek ``fusion-hat`` verwenden, um auf diese Funktionen zuzugreifen und sie zu steuern.

Führen Sie den folgenden Befehl im Terminal aus, um das ``fusion-hat``-Modul zu installieren:

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note::
   Weitere Details zum Fusion HAT+ finden Sie in der Dokumentation unter |shared_link_fusion_hat|.


Nach Abschluss der Installation starten Sie den Raspberry Pi neu.  
Führen Sie anschließend das Audio-Einrichtungsskript aus:

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Damit ist die Softwareinstallation für das Fusion HAT+ abgeschlossen.

.. end_install_fusion_hat

.. start_configure_safe_shutdown


Sicheres Herunterfahren konfigurieren und verwenden
------------------------------------------------------

Das Fusion HAT+ nutzt das Herunterfahr-Signal des Raspberry Pi, um die Stromversorgung vollständig zu steuern.  
Um einen sicheren und zuverlässigen Abschaltvorgang zu gewährleisten, müssen Sie das **Herunterfahrverhalten** entsprechend Ihrem Raspberry-Pi-Modell konfigurieren und anschließend den **Power-Taster** korrekt verwenden.

**Für Raspberry Pi 5 und 4B**

Diese Modelle unterstützen ein vollständiges Abschalten nach dem Herunterfahren.  
Das Fusion HAT+ überwacht die 3,3-V-Leitung, um den Betriebszustand des Raspberry Pi zu erkennen.

1. Setzen Sie den Jumper auf **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Öffnen Sie die EEPROM-Konfiguration manuell:

   .. code-block::

      sudo raspi-config

3. Navigieren Sie zu **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Wählen Sie **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Speichern Sie die Änderungen. Sie werden aufgefordert, das System neu zu starten, damit die Einstellungen wirksam werden.

**Für Raspberry Pi Zero 2W, 3B, 3B+**

Diese Modelle unterstützen **kein** vollständiges Abschalten über die 3,3-V-Leitung.  
Stattdessen muss GPIO26 als Statusanzeige für den Shutdown konfiguriert werden.

1. Setzen Sie den Jumper auf **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Bearbeiten Sie die Datei ``/boot/firmware/config.txt``:

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Fügen Sie am Ende der Datei folgende Zeile hinzu, um GPIO26 beim Herunterfahren auf LOW und beim Einschalten auf HIGH zu setzen:

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Starten Sie das System neu, um die Änderungen zu übernehmen:

   .. code-block::

      sudo reboot

**Verwendung des Power-Tasters für sicheres Herunterfahren**

Nach Abschluss der Konfiguration können Sie den PiCar-X über den Power-Taster des Fusion HAT+ sicher ausschalten.

* **Sanftes Herunterfahren (empfohlen)**

  * Halten Sie den Power-Taster **2 Sekunden** lang gedrückt.  
  * Die beiden Power-LEDs blinken schnell.  
  * Lassen Sie den Taster los → das Fusion HAT+ startet den Shutdown des Raspberry Pi.  
  * Nach Abschluss des Herunterfahrens trennt das Fusion HAT+ automatisch die Stromversorgung.  
  * Dies schützt Ihre SD-Karte und Ihre Dateien.

* **Hartes Ausschalten (nur im Notfall)**

  * Wenn das System nicht mehr reagiert, halten Sie den Power-Taster **5 Sekunden oder länger** gedrückt.  
  * Das Fusion HAT+ erzwingt ein sofortiges Abschalten.  
  * Warnung: Dies kann die SD-Karte oder Systemdateien beschädigen. Nur verwenden, wenn es unbedingt erforderlich ist.

.. end_configure_safe_shutdown