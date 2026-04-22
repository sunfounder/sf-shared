.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. start_setup_pi

Raspberry Pi einrichten
====================================

Um mit der Programmierung und Steuerung Ihres Raspberry Pi zu beginnen, müssen Sie zunächst darauf zugreifen.  
Diese Anleitung beschreibt zwei gängige Methoden:

* Verwendung von Monitor, Tastatur und Maus  
* Einrichtung einer Headless-Verbindung (ohne Bildschirm) für den Fernzugriff  

.. note::

   Der auf dem Roboter installierte Raspberry Pi Zero 2W lässt sich nur schwer mit einem Bildschirm verbinden.  
   Wir empfehlen daher die **Headless-Einrichtung**.

.. end_setup_pi

.. start_setup_pi_screen

-------------------------

Wenn Sie einen Bildschirm haben
----------------------------------------

**Erforderliche Komponenten**

* Raspberry Pi
* Offizielles Netzteil
* MicroSD-Karte
* HDMI-Kabel  
  (Für Raspberry Pi 4/5 verwenden Sie **HDMI0**, den Anschluss nahe am Stromanschluss.)
* Monitor
* Tastatur und Maus

**Schritte**

#. Stecken Sie die MicroSD-Karte in Ihren Raspberry Pi.
#. Schließen Sie Tastatur, Maus und Monitor an.
#. Schalten Sie den Raspberry Pi ein.
#. Nach dem Start erscheint der Desktop von Raspberry Pi OS. 

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. Öffnen Sie ein **Terminal**, um Befehle einzugeben.

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center

.. end_setup_pi_screen

.. start_setup_pi_headless

----------------------------------

Wenn Sie keinen Bildschirm haben (Headless)
------------------------------------------------------

Ohne Monitor können Sie Ihren Raspberry Pi aus der Ferne konfigurieren und sich anmelden.  
Dies ist für die meisten Nutzer die bequemste Methode.

**Erforderliche Komponenten**

* Raspberry Pi
* Offizielles Netzteil
* MicroSD-Karte
* Ein Computer im selben Netzwerk

**Tipps**

* Stellen Sie sicher, dass Sie bei der Installation des Systems mit Raspberry Pi Imager alle in :ref:`imager_custom` beschriebenen Einstellungen vorgenommen haben.
* Achten Sie darauf, dass sich Ihr Raspberry Pi und Ihr Computer im selben lokalen Netzwerk befinden.
* Für die beste Stabilität verwenden Sie nach Möglichkeit eine Ethernet-Verbindung.


**Verbindung über SSH**

#. Öffnen Sie ein Terminal auf Ihrem Computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) und verbinden Sie sich mit Ihrem Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local
      # Beispiel:
      ssh daisy@pi.local

2. Alternativ können Sie die IP-Adresse Ihres Raspberry Pi in der DHCP-Liste Ihres Routers ermitteln und sich wie folgt verbinden:

   .. code-block:: bash

      ssh <username>@<IP-Adresse>
      # Beispiel:
      ssh daisy@192.168.1.42

3. Geben Sie bei der ersten Anmeldung ``yes`` ein, um das SSH-Zertifikat zu bestätigen.

4. Geben Sie das Passwort ein, das Sie im Raspberry Pi Imager festgelegt haben.  
   (Während der Eingabe wird nichts angezeigt – das ist normal.)

5. Nach der Anmeldung haben Sie vollständigen Zugriff auf die Kommandozeile.

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center


.. end_setup_pi_headless




.. start_setup_pi_troubleshooting

----------------------

**Fehlerbehebung**

* **ssh: Could not resolve hostname ...**

  * Stellen Sie sicher, dass der Hostname korrekt ist.
  * Versuchen Sie die Verbindung über die IP-Adresse des Raspberry Pi.

* **The term 'ssh' is not recognized... (Windows)**

  * OpenSSH ist nicht installiert. Installieren Sie es manuell oder verwenden Sie einen SSH-Client eines Drittanbieters.  
  * Siehe :ref:`openssh_powershell` oder :ref:`login_windows`.

* **Permission denied (publickey,password)**

  * Vergewissern Sie sich, dass Sie den im Raspberry Pi Imager erstellten Benutzernamen und das Passwort verwenden.

* **Connection refused**

  * Warten Sie 1–2 Minuten nach dem Einschalten.
  * Prüfen Sie, ob SSH im Raspberry Pi Imager aktiviert wurde.

.. end_setup_pi_troubleshooting

.. start_setup_pi_remote_desktop

--------------------------------

Grafische Fernzugriffsoptionen
---------------------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

Wenn Sie eine grafische Oberfläche bevorzugen:

* :ref:`remote_desktop`: Aktivieren Sie **VNC (Virtual Network Computing)** für eine vollständige Desktop-Erfahrung auf Ihrem Raspberry Pi.

* |shared_link_rpi_connect|: Verwenden Sie Raspberry Pi Connect für sicheren Fernzugriff von überall aus, direkt im Browser. 

Nun können Sie Ihren Raspberry Pi auch ohne Monitor steuern – entweder über SSH für Kommandozeilenoperationen oder mit VNC bzw. Raspberry Pi Connect für eine grafische Desktop-Oberfläche.

.. end_setup_pi_remote_desktop