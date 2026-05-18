.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _filezilla:

FileZilla Software
============================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

Das File Transfer Protocol (FTP) wird häufig verwendet, um Dateien über ein Netzwerk zwischen Computern zu übertragen.  
**FileZilla** ist ein Open-Source-Client, der FTP, FTPS und **SFTP** unterstützt (für Raspberry Pi empfohlen).  
Mit FileZilla können Sie Dateien (z. B. Bilder, Audio-Dateien und Skripte) einfach von Ihrem Computer auf den Raspberry Pi hochladen oder Dateien vom Pi zurück auf Ihren Computer herunterladen.

FileZilla herunterladen
-------------------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. Besuchen Sie die offizielle Website |shared_link_filezilla| und laden Sie den **FileZilla Client** für Ihr Betriebssystem herunter.

#. Installieren und starten Sie das Programm.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Öffnen Sie FileZilla und geben Sie die folgenden Informationen ein:

   * **Host:** ``<hostname>.local`` oder die IP-Adresse des Raspberry Pi  
   * **Benutzername:** Ihr Pi-Benutzername  
   * **Passwort:** Das in Raspberry Pi Imager festgelegte Passwort  
   * **Port:** ``22`` (für SFTP)
   * Klicken Sie auf **Quickconnect** (oder drücken Sie **Enter**), um die Verbindung herzustellen.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Nach der Verbindung zeigt das linke Fenster Ihre **lokalen Dateien**, und das rechte Fenster die **Dateien des Raspberry Pi** an.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. Sie können:

   * Eine Datei **hochladen**: Ziehen Sie sie vom linken Fenster → ins rechte Fenster  
   * Eine Datei **herunterladen**: Ziehen Sie sie vom rechten Fenster → ins linke Fenster  

   FileZilla startet die Übertragung sofort, und der Status wird im unteren Bereich des Fensters angezeigt.
