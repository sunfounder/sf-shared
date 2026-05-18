.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _i2c_config:

I²C-Konfiguration
===================

Folgen Sie den untenstehenden Schritten, um die I²C-Schnittstelle auf Ihrem Raspberry Pi zu aktivieren und zu testen.  
Diese Anleitung gilt für Raspberry Pi 5, 4, 3 und Zero 2W.

I²C-Schnittstelle aktivieren
------------------------------

#. Öffnen Sie ein Terminal auf Ihrem Computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) und verbinden Sie sich mit Ihrem Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   oder:

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Öffnen Sie das Raspberry-Pi-Konfigurationstool:

   .. code-block:: bash

      sudo raspi-config

#. Wählen Sie **Interfacing Options** und drücken Sie **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Wählen Sie **I2C**.

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. Wählen Sie **<Yes>**, anschließend **<Ok> → <Finish>**, um die Änderungen zu übernehmen.  
   Starten Sie den Raspberry Pi neu, falls Sie dazu aufgefordert werden.

   .. image:: img/ssh_i2c_yes.png
      :align: center


I²C-Kernel-Module überprüfen
------------------------------

#. Führen Sie den folgenden Befehl aus:

   .. code-block:: bash

      lsmod | grep i2c

#. Wenn I²C aktiviert ist, sehen Sie Module wie zum Beispiel:

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. Wenn nichts angezeigt wird, starten Sie das System neu:

   .. code-block:: bash

      sudo reboot


i2c-tools installieren
------------------------

#. Installieren Sie die Dienstprogramme, die zum Scannen und Testen von I²C-Geräten erforderlich sind:

   .. code-block:: bash

      sudo apt install i2c-tools


Angeschlossene I²C-Geräte erkennen
------------------------------------

#. Scannen Sie den I²C-Bus:

   .. code-block:: bash

      i2cdetect -y 1

#. Beispielausgabe:

   .. code-block:: text

      pi@raspberrypi ~ $ i2cdetect -y 1
          0  1  2  3   4  5  6  7  8  9   a  b  c  d  e  f
      00:           -- -- -- -- -- -- -- -- -- -- -- -- --
      10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
      50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      70: -- -- -- -- -- -- -- --

#. Wenn ein Gerät angeschlossen ist, erscheint dessen Adresse (z. B. **0x48**) in der Tabelle.


Python-I²C-Bibliothek installieren
------------------------------------

#. Installieren Sie das Paket ``python3-smbus2``:

   .. code-block:: bash

      sudo apt install python3-smbus2

   Die Bibliothek ``smbus2`` stellt alle Funktionen bereit, die für die Kommunikation mit I²C-Geräten in Python erforderlich sind.

Ihr Raspberry Pi ist nun vollständig konfiguriert und bereit für die Kommunikation mit I²C-Geräten.
