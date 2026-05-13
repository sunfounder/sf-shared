.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !

.. _cpn_fusion_hat:

Fusion HAT+
=====================================

.. image:: img/fusionhat_v0.png
    :width: 500
    :align: center


La Fusion HAT+ est une carte d'extension puissante et polyvalente conçue pour transformer facilement un Raspberry Pi en un robot entièrement fonctionnel avec une configuration minimale, tout en prenant en charge des projets d'automatisation avancés.

Au cœur de la Fusion HAT+ se trouve un microcontrôleur (MCU) intégré, qui étend considérablement les fonctionnalités natives du Raspberry Pi en fournissant des sorties PWM supplémentaires et des entrées ADC — des capacités généralement absentes sur les modèles Raspberry Pi standard. Cela permet aux développeurs d'obtenir un contrôle plus précis des moteurs et une meilleure intégration des capteurs.

Compacte mais riche en fonctionnalités, la Fusion HAT+ intègre quatre pilotes de moteur, prenant en charge le contrôle indépendant de jusqu'à quatre moteurs à courant continu. Elle dispose également d'un module audio numérique I2S et d'un haut-parleur mono intégré, permettant une lecture audio de haute qualité et des fonctionnalités sonores interactives directement depuis la carte.

La carte accepte une alimentation de 6,0 V à 8,4 V via un connecteur XH2.54 à 3 broches. Elle comprend deux LED indicatrices d'alimentation pour surveiller l'état du système, une LED programmable par l'utilisateur pour la signalisation personnalisée, ainsi qu'un bouton intégré pratique pour les tests de fonction ou la simulation d'entrée — rendant le développement et le débogage plus efficaces et conviviaux.

.. |link_fusion_hat| raw:: html

    <a href="https://docs.sunfounder.com/projects/fusion-hat/en/latest/" target="_blank">SunFounder Fusion HAT+</a>

Pour des instructions détaillées, veuillez consulter : |link_fusion_hat|.

PinPal
============================

.. image:: img/pinpal_pic.png
    :width: 20%
    :align: center

PinPal est un petit circuit imprimé conçu par SunFounder avec les étiquettes des broches du Raspberry Pi.
Vous pouvez le placer directement sur le connecteur de broches de la Fusion HAT+, ce qui permet d'identifier facilement et rapidement la fonction de chaque broche lors de la construction de votre projet.
Cela aide à réduire les erreurs et à accélérer le câblage.

.. image:: img/pinpal_fusion_hat.png
    :width: 80%
    :align: center

Certaines broches sur PinPal sont **déconseillées pour une utilisation directe** car elles sont déjà utilisées par la Fusion HAT+ ou partagent des fonctions pouvant entraîner des conflits.


#. **SDA / SCL — I2C (GPIO2 / GPIO3)**

   * Broches I2C principales du Raspberry Pi.
   * La Fusion HAT+ fournit également un connecteur I2C P2.54 et un port SH1.0 Qwiic/STEMMA QT.
   * Les trois partagent le même bus, donc **un seul peut être utilisé à la fois**.

   .. image:: img/pinpal_i2c.png
       :width: 80%
       :align: center

#. **TXD / RXD — UART (GPIO14 / GPIO15)**

   * Broches UART principales du Raspberry Pi.
   * La Fusion HAT+ inclut un autre connecteur UART, partageant les mêmes broches — **choisissez-en un seul**.

   .. image:: img/pinpal_uart.png
       :width: 80%
       :align: center

#. **GPIO 17 / 4 / 27 / 22 — GPIO générales**

   * La Fusion HAT+ fournit un ensemble supplémentaire de ces broches, mais elles correspondent aux mêmes GPIO du Raspberry Pi.
   * **Utilisez un seul groupe** pour éviter les conflits.

   .. image:: img/pinpal_gpio.png
       :width: 80%
       :align: center

#. **MOSI / MISO / SCLK / CE0 / GPIO6 — Broches SPI**

   * La Fusion HAT+ fournit un autre connecteur SPI.
   * Le connecteur RGB (WS2812) utilise la broche MOSI.
   * **Utilisez un seul groupe SPI** pour éviter les conflits.


   .. list-table::
      :header-rows: 1

      * - Signal
        - Correspondance des broches
      * - BSY
        - GPIO6
      * - CS
        - CE0 / GPIO8
      * - SCK
        - SCLK / GPIO11
      * - MI
        - MISO / GPIO9
      * - MO
        - MOSI / GPIO10

   .. image:: img/pinpal_spi.png
       :width: 80%
       :align: center


#. **GPIO 18 / 19 / 20 / 21 — Broches audio I2S**

   * La Fusion HAT+ inclut un circuit audio I2S intégré (haut-parleur + microphone). Plus de détails :
     `I2S <https://docs.sunfounder.com/projects/fusion-hat/en/latest/hardware/interfaces.html#speaker-and-mic>`_.
   * Vous pouvez réutiliser ces broches uniquement lorsque le système audio est désactivé.
   * **N'utilisez pas WS ou SCLK lorsque les composants audio sont actifs.**

   .. image:: img/pinpal_i2s.png
       :width: 80%
       :align: center

   .. list-table::
      :header-rows: 1

      * - Signal
        - Broche Raspberry Pi
      * - WS
        - GPIO19
      * - SCLK
        - GPIO18
      * - Sortie audio (HP)
        - GPIO21
      * - Entrée audio (MIC)
        - GPIO20


#. **ID_SD / ID_SC — Broches EEPROM HAT**

   Ces broches sont réservées à l'EEPROM HAT du Raspberry Pi, qui stocke les données d'identification de la carte.
   La Fusion HAT+ utilise ces broches pour son EEPROM intégré, donc **ID_SD (GPIO0) et ID_SC (GPIO1) ne doivent pas être utilisées à d'autres fins**.


   .. image:: img/pinpal_eeprom.png
       :width: 80%
       :align: center

