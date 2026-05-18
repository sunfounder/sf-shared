.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !

.. _i2c_config:

Configuration I²C
===================

Suivez les étapes ci-dessous pour activer et tester l’interface I²C sur votre Raspberry Pi.  
Ces instructions s’appliquent aux Raspberry Pi 5, 4, 3 et Zero 2W.

Activer l’interface I²C
------------------------

#. Ouvrez un terminal sur votre ordinateur (Windows : **PowerShell** ; macOS/Linux : **Terminal**) et connectez-vous à votre Raspberry Pi :

   .. code-block:: bash

      ssh <nom_utilisateur>@<nom_hôte>.local

   ou :

   .. code-block:: bash

      ssh <nom_utilisateur>@<adresse_ip>

#. Ouvrez l’outil de configuration du Raspberry Pi :

   .. code-block:: bash

      sudo raspi-config

#. Sélectionnez **Interfacing Options** et appuyez sur **Entrée**.

   .. image:: /_shared/appendix/img/ssh_interface.png
      :align: center

#. Sélectionnez **I2C**.

   .. image:: img/ssh_i2c_i2c.png
      :align: center

#. Choisissez **<Yes>**, puis **<Ok> → <Finish>** pour appliquer les modifications.  
   Si demandé, redémarrez votre Raspberry Pi.

   .. image:: img/ssh_i2c_yes.png
      :align: center


Vérifier les modules noyau I²C
--------------------------------

#. Exécutez la commande suivante :

   .. code-block:: bash

      lsmod | grep i2c

#. Si I²C est activé, vous verrez des modules tels que :

   .. code-block:: text

      i2c_dev        6276    0
      i2c_bcm2708    4121    0

#. Si rien ne s’affiche, redémarrez le système :

   .. code-block:: bash

      sudo reboot


Installer i2c-tools
---------------------

#. Installez les utilitaires nécessaires pour analyser et tester les périphériques I²C :

   .. code-block:: bash

      sudo apt install i2c-tools


Détecter les périphériques I²C connectés
------------------------------------------

#. Analysez le bus I²C :

   .. code-block:: bash

      i2cdetect -y 1

#. Exemple de sortie :

   .. code-block:: text

      pi@raspberrypi ~ $ i2cdetect -y 1
          0  1  2  3   4  5  6  7  8  9   a  b  c  d  e  f
      00:           -- -- -- -- -- -- -- -- -- -- -- -- --
      10: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      20: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      30: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      40: -- -- -- -- -- -- -- -- 48 -- -- -- -- -- -- --
      50: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      60: -- -- -- -- -- -- -- -- -- -- -- -- -- -- -- --
      70: -- -- -- -- -- -- -- --

#. Si un périphérique est connecté, son adresse (par exemple **0x48**) apparaîtra dans le tableau.


Installer la bibliothèque Python I²C
--------------------------------------

#. Installez le paquet ``python3-smbus2`` :

   .. code-block:: bash

      sudo apt install python3-smbus2

   La bibliothèque ``smbus2`` fournit toutes les fonctions nécessaires pour communiquer avec des périphériques I²C en Python.

Votre Raspberry Pi est maintenant entièrement configuré et prêt à communiquer avec des périphériques I²C.
