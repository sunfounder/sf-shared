.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _install_os:

Installazione del Sistema Operativo
===================================

.. start_imager

Prima di utilizzare il tuo Raspberry Pi, devi installare **Raspberry Pi OS** su una scheda microSD.  
Questa guida spiega come farlo utilizzando **Raspberry Pi Imager** in modo semplice e adatto ai principianti.

**Componenti necessari**

* Un computer (Windows, macOS o Linux)
* Una scheda microSD (16 GB o superiore; marche consigliate: SanDisk, Samsung)
* Un lettore di schede microSD

-------------------

**1. Installare Raspberry Pi Imager**
------------------------------------

.. |shared_link_rpi_imager| raw:: html

    <a href="https://www.raspberrypi.com/software/" target="_blank">Raspberry Pi Imager</a>   

#. Visita la pagina ufficiale per il download di Raspberry Pi Imager: |shared_link_rpi_imager|. Scarica il programma di installazione corretto per il tuo sistema operativo.

   .. image:: /_shared/pi_start/img/imager_download.png
      :width: 70%

#. Segui le istruzioni di installazione (lingua, percorso di installazione, conferma). Al termine dell’installazione, avvia **Raspberry Pi Imager** dal desktop o dal menu delle applicazioni.

   .. image:: /_shared/pi_start/img/imager_install.png
      :width: 90%

-------------------

**2. Installare il sistema operativo sulla scheda microSD**
-----------------------------------------------------------

1. Inserisci la scheda microSD nel computer utilizzando un lettore di schede. Esegui un backup di eventuali dati importanti prima di procedere.

   .. image:: /_shared/pi_start/img/insert_sd.png
      :width: 90%

2. Quando si apre Raspberry Pi Imager, vedrai la schermata **Device**. Seleziona il modello del tuo Raspberry Pi dall’elenco (ad esempio Raspberry Pi 5, 4, 3 o Zero 2W).

   .. image:: /_shared/pi_start/img/imager_device.png
      :width: 90%

   .. end_imager

3. Vai alla sezione **OS** e scegli l’opzione consigliata **Raspberry Pi OS (64-bit)**.

   .. image:: /_shared/pi_start/img/imager_os.png
      :width: 90%

   .. start_choose_os

4. Nella sezione **Storage**, seleziona la tua scheda microSD. Per sicurezza, scollega le altre unità USB in modo che nell’elenco compaia solo la scheda SD.

   .. image:: /_shared/pi_start/img/imager_storage.png
      :width: 90%

5. Clicca su **Next** per passare alla fase di personalizzazione.

   .. note::

      * Se collegherai direttamente monitor, tastiera e mouse al Raspberry Pi, puoi cliccare su **SKIP CUSTOMISATION**.  
      * Se prevedi di configurare il Raspberry Pi in modalità *headless* (accesso remoto tramite Wi-Fi), devi completare le impostazioni di personalizzazione.

   .. image:: /_shared/pi_start/img/imager_custom_skip.png
      :width: 90%

-------------------

.. _imager_custom:

**3. Impostazioni di personalizzazione del sistema operativo**
--------------------------------------------------------------

#. **Impostare l’hostname**

   * Assegna un hostname univoco al tuo Raspberry Pi.  
   * Potrai collegarti in seguito utilizzando ``hostname.local``.

   .. image:: /_shared/pi_start/img/imager_custom_hostname.png
      :width: 90%

#. **Impostare la localizzazione**

   * Scegli la tua città principale.
   * Imager completerà automaticamente il fuso orario e il layout della tastiera in base alla selezione, ma potrai modificarli se necessario. Seleziona **Next**.
   
   .. image:: /_shared/pi_start/img/imager_custom_local.png
      :width: 90%

#. **Impostare nome utente e password**

   Crea un account utente per il tuo Raspberry Pi.
   
   .. image:: /_shared/pi_start/img/imager_custom_user.png
      :width: 90%

#. **Configurare il Wi-Fi**

   * Inserisci l’**SSID** (nome della rete) e la **password** del Wi-Fi.  
   * Il Raspberry Pi si connetterà automaticamente al primo avvio.
   
   .. image:: /_shared/pi_start/img/imager_custom_wifi.png
      :width: 90%

#. **Abilitare SSH (opzionale ma consigliato)**

   * Abilitando SSH potrai accedere da remoto al Raspberry Pi dal tuo computer.  
   * Puoi accedere utilizzando nome utente/password oppure configurare chiavi SSH.
   
   .. image:: /_shared/pi_start/img/imager_custom_ssh.png
      :width: 90%

#. **Abilitare Raspberry Pi Connect (opzionale)**

   Raspberry Pi Connect consente di accedere al desktop del Raspberry Pi tramite un browser web.
   
   * Attiva **Raspberry Pi Connect**, quindi clicca su **OPEN RASPBERRY PI CONNECT**.
   
     .. image:: /_shared/pi_start/img/imager_custom_connect.png
        :width: 90%

   * Il sito web di Raspberry Pi Connect si aprirà nel browser predefinito. Accedi con il tuo account Raspberry Pi ID oppure registrati se non ne hai ancora uno.

     .. image:: /_shared/pi_start/img/imager_custom_open.png
        :width: 90%

   * Nella pagina **New auth key**, crea la tua chiave di autenticazione monouso. 
      
      * Se il tuo account Raspberry Pi ID non fa parte di alcuna organizzazione, seleziona **Create auth key and launch Raspberry Pi Imager**.
      * Se fai parte di una o più organizzazioni, scegline una, quindi crea la chiave e avvia Imager.
      * Assicurati di accendere il Raspberry Pi e collegarlo a Internet prima che la chiave scada.
   
     .. image:: /_shared/pi_start/img/imager_custom_authkey.png
        :width: 90%
   
   * Il browser potrebbe chiederti di aprire Raspberry Pi Imager: consenti l’operazione.

     * Imager si aprirà nella scheda Raspberry Pi Connect mostrando il token di autenticazione.
     * Se il token non viene trasferito automaticamente, apri la sezione **Having trouble?** nella pagina Raspberry Pi Connect, copia il token e incollalo manualmente in Imager.

     .. image:: /_shared/pi_start/img/imager_custom_connect_token.png
        :width: 90%

-------------------

**4. Scrivere l’immagine del sistema operativo**

#. Ricontrolla tutte le impostazioni e clicca su **WRITE**.

   .. image:: /_shared/pi_start/img/imager_writing.png
      :width: 90%

#. Se la scheda contiene già dei dati, Raspberry Pi Imager mostrerà un avviso che indica che tutti i dati verranno cancellati. Verifica di aver selezionato l’unità corretta, quindi clicca su **I UNDERSTAND, ERASE AND WRITE** per continuare.

   .. image:: /_shared/pi_start/img/imager_erase.png
      :width: 90%

#. Attendi il completamento della scrittura e della verifica. Al termine, Raspberry Pi Imager mostrerà **Write complete!** e un riepilogo delle scelte effettuate. Il dispositivo di archiviazione verrà espulso automaticamente, così potrai rimuoverlo in sicurezza.

   .. image:: /_shared/pi_start/img/imager_finish.png
        :width: 90%

#. Rimuovi la scheda microSD e inseriscila nello slot sul lato inferiore del Raspberry Pi. Il tuo Raspberry Pi è ora pronto per avviarsi con il nuovo sistema operativo!

   .. image:: /_shared/pi_start/img/os_sd_to_pi.jpg
        :width: 70%

   .. end_choose_os
