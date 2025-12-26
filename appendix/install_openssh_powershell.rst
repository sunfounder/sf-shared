
.. _openssh_powershell:

Install OpenSSH via PowerShell
------------------------------

If you see the following error when running ``ssh <username>@<hostname>.local`` or ``ssh <username>@<IP>``:

.. code-block::

    ssh: The term 'ssh' is not recognized as the name of a cmdlet, function, script file, or operable program.

It means your Windows system does not have OpenSSH installed.  
Follow the steps below to install it manually.

#. Open the Windows Start Menu, type **powershell**, right-click **Windows PowerShell**, and select **Run as administrator**.

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. Install the OpenSSH Client:

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. After installation, you should see output similar to:

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. Verify the installation:

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. If OpenSSH is installed, the output will include:

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      If ``Installed`` does not appear, your Windows system may be too old.  
      In this case, we recommend using a third-party SSH tool. See: :ref:`login_windows`

#. Close PowerShell, reopen it (no need to run as administrator this time), and use the ``ssh`` command to log in:

   .. code-block:: bash

      ssh <username>@<hostname>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center

