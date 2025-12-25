.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _i2c_config:

Configurazione I²C
======================

Segui i passaggi seguenti per abilitare e testare l’interfaccia I²C sul tuo Raspberry Pi.  
Queste istruzioni si applicano a Raspberry Pi 5, 4, 3 e Zero 2W.

Abilitare l’interfaccia I²C
--------------------------------

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

#. Seleziona **I2C**.

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. Scegli **<Yes>**, quindi **<Ok> → <Finish>** per applicare le modifiche.  
   Se richiesto, riavvia il Raspberry Pi.

   .. image:: img/ssh_i2c_yes.png
      :align: center


Verificare i moduli kernel I²C
------------------------------------

#. Esegui il seguente comando:

   .. code-block:: bash

      lsmod | grep i2c

#. Se I²C è abilitato, vedrai moduli come:

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. Se non appare nulla, riavvia il sistema:

   .. code-block:: bash

      sudo reboot


Installare i2c-tools
------------------------

#. Installa le utilità necessarie per la scansione e il test dei dispositivi I²C:

   .. code-block:: bash

      sudo apt install i2c-tools


Rilevare i dispositivi I²C collegati
-----------------------------------------

#. Esegui la scansione del bus I²C:

   .. code-block:: bash

      i2cdetect -y 1

#. Esempio di output:

   .. code-block:: text

      pi@raspberrypi ~ $ i2cdetect -y 1
          0  1  2  3   4  5  6  7  8  9   a  b  c  d  e  f
      00:           -- -- -- -- -- -- -- -- -- -- -- -- --
      10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
      50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      70: -- -- -- -- -- -- -- --

#. Se un dispositivo è collegato, il suo indirizzo (ad esempio **0x48**) apparirà nella tabella.


Installare la libreria I²C per Python
-----------------------------------------

#. Installa il pacchetto ``python3-smbus2``:

   .. code-block:: bash

      sudo apt install python3-smbus2

   La libreria ``smbus2`` fornisce tutte le funzioni necessarie per comunicare con dispositivi I²C in Python.

Il tuo Raspberry Pi è ora completamente configurato e pronto per comunicare con dispositivi I²C.
