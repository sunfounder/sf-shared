.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme ad altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi problemi post-vendita e sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e Condividi**: Scambia consigli e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Accedi in anteprima a nuovi annunci di prodotti e anticipazioni.
    - **Sconti speciali**: Godi di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e omaggi**: Partecipa a omaggi e promozioni durante le festività.

    👉 Pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _cpn_led_matrix:

Matrice LED a punti
======================

.. image:: img/matrix_pic.png
    :width: 300

La matrice LED a punti può essere suddivisa in due tipi: **Catodo Comune (CC)** e **Anodo Comune (CA)**.  
All’esterno hanno un aspetto simile, ma la loro struttura elettrica interna è diversa.

La matrice LED utilizzata in questo kit è di tipo **Anodo Comune (CA)**.  
Puoi identificarla dalla marcatura **“788BS”** stampata sul lato del modulo.

Disposizione dei pin
--------------------

I pin si trovano su entrambi i lati del retro del modulo.  
Guardando il lato con l’etichetta:

* I pin **1–8** si trovano su un lato  
* I pin **9–16** si trovano sul lato opposto  

Vista esterna:

.. image:: img/matrix_pin.png

Struttura interna
-----------------------

La figura seguente mostra la struttura interna della matrice LED a punti.

* In una matrice **Anodo Comune (CA)**, **ROW = Anodo** e **COL = Catodo**
* In una matrice **Catodo Comune (CC)**, **ROW = Catodo** e **COL = Anodo**

.. image:: img/matrix_internal.png
   :width: 400
   :align: center

Sia per il tipo CA che per il tipo CC, la posizione fisica dei pin di righe e colonne è la stessa — cambia solo la polarità elettrica.

Mappatura dei pin
-----------------------

.. list-table::
   :header-rows: 2
   :align: center

   * - **COL**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Pin n.**
     - **13**
     - **3**
     - **4**
     - **10**
     - **6**
     - **11**
     - **15**
     - **16**
   * - **ROW**
     - **1**
     - **2**
     - **3**
     - **4**
     - **5**
     - **6**
     - **7**
     - **8**
   * - **Pin n.**
     - **9**
     - **14**
     - **8**
     - **12**
     - **1**
     - **7**
     - **2**
     - **5**

Come si accendono i LED
----------------------------

Per controllare un singolo LED, è necessario attivare correttamente i pin di **ROW** e **COL**.

*Esempio: LED in alto a sinistra (ROW 1, COL 1)*

- **Tipo CA**  
  Impostare **ROW pin 9 = High**, **COL pin 13 = Low**

- **Tipo CC**  
  Impostare **COL pin 13 = High**, **ROW pin 9 = Low**

*Esempio: accendere l’intera prima colonna*

- **Tipo CA**  
  Impostare **COL pin 13 = Low**  
  Impostare **ROW pin 9, 14, 8, 12, 1, 7, 2, 5 = High**

- **Tipo CC**  
  Impostare **COL pin 13 = High**  
  Impostare **ROW pin 9, 14, 8, 12, 1, 7, 2, 5 = Low**

Questo metodo di scansione riga-colonna consente di controllare ogni LED singolarmente utilizzando il multiplexing.
