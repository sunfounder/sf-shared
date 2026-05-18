.. note::

    Hallo und willkommen in der SunFounder Raspberry Pi & Arduino & ESP32 Enthusiasten-Gemeinschaft auf Facebook! Tauchen Sie tiefer ein in die Welt von Raspberry Pi, Arduino und ESP32 mit anderen Enthusiasten.

    **Warum beitreten?**

    - **Expertenunterstützung**: Lösen Sie Nachverkaufsprobleme und technische Herausforderungen mit Hilfe unserer Gemeinschaft und unseres Teams.
    - **Lernen & Teilen**: Tauschen Sie Tipps und Anleitungen aus, um Ihre Fähigkeiten zu verbessern.
    - **Exklusive Vorschauen**: Erhalten Sie frühzeitigen Zugang zu neuen Produktankündigungen und exklusiven Einblicken.
    - **Spezialrabatte**: Genießen Sie exklusive Rabatte auf unsere neuesten Produkte.
    - **Festliche Aktionen und Gewinnspiele**: Nehmen Sie an Gewinnspielen und Feiertagsaktionen teil.

    👉 Sind Sie bereit, mit uns zu erkunden und zu erschaffen? Klicken Sie auf [|link_sf_facebook|] und treten Sie heute bei!

.. _openssh_powershell:

OpenSSH über PowerShell installieren
--------------------------------------

Wenn beim Ausführen von ``ssh <username>@<hostname>.local`` oder ``ssh <username>@<IP>`` der folgende Fehler erscheint:

.. code-block::

    ssh: The term 'ssh' is not recognized as the name of a cmdlet, function, script file, or operable program.

bedeutet dies, dass auf Ihrem Windows-System OpenSSH nicht installiert ist.  
Befolgen Sie die folgenden Schritte, um es manuell zu installieren.

#. Öffnen Sie das Windows-Startmenü, geben Sie **powershell** ein, klicken Sie mit der rechten Maustaste auf **Windows PowerShell** und wählen Sie **Als Administrator ausführen**.

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. Installieren Sie den OpenSSH-Client:

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. Nach der Installation sollten Sie eine ähnliche Ausgabe sehen:

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. Überprüfen Sie die Installation:

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. Wenn OpenSSH installiert ist, enthält die Ausgabe:

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      Wenn ``Installed`` nicht erscheint, ist Ihr Windows-System möglicherweise zu alt.  
      In diesem Fall empfehlen wir die Verwendung eines SSH-Tools eines Drittanbieters. Siehe: :ref:`login_windows`

#. Schließen Sie PowerShell, öffnen Sie sie erneut (diesmal ohne Administratorrechte) und verwenden Sie den Befehl ``ssh``, um sich anzumelden:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center
