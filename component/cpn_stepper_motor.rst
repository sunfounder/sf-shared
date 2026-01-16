.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme ad altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi problemi post-vendita e sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e Condividi**: Scambia consigli e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Accedi in anteprima a nuovi annunci di prodotti e anticipazioni.
    - **Sconti speciali**: Godi di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e omaggi**: Partecipa a omaggi e promozioni durante le festività.

    👉 Pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!


Stepper Motor e Modulo ULN2003
=========================================

**Motore Passo-Passo**

Il 28BYJ-48 è un motore passo-passo unipolare a 5 fili che funziona a 5V. I motori passo-passo sono motori di precisione che possono essere controllati in modo molto accurato senza bisogno di feedback da sensori. Questo perché l’albero del motore è dotato di magneti ed è controllato da bobine elettromagnetiche che si accendono e si spengono secondo una sequenza specifica, muovendo l’albero in piccoli passi precisi.

.. image:: img/step_stepper.png
  :align: center

Lo statore del motore passo-passo che utilizziamo ha 32 poli magnetici, quindi per completare un giro sono necessari 32 passi. L’albero di uscita del motore passo-passo è collegato a un riduttore, con un rapporto di riduzione di 1/64. Pertanto, l’albero di uscita finale compie un giro completo richiedendo 32*64 = 2048 passi.

**Come funziona un motore passo-passo unipolare**

Un motore passo-passo unipolare ha in genere quattro fasi e funziona con alimentazione in corrente continua. Temporizzando correttamente la corrente elettrica nelle fasi del motore, è possibile farlo ruotare passo dopo passo. Immagina che al centro del motore ci sia un magnete a forma di ingranaggio (il rotore) circondato da diversi denti numerati da 0 a 5. Attorno a questi denti si trovano otto poli magnetici disposti a coppie (da A a D), collegati tramite bobine.

.. image:: img/step_interal.png
  :align: center

Quando alimenti i diversi interruttori collegati a queste bobine (indicati come SA, SB, SC e SD), controlli quali poli magnetici vengono attivati. Ad esempio, se l’interruttore SB è acceso (e gli altri sono spenti), i poli magnetici B si allineano con determinati denti del rotore, facendolo muovere. Quando accendi successivamente l’interruttore SC, il rotore ruota per allinearsi ai poli magnetici C, e così via. Alternando ciclicamente gli interruttori A, B, C e D, il rotore ruota in modo continuo.

**Modulo ULN2003**

.. image:: img/step_uln2003.png
    :align: center

Il modulo driver per motore passo-passo ULN2003 è fondamentale per integrare il motore passo-passo nei circuiti. Funziona come un inverter a 7 canali, il che significa che converte i segnali di ingresso nelle azioni di uscita necessarie per il motore. Ad esempio, se viene inviato un segnale alto a IN1 e segnali bassi a IN2, IN3 e IN4, allora OUT1 va a livello basso e le altre uscite rimangono alte, facendo ruotare il motore di un passo. Fornendo sequenze specifiche come questa, il motore può ruotare in modo fluido passo dopo passo. Il modulo ULN2003 semplifica il controllo delle sequenze di temporizzazione necessarie per il funzionamento del motore.
