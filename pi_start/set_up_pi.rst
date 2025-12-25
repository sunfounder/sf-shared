.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des conseils et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et à des aperçus exclusifs.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos nouveaux produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et à des promotions festives.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _setup_pi:

Configurer votre Raspberry Pi
=============================

Pour commencer à programmer et à contrôler votre Raspberry Pi, vous devez d’abord y accéder.  
Ce guide décrit deux méthodes courantes :

* Utiliser un écran, un clavier et une souris  
* Mettre en place une connexion *headless* (sans écran) pour un accès à distance  

.. note::

   Le Raspberry Pi Zero 2W installé sur le robot n’est pas facile à connecter à un écran.  
   Nous recommandons d’utiliser la méthode de **configuration headless**.

-------------------------
Si vous avez un écran
-------------------------

**Composants requis**

* Raspberry Pi
* Alimentation officielle
* Carte microSD
* Câble HDMI  
  (Pour Raspberry Pi 4/5, utilisez **HDMI0**, le port le plus proche du connecteur d’alimentation.)
* Écran
* Clavier et souris

**Étapes**

#. Insérez la carte microSD dans votre Raspberry Pi.
#. Connectez le clavier, la souris et l’écran.
#. Allumez votre Raspberry Pi.
#. Après le démarrage, le bureau de Raspberry Pi OS apparaîtra. 

   .. image:: /_shared/pi_start/img/plug_screen_trixie.png
      :width: 80%
      :align: center

#. Ouvrez un **Terminal** pour saisir des commandes.

   .. image:: /_shared/pi_start/img/open_terminal.png
      :width: 80%
      :align: center


----------------------------------
Si vous n’avez pas d’écran (Headless)
----------------------------------

Sans écran, vous pouvez configurer et vous connecter à votre Raspberry Pi à distance.  
C’est la méthode la plus pratique pour la plupart des utilisateurs.

**Composants requis**

* Raspberry Pi
* Alimentation officielle
* Carte microSD
* Un ordinateur sur le même réseau

**Conseils**

* Assurez-vous d’avoir complété tous les paramètres décrits dans :ref:`imager_custom` lors de l’installation du système avec Raspberry Pi Imager.
* Vérifiez que votre Raspberry Pi et votre ordinateur sont sur le même réseau local.
* Pour une meilleure stabilité, utilisez Ethernet si possible.


**Connexion via SSH**

#. Ouvrez un terminal sur votre ordinateur (Windows : **PowerShell** ; macOS/Linux : **Terminal**) et connectez-vous à votre Raspberry Pi :

   .. code-block:: bash

      ssh <nom_utilisateur>@<nom_hôte>.local
      # Exemple :
      ssh daisy@pi.local

2. Vous pouvez également trouver l’adresse IP de votre Pi dans la liste DHCP de votre routeur et vous connecter avec :

   .. code-block:: bash

      ssh <nom_utilisateur>@<adresse_IP>
      # Exemple :
      ssh daisy@192.168.1.42

3. Lors de la première connexion, tapez ``yes`` pour confirmer le certificat SSH.

4. Saisissez le mot de passe que vous avez configuré dans Raspberry Pi Imager.  
   (Rien ne s’affiche pendant la saisie — c’est normal.)

5. Après la connexion, vous disposez désormais d’un accès complet en ligne de commande.

   .. image:: /_shared/pi_start/img/ssh_login.png
      :align: center

----------------------

**Dépannage**

* **ssh: Could not resolve hostname ...**

  * Vérifiez que le nom d’hôte est correct.
  * Essayez de vous connecter en utilisant l’adresse IP du Pi.

* **The term 'ssh' is not recognized... (Windows)**

  * OpenSSH n’est pas installé. Installez-le manuellement ou utilisez un client SSH tiers.  
  * Voir :ref:`openssh_powershell` ou :ref:`login_windows`.

* **Permission denied (publickey,password)**

  * Assurez-vous d’utiliser le nom d’utilisateur et le mot de passe créés dans Raspberry Pi Imager.

* **Connection refused**

  * Attendez 1 à 2 minutes après la mise sous tension.
  * Vérifiez que SSH a bien été activé dans Raspberry Pi Imager.

--------------------------------

Options d’accès graphique à distance
-------------------------------------

.. |shared_link_rpi_connect| raw:: html

    <a href="https://www.raspberrypi.com/documentation/services/connect.html" target="_blank">Raspberry Pi Connect</a> 

Si vous préférez une interface graphique :

* :ref:`remote_desktop` : activez **VNC (Virtual Network Computing)** pour une expérience de bureau complète sur votre Pi.

* |shared_link_rpi_connect| : utilisez Raspberry Pi Connect pour un accès distant sécurisé depuis n’importe où, directement dans un navigateur. 

Vous pouvez maintenant contrôler votre Raspberry Pi sans écran, soit via SSH pour les opérations en ligne de commande, soit avec VNC / Raspberry Pi Connect pour une expérience de bureau graphique.
