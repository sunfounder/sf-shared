.. note::

    Bonjour, bienvenue dans la communauté des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder sur Facebook ! Plongez dans l'univers de Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi nous rejoindre ?**

    - **Support d'experts** : Résolvez des problèmes après-vente et des défis techniques grâce à l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Obtenez un accès anticipé aux annonces de nouveaux produits et aux avant-premières.
    - **Réductions exclusives** : Profitez de réductions spéciales sur nos derniers produits.
    - **Promotions et cadeaux festifs** : Participez à des concours et promotions festifs.

    👉 Prêt à explorer et à créer avec nous ? Cliquez sur [|link_sf_facebook|] et rejoignez-nous dès aujourd'hui !


.. _spi_configuration:

Configuration SPI
=================

Suivez les étapes ci-dessous pour activer et vérifier l’interface SPI sur votre Raspberry Pi.  
Ces instructions s’appliquent aux Raspberry Pi 5, 4, 3 et Zero 2W.

Activer l’interface SPI
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

#. Sélectionnez **SPI**.

   .. image:: img/ssh_spi_spi.png
      :align: center

#. Choisissez **<Yes>**, puis **<Ok> → <Finish>** pour appliquer les modifications. Si nécessaire, redémarrez votre Raspberry Pi.

   .. image:: img/ssh_spi_enable.png
      :align: center


Vérifier l’interface SPI
------------------------

#. Vérifiez si les périphériques SPI existent :

   .. code-block:: bash

      ls /dev/sp*

#. Si l’interface SPI est activée, la sortie inclura :

   .. code-block:: text

      /dev/spidev0.0
      /dev/spidev0.1

   * Si ces périphériques apparaissent, SPI est actif et prêt à être utilisé.  
   * Dans le cas contraire, redémarrez votre Raspberry Pi et vérifiez à nouveau.


Installer spidev (bibliothèque SPI pour Python)
-----------------------------------------------

#. Installez le paquet ``spidev`` pour utiliser SPI en Python :

   .. code-block:: bash

      sudo apt install python3-spidev

   La bibliothèque ``spidev`` permet d’accéder aux périphériques SPI via l’interface ``/dev/spidevX.Y``.

----------------------

Votre Raspberry Pi est maintenant configuré pour communiquer avec des périphériques SPI, à la fois via les outils en ligne de commande et en Python.
