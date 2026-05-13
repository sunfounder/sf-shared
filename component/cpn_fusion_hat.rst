.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _cpn_fusion_hat:

Fusion HAT+
=====================================

.. image:: img/fusionhat_v0.png
    :width: 500
    :align: center


La Fusion HAT+ è una scheda di espansione potente e versatile progettata per trasformare facilmente un Raspberry Pi in un robot completamente funzionale con una configurazione minima, e può anche supportare progetti di automazione avanzata.

Al centro della Fusion HAT+ c'è un microcontrollore (MCU) integrato, che estende significativamente la funzionalità nativa del Raspberry Pi fornendo uscite PWM aggiuntive e ingressi ADC, capacità tipicamente assenti sui modelli Raspberry Pi standard. Questo permette agli sviluppatori di ottenere un controllo più preciso dei motori e una migliore integrazione dei sensori.

Compatta ma ricca di funzionalità, la Fusion HAT+ integra quattro chip driver per motori, supportando il controllo indipendente di fino a quattro motori DC. Dispone anche di un modulo audio digitale I2S e un altoparlante mono integrato, consentendo una riproduzione audio di alta qualità e funzioni sonore interattive direttamente dalla scheda.

La scheda accetta un ingresso di alimentazione da 6,0 V a 8,4 V tramite un connettore XH2.54 a 3 pin. Include due LED indicatori di alimentazione per monitorare lo stato del sistema, un LED programmabile dall'utente per segnalazioni personalizzate e un pratico pulsante integrato per test funzionali immediati o simulazione di input, rendendo lo sviluppo e il debug più efficienti e intuitivi.

.. |link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">SunFounder Fusion HAT+</a>

Per istruzioni dettagliate, consulta: |link_fusion_hat|.

PinPal
============================

.. image:: img/pinpal_pic.png
    :width: 20%
    :align: center

PinPal è una piccola scheda PCB progettata da SunFounder con le etichette dei pin del Raspberry Pi.
Puoi posizionarla direttamente sull'header dei pin della Fusion HAT+, facilitando l'identificazione della funzione di ciascun pin in modo chiaro e rapido durante la costruzione del progetto.
Questo aiuta a ridurre gli errori e ad accelerare il cablaggio.

.. image:: img/pinpal_fusion_hat.png
    :width: 80%
    :align: center

Alcuni pin su PinPal sono **sconsigliati per l'uso diretto** perché già utilizzati dalla Fusion HAT+ o perché condividono funzioni che potrebbero causare conflitti.


#. **SDA / SCL — I2C (GPIO2 / GPIO3)**

   * Pin I2C principali del Raspberry Pi.
   * La Fusion HAT+ fornisce anche un header I2C P2.54 e una porta SH1.0 Qwiic/STEMMA QT.
   * Tutti e tre condividono lo stesso bus, quindi **solo uno può essere usato alla volta**.

   .. image:: img/pinpal_i2c.png
       :width: 80%
       :align: center

#. **TXD / RXD — UART (GPIO14 / GPIO15)**

   * Pin UART principali del Raspberry Pi.
   * La Fusion HAT+ include un altro header UART, che condivide gli stessi pin — **scegline solo uno**.

   .. image:: img/pinpal_uart.png
       :width: 80%
       :align: center

#. **GPIO 17 / 4 / 27 / 22 — GPIO Generici**

   * La Fusion HAT+ fornisce un set aggiuntivo di questi pin, ma corrispondono agli stessi GPIO del Raspberry Pi.
   * **Usa un solo gruppo** per evitare conflitti.

   .. image:: img/pinpal_gpio.png
       :width: 80%
       :align: center

#. **MOSI / MISO / SCLK / CE0 / GPIO6 — Pin SPI**

   * La Fusion HAT+ fornisce un altro header SPI.
   * Il connettore RGB (WS2812) utilizza il pin MOSI.
   * **Usa un solo gruppo SPI** per evitare conflitti.


   .. list-table::
      :header-rows: 1

      * - Segnale
        - Mappatura Pin
      * - BSY
        - GPIO6
      * - CS
        - CE0 / GPIO8
      * - SCK
        - SCLK / GPIO11
      * - MI
        - MISO / GPIO9
      * - MO
        - MOSI / GPIO10

   .. image:: img/pinpal_spi.png
       :width: 80%
       :align: center


#. **GPIO 18 / 19 / 20 / 21 — Pin Audio I2S**

   * La Fusion HAT+ include audio I2S integrato (altoparlante + microfono). Maggiori dettagli:
     `I2S <https://docs.sunfounder.com/projects/fusion-hat/en/latest/hardware/interfaces.html#speaker-and-mic>`_.
   * Puoi riutilizzare questi pin solo quando il sistema audio è disattivato.
   * **Non usare WS o SCLK mentre i componenti audio sono attivi.**

   .. image:: img/pinpal_i2s.png
       :width: 80%
       :align: center

   .. list-table::
      :header-rows: 1

      * - Segnale
        - Pin Raspberry Pi
      * - WS
        - GPIO19
      * - SCLK
        - GPIO18
      * - Uscita Audio (Altoparlante)
        - GPIO21
      * - Ingresso Audio (MIC)
        - GPIO20


#. **ID_SD / ID_SC — Pin EEPROM HAT**

   Questi pin sono riservati per l'EEPROM HAT del Raspberry Pi, che memorizza i dati di identificazione della scheda.
   La Fusion HAT+ utilizza questi pin per il suo EEPROM integrato, quindi **ID_SD (GPIO0) e ID_SC (GPIO1) non devono essere usati per altri scopi**.


   .. image:: img/pinpal_eeprom.png
       :width: 80%
       :align: center

