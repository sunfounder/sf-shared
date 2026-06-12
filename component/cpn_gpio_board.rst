.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_gpio_extension_board:
.. _cpn_gpio_board:

GPIO-Erweiterungsplatine
===========================

Bevor Sie mit dem Erlernen der Befehle beginnen, müssen Sie zunächst mehr
über die Pins des Raspberry Pi wissen, was für das weitere Studium
entscheidend ist.

Wir können die Pins des Raspberry Pi mithilfe der GPIO-Erweiterungsplatine
problemlos auf das Breadboard führen, um GPIO-Schäden durch häufiges Ein-
und Ausstecken zu vermeiden. Dies ist unsere 40-Pin GPIO-Erweiterungsplatine
und das GPIO-Kabel für Raspberry Pi Modell B+, 2 Modell B und 3, 4 Modell B.

.. image:: img/image32.png
    :align: center

**Pin-Nummer**

Die Pins des Raspberry Pi werden auf drei verschiedene Arten benannt:
WiringPi, BCM und Board.

Bei diesen Benennungsmethoden verwendet die 40-Pin GPIO-Erweiterungsplatine
die BCM-Benennung. Für einige spezielle Pins wie den I2C- und den SPI-Port
wird jedoch der eigene Name verwendet.

Die folgende Tabelle zeigt die Benennungsmethoden WiringPi, Board und den
eigentlichen Namen jedes Pins auf der GPIO-Erweiterungsplatine. Zum Beispiel
ist für GPIO17 die Board-Benennung 11, die WiringPi-Benennung 0 und der
eigentliche Name GPIO0.

.. note::

    1) In der Sprache C wird die Benennungsmethode WiringPi verwendet.

    2) In Python werden die Benennungsmethoden **Board** und **BCM** verwendet,
       die mit der Funktion ``GPIO.setmode()`` eingestellt werden.

    3) In Scratch 3 und Processing wird die Benennungsmethode **BCM** verwendet.

.. image:: img/gpio_board.png