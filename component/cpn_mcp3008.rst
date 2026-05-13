.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_mcp3008:

MCP3008
==============

Der MCP3008 ist ein 10-Bit-Analog-Digital-Wandler (ADC) mit sukzessiver Approximation, 8 Eingangskanälen und einem SPI-Kommunikationsprotokoll (Serial Peripheral Interface).  
Er kann mit einem Mikrocontroller verbunden werden, um analoge Eingangssignale in digitale Daten für die weitere Verarbeitung umzuwandeln.

.. image:: img/MCP3008.jpg
      :width: 40%

**Ablauf des Betriebs**

Eine Konvertierung auf dem MCP3008 beginnt, indem der CS-Pin (Chip Select) auf LOW gesetzt wird, wodurch die Kommunikation mit dem Gerät aktiviert wird.  
Der Mikrocontroller sendet dann einen 3-Byte-Steuerstrom über die SPI-Schnittstelle, um die Konfiguration festzulegen und den Eingangskanal auszuwählen.

Das erste Byte enthält das Startbit und das Bit zur Auswahl von Einzel-/Differenzeingang. Die nächsten Bits geben an, welcher der 8 Kanäle (CH0–CH7) ausgelesen werden soll.  
Daten werden mit jeder steigenden Flanke des SPI-Takts (SCLK) in das Gerät verschoben, und das Konvertierungsergebnis wird gleichzeitig zurückgesendet.

Eine kurze interne Verzögerung ist enthalten, damit sich der ausgewählte Eingangskanal vor Beginn der Konvertierung stabilisieren kann.  
Der MCP3008 führt dann eine 10-Bit-Analog-Digital-Umwandlung unter Verwendung einer Sample-and-Hold-Schaltung und eines sukzessiven Approximation-Registers (SAR) durch.

Das Konvertierungsergebnis wird über die MISO-Leitung (Master In Slave Out) an den Mikrocontroller zurückübertragen.  
Das höchstwertige Bit (MSB) des 10-Bit-Ergebnisses wird zuerst gesendet, gefolgt von den restlichen Bits.  
Der Mikrocontroller liest das Ergebnis während dieser Zeit über den SPI-Bus.

Nach dem vollständigen Übertragen des 10-Bit-Digitalwertes schließt der MCP3008 den Zyklus ab und wartet auf den nächsten Befehl.

* `MCP3008-Serie Datenblatt <https://www.alldatasheet.com/datasheet-pdf/view/304558/MICROCHIP/MCP3008-ISLASHP.html>`_

.. image:: img/MCP3008detail.png

.. **Beispiele**

.. * :ref:`2.1.7_c_mcp3008` (C-Projekt)
.. * :ref:`2.2.1_c_mcp3008` (C-Projekt)
.. * :ref:`2.2.2_c_mcp3008` (C-Projekt)
.. * :ref:`3.1.4_c_mcp3008` (C-Projekt)
.. * :ref:`3.1.5_c_mcp3008` (C-Projekt)
.. * :ref:`3.1.7_c_mcp3008` (C-Projekt)
.. * :ref:`2.1.7_py_mcp3008` (Python-Projekt)
.. * :ref:`2.2.1_py_mcp3008` (Python-Projekt)
.. * :ref:`2.2.2_py_mcp3008` (Python-Projekt)
.. * :ref:`4.1.10_py_mcp3008` (Python-Projekt)
.. * :ref:`4.1.11_py_mcp3008` (Python-Projekt)
.. * :ref:`4.1.13_py_mcp3008` (Python-Projekt)
