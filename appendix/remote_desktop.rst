.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _remote_desktop:

Bureau à distance
===================

.. |shared_link_realvnc| raw:: html

    <a href="https://www.realvnc.com/en/connect/download/viewer/" target="_blank">RealVNC® Viewer</a>   

Vous pouvez accéder au bureau du Raspberry Pi et le contrôler à distance depuis un autre ordinateur.  
La méthode recommandée est **VNC**, officiellement prise en charge par Raspberry Pi OS et offrant une expérience de bureau fiable et cohérente.

La section suivante explique comment activer VNC sur votre Raspberry Pi et vous y connecter à l’aide de |shared_link_realvnc|.

-----------------

Activer le service VNC
------------------------

RealVNC Server est préinstallé sur Raspberry Pi OS, mais il est **désactivé par défaut**.  
Vous devez l’activer via l’outil de configuration.

#. Ouvrez un terminal sur votre ordinateur (Windows : **PowerShell** ; macOS/Linux : **Terminal**) et connectez-vous à votre Raspberry Pi :

   .. code-block:: bash

      ssh <nom_utilisateur>@<nom_hôte>.local

   ou

   .. code-block:: bash

      ssh <nom_utilisateur>@<adresse_ip>

#. Lancez l’outil de configuration :

   .. code-block:: bash

      sudo raspi-config

   .. image:: /_shared/appendix/img/ssh_raspi_config.png


#. Sélectionnez **Interfacing Options** et appuyez sur **Entrée**.

   .. image:: /_shared/appendix/img/ssh_interface.png


#. Sélectionnez **VNC**.

   .. image:: /_shared/appendix/img/ssh_vnc_vnc.png


#. Choisissez **Yes**, puis **OK**, et enfin **Finish** pour quitter.

   .. image:: /_shared/appendix/img/ssh_vnc_enable.png



Connexion avec RealVNC® Viewer
---------------------------------

#. Téléchargez et installez |shared_link_realvnc| pour votre système d’exploitation.

   .. image:: /_shared/appendix/img/ssh_vnc_download.png


#. Ouvrez **RealVNC Viewer**, puis saisissez l’adresse IP de votre Raspberry Pi ou ``<nom_hôte>.local`` et appuyez sur **Entrée**.

   .. image:: /_shared/appendix/img/ssh_vnc_login.png


#. Saisissez le **nom d’utilisateur** et le **mot de passe** de votre Raspberry Pi, puis sélectionnez **OK**.

   .. note::

      Lors de la première connexion, un message tel que « VNC Server not recognized » peut apparaître. Sélectionnez **Continue** pour poursuivre.

   .. image:: /_shared/appendix/img/ssh_vnc_username.png


#. Vous devriez maintenant voir le bureau du Raspberry Pi :

   .. image:: /_shared/appendix/img/ssh_vnc_desktop.png


Cela termine le processus de configuration de VNC.

-----------------


Remarques supplémentaires
---------------------------

* **Version Desktop requise**

  * VNC nécessite que le Raspberry Pi exécute la version complète avec interface graphique de Raspberry Pi OS.  
  * Si vous utilisez **Raspberry Pi OS Lite**, installez manuellement VNC Server : ``sudo apt install realvnc-vnc-server``


* **Conseils sur les performances réseau** 

  * En cas de latence ou de rafraîchissement lent, vérifiez la qualité de votre réseau.  
  * Une connexion Ethernet filaire offre généralement les meilleures performances.


* **Résoudre les problèmes de résolution d’affichage**

  * Si la fenêtre VNC apparaît trop petite ou avec une résolution incorrecte, définissez une résolution fixe via : ``sudo raspi-config`` → **Display Options** → **VNC Resolution**


* **Vérifier que VNC est activé**

  Si la connexion VNC échoue, vérifiez qu’il est bien activé dans : ``sudo raspi-config`` → ``Interfacing Options`` → ``VNC``


* **Arrêter le service VNC**

  Pour arrêter manuellement le serveur VNC : ``sudo systemctl stop vncserver-x11-serviced``


* **Rappel de sécurité**

  * VNC est conçu pour des réseaux locaux de confiance.  
  * N’exposez **pas** VNC directement sur Internet.  
  * Pour un accès distant sécurisé depuis l’extérieur de votre réseau, utilisez **Raspberry Pi Connect** ou un VPN.
