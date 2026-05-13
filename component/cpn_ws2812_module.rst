.. _cpn_circular_ws2812_module:

Modulo LED WS2812 Circolare
===========================================================

.. image:: img/c_ws2812_module.png
    :width: 40%
    :align: center

Questo modulo LED WS2812 circolare contiene 12 LED RGB indirizzabili individualmente, ciascuno con un driver integrato che supporta il controllo del colore a 24 bit su una singola linea dati. Il modulo espone quattro pin — VCC, GND, DIN e DOUT — per una facile connessione a controller come Raspberry Pi o Arduino.

**Panoramica dei Pin**

* **V (VCC)**: Ingresso di alimentazione a 5 V. Assicurati che l'alimentatore possa fornire corrente sufficiente per tutti i LED.
* **G (GND)**: Massa. Deve essere condivisa con il controller per una corretta segnalazione.
* **R (DIN)**: Riceve i dati dal microcontrollore. È l'ingresso di controllo.
* **D (DOUT)**: Invia i dati ad anelli o strisce LED aggiuntivi, consentendo l'espansione a margherita.

**Utilizzo**

I LED si passano i dati l'un l'altro, consentendo il controllo indipendente di ciascun LED e permettendo effetti come dissolvenze di colore, gradienti, rotazioni e motivi di animazione.
Questo anello compatto da 12 LED è adatto per indicatori, illuminazione decorativa, robotica, dispositivi indossabili, orologi e piccoli progetti di visualizzazione.
