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
==================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

Das File Transfer Protocol (FTP) wird häufig verwendet, um Dateien über ein Netzwerk zwischen Computern zu übertragen.  
**FileZilla** ist ein Open-Source-Client, der FTP, FTPS und **SFTP** (für Raspberry Pi empfohlen) unterstützt.  
Mit FileZilla können Sie ganz einfach Dateien (z. B. Bilder, Audio oder Skripte) von Ihrem Computer auf den Raspberry Pi hochladen oder Dateien vom Pi auf Ihren Computer herunterladen.

Download FileZilla
------------------

#. Besuchen Sie die offizielle Website |shared_link_filezilla| und laden Sie den **FileZilla Client** für Ihr Betriebssystem herunter.

#. Installieren und starten Sie das Programm.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Öffnen Sie FileZilla und geben Sie folgende Informationen ein:

   * **Host:** ``<hostname>.local`` oder die IP-Adresse des Raspberry Pi  
   * **Benutzername:** Ihr Pi-Benutzername  
   * **Passwort:** das in Raspberry Pi Imager gesetzte Passwort  
   * **Port:** ``22`` (für SFTP)  
   * Klicken Sie auf **Quickconnect** (oder drücken Sie **Enter**), um die Verbindung herzustellen.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Nach dem Verbinden zeigt das linke Panel Ihre **lokalen Dateien**, und das rechte Panel die **Dateien auf dem Raspberry Pi**.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. Sie können:

   * **Eine Datei hochladen:** per Drag & Drop vom linken Panel → rechtes Panel  
   * **Eine Datei herunterladen:** per Drag & Drop vom rechten Panel → linkes Panel  

   FileZilla startet den Transfer sofort, und der Status erscheint im unteren Bereich des Fensters.
