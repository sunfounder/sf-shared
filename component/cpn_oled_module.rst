.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_oled:

OLED Display Module
==========================

.. image:: img/oled.png
    :width: 300
    :align: center

Einführung
---------------------------
Ein OLED-Displaymodul (Organic Light-Emitting Diode) ist ein Anzeigemodul, das Text, Grafiken und Bilder auf einem dünnen und flexiblen Bildschirm darstellen kann. Dabei werden organische Materialien verwendet, die Licht emittieren, sobald elektrischer Strom angelegt wird.

Der wichtigste Vorteil eines OLED-Displays besteht darin, dass es selbst Licht erzeugt und keine zusätzliche Hintergrundbeleuchtung benötigt. Dadurch bieten OLED-Displays im Vergleich zu LCD-Displays häufig einen besseren Kontrast, eine höhere Helligkeit und größere Betrachtungswinkel.

Ein weiteres wichtiges Merkmal von OLED-Displays sind ihre tiefen Schwarztöne. Da jedes Pixel in einem OLED-Display selbst Licht erzeugt, kann zur Darstellung von Schwarz das jeweilige Pixel einfach ausgeschaltet werden.

Dank ihres geringeren Stromverbrauchs (nur aktive Pixel benötigen Strom) werden OLED-Displays häufig in batteriebetriebenen Geräten wie Smartwatches, Gesundheits-Trackern und anderen Wearables eingesetzt.

Prinzip
---------------------------
Ein OLED-Displaymodul besteht aus einem OLED-Panel sowie einem OLED-Treiberchip, der auf der Rückseite des Moduls montiert ist. Das OLED-Panel besteht aus vielen kleinen Pixeln, die Licht in verschiedenen Farben erzeugen können. Jedes Pixel besteht aus mehreren Schichten organischer Materialien, die zwischen zwei Elektroden (Anode und Kathode) eingebettet sind. Wenn elektrischer Strom durch diese Elektroden fließt, emittieren die organischen Materialien Licht unterschiedlicher Wellenlängen, abhängig von ihrer chemischen Zusammensetzung.

Der OLED-Treiberchip steuert die Pixel des OLED-Panels über ein serielles Kommunikationsprotokoll namens I2C (Inter-Integrated Circuit).

Der OLED-Treiberchip wandelt die Signale vom Arduino in Steuerbefehle für das OLED-Panel um. Der Arduino kann Daten über eine Bibliothek senden, die das I2C-Protokoll unterstützt. Eine solche Bibliothek ist beispielsweise die Adafruit SSD1306 Library. Mit dieser Bibliothek können Sie das OLED-Displaymodul initialisieren, die Helligkeit einstellen sowie Text, Grafiken oder Bilder anzeigen.