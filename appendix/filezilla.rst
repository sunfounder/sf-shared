.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _filezilla:

Software FileZilla
==================

.. image:: /_shared/appendix/img/filezilla_icon.png
   :width: 20%

Il File Transfer Protocol (FTP) è comunemente utilizzato per trasferire file tra computer tramite una rete.  
**FileZilla** è un client open-source che supporta FTP, FTPS e **SFTP** (consigliato per Raspberry Pi).  
Con FileZilla puoi caricare facilmente file (come immagini, audio e script) dal tuo computer al Raspberry Pi, oppure scaricare file dal Pi al tuo computer.

Scaricare FileZilla
-------------------

.. |shared_link_filezilla| raw:: html

    <a href="https://filezilla-project.org/" target="_blank">FileZilla</a> 

#. Visita il sito ufficiale |shared_link_filezilla| e scarica **FileZilla Client** per il tuo sistema operativo.

#. Installa e avvia il programma.

   .. image:: /_shared/appendix/img/filezilla_install.png

#. Apri FileZilla e inserisci le seguenti informazioni:

   * **Host:** ``<hostname>.local`` oppure l’indirizzo IP del Raspberry Pi  
   * **Username:** il nome utente del tuo Pi  
   * **Password:** la password impostata in Raspberry Pi Imager  
   * **Port:** ``22`` (per SFTP)
   * Clicca su **Quickconnect** (oppure premi **Invio**) per stabilire la connessione.

   .. image:: /_shared/appendix/img/filezilla_connect.png
      :align: center

#. Una volta connesso, il pannello di sinistra mostra i **file locali**, mentre il pannello di destra mostra i **file del Raspberry Pi**.

    .. image:: /_shared/appendix/img/filezilla_in.png
       :align: center

#. Puoi:

   * **Caricare** un file: trascina dal pannello di sinistra → pannello di destra  
   * **Scaricare** un file: trascina dal pannello di destra → pannello di sinistra  

   FileZilla avvierà immediatamente il trasferimento e lo stato verrà mostrato nel pannello inferiore.
