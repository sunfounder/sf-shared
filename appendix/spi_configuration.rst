.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!


.. _spi_configuration:

Configurazione SPI
==============================

Segui i passaggi seguenti per abilitare e verificare l’interfaccia SPI sul tuo Raspberry Pi.  
Queste istruzioni si applicano a Raspberry Pi 5, 4, 3 e Zero 2W.

Abilitare l’interfaccia SPI
--------------------------------------

#. Apri un terminale sul tuo computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) e collegati al tuo Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   oppure:

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Apri lo strumento di configurazione del Raspberry Pi:

   .. code-block:: bash

      sudo raspi-config

#. Seleziona **Interfacing Options** e premi **Invio**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Seleziona **SPI**.

   .. image:: img/ssh_spi_spi.png
      :align: center

#. Scegli **<Yes>**, quindi **<Ok> → <Finish>** per applicare le modifiche. Se richiesto, riavvia il Raspberry Pi.

   .. image:: img/ssh_spi_enable.png
      :align: center


Verificare l’interfaccia SPI
------------------------------

#. Verifica se esistono i nodi del dispositivo SPI:

   .. code-block:: bash

      ls /dev/sp*

#. Se l’interfaccia SPI è abilitata, l’output includerà:

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * Se questi dispositivi sono presenti, SPI è attivo e pronto all’uso.  
   * In caso contrario, riavvia il Raspberry Pi e controlla di nuovo.


Installare spidev (libreria SPI per Python)
---------------------------------------------

#. Installa il pacchetto ``spidev`` per utilizzare SPI in Python:

   .. code-block:: bash

      sudo apt install python3-spidev

   La libreria ``spidev`` fornisce l’accesso ai dispositivi SPI tramite l’interfaccia ``/dev/spidevX.Y``.

----------------------

Il tuo Raspberry Pi è ora configurato per comunicare con dispositivi SPI sia tramite strumenti da riga di comando sia tramite Python.
