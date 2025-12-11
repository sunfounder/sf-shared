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

Bevor wir mit diesem Kit loslegen, bereiten wir zunächst die wichtigsten Hardwarekomponenten vor.

Benötigte Komponenten
------------------------------

* **Raspberry Pi**

  Der Raspberry Pi dient als **Gehirn** des Systems und übernimmt alle Rechen-, Sensor- und Steueraufgaben.
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **Kompatible Modelle**: Raspberry Pi 5, Raspberry Pi 4, 3 oder Raspberry Pi Zero 2W  
  * **Minimum**: **2 GB RAM** — ausreichend für alle Standard-Python-Projekte sowie für die Nutzung **onlinebasierter KI-Dienste** wie OpenAI Whisper, TTS oder LLMs.  
  * **Empfohlen**: **4 GB RAM oder mehr** — sorgt für flüssigere Leistung, insbesondere wenn **lokale KI-Modelle** (z. B. Vosk-Spracherkennung, Piper TTS oder leichte LLMs) parallel zu Kamera-Streaming und Steuerungsaufgaben laufen.  


* **Netzadapter**

  Dieses Kit enthält ein **18650-Akkupack** sowie ein **Fusion HAT** mit integrierter Ladeelektronik.
  
  .. image:: /_shared/pi_start/img/need_power.png
     :width: 400

  * Für das Laden wird ein **5V-3A-Netzteil** empfohlen, z. B. der offizielle **Raspberry Pi 15W USB-C Adapter**.  
  * Alternativ können **USB-C Power Delivery (PD)** oder **QC 2.0 Schnellladegeräte** verwendet werden.  
  * Eine vollständige Ladung dauert typischerweise etwa **2 Stunden** (von 0 % auf 100 %).  


* **Micro-SD-Karte**

  Der Raspberry Pi besitzt kein internes Laufwerk. Er startet und speichert alle Daten auf einer **Micro-SD-Karte**.
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
     :width: 200

  * Minimum: **16 GB**  
  * Empfohlen: **32 GB** für bessere Stabilität  
  * Marke: Verwenden Sie zuverlässige Hersteller wie **SanDisk** oder **Samsung**, um Lese-/Schreibfehler zu vermeiden  
  
Optionale Komponenten
------------------------

Diese Komponenten sind nicht zwingend notwendig, verbessern jedoch Ihr Lern- und Debugging-Erlebnis erheblich:

* **Monitor (HDMI oder Fernseher)**

  Für Anfänger empfehlen wir dringend ein Display mit HDMI-Eingang, um Raspberry Pi OS leichter einzurichten und grafische Anwendungen auszuführen.

  .. image:: /_shared/pi_start/img/need_screen.png
     :width: 400

* **HDMI-Kabel (Standard / Mini / Micro)**
 
  Da verschiedene Raspberry-Pi-Modelle unterschiedliche HDMI-Anschlüsse verwenden, stellen Sie sicher, dass Sie das passende Kabel bereithalten.
  
  * **Raspberry Pi 4 / 5**: Micro HDMI  
  * **Raspberry Pi 3**: Standard HDMI  
  * **Raspberry Pi Zero 2W**: Mini HDMI 

  .. image:: /_shared/pi_start/img/need_hdmi.png
     :width: 400

* **Tastatur & Maus**

  Sehr hilfreich während der Ersteinrichtung von Raspberry Pi OS. Später können Sie per SSH/VNC fernzugreifen, doch für Einsteiger ist ein einfaches USB- oder Funktastatur-/Maus-Set empfehlenswert.

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
     :width: 500
 

**Tipps zur Vorbereitung**

* Wenn Sie dieses Kit gekauft haben, sind die meisten Zubehörteile bereits enthalten, aber Sie müssen **Raspberry-Pi-Board**, **Micro-SD-Karte** und **Netzteil** separat vorbereiten.  
* Unsicher, was Sie kaufen sollen? Eine stabile und universelle Empfehlung lautet:  
  **Raspberry Pi 4 (2 GB) + offizielles Netzteil + 32 GB Micro-SD-Karte**.
