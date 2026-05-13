.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !

.. _cpn_oled:

Module d'affichage OLED
==========================

.. image:: img/oled.png
    :width: 300
    :align: center

Introduction
---------------------------
Un module d'affichage OLED (Organic Light-Emitting Diode) est un dispositif qui peut afficher du texte, des graphiques et des images sur un écran fin et flexible en utilisant des matériaux organiques qui émettent de la lumière lorsqu'un courant électrique est appliqué.

Le principal avantage d'un affichage OLED est qu'il émet sa propre lumière et n'a pas besoin d'une autre source de rétroéclairage. Pour cette raison, les affichages OLED offrent souvent un meilleur contraste, une meilleure luminosité et des angles de vision plus larges par rapport aux affichages LCD.

Une autre caractéristique importante des affichages OLED est le niveau de noir profond. Étant donné que chaque pixel émet sa propre lumière dans un affichage OLED, pour produire la couleur noire, le pixel individuel peut être éteint.

En raison de leur faible consommation d'énergie (seuls les pixels allumés consomment du courant), les affichages OLED sont également populaires dans les appareils alimentés par batterie comme les montres connectées, les trackers de santé et autres dispositifs portables.

Principe
---------------------------
Un module d'affichage OLED se compose d'un panneau OLED et d'une puce de pilotage OLED montée à l'arrière du module. Le panneau OLED est constitué de nombreux petits pixels qui peuvent produire différentes couleurs de lumière. Chaque pixel est composé de plusieurs couches de matériaux organiques prises en sandwich entre deux électrodes (anode et cathode). Lorsque le courant électrique traverse les électrodes, les matériaux organiques émettent de la lumière de différentes longueurs d'onde selon leur composition.

La puce de pilotage OLED est une puce qui peut contrôler les pixels du panneau OLED en utilisant un protocole de communication série appelé I2C (Inter-Integrated Circuit).

La puce de pilotage OLED convertit les signaux de l'Arduino en commandes pour le panneau OLED. L'Arduino peut envoyer des données à la puce de pilotage OLED en utilisant une bibliothèque qui peut contrôler le protocole I2C. L'une de ces bibliothèques est la bibliothèque Adafruit SSD1306. Avec cette bibliothèque, vous pouvez initialiser le module d'affichage OLED, régler le niveau de luminosité, imprimer du texte, des graphiques ou des images, etc.

.. **Exemple**

.. * :ref:`basic_oled` (Projet de base)
.. * :ref:`fun_pong` (Projet ludique)
.. * :ref:`iot_weathertime_screen` (Projet IoT)
