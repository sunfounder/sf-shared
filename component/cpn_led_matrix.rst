.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_led_matrix:

LED-Punktmatrix
======================

.. image:: img/matrix_pic.png
    :width: 300

Die LED-Punktmatrix kann in zwei Typen unterteilt werden: **Common Cathode (CC)** und **Common Anode (CA)**.  
Äußerlich sehen sie ähnlich aus, jedoch unterscheidet sich ihre interne elektrische Struktur.

Die in diesem Kit verwendete LED-Punktmatrix ist vom Typ **Common Anode (CA)**.  
Sie können sie anhand der seitlich auf dem Modul aufgedruckten Kennzeichnung **„788BS“** identifizieren.

Pinbelegung
--------------------

Die Pins befinden sich auf beiden Seiten der Rückseite des Moduls.  
Wenn Sie auf die Seite mit der Beschriftung schauen:

* Die Pins **1–8** befinden sich auf einer Seite  
* Die Pins **9–16** befinden sich auf der gegenüberliegenden Seite  

Außenansicht:

.. image:: img/matrix_pin.png

Interne Struktur
-----------------------

Die folgende Abbildung zeigt die interne Struktur der LED-Punktmatrix.

* Bei einer **Common Anode (CA)**-Matrix gilt: **ROW = Anode** und **COL = Kathode**
* Bei einer **Common Cathode (CC)**-Matrix gilt: **ROW = Kathode** und **COL = Anode**

.. image:: img/matrix_internal.png
   :width: 400
   :align: center

Bei beiden Typen, CA und CC, sind die physischen Pinpositionen für Reihen und Spalten identisch — nur die elektrische Polarität ist unterschiedlich.

Pin-Zuordnung
-----------------------

.. list-table::
   :header-rows: 2
   :align: center

   * - **COL**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Pin-Nr.**
     - **13**
     - **3**
     - **4**
     - **10**
     - **6**
     - **11**
     - **15**
     - **16**
   * - **ROW**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Pin-Nr.**
     - **9**
     - **14**
     - **8**
     - **12**
     - **1**
     - **7**
     - **2**
     - **5**

Wie LEDs eingeschaltet werden
------------------------------------

Um eine einzelne LED zu steuern, müssen die zugehörigen **ROW**- und **COL**-Pins korrekt aktiviert werden.

*Beispiel: LED oben links (ROW 1, COL 1)*

- **CA-Typ**  
  Setze **ROW-Pin 9 = High**, **COL-Pin 13 = Low**

- **CC-Typ**  
  Setze **COL-Pin 13 = High**, **ROW-Pin 9 = Low**

*Beispiel: die gesamte erste Spalte einschalten*

- **CA-Typ**  
  Setze **COL-Pin 13 = Low**  
  Setze **ROW-Pins 9, 14, 8, 12, 1, 7, 2, 5 = High**

- **CC-Typ**  
  Setze **COL-Pin 13 = High**  
  Setze **ROW-Pins 9, 14, 8, 12, 1, 7, 2, 5 = Low**

Diese Zeilen-Spalten-Scanmethode ermöglicht es, jede LED einzeln mittels Multiplexing zu steuern.
