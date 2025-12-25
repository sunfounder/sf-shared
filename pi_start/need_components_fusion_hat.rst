.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

Cos’altro ti serve?
===================

Prima di iniziare a giocare con questo kit, prepariamo l’hardware essenziale.

Componenti necessari
--------------------

* **Raspberry Pi**

  Il Raspberry Pi funge da **cervello**, gestendo tutte le attività di calcolo, rilevamento e controllo.  
  
  .. image:: /_shared/pi_start/img/need_pi.jpg

  * **Modelli compatibili**: Raspberry Pi 5, Raspberry Pi 4, 3 o Raspberry Pi Zero 2W  
  * **Minimo**: **2GB di RAM** — sufficiente per tutti i progetti Python standard e per l’utilizzo di **servizi AI online** come OpenAI Whisper, TTS o LLM.  
  * **Consigliato**: **4GB di RAM o più** — garantisce prestazioni più fluide quando si eseguono **modelli AI locali** (ad esempio riconoscimento vocale Vosk, Piper TTS o LLM leggeri) insieme allo streaming della fotocamera e alle attività di controllo.  
  

* **Alimentatore**

  Questo kit include un **pacco batterie 18650** e una scheda **Fusion HAT+** con circuito di ricarica integrato.
  
  .. image:: /_shared/pi_start/img/need_power.png
    :width: 400

  * Per la ricarica, si consiglia di utilizzare un **alimentatore da 5V 3A**, come l’**adattatore USB-C ufficiale Raspberry Pi da 15W**.  
  * È possibile utilizzare anche un **caricatore USB-C Power Delivery (PD)** o un **caricatore rapido QC 2.0**.  
  * Una ricarica completa richiede in genere circa **2 ore** (dallo 0% al 100%).  


* **Scheda Micro SD**

  Il Raspberry Pi non dispone di un disco rigido integrato. L’avvio e l’archiviazione di tutti i file avvengono su una **scheda Micro SD**.  
  
  .. image:: /_shared/pi_start/img/need_sd.jpg
    :width: 200

  * Minimo: **16GB**  
  * Consigliato: **32GB** per una maggiore stabilità  
  * Marca: utilizza opzioni affidabili come **SanDisk** o **Samsung** per evitare errori di lettura/scrittura  
  

Componenti opzionali
--------------------

Sebbene non siano strettamente necessari, le seguenti periferiche miglioreranno notevolmente l’esperienza di apprendimento e di debug:

* **Monitor (HDMI o TV)** 

  Per i principianti, consigliamo vivamente un display con ingresso HDMI, così da poter configurare facilmente Raspberry Pi OS ed eseguire programmi grafici.  

  .. image:: /_shared/pi_start/img/need_screen.png
    :width: 400

* **Cavo HDMI (Standard / Mini / Micro)**
 
  I diversi modelli di Raspberry Pi utilizzano connettori HDMI differenti; assicurati di verificare il modello del tuo Pi e di preparare il cavo corretto. 
  
  * **Raspberry Pi 4 / 5**: Micro HDMI  
  * **Raspberry Pi 3**: HDMI standard  
  * **Raspberry Pi Zero 2W**: Mini HDMI 

  .. image:: /_shared/pi_start/img/need_hdmi.png
    :width: 400

* **Tastiera e mouse**

  Molto utili durante la configurazione iniziale di Raspberry Pi OS. In seguito potrai passare all’accesso remoto (SSH/VNC), ma per i principianti consigliamo di preparare un set USB o wireless di base.  

  .. image:: /_shared/pi_start/img/need_keyboard_mouse.png
    :width: 500
 

**Suggerimenti per la preparazione**

* Se hai acquistato questo kit, la maggior parte degli accessori è inclusa, ma dovrai comunque procurarti separatamente la scheda Raspberry Pi, la scheda Micro SD e l’alimentatore.  
* Non sai cosa acquistare? La scelta più stabile e universale è: **Raspberry Pi 4 (2GB) + alimentatore ufficiale + scheda Micro SD da 32GB**.  
