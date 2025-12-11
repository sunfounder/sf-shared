.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

Was benötigen Sie sonst noch?
===============================

Bevor wir mit diesem Kit beginnen, bereiten wir zunächst die wichtigsten Hardwarekomponenten vor.

Benötigte Komponenten
------------------------------

* **Raspberry Pi**

  Der Raspberry Pi fungiert als **Gehirn** des Systems und übernimmt alle Rechen-, Sensor- und Steueraufgaben.
  
  * **Kompatible Modelle**: Raspberry Pi 5, Raspberry Pi 4, 3 oder Raspberry Pi Zero 2W  

  .. image:: /_shared/pi_start/img/need_pi.jpg


* **Netzadapter**

  Bereiten Sie ein geeignetes Netzteil vor, abhängig von Ihrem Raspberry-Pi-Modell:

  .. image:: /_shared/pi_start/img/need_power.png
     :width: 400

  - **Raspberry Pi 5**: 5V 5A USB-C (empfohlen: offizielles 27W-PD-Netzteil)  
  - **Raspberry Pi 4**: 5V 3A USB-C  
  - **Raspberry Pi 3B/3B+**: 5V 2.5A Micro-USB  
  - **Raspberry Pi Zero 2W**: 5V 2A Micro-USB  

  Eine stabile Stromversorgung verhindert Unterspannung und sorgt für einen zuverlässigen Betrieb.


* **Micro-SD-Karte**

  Der Raspberry Pi besitzt kein integriertes Laufwerk. Er startet und speichert alle Daten auf einer **Micro-SD-Karte**.
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
     :width: 200

  * Minimum: **16 GB**  
  * Empfohlen: **32 GB** für mehr Stabilität  
  * Marke: Verwenden Sie zuverlässige Hersteller wie **SanDisk** oder **Samsung**, um Lese-/Schreibfehler zu vermeiden  
  

Optionale Komponenten
------------------------

Diese Komponenten sind nicht zwingend erforderlich, verbessern jedoch das Lernen und Debuggen erheblich:

* **Monitor (HDMI oder Fernseher)** 

  Für Anfänger empfehlen wir ein Display mit HDMI-Eingang, um Raspberry Pi OS einfacher einzurichten und grafische Programme auszuführen.

  .. image:: /_shared/pi_start/img/need_screen.png
     :width: 400

* **HDMI-Kabel (Standard / Mini / Micro)**
 
  Verschiedene Raspberry-Pi-Modelle verwenden unterschiedliche HDMI-Anschlüsse – prüfen Sie daher Ihr Modell und bereiten Sie das passende Kabel vor.
  
  * **Raspberry Pi 4 / 5**: Micro HDMI  
  * **Raspberry Pi 3**: Standard HDMI  
  * **Raspberry Pi Zero 2W**: Mini HDMI

  .. image:: /_shared/pi_start/img/need_hdmi.png
     :width: 400

* **Tastatur & Maus**

  Sehr nützlich bei der Ersteinrichtung von Raspberry Pi OS. Später können Sie per SSH/VNC fernzugreifen, aber für Einsteiger empfehlen wir eine einfache USB- oder Funktastatur mit Maus.

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
     :width: 500


**Tipps zur Vorbereitung**

* Wenn Sie dieses Kit gekauft haben, sind die meisten Zubehörteile enthalten, aber **Raspberry-Pi-Board**, **Micro-SD-Karte** und **Netzteil** müssen separat vorbereitet werden.  
* Unsicher, was Sie kaufen sollen? Eine stabile und universelle Empfehlung lautet:  
  **Raspberry Pi 4/5 (2 GB) + offizielles Netzteil + 32-GB-Micro-SD-Karte**.
