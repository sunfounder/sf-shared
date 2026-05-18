.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _remote_desktop:

Desktop Remoto
================

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

Puoi accedere e controllare il desktop del Raspberry Pi da remoto tramite un altro computer.  
Il metodo consigliato è **VNC**, ufficialmente supportato da Raspberry Pi OS e in grado di fornire un’esperienza desktop affidabile e coerente.

La sezione seguente spiega come abilitare VNC sul tuo Raspberry Pi e come collegarti utilizzando |shared_link_realvnc|.

-----------------

Abilitare il servizio VNC
--------------------------------------

RealVNC Server è preinstallato su Raspberry Pi OS, ma è **disabilitato per impostazione predefinita**.  
Deve essere abilitato tramite lo strumento di configurazione.

#. Apri un terminale sul tuo computer (Windows: **PowerShell**; macOS/Linux: **Terminal**) e collegati al tuo Raspberry Pi:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   oppure

   .. code-block:: bash

      ssh <username>@<ip_address>

#. Avvia lo strumento di configurazione:

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. Seleziona **Interfacing Options** e premi **Invio**.

   .. image:: /_shared/appendix/img/ssh_interface.png


#. Seleziona **VNC**.

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. Scegli **Yes**, poi **OK** e infine **Finish** per uscire.

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



Accedere con RealVNC® Viewer
------------------------------

#. Scarica e installa |shared_link_realvnc| per il tuo sistema operativo.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Apri **RealVNC Viewer**, quindi inserisci l’indirizzo IP del tuo Raspberry Pi o ``<hostname>.local`` e premi **Invio**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Inserisci il **nome utente** e la **password** del tuo Raspberry Pi, quindi seleziona **OK**.

   .. note::

      Al primo collegamento potresti visualizzare un messaggio come “VNC Server not recognized”. Seleziona **Continue** per procedere.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Ora dovresti vedere il desktop del Raspberry Pi:

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Questo completa il processo di configurazione di VNC.

-----------------


Note aggiuntive
-----------------

* **È richiesta la versione Desktop**

  * VNC richiede che il Raspberry Pi esegua la versione completa di Raspberry Pi OS con interfaccia grafica.  
  * Se utilizzi **Raspberry Pi OS Lite**, installa manualmente VNC Server: ``sudo apt install realvnc-vnc-server``


* **Suggerimenti sulle prestazioni di rete**

  * Se riscontri ritardi o una bassa velocità di aggiornamento, verifica la qualità della rete.  
  * La connessione Ethernet cablata offre generalmente le migliori prestazioni.


* **Correzione dei problemi di risoluzione dello schermo**

  * Se la finestra VNC appare troppo piccola o la risoluzione non è corretta, imposta una risoluzione fissa tramite: ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Verificare che VNC sia abilitato**

  Se la connessione VNC non riesce, verifica che sia abilitata in: ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``


* **Arrestare il servizio VNC**

  Per arrestare manualmente il server VNC: ``sudo systemctl stop vncserver-x11-serviced``


* **Promemoria sulla sicurezza**

  * VNC è pensato per reti locali affidabili.  
  * Non esporre **direttamente** VNC su Internet.  
  * Per un accesso remoto sicuro dall’esterno della rete, utilizza **Raspberry Pi Connect** o una VPN.
