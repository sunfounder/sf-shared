.. note::

    Ciao, benvenuto nella community di SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasts su Facebook! Approfondisci Raspberry Pi, Arduino ed ESP32 insieme agli altri appassionati.

    **Perché unirsi?**

    - **Supporto esperto**: Risolvi i problemi post-vendita e le sfide tecniche con l'aiuto della nostra community e del nostro team.
    - **Impara e condividi**: Scambia suggerimenti e tutorial per migliorare le tue competenze.
    - **Anteprime esclusive**: Ottieni l'accesso anticipato agli annunci di nuovi prodotti e anteprime.
    - **Sconti speciali**: Approfitta di sconti esclusivi sui nostri prodotti più recenti.
    - **Promozioni festive e giveaway**: Partecipa a giveaway e promozioni per le festività.

    👉 Sei pronto a esplorare e creare con noi? Clicca su [|link_sf_facebook|] e unisciti oggi stesso!

.. _openssh_powershell:

Installare OpenSSH tramite PowerShell
------------------------------------

Se vedi il seguente errore quando esegui ``ssh <username>@<hostname>.local`` oppure ``ssh <username>@<IP>``:

.. code-block::

    ssh: The term 'ssh' is not recognized as the name of a cmdlet, function, script file, or operable program.

Significa che il tuo sistema Windows non ha OpenSSH installato.  
Segui i passaggi seguenti per installarlo manualmente.

#. Apri il menu Start di Windows, digita **powershell**, fai clic con il tasto destro su **Windows PowerShell** e seleziona **Esegui come amministratore**.

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. Installa il client OpenSSH:

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. Dopo l’installazione, dovresti vedere un output simile a:

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. Verifica l’installazione:

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. Se OpenSSH è installato, l’output includerà:

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      Se ``Installed`` non appare, il tuo sistema Windows potrebbe essere troppo vecchio.  
      In questo caso, consigliamo di utilizzare uno strumento SSH di terze parti. Vedi: :ref:`login_windows`

#. Chiudi PowerShell, riaprilo (questa volta non è necessario eseguirlo come amministratore) e utilizza il comando ``ssh`` per accedere:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center

