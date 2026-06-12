.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_buzzer:

Summer
=========

.. image:: img/buzzer.png
    :width: 600

Als eine Art elektronischer Summer mit integrierter Struktur, die mit Gleichstrom versorgt werden, sind Summer weit verbreitet in Computern, Druckern, Kopierern, Alarmen, elektronischem Spielzeug, Automobil-Elektronik, Telefonen, Zeitgebern und anderen elektronischen Produkten oder Sprachgeräten.

Summer können in aktive und passive unterteilt werden (siehe folgendes Bild). Drehen Sie den Summer so, dass seine Pins nach oben zeigen, und der Summer mit einer grünen Platine ist ein passiver Summer, während der mit schwarzem Klebeband umwickelte ein aktiver Summer ist.

Der Unterschied zwischen einem aktiven und einem passiven Summer:

Ein aktiver Summer hat eine eingebaute Oszillationsquelle, daher gibt er beim Elektrifizieren Töne von sich. Ein passiver Summer hat jedoch keine solche Quelle, daher gibt er keinen Ton von sich, wenn er mit Gleichstromsignalen versorgt wird; stattdessen müssen Sie ihn mit Rechteckwellen antreiben, deren Frequenz zwischen 2K und 5K liegt. Wegen der vielen eingebauten Oszillationsschaltungen ist der aktive Summer oft teurer als der passive.

Im Folgenden ist das elektrische Symbol eines Summers dargestellt. Er hat zwei Pins, positiv und negativ. Ein + auf der Oberfläche repräsentiert die Anode, der andere die Kathode.

.. image:: img/buzzer_symbol.png
    :width: 150

Sie können die Pins des Summers überprüfen; der längere ist die Anode und der kürzere die Kathode. Bitte verwechseln Sie sie beim Anschließen nicht, sonst gibt der Summer keinen Ton von sich.

`Summer - Wikipedia <https://en.wikipedia.org/wiki/Buzzer>`_

.. **Beispiel**

.. * :ref:`1.2.1_c` (C-Projekt)
.. * :ref:`1.2.2_c` (C-Projekt)
.. * :ref:`1.2.1_py` (Python-Projekt)
.. * :ref:`1.2.2_py` (Python-Projekt)
.. * :ref:`1.13_scratch` (Scratch-Projekt)
.. * :ref:`1.14_scratch` (Scratch-Projekt)
