.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!


.. _cpn_circular_ws2812_module:

Circular WS2812 LED Module
===========================================================

.. image:: img/c_ws2812_module.png
    :width: 40%
    :align: center

Dieses kreisförmige WS2812-LED-Modul enthält 12 einzeln adressierbare RGB-LEDs. Jede LED verfügt über einen integrierten Treiber und unterstützt eine 24-Bit-Farbsteuerung über eine einzelne Datenleitung. Das Modul stellt vier Pins—VCC, GND, DIN und DOUT—zur einfachen Verbindung mit Controllern wie Raspberry Pi oder Arduino bereit.

**Pin-Übersicht**

* **V (VCC)**: 5V-Stromeingang. Stellen Sie sicher, dass Ihr Netzteil genügend Strom für alle LEDs bereitstellen kann.
* **G (GND)**: Masse. Muss mit der Masse des Controllers verbunden sein, damit die Signalübertragung korrekt funktioniert.
* **R (DIN)**: Empfängt Daten vom Mikrocontroller. Dies ist der Steuereingang.
* **D (DOUT)**: Gibt Daten an zusätzliche LED-Ringe oder LED-Streifen weiter und ermöglicht so eine Daisy-Chain-Erweiterung.

**Verwendung**

Die LEDs leiten die Daten von einer LED zur nächsten weiter. Dadurch kann jede LED unabhängig gesteuert werden, und es lassen sich Effekte wie Farbverläufe, Rotationen oder verschiedene Animationsmuster erzeugen.  
Dieser kompakte 12-LED-Ring eignet sich ideal für Statusanzeigen, dekorative Beleuchtung, Robotik-Projekte, Wearables, Uhren sowie kleine Anzeige- oder Visualisierungsprojekte.