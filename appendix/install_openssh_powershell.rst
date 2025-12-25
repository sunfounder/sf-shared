.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _openssh_powershell:

Installer OpenSSH via PowerShell
---------------------------------------------

Si vous voyez l’erreur suivante lors de l’exécution de ``ssh <nom_utilisateur>@<nom_hôte>.local`` ou ``ssh <nom_utilisateur>@<IP>`` :

.. code-block::

    ssh : le terme « ssh » n’est pas reconnu comme nom d’applet de commande, de fonction, de fichier de script ou de programme exécutable.

Cela signifie que votre système Windows n’a pas OpenSSH installé.  
Suivez les étapes ci-dessous pour l’installer manuellement.

#. Ouvrez le menu Démarrer de Windows, tapez **powershell**, faites un clic droit sur **Windows PowerShell**, puis sélectionnez **Exécuter en tant qu’administrateur**.

   .. image:: /_shared/appendix/img/powershell_ssh.png
      :align: center

#. Installez le client OpenSSH :

   .. code-block:: bash

      Add-WindowsCapability -Online -Name OpenSSH.Client~~~~0.0.1.0

#. Après l’installation, vous devriez voir une sortie similaire à :

   .. code-block::

        Path          :
        Online        : True
        RestartNeeded : False

#. Vérifiez l’installation :

   .. code-block:: bash

      Get-WindowsCapability -Online | Where-Object Name -like 'OpenSSH*'

#. Si OpenSSH est installé, la sortie inclura :

   .. code-block::

        Name  : OpenSSH.Client~~~~0.0.1.0
        State : Installed
        Name  : OpenSSH.Server~~~~0.0.1.0
        State : NotPresent

   .. warning::
      Si ``Installed`` n’apparaît pas, votre système Windows est peut-être trop ancien.  
      Dans ce cas, nous recommandons d’utiliser un outil SSH tiers. Voir : :ref:`login_windows`

#. Fermez PowerShell, rouvrez-le (il n’est pas nécessaire de l’exécuter en tant qu’administrateur cette fois), puis utilisez la commande ``ssh`` pour vous connecter :

   .. code-block:: bash

      ssh <nom_utilisateur>@<nom_hôte>.local

   .. image:: /_shared/appendix/img/powershell_login.png
      :align: center
