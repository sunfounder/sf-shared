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
==============

Sie können den Desktop des Raspberry Pi von einem anderen Computer aus fernsteuern und darauf zugreifen.  
Die empfohlene Methode ist **VNC**, das offiziell unter Raspberry Pi OS unterstützt wird und eine zuverlässige sowie konsistente Desktop-Erfahrung bietet.

Der folgende Abschnitt erklärt, wie Sie VNC auf Ihrem Raspberry Pi aktivieren und anschließend mit |shared_link_realvnc| eine Verbindung herstellen.

-----------------

VNC-Dienst aktivieren
----------------------

Der RealVNC Server ist unter Raspberry Pi OS vorinstalliert, jedoch **standardmäßig deaktiviert**.  
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


#. Wählen Sie **Yes**, anschließend **OK**, und schließlich **Finish**, um zu beenden.

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



Mit RealVNC® Viewer einloggen
-----------------------------

#. Laden Sie |shared_link_realvnc| für Ihr Betriebssystem herunter und installieren Sie es.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Öffnen Sie **RealVNC Viewer**, geben Sie die IP-Adresse Ihres Raspberry Pi oder ``<hostname>.local`` ein und drücken Sie **Enter**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Geben Sie den **Benutzernamen** und das **Passwort** Ihres Raspberry Pi ein und wählen Sie **OK**.

   .. note::

      Beim ersten Verbinden kann eine Meldung wie „VNC Server not recognized“ erscheinen. Wählen Sie **Continue**, um fortzufahren.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Nun sollte der Raspberry Pi Desktop angezeigt werden:

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Damit ist die VNC-Einrichtung abgeschlossen.

-----------------


Zusätzliche Hinweise
--------------------

* **Desktop-Version erforderlich**

  * Für VNC muss die Desktop-Version von Raspberry Pi OS installiert sein.  
  * Wenn Sie **Raspberry Pi OS Lite** verwenden, installieren Sie den VNC-Server manuell:  
    ``sudo apt install realvnc-vnc-server``


* **Tipps zur Netzwerkleistung** 

  * Bei Verzögerungen oder niedrigen Bildraten sollten Sie Ihre Netzwerkqualität prüfen.  
  * Ein kabelgebundenes Ethernet bietet in der Regel die beste Leistung.


* **Probleme mit der Bildschirmauflösung beheben**

  * Wenn das VNC-Fenster zu klein angezeigt wird oder die Auflösung nicht stimmt, legen Sie eine feste Auflösung fest:  
    ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Sicherstellen, dass VNC aktiviert ist**

  Wenn keine Verbindung hergestellt werden kann, prüfen Sie, ob VNC aktiviert ist:  
  ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``

* **VNC-Dienst stoppen**

  Um den VNC-Server manuell zu stoppen:  
  ``sudo systemctl stop vncserver-x11-serviced``


* **Sicherheitshinweis**

  * VNC ist für vertrauenswürdige lokale Netzwerke ausgelegt.  
  * Setzen Sie VNC **nicht** direkt dem Internet aus.  
  * Für sicheren Fernzugriff von außerhalb des Netzwerks verwenden Sie **Raspberry Pi Connect** oder ein VPN.
