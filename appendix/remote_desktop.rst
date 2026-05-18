.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _remote_desktop:

Remote Desktop
================

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

Sie können den Desktop des Raspberry Pi von einem anderen Computer aus fernsteuern und bedienen.  
Die empfohlene Methode ist **VNC**, da sie offiziell von Raspberry Pi OS unterstützt wird und eine zuverlässige sowie konsistente Desktop-Erfahrung bietet.

Der folgende Abschnitt erklärt, wie Sie VNC auf Ihrem Raspberry Pi aktivieren und sich anschließend mit dem |shared_link_realvnc| verbinden.

-----------------

VNC-Dienst aktivieren
-----------------------

Der RealVNC Server ist auf Raspberry Pi OS vorinstalliert, aber **standardmäßig deaktiviert**.  
Sie müssen ihn über das Konfigurationstool aktivieren.

#. Öffnen Sie ein Terminal auf Ihrem Computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) und verbinden Sie sich mit Ihrem Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   oder

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Starten Sie das Konfigurationstool:

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. Wählen Sie **Interfacing Options** und drücken Sie **Enter**.

   .. image:: /_shared/appendix/img/ssh_interface.png


#. Wählen Sie **VNC**.

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. Wählen Sie **Yes**, anschließend **OK** und schließlich **Finish**, um das Tool zu verlassen.

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



Anmeldung mit RealVNC® Viewer
-------------------------------

#. Laden Sie den |shared_link_realvnc| für Ihr Betriebssystem herunter und installieren Sie ihn.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Öffnen Sie den **RealVNC Viewer**, geben Sie dann die IP-Adresse Ihres Raspberry Pi oder ``<hostname>.local`` ein und drücken Sie **Enter**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Geben Sie den **Benutzernamen** und das **Passwort** Ihres Raspberry Pi ein und wählen Sie anschließend **OK**.

   .. note::

      Bei der ersten Verbindung kann eine Meldung wie „VNC Server not recognized“ erscheinen.  
      Wählen Sie **Continue**, um fortzufahren.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Nun sollten Sie den Desktop des Raspberry Pi sehen:

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Damit ist die VNC-Einrichtung abgeschlossen.

-----------------


Zusätzliche Hinweise
----------------------

* **Desktop-Version erforderlich**

  * VNC setzt voraus, dass auf dem Raspberry Pi die vollständige Desktop-Version von Raspberry Pi OS läuft.  
  * Wenn Sie **Raspberry Pi OS Lite** verwenden, installieren Sie den VNC Server manuell: ``sudo apt install realvnc-vnc-server``


* **Tipps zur Netzwerkleistung**

  * Wenn Verzögerungen oder niedrige Bildwiederholraten auftreten, überprüfen Sie die Qualität Ihres Netzwerks.  
  * Eine kabelgebundene Ethernet-Verbindung bietet in der Regel die beste Leistung.


* **Behebung von Problemen mit der Bildschirmauflösung**

  * Wenn das VNC-Fenster zu klein erscheint oder die Auflösung nicht korrekt ist, legen Sie eine feste Auflösung fest über:  
    ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Sicherstellen, dass VNC aktiviert ist**

  Falls keine Verbindung hergestellt werden kann, überprüfen Sie, ob VNC aktiviert ist unter:  
  ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``


* **VNC-Dienst stoppen**

  Um den VNC Server manuell zu stoppen:  
  ``sudo systemctl stop vncserver-x11-serviced``


* **Sicherheitshinweis**

  * VNC ist für vertrauenswürdige lokale Netzwerke vorgesehen.  
  * Setzen Sie VNC **nicht** direkt dem Internet aus.  
  * Für sicheren Fernzugriff von außerhalb Ihres Netzwerks verwenden Sie **Raspberry Pi Connect** oder ein VPN.
