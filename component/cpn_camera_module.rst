.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _cpn_camera_module:

Kameramodul
====================================

**Beschreibung**

.. image:: /_shared/component/img/camera_module_pic.png
   :width: 200
   :align: center

Dies ist ein 5MP Raspberry Pi Kameramodul mit OV5647 Sensor. Es ist Plug-and-Play; schließen Sie das beiliegende Flachbandkabel an den CSI (Camera Serial Interface) Anschluss Ihres Raspberry Pi an, und Sie können loslegen.

Die Platine ist klein, etwa 25mm x 23mm x 9mm, und wiegt 3g. Das macht sie ideal für mobile Anwendungen oder andere Anwendungen, bei denen Größe und Gewicht kritisch sind. Das Kameramodul hat eine native Auflösung von 5 Megapixeln und verfügt über eine fest eingestellte Linse, die Standbilder mit 2592 x 1944 Pixel aufnimmt. Es unterstützt auch 1080p30, 720p60 und 640x480p90 Video.

.. note:: 

   Das Modul kann nur Bilder und Videos aufnehmen, keinen Ton.

**Spezifikation**

* **Auflösung statischer Bilder**: 2592×1944 
* **Unterstützte Videoauflösung**: 1080p/30 fps, 720p/60fps und 640x480p 60/90 Videoaufnahme 
* **Blende (F)**: 1.8 
* **Betrachtungswinkel**: 65 Grad 
* **Maße**: 24mmx23.5mmx8mm 
* **Gewicht**: 3g 
* **Schnittstelle**: CSI Anschluss 
* **Unterstütztes Betriebssystem**: Raspberry Pi OS(neueste Version empfohlen) 

Montage des Kameramoduls
---------------------------------------


Am Kameramodul oder Raspberry Pi finden Sie einen flachen Kunststoffanschluss. Ziehen Sie vorsichtig den schwarzen Befestigungsschalter heraus, bis er teilweise herausgezogen ist. Führen Sie das FFC-Kabel in die gezeigte Richtung in den Kunststoffanschluss ein und schieben Sie den Befestigungsschalter wieder zurück.

Wenn das FFC-Kabel korrekt installiert ist, wird es gerade sein und sich nicht herausziehen lassen, wenn Sie leicht daran ziehen. Wenn nicht, installieren Sie es erneut.

.. image:: /_shared/component/img/connect_ffc.png
.. image:: /_shared/component/img/1.10_camera.png
   :width: 700

.. warning::

   Schließen Sie die Kamera nicht an, wenn die Stromversorgung eingeschaltet ist. Dies kann Ihre Kamera beschädigen.

   
.. **Beispiel**

.. * :ref:`3.1.1_py` (Python-Projekt)
.. * :ref:`3.1.2_py` (Python-Projekt)
.. * :ref:`4.1.1_py` (Python-Projekt)
.. * :ref:`4.1.4_py` (Python-Projekt)
.. * :ref:`4.1.5_py` (Python-Projekt)
.. * :ref:`1.10_scratch` (Scratch-Projekt)
.. * :ref:`1.18_scratch` (Scratch-Projekt)
