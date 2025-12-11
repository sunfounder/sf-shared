.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!


.. _spi_configuration:

SPI-Konfiguration
=================

Folgen Sie den untenstehenden Schritten, um die SPI-Schnittstelle auf Ihrem Raspberry Pi zu aktivieren und zu überprüfen.  
Diese Anleitung gilt für Raspberry Pi 5, 4, 3 und Zero 2W.

SPI-Schnittstelle aktivieren
----------------------------

#. Öffnen Sie ein Terminal auf Ihrem Computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) und verbinden Sie sich mit Ihrem Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   oder:

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Öffnen Sie das Konfigurationstool des Raspberry Pi:

   .. code-block:: bash

      sudo raspi-config

#. Wählen Sie **Interfacing Options** und drücken Sie **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Wählen Sie **SPI**.

   .. image:: img/ssh_spi_spi.png
      :align: center

#. Wählen Sie **<Yes>**, dann **<Ok> → <Finish>**, um die Änderungen zu übernehmen.  
   Falls Sie dazu aufgefordert werden, starten Sie Ihren Raspberry Pi neu.

   .. image:: img/ssh_spi_enable.png
      :align: center


SPI-Schnittstelle überprüfen
----------------------------

#. Prüfen Sie, ob die SPI-Geräte vorhanden sind:

   .. code-block:: bash

      ls /dev/sp*

#. Wenn die SPI-Schnittstelle aktiviert ist, enthält die Ausgabe:

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * Wenn diese Geräte angezeigt werden, ist SPI aktiv und einsatzbereit.  
   * Wenn nicht, starten Sie Ihren Raspberry Pi neu und prüfen Sie erneut.


spidev installieren (Python-SPI-Bibliothek)
-------------------------------------------

#. Installieren Sie das Paket ``spidev``, um SPI in Python zu verwenden:

   .. code-block:: bash

      sudo apt install python3-spidev

   Die Bibliothek ``spidev`` bietet Zugriff auf SPI-Geräte über die ``/dev/spidevX.Y``-Schnittstelle.

----------------------

Ihr Raspberry Pi ist nun konfiguriert und bereit, über SPI sowohl mit Kommandozeilenwerkzeugen als auch mit Python zu kommunizieren.
