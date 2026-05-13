.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _cpn_motor_xh254:

Motore DC XH2.54
===================

.. image:: img/motor_254_pic.png
    :width: 50%
    :align: center

Un motore a corrente continua (DC) è un semplice attuatore elettrico che converte l'energia elettrica in rotazione meccanica.
È ampiamente utilizzato in dispositivi come pompe, ventilatori, compressori e piccoli robot grazie alla sua capacità di fornire un movimento rotatorio continuo.

**Specifiche del motore**

* **Tensione di funzionamento**: 3–5 V
* **Corrente a vuoto (3 V)**: 100–120 mA
* **Velocità a vuoto (3 V)**: 8000 giri/min
* **Coppia di stallo (3 V)**: 140 g·cm
* **Corrente di stallo (3 V)**: 650 mA
* **Tipo di connettore**: XH2.54 2P (bianco)
* **Lunghezza cavi**: Rosso/Nero, 10 cm, 24 AWG
* **Dimensioni**: 25 × 20 × 15 mm

Un motore DC è composto da due parti principali: lo **statore**, che rimane fisso, e il **rotore** (o **indotto**), che ruota per generare movimento.
Il rotore è posto all'interno di un campo magnetico creato da magneti permanenti. Quando la corrente scorre attraverso gli avvolgimenti dell'indotto, produce un campo magnetico che interagisce con il campo dello statore, generando una coppia che provoca la rotazione.

.. image:: img/motor_sche.png
    :align: center

La corrente fluisce dall'alimentatore alle spazzole, al commutatore e quindi agli avvolgimenti dell'indotto.
Il commutatore inverte periodicamente la direzione della corrente ogni mezzo giro, assicurando che la coppia agisca sempre nella direzione corretta per mantenere una rotazione continua.
Questa azione di commutazione converte effettivamente l'alimentazione DC in una forma di corrente alternata all'interno del motore, consentendo un movimento fluido e sostenuto.
