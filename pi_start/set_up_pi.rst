.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. start_setup_pi

Configurare il tuo Raspberry Pi
=================================

Per iniziare a programmare e controllare il tuo Raspberry Pi, devi prima accedervi.  
Questa guida descrive due metodi comuni:

* Utilizzare un monitor, una tastiera e un mouse  
* Impostare una connessione *headless* (senza schermo) per l’accesso remoto  

.. note::

   Il Raspberry Pi Zero 2W installato sul robot non è facile da collegare a uno schermo.  
   Consigliamo di utilizzare il metodo di configurazione **headless**.

.. end_setup_pi

.. start_setup_pi_screen

-------------------------
Se hai uno schermo
-------------------------

**Componenti necessari**

* Raspberry Pi
* Alimentatore ufficiale
* Scheda MicroSD
* Cavo HDMI  
  (Per Raspberry Pi 4/5, utilizza **HDMI0**, la porta più vicina al connettore di alimentazione.)
* Monitor
* Tastiera e mouse

**Passaggi**

#. Inserisci la scheda microSD nel Raspberry Pi.
#. Collega tastiera, mouse e monitor.
#. Accendi il Raspberry Pi.
#. Dopo l’avvio, apparirà il desktop di Raspberry Pi OS. 

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. Apri un **Terminale** per inserire i comandi.

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center

.. end_setup_pi_screen

.. start_setup_pi_headless

------------------------------------
Se non hai uno schermo (Headless)
------------------------------------

Senza un monitor, puoi configurare e accedere al tuo Raspberry Pi da remoto.  
Questo è il metodo più comodo per la maggior parte degli utenti.

**Componenti necessari**

* Raspberry Pi
* Alimentatore ufficiale
* Scheda MicroSD
* Un computer sulla stessa rete

**Suggerimenti**

* Assicurati di aver completato tutte le impostazioni descritte in :ref:`imager_custom` durante l’installazione del sistema con Raspberry Pi Imager.
* Verifica che il Raspberry Pi e il tuo computer siano sulla stessa rete locale.
* Per una maggiore stabilità, utilizza Ethernet se disponibile.


**Connessione tramite SSH**

#. Apri un terminale sul tuo computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) e collegati al tuo Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local
      # Esempio:
      ssh daisy@pi.local

2. In alternativa, individua l’indirizzo IP del Pi dall’elenco DHCP del tuo router e collegati con:

   .. code-block:: bash

      ssh <username>@<IP address>
      # Esempio:
      ssh daisy@192.168.1.42

3. Al primo accesso, digita ``yes`` per confermare il certificato SSH.

4. Inserisci la password che hai configurato in Raspberry Pi Imager.  
   (Durante la digitazione non verrà visualizzato nulla — è normale.)

5. Dopo l’accesso, avrai pieno accesso alla riga di comando.

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

.. end_setup_pi_headless


.. start_setup_pi_troubleshooting


----------------------

**Risoluzione dei problemi**

* **ssh: Could not resolve hostname ...**

  * Assicurati che l’hostname sia corretto.
  * Prova a collegarti utilizzando l’indirizzo IP del Pi.

* **The term 'ssh' is not recognized... (Windows)**

  * OpenSSH non è installato. Installalo manualmente o utilizza un client SSH di terze parti.  
  * Vedi :ref:`openssh_powershell` o :ref:`login_windows`.

* **Permission denied (publickey,password)**

  * Verifica di utilizzare il nome utente e la password creati in Raspberry Pi Imager.

* **Connection refused**

  * Attendi 1–2 minuti dopo l’accensione.
  * Conferma che SSH sia stato abilitato in Raspberry Pi Imager.

.. end_setup_pi_troubleshooting


.. start_setup_pi_remote_desktop

--------------------------------

Opzioni di accesso remoto grafico
-----------------------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

Se preferisci un’interfaccia grafica:

* :ref:`remote_desktop`: abilita **VNC (Virtual Network Computing)** per un’esperienza desktop completa sul tuo Pi.

* |shared_link_rpi_connect|: utilizza Raspberry Pi Connect per un accesso remoto sicuro da qualsiasi luogo, direttamente tramite browser. 

Ora puoi controllare il tuo Raspberry Pi senza monitor, tramite SSH per le operazioni da riga di comando, oppure con VNC / Raspberry Pi Connect per un’esperienza desktop grafica.

.. end_setup_pi_remote_desktop
