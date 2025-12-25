.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!


.. _install_all_modules_fusion_hat:

Configurare l’alimentazione e installare il software (Importante)
=================================================================

In questo capitolo installerai il software necessario, configurerai l’audio, imposterai una gestione sicura dell’alimentazione e imparerai come gestire correttamente lo spegnimento.

.. start_install_fusion_hat

.. _install_fusion_hat:

Installare il modulo ``fusion-hat``
-----------------------------------

Per questo kit, tutte le funzionalità GPIO sono gestite tramite la Fusion HAT+.  
Pertanto, è necessario utilizzare la libreria ``fusion-hat`` dedicata per accedervi e controllarle.

Esegui il seguente comando nel terminale per installare il modulo ``fusion-hat``.

   .. raw:: html

      <run></run>

   .. code-block::

      curl -sSL https://raw.githubusercontent.com/sunfounder/sunfounder-installer-scripts/main/install-fusion-hat.sh | sudo bash

.. |shared_link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">Fusion HAT+</a>

.. note:: Per i dettagli su fusion-hat, fai riferimento alla documentazione |shared_link_fusion_hat|.


Al termine dell’installazione, riavvia il Raspberry Pi. Quindi esegui lo script di configurazione audio:

   .. raw:: html

      <run></run>

   .. code-block::

      sudo /opt/setup_fusion_hat_audio.sh

Questo completa il processo di installazione del software per la Fusion HAT+.

Configurare e utilizzare lo spegnimento sicuro
----------------------------------------------

La Fusion HAT+ si basa sul segnale di spegnimento del Raspberry Pi per gestire completamente l’alimentazione del sistema.  
Per garantire uno spegnimento sicuro e affidabile, è necessario **configurare il comportamento di spegnimento** in base al modello di Raspberry Pi e poi utilizzare correttamente il **pulsante di alimentazione**.

**Per Raspberry Pi 5 e 4B**

Questi modelli supportano lo spegnimento completo dopo l’arresto del sistema.  
La Fusion HAT+ monitora la linea a 3,3 V per rilevare lo stato di alimentazione del Raspberry Pi.

1. Posiziona il jumper su **RPI_STATE → Pi3V3**.

   .. image:: /_shared/pi_start/img/state_3v3.jpg
      :width: 400

2. Modifica manualmente la configurazione EEPROM:

   .. code-block::

      sudo raspi-config

3. Vai a **Advanced Options → A12 Shutdown Behaviour**.

   .. image:: /_shared/pi_start/img/shutdown_behaviour.png

4. Seleziona **B1 Full Power Off**.

   .. image:: /_shared/pi_start/img/run_power_off.png

5. Salva le modifiche. Ti verrà richiesto di riavviare affinché le nuove impostazioni abbiano effetto.

**Per Raspberry Pi Zero 2W, 3B, 3B+**

Questi modelli **non** supportano lo spegnimento completo tramite la linea a 3,3 V.  
In alternativa, è necessario configurare GPIO26 come indicatore dello stato di spegnimento.

1. Posiziona il jumper su **RPI_STATE → IO26**.

   .. image:: /_shared/pi_start/img/state_io26.jpg
      :width: 400

2. Modifica il file ``/boot/firmware/config.txt``:

   .. code-block::

      sudo nano /boot/firmware/config.txt

3. Aggiungi la seguente riga alla fine del file per impostare GPIO26 a livello basso durante lo spegnimento e alto all’accensione:

   .. code-block::

      dtoverlay=gpio-poweroff,gpio_pin=26,active_low=1

4. Riavvia per applicare le modifiche:

   .. code-block::

      sudo reboot

**Utilizzo del pulsante di alimentazione per uno spegnimento sicuro**

Dopo aver completato la configurazione dello spegnimento, puoi spegnere in sicurezza il PiCar-X utilizzando il pulsante di alimentazione della Fusion HAT+.

* **Spegnimento soft (consigliato)**

  * Tieni premuto il pulsante di alimentazione per **2 secondi**.  
  * I due LED di alimentazione lampeggeranno rapidamente.  
  * Rilascia il pulsante → la Fusion HAT+ avvia lo spegnimento del Raspberry Pi.  
  * Una volta completato lo spegnimento, la Fusion HAT+ interromperà automaticamente l’alimentazione.  
  * Questo protegge la scheda SD e i file di sistema.

* **Spegnimento forzato (solo emergenze)**

  * Se il sistema non risponde, tieni premuto il pulsante di alimentazione per **oltre 5 secondi**.  
  * La Fusion HAT+ forzerà l’interruzione dell’alimentazione.  
  * Avvertenza: questa operazione può corrompere la scheda SD o i file di sistema. Usala solo se strettamente necessario.

.. end_install_fusion_hat
