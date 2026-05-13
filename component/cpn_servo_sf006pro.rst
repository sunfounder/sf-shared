.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _cpn_sf006pro_servo:

Servo SF006PRO
===================

.. image:: img/servo_metal.png
    :width: 50%
    :align: center

Questo servo è un attuatore piccolo e affidabile che funziona a 4–6 V, offrendo un movimento fluido e fino a 180° di controllo. Fornisce una buona coppia, risposta rapida e basso consumo energetico, rendendolo adatto a robotica, meccanismi e progetti hobbistici in generale.
La sua interfaccia PWM standard a 3 pin facilita il collegamento a microcontrollori come Arduino o Raspberry Pi.

**Come funziona un servo**


Un servo tipico è composto da diversi componenti interni:

* Custodia
* Albero di uscita
* Sistema di ingranaggi
* Potenziometro
* Motore DC
* Scheda di controllo (integrata)

Il microcontrollore invia segnali di controllo PWM al servo attraverso il pin del segnale.
La scheda di controllo interpreta il segnale e aziona il motore DC, che fa ruotare il sistema di ingranaggi. Dopo aver attraversato il sistema di riduzione a ingranaggi, l'albero ruota con una coppia maggiore.

L'albero di uscita è collegato meccanicamente al potenziometro. Quando l'albero ruota, il potenziometro cambia la sua tensione di uscita. La scheda di controllo legge questo feedback per determinare la posizione attuale, regolando la rotazione del motore fino a quando l'albero raggiunge e mantiene l'angolo desiderato.

.. image:: img/servo_internal.png
    :align: center

**Controllo PWM**

L'angolo di rotazione del servo è determinato dalla larghezza dell'impulso PWM. Il servo normalmente si aspetta un impulso ogni **20 ms**.

Comportamento tipico dell'impulso:

* **1,5 ms** → Posizione neutra (circa 90°)
* **< 1,5 ms** → Si sposta in senso antiorario dal centro
* **> 1,5 ms** → Si sposta in senso orario dal centro

La maggior parte dei servi hobbistici accetta larghezze di impulso tra **0,5 ms e 2,5 ms**, corrispondenti alla loro gamma di movimento completa.

.. image:: img/servo_duty.png
    :width: 600
    :align: center


**Parametri**

.. list-table::
   :header-rows: 1
   :widths: 25 75

   * - Parametro
     - Specifica

   * - Tensione di funzionamento
     - DC 4 V–6 V (Nominale 5 V, si consiglia alimentazione a 5 V)

   * - Corrente di standby
     - ≤ 5 mA

   * - Corrente a vuoto
     - ≤ 350 mA a 5 V (picco misurato manualmente)

   * - Corrente di stallo
     - ≤ 1,2 A a 5 V (scende a ≤ 250 mA dopo 5 secondi di stallo)

   * - Coppia nominale
     - 0,75 kgf·cm (a 5 V)

   * - Carico dinamico massimo
     - ≥ 2,2 kgf·cm (a 5 V)

   * - Coppia di stallo (statica)
     - ≥ 5 kgf·cm (testato con misuratore di coppia)

   * - Velocità a vuoto
     - ≤ 0,17 sec/60° (a 5 V)

   * - Angolo di corsa operativo
     - 90° ±10° (1000–2000 μs)

   * - Angolo massimo di funzionamento
     - 180° ±10° (500–2500 μs)

   * - Angolo limite meccanico
     - 360°

   * - Intervallo di larghezza dell'impulso
     - 500 μs ~ 2500 μs

   * - Posizione neutra
     - 1500 μs

   * - Larghezza della banda morta
     - ≤ 6 μs

   * - Gioco meccanico
     - ≤ 0,5°

   * - Peso
     - 13,5 ± 0,5 g

   * - Materiale degli ingranaggi
     - Ingranaggi ibridi plastica + metallo

   * - Tipo di motore
     - Motore a nucleo di ferro

   * - Tipo di potenziometro
     - Pellicola di carbonio, angolo 220°, ≥ 100.000 cicli

   * - Cavo
     - 250 ±5 mm, connettore JR a 3 pin (Marrone–Rosso–Arancione)

   * - Piedinatura del connettore
     - Arancione: Segnale PWM

       Rosso: VCC

       Marrone: GND

   * - Interfaccia di comunicazione
     - PWM

       Tensione del segnale: ALTO 2,0–5,0 V / BASSO 0,0–0,6 V

       Frequenza fotogrammi: 3–30 ms (Predefinito 20 ms)

       Intervallo impulsi: 500–2500 μs

**Dimensioni**

.. image:: img/servo_metal_size.png
    :width: 80%
    :align: center
