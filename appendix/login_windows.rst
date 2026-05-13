.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _login_windows:

PuTTY
=========================

PuTTY è un client SSH semplice e affidabile per utenti Windows, utilizzato per accedere da remoto al Raspberry Pi.  


.. |shared_link_putty| raw:: html

    <a href="https://www.chiark.greenend.org.uk/~sgtatham/putty/latest.html" target="_blank">PuTTY</a> 


#. Scarica PuTTY da |shared_link_putty| e installalo sul tuo computer.

   .. image:: /_shared/appendix/img/putty_download.png
      :width: 70%


#. Apri PuTTY e prepara la connessione:

   * Inserisci il **nome host o l’indirizzo IP** del tuo Raspberry Pi in **Host Name**.
   * Imposta la **Port** su ``22``.
   * Clicca su **Open** per connetterti.


   .. image:: /_shared/appendix/img/putty_open.png
      :width: 70%
   
#. Se al primo utilizzo compare un avviso di sicurezza, clicca su **Accept** per continuare.

   .. image:: /_shared/appendix/img/putty_accept.png
      :width: 70%

#. Accedi al Raspberry Pi:

   * Quando vedi **login as:**, inserisci il nome utente che hai impostato in **Raspberry Pi Imager**.
   * Inserisci la password (non verrà visualizzata mentre digiti — è normale).
   * Dopo l’accesso, il terminale sarà pronto per inserire comandi e gestire il tuo Raspberry Pi da remoto.

   .. image:: /_shared/appendix/img/putty_login.png
      :width: 70%

.. note::

    Se PuTTY mostra **inactive**, significa che la connessione è stata persa e deve essere ristabilita.
