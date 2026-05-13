.. note::

    Bonjour et bienvenue dans la Communauté Facebook des passionnés de Raspberry Pi, Arduino et ESP32 de SunFounder ! Plongez plus profondément dans l'univers des Raspberry Pi, Arduino et ESP32 avec d'autres passionnés.

    **Pourquoi rejoindre ?**

    - **Support d'experts** : Résolvez les problèmes après-vente et les défis techniques avec l'aide de notre communauté et de notre équipe.
    - **Apprendre et partager** : Échangez des astuces et des tutoriels pour améliorer vos compétences.
    - **Aperçus exclusifs** : Accédez en avant-première aux annonces de nouveaux produits et aux aperçus.
    - **Réductions spéciales** : Profitez de réductions exclusives sur nos produits les plus récents.
    - **Promotions festives et cadeaux** : Participez à des cadeaux et des promotions de vacances.

    👉 Prêt à explorer et à créer avec nous ? Cliquez [|link_sf_facebook|] et rejoignez-nous aujourd'hui !

.. _cpn_10_axis_imu:

Module IMU 10 axes
============================

.. image:: img/10_axis.png
    :align: center
    :width: 40%

Le module IMU 10 axes est un module haute-précision à 10 axes (10DOF) capable de mesurer l'accélération, la vitesse angulaire et l'intensité du champ magnétique sur trois axes : x, y et z. Il se compose de trois capteurs principaux : SH3001, QMC6310 et SPL06_001, et communique via le protocole I2C.

Ce module est basé sur trois capteurs :

1. **SH3001** : Il s'agit d'un accéléromètre et gyroscope à 6 axes qui peut mesurer l'accélération et la vitesse angulaire sur les trois axes x, y et z.
2. **QMC6310** : Il s'agit d'une boussole numérique à 3 axes qui peut mesurer l'intensité du champ magnétique sur les trois axes x, y et z.
3. **SPL06_001** : Il s'agit d'un capteur barométrique de température et de pression qui peut mesurer la pression atmosphérique et la température.

Le SH3001 mesure l'accélération et la vitesse angulaire sur les trois axes x, y et z. Le QMC6310 mesure l'intensité du champ magnétique sur les trois axes x, y et z. Le SPL06_001 mesure la pression atmosphérique et la température. Les données de ces capteurs sont combinées pour fournir des informations précises sur l'orientation du module dans l'espace.

Le module IMU 10 axes est couramment utilisé dans des applications telles que les drones, la robotique et d'autres projets nécessitant des informations d'orientation précises. Il est compatible avec les cartes Arduino et peut être facilement interfacé avec celles-ci via le protocole de communication I2C.
