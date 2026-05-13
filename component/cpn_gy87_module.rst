.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _cpn_gy87:

Modulo IMU GY-87
============================

.. image:: img/gy87.png
    :align: center
    :width: 40%

Il modulo sensore GY-87 è un modulo ad alta precisione a 10 assi (10DOF) in grado di misurare accelerazione, velocità angolare e intensità del campo magnetico su tre assi: x, y e z. È composto da tre sensori principali: MPU6050, QMC5883L e BMP180, e comunica tramite il protocollo I2C.

Il modulo sensore GY-87 è basato su tre sensori:

1. **MPU6050**: Un accelerometro e giroscopio a 6 assi che misura l'accelerazione e la velocità angolare sui tre assi x, y e z.
2. **QMC5883L**: Una bussola digitale a 3 assi che misura l'intensità del campo magnetico sui tre assi x, y e z.
3. **BMP180**: Un sensore barometrico di temperatura e pressione che misura la pressione atmosferica e la temperatura.

L'MPU6050 misura l'accelerazione e la velocità angolare sui tre assi x, y e z. Il QMC5883L misura l'intensità del campo magnetico sui tre assi x, y e z. Il BMP180 misura la pressione atmosferica e la temperatura. I dati di questi sensori vengono combinati per fornire informazioni precise sull'orientamento del modulo nello spazio.

Il modulo sensore GY-87 è comunemente utilizzato in applicazioni come droni, robotica e altri progetti che richiedono informazioni di orientamento accurate. È compatibile con le schede Arduino e può essere facilmente interfacciato tramite il protocollo di comunicazione I2C.
