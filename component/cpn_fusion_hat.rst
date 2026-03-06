.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_fusion_hat:

Fusion HAT+
=====================================

.. image:: img/fusionhat_v0.png
    :width: 500
    :align: center
   

Das Fusion HAT+ ist eine leistungsstarke und vielseitige Erweiterungsplatine, die entwickelt wurde, um einen Raspberry Pi mit minimalem Einrichtungsaufwand in einen voll funktionsfähigen Roboter zu verwandeln. Gleichzeitig eignet sie sich auch hervorragend für anspruchsvolle Automatisierungsprojekte.

Im Zentrum des Fusion HAT+ befindet sich ein integrierter Mikrocontroller (MCU), der die native Funktionalität des Raspberry Pi erheblich erweitert. Er stellt zusätzliche PWM-Ausgänge und ADC-Eingänge bereit – Funktionen, die auf Standard-Raspberry-Pi-Modellen normalerweise nicht vorhanden sind. Dadurch können Entwickler eine präzisere Motorsteuerung und eine bessere Sensorintegration realisieren.

Trotz seiner kompakten Größe bietet das Fusion HAT+ umfangreiche Funktionen. Es integriert vier Motortreiber-Chips, die eine unabhängige Steuerung von bis zu vier DC-Motoren ermöglichen. Darüber hinaus verfügt es über ein digitales I2S-Audiomodul und einen integrierten Mono-Lautsprecher, wodurch hochwertige Audiowiedergabe und interaktive Soundfunktionen direkt über die Platine möglich sind.

Die Platine akzeptiert eine Eingangsspannung von 6,0 V bis 8,4 V über einen 3-poligen XH2.54-Steckverbinder. Sie verfügt über zwei Power-Status-LEDs zur Überwachung des Systemzustands, eine frei programmierbare Benutzer-LED für individuelle Signalisierungen sowie praktische Onboard-Tasten für sofortige Funktionstests oder Eingabesimulationen. Dadurch werden Entwicklung und Fehlersuche deutlich effizienter und benutzerfreundlicher.

.. |link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">SunFounder Fusion HAT+</a>

Detaillierte Anleitungen finden Sie unter: |link_fusion_hat|.

PinPal
============================

.. image:: img/pinpal_pic.png
    :width: 20%
    :align: center

PinPal ist eine kleine Leiterplatte (PCB), die von SunFounder entwickelt wurde und mit Beschriftungen der Raspberry-Pi-Pins versehen ist.  
Sie kann direkt auf die Pinleiste des Fusion HAT+ gesteckt werden, sodass sich die Funktion jedes Pins beim Aufbau Ihres Projekts schnell und eindeutig erkennen lässt.  
Dadurch werden Verdrahtungsfehler reduziert und die Arbeit deutlich beschleunigt.

.. image:: img/pinpal_fusion_hat.png
    :width: 80%
    :align: center

Einige Pins auf PinPal werden **nicht für die direkte Verwendung empfohlen**, da sie bereits vom Fusion HAT+ genutzt werden oder Funktionen teilen, die zu Konflikten führen können.


#. **SDA / SCL — I2C (GPIO2 / GPIO3)**

   * Haupt-I2C-Pins des Raspberry Pi.  
   * Das Fusion HAT+ stellt zusätzlich einen P2.54-I2C-Header sowie einen SH1.0-Qwiic/STEMMA-QT-Port bereit.  
   * Alle drei verwenden denselben Bus, daher kann **immer nur einer gleichzeitig genutzt werden**.

   .. image:: img/pinpal_i2c.png
       :width: 80%
       :align: center

#. **TXD / RXD — UART (GPIO14 / GPIO15)**

   * Haupt-UART-Pins des Raspberry Pi.  
   * Das Fusion HAT+ verfügt über einen zusätzlichen UART-Anschluss, der dieselben Pins nutzt — **verwenden Sie daher nur einen davon**.

   .. image:: img/pinpal_uart.png
       :width: 80%
       :align: center

#. **GPIO 17 / 4 / 27 / 22 — Allgemeine GPIOs**

   * Das Fusion HAT+ stellt einen zusätzlichen Satz dieser Pins bereit, sie sind jedoch denselben Raspberry-Pi-GPIOs zugeordnet.  
   * **Verwenden Sie jeweils nur eine Gruppe**, um Konflikte zu vermeiden.

   .. image:: img/pinpal_gpio.png
       :width: 80%
       :align: center

#. **MOSI / MISO / SCLK / CE0 / GPIO6 — SPI-Pins**

   * Das Fusion HAT+ bietet einen zusätzlichen SPI-Anschluss.  
   * Der RGB-Connector (WS2812) verwendet den MOSI-Pin.  
   * **Verwenden Sie jeweils nur eine SPI-Gruppe**, um Konflikte zu vermeiden.


   .. list-table::
      :header-rows: 1

      * - Signal
        - Pin Mapping
      * - BSY
        - GPIO6
      * - CS
        - CE0 / GPIO8
      * - SCK
        - SCLK / GPIO11
      * - MI
        - MISO / GPIO9
      * - MO
        - MOSI / GPIO10

   .. image:: img/pinpal_spi.png
       :width: 80%
       :align: center


#. **GPIO 18 / 19 / 20 / 21 — I2S-Audio-Pins**

   * Das Fusion HAT+ verfügt über integriertes I2S-Audio (Lautsprecher + Mikrofon). Weitere Details:  
     `I2S <https://docs.sunfounder.com/projects/fusion-hat/en/latest/hardware/interfaces.html#speaker-and-mic>`_.
   * Diese Pins können nur dann wiederverwendet werden, wenn das Audiosystem deaktiviert ist.
   * **WS oder SCLK dürfen nicht verwendet werden, solange die Audiokomponenten aktiv sind.**

   .. image:: img/pinpal_i2s.png
       :width: 80%
       :align: center

   .. list-table::
      :header-rows: 1

      * - Signal
        - Raspberry Pi Pin
      * - WS
        - GPIO19
      * - SCLK
        - GPIO18
      * - Audio OUT (Speaker)
        - GPIO21
      * - Audio IN (MIC)
        - GPIO20


#. **ID_SD / ID_SC — HAT-EEPROM-Pins**

   Diese Pins sind für das Raspberry-Pi-HAT-EEPROM reserviert, in dem Identifikationsdaten der Erweiterungsplatine gespeichert werden.  
   Das Fusion HAT+ nutzt diese Pins für sein integriertes EEPROM, daher **dürfen ID_SD (GPIO0) und ID_SC (GPIO1) nicht für andere Zwecke verwendet werden**.

   .. image:: img/pinpal_eeprom.png
       :width: 80%
       :align: center
   

