.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_sf006pro_servo:

SF006PRO Servo
===================

.. image:: img/servo_metal.png
    :width: 50%
    :align: center

Dieses Servo ist ein kleiner und zuverlässiger Aktuator, der mit einer Betriebsspannung von 4–6 V arbeitet und eine gleichmäßige Bewegung mit bis zu 180° Steuerbereich ermöglicht. Es bietet ein gutes Drehmoment, eine schnelle Reaktionszeit und einen geringen Stromverbrauch, wodurch es sich ideal für Robotik, mechanische Konstruktionen und allgemeine Hobbyprojekte eignet.  
Dank der standardisierten 3-Pin-PWM-Schnittstelle lässt es sich problemlos mit Mikrocontrollern wie Arduino oder Raspberry Pi verbinden.

**Funktionsweise eines Servos**


Ein typisches Servo besteht aus mehreren internen Komponenten:

* Gehäuse  
* Ausgangswelle  
* Getriebesystem  
* Potentiometer  
* DC-Motor  
* Steuerplatine (integrierte Elektronik)  

Der Mikrocontroller sendet PWM-Steuersignale über den Signalpin an das Servo.  
Die Steuerplatine interpretiert dieses Signal und treibt den DC-Motor an, der das Getriebesystem dreht. Durch die Untersetzung im Getriebe wird die Drehbewegung mit erhöhtem Drehmoment auf die Ausgangswelle übertragen.

Die Ausgangswelle ist mechanisch mit dem Potentiometer verbunden. Wenn sich die Welle dreht, verändert sich die vom Potentiometer ausgegebene Spannung. Die Steuerplatine liest dieses Feedback, um die aktuelle Position zu bestimmen, und passt die Motorbewegung an, bis die Zielposition erreicht und gehalten wird.

.. image:: img/servo_internal.png
    :align: center

**PWM-Steuerung**

Der Drehwinkel des Servos wird durch die Pulsbreite des PWM-Signals bestimmt. Das Servo erwartet normalerweise einen Steuerimpuls alle **20 ms**.

Typisches Pulsverhalten:

* **1.5 ms** → Neutralposition (ca. 90°)  
* **< 1.5 ms** → Bewegung gegen den Uhrzeigersinn von der Mittelposition  
* **> 1.5 ms** → Bewegung im Uhrzeigersinn von der Mittelposition  

Die meisten Hobby-Servos akzeptieren Pulsbreiten zwischen **0.5 ms und 2.5 ms**, was ihrem gesamten Bewegungsbereich entspricht.

.. image:: img/servo_duty.png
    :width: 600
    :align: center


**Parameter**

.. list-table::
   :header-rows: 1
   :widths: 25 75

   * - Parameter
     - Spezifikation

   * - Betriebsspannung
     - DC 4V–6V (Nennspannung 5V, empfohlen wird eine 5V-Versorgung)

   * - Ruhestrom
     - ≤ 5 mA

   * - Leerlaufstrom
     - ≤ 350 mA bei 5V (manuell gemessener Spitzenwert)

   * - Blockierstrom
     - ≤ 1.2 A bei 5V (sinkt nach 5 Sekunden Blockierung auf ≤250 mA)

   * - Nenn-Drehmoment
     - 0.75 kgf·cm (bei 5V)

   * - Maximale dynamische Last
     - ≥ 2.2 kgf·cm (bei 5V)

   * - Blockiermoment (statisch)
     - ≥ 5 kgf·cm (mit Drehmomentmessgerät getestet)

   * - Leerlaufgeschwindigkeit
     - ≤ 0.17 s/60° (bei 5V)

   * - Betriebs-Drehwinkel
     - 90° ±10° (1000–2000 μs)

   * - Maximaler Drehwinkel
     - 180° ±10° (500–2500 μs)

   * - Mechanischer Grenzwinkel
     - 360°

   * - Pulsbreitenbereich
     - 500 μs ~ 2500 μs

   * - Neutralposition
     - 1500 μs

   * - Totbandbreite
     - ≤ 6 μs

   * - Spiel (Backlash)
     - ≤ 0.5°

   * - Gewicht
     - 13.5 ± 0.5 g

   * - Getriebematerial
     - Kunststoff + Metall (Hybridgetriebe)

   * - Motortyp
     - Eisenkernmotor

   * - Potentiometertyp
     - Kohleschicht, Winkel 220°, ≥100.000 Zyklen

   * - Kabel
     - 250 ±5 mm, 3-Pin-JR-Stecker (Braun–Rot–Orange)

   * - Anschlussbelegung
     - Orange: PWM-Signal 

       Rot: VCC  

       Braun: GND

   * - Kommunikationsschnittstelle
     - PWM  

       Signalspannung: HIGH 2.0–5.0V / LOW 0.0–0.6V 

       Frame-Rate: 3–30 ms (Standard 20 ms)  

       Pulsbereich: 500–2500 μs

**Abmessungen**

.. image:: img/servo_metal_size.png
    :width: 80%
    :align: center