.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _setup_pi:

Richten Sie Ihren Raspberry Pi ein
==================================

Um mit dem Programmieren und Steuern Ihres Raspberry Pi zu beginnen, müssen Sie zunächst Zugriff auf ihn erhalten.  
Diese Anleitung beschreibt zwei gängige Methoden:

* Verwendung von Monitor, Tastatur und Maus  
* Headless-Setup (ohne Bildschirm) für den Fernzugriff  

.. note::

   Der auf dem Roboter installierte Raspberry Pi Zero 2W lässt sich nur schwer an einen Bildschirm anschließen.  
   Wir empfehlen daher das **Headless-Setup**.

-------------------------
Wenn Sie einen Bildschirm haben
-------------------------

**Benötigte Komponenten**

* Raspberry Pi  
* Offizielles Netzteil  
* Micro-SD-Karte  
* HDMI-Kabel  
  (Für Raspberry Pi 4/5 verwenden Sie **HDMI0**, den Anschluss in der Nähe des Stromanschlusses.)  
* Monitor  
* Tastatur und Maus  

**Schritte**

#. Stecken Sie die microSD-Karte in Ihren Raspberry Pi.
#. Schließen Sie Tastatur, Maus und Monitor an.
#. Schalten Sie Ihren Raspberry Pi ein.
#. Nach dem Booten erscheint der Desktop von Raspberry Pi OS.

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. Öffnen Sie ein **Terminal**, um Befehle einzugeben.

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 60%
      :align: center


----------------------------------
Wenn Sie keinen Bildschirm haben (Headless)
----------------------------------

Ohne Monitor können Sie Ihren Raspberry Pi vollständig per Fernzugriff konfigurieren und steuern.  
Dies ist für die meisten Benutzer die bequemste Methode.

**Benötigte Komponenten**

* Raspberry Pi  
* Offizielles Netzteil  
* Micro-SD-Karte  
* Ein Computer im selben Netzwerk  

**Tipps**

* Stellen Sie sicher, dass Sie alle Einstellungen aus :ref:`imager_custom` im Raspberry Pi Imager vorgenommen haben.
* Raspberry Pi und Computer müssen sich im selben lokalen Netzwerk befinden.
* Für maximale Stabilität nutzen Sie Ethernet, sofern verfügbar.


**Verbindung über SSH herstellen**

#. Öffnen Sie ein Terminal auf Ihrem Computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) und verbinden Sie sich mit Ihrem Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local
      # Beispiel:
      ssh daisy@pi.local

2. Alternativ können Sie die IP-Adresse Ihres Raspberry Pi über die DHCP-Liste Ihres Routers herausfinden und sich damit verbinden:

   .. code-block:: bash

      ssh <username>@<IP address>
      # Beispiel:
      ssh daisy@192.168.1.42

3. Beim ersten Login geben Sie ``yes`` ein, um das SSH-Zertifikat zu akzeptieren.

4. Geben Sie das Passwort ein, das Sie im Raspberry Pi Imager festgelegt haben.  
   (Während der Eingabe wird nichts angezeigt — das ist normal.)

5. Nach der Anmeldung haben Sie vollständigen Zugriff auf die Kommandozeile.

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

----------------------

**Fehlerbehebung**

* **ssh: Could not resolve hostname ...**

  * Stellen Sie sicher, dass der Hostname korrekt ist.  
  * Versuchen Sie die Verbindung über die IP-Adresse des Raspberry Pi.  

* **The term 'ssh' is not recognized... (Windows)**

  * OpenSSH ist nicht installiert. Installieren Sie es manuell oder nutzen Sie einen SSH-Client eines Drittanbieters.  
  * Siehe :ref:`openssh_powershell` oder :ref:`login_windows`.  

* **Permission denied (publickey,password)**

  * Vergewissern Sie sich, dass Sie Benutzername und Passwort verwenden, die im Raspberry Pi Imager erstellt wurden.  

* **Connection refused**

  * Warten Sie 1–2 Minuten nach dem Einschalten.  
  * Stellen Sie sicher, dass SSH im Raspberry Pi Imager aktiviert wurde.  

--------------------------------

Grafische Fernzugriffsmöglichkeiten
-------------------------------------

Wenn Sie eine grafische Oberfläche bevorzugen:

* :ref:`remote_desktop`: Aktivieren Sie **VNC (Virtual Network Computing)** für einen vollständigen Desktopzugriff.
* |shared_link_rpi_connect|: Verwenden Sie Raspberry Pi Connect für sicheren Fernzugriff von überall direkt im Browser.

Jetzt können Sie Ihren Raspberry Pi ohne Monitor steuern – entweder über SSH für die Kommandozeile oder über VNC / Raspberry Pi Connect für eine grafische Desktop-Erfahrung.
